# Open Diffix Website

## Running and deploying

To start a local development server on http://localhost:8080, run:

```
docker compose up
```

To make a deployment, push to `main`.

The build lives in the `gh-pages` branch, which must not be deleted.

## FAQ

:question: **Where is the content of the site located?**

Static pages are found in the `_pages` directory. Blog posts and announcements work a little differently and they must be configured first.

:question: **How do I add a new page?**

Create a new markdown file under `_pages`. To add it to the navbar, set the following frontmatter:

```
---
layout: page
title: My New Page
description: Some optional description
permalink: /some-path
nav: true
---

Content...
```

If you want to tweak the order of links in the nav bar, set `nav_order: x` where `x` is a number. Make sure to adjust other pages as well.

:question: **How do I add an image to a page?**

First add the file under `assets/img/file.png`. Then, in your markdown content you write:

```
![My figure caption](/assets/img/file.png)
```

:question: **How do I add the table of contents to a page?**

Add the following to the page's frontmatter:

```
toc:
  sidebar: left
```

Make sure to preserve the indentation. You can also set `sidebar: right`.

:question: **How do I change contact information and other site settings?**

Look through the file `_config.yml`. Most properties should be self-explanatory.

:question: **How do I set a custom domain?**

You need to change repository settings as well as modifying the `CNAME` file.
Please see the FAQ of [al-folio](https://github.com/alshedivat/al-folio).

:question: **What are page layouts?**

The layouts are the templates found in `_layouts`. Currently we have:

1. `layout: page` - General page which you probably will use the most.
2. `layout: about` - This is the layout of the home page.
3. `layout: default` - Base template used by other templates. You probably won't need this.
4. `layout: none` - Raw, unstyled content. You probably won't need this.

:question: **I need something else. Where can I learn more?**

See the readme of [al-folio](https://github.com/alshedivat/al-folio).
Also look for general resources on Jekyll.
If those don't help, open an issue and Edon will address it as soon as possible.
