---
layout: post
title:  "Your Recruiter Pro Version is in the works"
date:   2025-04-21
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: "Jennifer did get enough from the original app and begins a pro version."
---

Today I began the pro version of Your Recruiter

<h2>Pro: What's the diff?</h2>

Pro would connect job seekers with professionals like enemployment office reps and recruiters. These additional party members would help the candidate and have role-specific abilities:

<dl>
  <dt>Advisors</dt>
  <dd>Advisors can add listings and write notes to help with cover letters and resumes. They can update the status of a listing, such as when a position closes. Advisors also bridge the gap between candidates and recruiters, assigning one to the other.</dd>

  <dt>Recruiters</dt>
  <dd>Recruiters work for a company matching candidates to jobs. They can add listings and update the status. Recruiters can write notes helping with cover letters and resumes.</dd>

  <dt>Candidates</dt>
  <dd>Candidates have the most abilities in that they can write, edit, and delete listings, cover letters, and resumes. The reason the candidates have the most power is because they are the main character :D</dd>
</dl>

There is an additional role, the Admin, that can view all roles for development, troubleshooting, and help others navigate the app. It is a hidden role.

<h3>Musings</h3>

I am currently thinking about allowing candidates to add their own recruiters or only allow the Advisor that ability. When a candidate with working with an Advisor in the unemployment office or an HR rep the Advisor may not want to have too many chefs in the kitchen - so to speak. I do not know enough about the admin side of unemployment offices to know if this is a help or hinderance. I might add it to the advisor settings for each candidate. 

Recruiters will have the least amount of "power" on this application. For sanity and book keeping they cannot update cover letters and resumes. That might be another future option to allow the Candidate to open a cover letter or resume for editing by Recruiters and Advisors - would want an activity tracker and badge to show when something has been edited and maintain a copy of the last version in case the Candidate wishes to revert the changes.

Candidates have the most "power", only they can add/edit cover letters and resumes, and they can edit the listing information. For lack of corporate-safe translation I'm going to say it's because the Candidate needs our protection and integrity. It would be terrible to see this service abused with bait n' switch salaries, remote options, and job duties. This places the onus of making sure the information is maintained on the Candidate and that they double check *everything* before agreeing to a work contract.

<h2>Links</h2>

These links will take you to the original Your Recruiter (currently in beta testing).

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>