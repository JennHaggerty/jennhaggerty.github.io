---
layout: post
title:  "Your Recruiter"
date:   2025-04-07
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: Jennifer's progress on the app.
---

Today I moved the listing actions to their own context and cleaned up the Detail Modal's action buttons.

<h2>Listing Actions Context</h2>

Each listing has the following actions: 
<ul>
  <li>Get Listing Information</li>
  <li>Write Cover Letter</li>
  <li>Write Cover Letter with AI</li>
  <li>View Cover Letter</li>
  <li>Write Resume</li>
  <li>View Resume</li>
  <li>Edit Listing Information</li>
  <li>Delete Application</li>
</ul>

Writing it all out, it feels like a LOT but as I actively use the application I know these are necessary. For some of the actions, the Write button will be swapped with the View button as the modal that opens will have the Edit/Write option for a cleaner UI. There wasn't too much prop-drilling however the amount of actions in the locations present became overwhelming as I added the latest (View/Write Resume) so I moved them to their own context for my own sanity. 

<h2>Detail Modal Cleanup</h2>

Because there are so many actions, the buttons at the bottom of the Details Modal was overwhelmed with a combination of Icon Only and Text buttons. On mobile, the user will see the Text version on all of the buttons, if there is a manual and AI option those buttons will appear on the same line while the stand alone buttons are on their own. The desktop has more breathing room with a combination of Text and Icon Only buttons with the Tooltips helping to covey the purpose of the Icon Only buttons.

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>