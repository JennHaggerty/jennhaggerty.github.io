---
layout: post
title:  "The Making of Your Recruiter"
date:   2025-04-03
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: Jennifer's progress on the app.
---

Users can now write in their own cover letter and edit both the AI version and their own. Users may also write in an application specific resume.

<h2>Write your own Cover Letter</h2>

Prior to today, the only option for getting a cover letter was to have AI write it. Now users have the option to write their own instead of being forced to use AI. Users may also edit the cover letter, whether it is their own or was AI generated.

<h2>Resumes</h2>

I need to add a place for the user to enter their primary resume, write now I just uploaded my own to the database to get everything else working. Currently, when the user has a resume attached to their profile that is used by the AI to generate a cover letter, the resume is then attached to that application so the user can see which resume was used to apply for the position. Users can now write in their own resume per application which overrides the primary resume (if available).

<h2>Additionally</h2>

The table view and modals were updated with the appropriate buttons for the cover letter and resume. The Write buttons will be swapped with View in the overview and the detailed modals will show the Edit options.

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter">Github respository</a>