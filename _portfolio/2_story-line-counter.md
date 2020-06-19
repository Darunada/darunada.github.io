---
title: story-line-counter
date: 2019-08-02 00:00:00 Z
permalink: "/portfolio/story-line-counter"
tags:
- portfolio
- native
- rust
- git
layout: post
description: A tool for counting code changes per SAFE story point.
img: 
open_source: true
meta: Gather information from your repos, then graph it to gain insights on your code
  changes.
link: https://www.leafairbanks.com/story-line-counter
repo_link: https://github.com/Darunada/story-line-counter
repo_icon: fa-github
---

I am plagued by a problem - how big is a [story point](https://www.scaledagileframework.com/story/)?  It keeps me up 
at night, and when I fall asleep I dream about it. How am I supposed to quote my work when the one point story 
model is ambiguous - 'a simple login page' - AHHHHHHHHH!

I realized an interesting metric I would like to see would be the number of code changes per story point.  I 
searched around a bit, trying to find an application that counted code changes by a commit message, and came up with
nothing. I had written a tool that does something similar a few years ago with my 
[git-asana-post-commit-hook](https://github.com/Darunada/git-asana-post-commit-hook), so I was slightly familiar with 
what it would take to make, and then it sat on the back burner.  Another good idea that I'll get to later.  

A few weeks later, I got really charged up about learning Rust.  After practicing about a week, I thought this might 
be an appropriate challenge to try out.  I found all the bits I needed in other open source projects, and quickly put together 
a prototype.  Then I decided it was worth refining into a finished application.

I have also been thinking about how I learn new things, since a colleague presented the question. Part of me learning 
Rust has been a conscious effort to deliberately practice that process. I am planning to write a blog post about it, soon.

<div class="col three">
    <img src="/img/portfolio/story-line-counter/helps-screen.png" alt="The story-line-counter Help page" 
    title="That is some nice help."/>
</div>

# Design

The application works in two steps, collect and total.  During collection, it computes diffs between changes
and collects the number of lines changed.  It also scans the commit message for story numbers, and tracks those per diff.
Next, with the total command, it sums the number of line changes and groups them by story number, giving a 
total number of lines changed.  Separating the process into two commands allowed me to total multiple repos together, 
which is fantastic because we never have just ~One~ repo.

# Release

This application is the first native application I ever released publicly, and I'm happy to share that it has been published
to [crates.io](https://crates.io).  You can view the release [here](https://crates.io/crates/story-line-counter), or view the most 
recent version on [github](https://github.com/Darunada/story-line-counter).  It is open source and contributions are welcome!

# Next Steps

I will be collecting some data and creating some visualizations to share the conslusions.  More on that, soon!