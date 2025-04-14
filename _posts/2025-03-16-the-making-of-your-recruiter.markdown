---
layout: post
title:  "Your Recruiter"
date:   2025-03-16
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: Jennifer's progress on the app.
---

The table gets a facelift with pagination and the option to adjust how many rows are visible per page. I also added the user signup option but disabled it until I'm ready. 

I brought in a Skeleton version of the list that becomes visible when the table is loading or when a call to the applications database is made. I needed to have the table refresh because each time a new listing was added the table would add the new listing but the actions would not be available until a page refresh. To clean the state and ensure the actions where available for the new listings a total applications refresh happens. 

At this point I'm switching repositories. When I began this project I hardcoded my personal data in to get it up and running with minimal headaches and I do not want my address and phone number visible in the repository so I'm copying what I have to a new public repo!

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>