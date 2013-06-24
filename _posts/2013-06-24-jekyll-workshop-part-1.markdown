---
layout: post
title: Jekyll Workshop Part 1 - Getting Started
---

Let's get started with Jekyll!

### Install Ruby

If you haven't installed Ruby yet, please do! The easiest way to install it on most platforms just to get started is the [Rails Installer](http://railsinstaller.org/). You'll also need a text editor, [Sublime Text](http://www.sublimetext.com/) works great on just about everything.

### Make a Jekyll site

Next up open up Terminal (or whatever you're using), and run:

    jekyll new workshop
    cd workshop

This will make a new Jekyll site in a directory called `workshop`, and then jump inside that directory.

### Serve up your Jekyll site

Let's look at what we generated. We're going to keep this running from here on. Just run:

    jekyll serve --watch

You'll see a bunch of stuff spit out to your screen. You now should be able to browse to [http://localhost:4000](http://localhost:4000) in your favorite browser, and see your Jekyll site!

### Open up the Jekyll docs

Keep the official [Jekyll docs][jekyll] open in case you need them for reference throughout.

[jekyll]:    http://jekyllrb.com
