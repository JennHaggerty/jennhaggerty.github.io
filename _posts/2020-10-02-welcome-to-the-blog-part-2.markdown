---
layout: post
title:  "Welcome to the blog. Here's how I did it, part 2."
date:   2020-10-02
tags: GitHub GitHubPages Jekyll Ruby HTML SCSS
description: The second post where Jennifer Haggerty details the creation of a blog using Jekyll, GitHub Pages, and SCSS.
---

Yes, there is a part 2 to this because as I took a look at my <a href="https://github.com/JenniferHaggerty">GitHub profile</a> to see that pretty green-filled box I noticed it wasn't there. That's because when you fork a project it doesn't work to fill in the gaps on your repo but if you make a pull request that gets accepted on the source repo that profile will see a green box. Keep making those contributions, but if you're wanting the green box on your profile here's how to do it.

The following instructions will be for Mac OSX using the terminal. Checkout out the <a href="https://jekyllrb.com/docs/installation/">Jekyll installation guides</a> for Linux and Widnows.

<h2>Step 1: Install Ruby and Jekyll</h2>

Jekyll is a static website builder and Ruby is a programming language. Install Ruby with `$ brew install ruby`, and install Jekyll with `$ gem install jekyll bundler`

<h2>Step 2: Create the static site</h2>

`$ jekyll new <yourGithubUsername>.github.io`

This will give you a new directory on your computer with everything you need in the same setup as the previous guide. If you notice things are looking different when you're altering the look of your website, perhaps there was an update, then run `$ open $(bundle info --path minima)` which will show the directory layout and file names for the Jekyll theme Minima. If you assigned a different theme on installation or have since changed the defaults then be sure to modify the command as needed.

<h2>Step 3: Push to GitHub</h2>

Rename the previous Jekyll site repo from <i>yourGitHubUsername.github.io</i> to a new name, something like <i>yourGitHubUsername_github_io</i> so it would no longer use the one pages slot GitHub gives us. By doing so you can keep a backup of all the work you did before. 

Create a new repository with the <i>yourGitHubUsername.github.io</i> and follow the new repo's instructions for adding an existing project and connect the repo to your computer's project directory. Push the new code to your GitHub via `$ git add . && git commit -m "Initial commit" && git push -u origin`.

Allow a few minutes to pass and you should see the new website up and running and the lovely green box on your GitHub Profile.

<h2>Thank you for reading</h2>

Happy coding!