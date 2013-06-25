---
layout: post
title: Jekyll Workshop Part 2 - Publish your site
---

What? Already? Let's ship it!

### Create a GitHub account

GitHub hosts Jekyll sites for free via [GitHub Pages](http://pages.github.com). Please register for an account on GitHub if you haven't yet.

### Create a repo

We'll need to make a repo in order to host your content on GitHub. Once you're signed in, hit the big "Create Repo" button, or [follow this guide](https://help.github.com/articles/create-a-repo). Call the repo `workshop`.

### First time Git setup?

No problem! GitHub has a great [setup guide](https://help.github.com/articles/set-up-git) that covers everything you'll need to do.

### Ship it!

Next we need to send your code up to GitHub. I'm going to pretend your github username is `johndoe`, make sure to replace it with yours! From your terminal, run:

    $ git init
    $ git add .
    $ git commit -m "Initial commit"
    $ git branch -m gh-pages
    $ git remote add origin git@github.com:johndoe/workshop.git
    $ git push origin gh-pages -u

### View your site

That should be it! In a few moments your site will appear at [http://johndoe.github.io/workshop/](http://johndoe.github.io/workshop/).

### But it's broken!

By default Jekyll assumes you're going to be serving a site off the root domain, and not in a subdirectory. We'll have to make a quick edit to make our CSS work again. Open up `_layouts/default.html` in your favorite editor and replace these two `<link>` tags with (just remove the leading slash on `css/`):

    <!-- syntax highlighting CSS -->
    <link rel="stylesheet" href="css/syntax.css">

    <!-- Custom CSS -->
    <link rel="stylesheet" href="css/main.css">

Now let's push this fix out to GitHub:

    $ git commit -am "Fixed CSS"
    $ git push
