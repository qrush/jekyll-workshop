---
layout: post
title: Jekyll Workshop Part 2 - Publish your site
---

What? Already? Let's ship it!

### Create a GitHub account

GitHub hosts Jekyll sites for free via [GitHub Pages](http://pages.github.com). Please register for an account on GitHub if you haven't yet.

### Create a repo

We'll need to make a repo in order to host your content on GitHub. Once you're signed in, hit the big "Create Repo" button, or [follow this guide](https://help.github.com/articles/create-a-repo). If your username is `johndoe`, call the repo `johndoe.github.io`.

### First time Git setup?

No problem! GitHub has a great [setup guide](https://help.github.com/articles/set-up-git) that covers everything you'll need to do.

### Ship it!

Next we need to send your code up to GitHub. I'm going to pretend your github username is `johndoe`, make sure to replace it with yours! From your terminal, run:

    $ git init
    $ git add .
    $ git commit -m "Initial commit"
    $ git remote add origin git@github.com:johndoe/johndoe.github.io.git
    $ git push origin master -u

### View your site

That should be it! In a few moments your site will appear at [http://johndoe.github.io/](http://johndoe.github.io/).
