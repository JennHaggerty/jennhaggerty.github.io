---
layout: post
title:  "Your Recruiter"
date:   2025-01-23
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: Jennifer's progress on the app.
---

Today I made my own toasts and brought in Firecrawl to scrape listings.

<h2>Toasts</h2>

HeroUI is currently working on their own toasts so I modified their Alert component to act as a toast in the interim. I'll be keeping a close eye on HeroUI updates because I prefer to use components in their intended use to avoid negative side-effects later on.

<h2>Firecrawl</h2>

<a href="https://www.firecrawl.dev">Firecrawl</a> has excellent pricing options for scraping and extracting web data. I was able to utilize their free services with a minor change. I initially was using their scrape functionality to grab the listing data and it was going really well for about a month before I hit the limit on requests. Taking a look at their documentation I realized I should have been using their Extract feature which uses significantly less tokens per requests and haven't reached the new limit yet. 

There are priced options to avoid reaching any limits and I will add the User Settings area where users can add and edit their api keys.

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>