---
layout: post
title:  "Your Recruiter Password Reset"
date:   2025-04-24
tags:   Next.js, React, Typescript, TailwindCSS, HeroUI, MongoDB, Vercel, OpenAI
description: "Did you forget your password? I did too, let's reset it."
---
Today I brought in Nodemailer and added a reset password function to Your Recruiter. Now if you forget your password you can click the link on the Login form and request a reset password link.

<h2>I forgot my password, now what?</h2>

<div class="tenor-gif-embed" data-postid="13730108" data-share-method="host" data-aspect-ratio="1.77778" data-width="100%"><a href="https://tenor.com/view/let-me-in-eric-andre-wanna-come-in-gif-13730108">Let Me In Eric Andre GIF</a>from <a href="https://tenor.com/search/let+me+in-gifs">Let Me In GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>

<h2>The Goods</h2>

<img src="/assets/image.png" alt="forgot password link">

<p>The new Forgot Password link can be found in the Login form.</p>

<img src="/assets/image-1.png" alt="forgot password form">

<p>Once clicked the link will open the modal to enter the account email. If the account is found a email will be sent.</p>

<img src="/assets/image-3.png" alt="reset email">

<p>Currently, the email comes from my own account since this is a one-woman show :D You can tell it's the right email with the Morticia portrait.</p>

<img src="/assets/image-2.png" alt="reset password form">

<p>Clicking on the link takes you to the reset password form.</p>

<h2>The Process</h2>

<p>This was really quick and easy to setup. Nodemailer is pretty ready to go out the box. I am using Gmail and Google requires an app specific password for the Nodemailer which I appreciate on a security front. I copied the existing update password form, removing the current password field, and added a new api endpoint to handle the change. A few tests helped me figure out the timing for the toasts and UX and it was ready to go!</p>

<h2>Links</h2>

<a href="https://your-recruiter.vercel.app">Your Recruiter website</a>

<a href="https://github.com/JennHaggerty/your-recruiter-reports">Github respository</a>