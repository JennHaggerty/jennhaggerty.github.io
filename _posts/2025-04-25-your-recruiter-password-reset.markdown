---
layout: post
title:  "Your Recruiter Password Reset SECURED"
date:   2025-04-25
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: "I couldn't sleep, I was thinking about securing the forgot password flow"
---

After creating the Forgot Password flow yesterday I immediately began thinking about how to hack it and steal someone's info. Today, I secured it!

<h2>ACCESS DENIED</h2>

I added an additional database to store password recovery requests. Each request now has a 10 minute lifespan before the database deletes the entry eliminating the possibility of someone getting a hold of a user's id and changing their password anytime they want. There are additional checks in the api to compare the creation and expiration dates and delete entries on error and success.

This still doesn't *feel* fool-proof, I think I should create a random url next for the password reset flow.

<iframe src="https://giphy.com/embed/xUPJPhanYiB7z9xlCg" width="480" height="360" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/spongebob-spongebob-squarepants-season-8-xUPJPhanYiB7z9xlCg">via GIPHY</a></p>

Ok, so instead of using the user's id we're not using the *request id*! Much more difficult to get a hold of and no user information is provided at any point! Yeah, that feels much better.

<h3>Questions, comments, concerns?</h3>

<a href="mailto:thejenniferhaggerty@gmail.com">Email me</a> or leave a comment below!

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>