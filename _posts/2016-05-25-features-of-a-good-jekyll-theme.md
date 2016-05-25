---
layout: post
title: Features of a good Jekyll theme
tags: [jekyll]
---

I wanted to refocus on my efforts to write personal blog, hence started looking into *Jekyll*. I once had some initial code/content   on my Github which I checked out. Meanwhile, I've got a new Mac, so I had to install Jekyll on it. To my surprise, when I ran `jekyll serve`, Jekyll started complaining.

Issues were:

- Apparently I was using an older version of Jekyll, and I have 3.x.
- Some plugins needed gem installation, which I didn't have.

Reading the error messages and [googling](https://github.com/blog/2100-github-pages-now-faster-and-simpler-with-jekyll-3-0) helped. To be specific:

- I had to remove a tag that was configuring things for permanent link.
- The code highlighter is now `rouge`, not `pygment`.
- I had to add a `gems` property to enlist two plugins that I got from [Hyde](http://hyde.getpoole.com/) (the template I am using). I also had to install these gems manually.

I am now convinced that a theme should make users' life easier by providing a `Gemfile`, thus allowing `bundle install` to run. More on this [here](https://jekyllrb.com/docs/plugins/), and [here](https://github.com/mmistakes/so-simple-theme).
