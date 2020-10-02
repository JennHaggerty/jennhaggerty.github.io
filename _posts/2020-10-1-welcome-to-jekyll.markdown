---
layout: post
title:  "Welcome to the blog. Here's how I did it."
date:   2020-10-01
---
As I was setting up my best friend's website <a href="http://getthisoutofmycloset.shop">GetThisOutOfMyCloset.shop</a>, she has amassed a large collection of art supplies, artworks, and skin care products that are taking over her closet space so we're making an online shop to clear it out, she mentioned me setting up a blog to detail the technical work I've been doing. For a long time I've been reluctant to begin a blog finding them to be time consuming, per my attempts to start a blog for my hobby with photography and painting, yet I now equate them to documenting client projects, which I'm a fan of doing so here it goes.

<h2>Step 1: Make a <a href="https://github.com">GitHub</a> account, if you do not have one.</h2>

Why am I using GitHub pages? My <a href="https://jenniferhaggerty.com">website</a> was made with VueJS and Bootstrap to get something showcasing my client portfolio up quickly, getting a blog running would need  MySQL, custom queries to make the CRUD operations, and a user base to interact with the blog. It's totally doable, but with a one-woman team who likes to do things the very manual way on her own sites for learning sake I opted to look at hosting a blog on GitHub. Not only do hiring managers require a GitHub for developer related roles the green box on one's profile is very satisfying to see, and you get content now and not a year from now.

<h2>Step 2: Fork the <a href="https://github.com/barryclark/jekyll-now">barryclark/jekyll-now</a> repository.</h2>

This awesome repo uses Ruby, Jekyll, and SCSS to make a GitHub pages website and blog.

<h2>Step 3: Customize colors, fonts, and the _config.yml.</h2>

What you get from the repo is a nice, clean website and blog template with the majority of the work already done on the front end and all of the routing and website structure setup. The README.md included in the repo has excellent instructions on how to customize it for your purposes. The TL;DR version:

1. Input your information and social networks in the _config.yml. 
2. Change the global color palette and fonts go to _sass/_variables.scss and alter the $variables to your liking.
3. If that isn't enough, edit the style.scss in the root directory of your repo to further customize the look of your new GitHub pages site.

<h2>Thank you for reading</h2>

I hope this was informational and makes you a bit more confident if you're looking to setup your own GitHub pages blog. If you have any questions or are looking to setup your own website with VueJS, WordPress, or ReactJS with a freelancer <a href="mailto:{{ site.email }}">email me</a>.
