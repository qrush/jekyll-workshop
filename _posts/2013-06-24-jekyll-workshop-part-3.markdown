---
layout: post
title: Jekyll Workshop Part 3 - Make a page
---

Pages are the easiest way to just publish content with Jekyll. Pages are a single file that contain your content and metadata.

### Make a page

There's already one page in your Jekyll site by default: `index.html`. Let's make a new one:

    $ touch about.html

Open this up in Sublime (or your text editor of choice), and copy/paste this in:

    <p>
      I'm _____________.
    </p>
    <p>
      I enjoy _____________ and frequently _____________.
    </p>
    <p>
      I'd love to use Jekyll in order to _____________.
    </p>

Fill in the blanks! Now if you browse to [http://localhost:4000/about.html](http://localhost:4000/about.html) you should see your about page.

### But it's unstyled!?

By default pages in Jekyll don't have a layout, which we use as basically a template to share code, such as your stylesheets, javascripts, etc. You have to opt-in to a layout. Luckily we already have one when we generated our Jekyll site.

Let's add a chunk of code to the top of your `about.html` page to specify a layout:

    ---
    layout: default
    ---

    <p>
      I'm _____________.
    </p>
    <p>
      I enjoy _____________ and frequently _____________.
    </p>
    <p>
      I'd love to use Jekyll in order to _____________.
    </p>

This piece of metadata is called the "YAML Frontmatter" in the Jekyll docs. YAML is a simple way to specify data in key/value pairs. In this case, the key is `layout`, and the value is `default`.

### Refresh it!

If you reload your `about.html` page in the browser, the content will now be styled! Where did that come from? If you take a look in your `_layouts` folder, you'll see a `default.html`:

    $ tree _layouts

    _layouts
    ├── default.html
    └── post.html

Once you specify a `layout`, Jekyll will run each page through the layout and inject its content. (Where the `content` code snippet is!)

While you're in there, edit the header and footer to include your name and a different title. You might need to restart `jekyll serve --watch` in order to get the header and footer to refresh.

### Whoa, what?

Jekyll basically injects your content into layouts, using the [Liquid](http://liquidmarkup.org/) templating language. If pictures are more your thing, here's what Jekyll's processing pipeline looks like.

Before we specified the layout:

    =
    
    *------------*  =====>  *------------------*
    *            *          *                  *
    * about.html *  Jekyll  * _site/about.html *
    *            *          *                  *
    *------------*  =====>  *------------------*
    
    =

And after we specified the layout:

    =
    
                            *-----------------------*
                            * _layouts/default.html *
                            *                       *
    *------------*  =====>  *     *------------*    *  =====>  *------------------*
    *            *          *     *            *    *          *                  *
    * about.html *  Jekyll  *     * about.html *    *  Jekyll  * _site/about.html *
    *            *          *     *            *    *          *                  *
    *------------*  =====>  *     *------------*    *  =====>  *------------------*
                            *                       *
                            *-----------------------*
    
    =

### Ship it!

It's that time again: Deploy your site! Let's commit our work and push it to GitHub:

    $ git add .
    $ git commit -m "Added a page"
    $ git push origin master

With luck, in a few moments you'll see your page appear up on GitHub.
