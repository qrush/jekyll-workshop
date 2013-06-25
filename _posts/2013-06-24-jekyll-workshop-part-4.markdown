---
layout: post
title: Jekyll Workshop Part 4 - Write a post
---

Jekyll can be used as a simple CMS as well as a blog. Posts are just pages, but with a specific naming convention.

### Make a post

Posts are created in the `_posts` directory, with this scheme:

    YEAR-MONTH-DAY-title.MARKUP

Here's some example posts:

    2011-12-31-new-years-eve-is-awesome.md
    2012-09-12-how-to-write-a-blog.textile

Let's make one now! In your terminal, run:

    $ touch _posts/2013-06-25-my-first-jekyll-post.markdown

### Get to writing

Let's use [Markdown](http://daringfireball.net/projects/markdown/syntax), which is a lot easier to publish content with online than HTML. Open up your new post in a text editor, and let's put content in (feel free to write more, too!)

    ## My first post

    Yada **yada** yada...

    _Awesome!_

If you refresh your site, you should see this post appear in the list, but it won't be styled yet. Add a layout just like we did with the `about.html` page, but instead use the `post` layout.

**Note:** Layouts can be nested! The `post` layout specifies the `default` layout. [Whoa.](http://www.legalproductivity.com/wp-content/uploads/2010/12/whoa-300x223.jpg).

## Attach an image

Write some markdown, and make sure to include an image too!

Let's make a directory for images:

    $ mkdir images

Find an image somewhere online, and move it into this folder. If you're on OSX, a shortcut to open your images folder in Finder is to run `open images/` in your terminal. Let's pretend you found an image called `dog.jpg`. Here's how you can refer to it in your post:

    ## My first post

    Yada **yada** yada...

    ![The best dog ever.](/images/dog.jpg)

    _Awesome!_
