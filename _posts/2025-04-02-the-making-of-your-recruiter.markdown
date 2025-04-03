---
layout: post
title:  "The Making of Your Recruiter"
date:   2025-04-03
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: Jennifer makes an AI supported job applications CMS.
---

Today I:

<h2>Added the table settings to `sessionStorage`!</h2>

I found the need for this when I wanted to remove some older applications that were `closed` or `rejected` and after deleting one I had to reapply the table filters to get back where I was. With today's update when the user changes the page, the stages visible, and the columns visible, that data to saved to `sessionStorage` so when the user refreshes the page those settings are reapplied and the user won't lose their place. Some of the table functions must refresh the page and this will make it much easier to manage the applications and navigate the table. The `sessionStorage` is cleared when the user closes the tab, not when the user is logged out because I thought about accidental logouts that could lead to user frustration if they couldn't remember what settings they had before the accident.

<h2>Consolidated functions to update state.</h2>

Previously, functions would have to make two calls:
```sh
setTableState((prevState) => ({
  ...prevState,
  key: value
}));

setTableSession({key: value});
```
Added `updateTableState()` to take any and all changes to the table settings and update the `tableState` and `sessionStorage`. 

```sh
const updateTableState = (args: { key: string; value: any }[]) => {
  const updates = args;
  updates.forEach((update: { key: string; value: any }) => {
    const { key, value } = update;
    setTableState((prevState) => ({
      ...prevState,
      [key]: value,
    }));
    // handle Sets
    if (
      key === 'visibleColumns' ||
      key === 'statusFilter' ||
      key === 'selectedRows'
    ) {
      setTableSession({ key, value: JSON.stringify([...value]) });
    } else {
      setTableSession({ key, value });
    }
  });
};

// example
updateTableState([
  { 
    key: 'page', value: 1 
  },
  { 
    key: 'rowsPerPage', value: 15
  },
  {
    key: 'visibleColumns', value: [ 
      "details",
      "salary",
      "location",
      "stage"
    ]
  }
]);
```

<h2>Relocated the Legend</h2>

The Legend was never meant to stay in the Nav, I wanted it there during the early days to check my own color rules and make sure I stuck to them or updated as needed. Now the Legend exists in the Footer. It's important to me to keep the Legend because I have a color code and use it as a style guide. I also want new and older users to have a reference to use the app more efficiently and confidently: purple buttons will always mean there's an AI action happening while red always represents a destructive action or error.