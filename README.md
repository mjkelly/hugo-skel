# Hugo Skeleton

This is a simple, minimal example of a website built with
[Hugo](https://gohugo.io/).

This may be interesting to you if you're content to write your own HTML,
CSS/SASS, and Javascript but want to make use of Hugo's templating features so
you can do things like maintain consistent headers and footers, automatically
generate nav bars, etc.

It's intended both as a basic demonstration of Hugo's templating features, and
as a skeleton directory you can copy to start new sites.

## Overview

- `layouts/_default/baseof.html`: This is the [base template](https://gohugo.io/templates/base/). We use this to define the layout for all pages.
  It does a few things:
    - We build the skeleton of the HTML page (doctype, `<html>` tags, etc)
    - We build a common header (with an `<h1>` tag)
    - We build a [menu bar](https://gohugo.io/content-management/menus/)
    - We build a common footer
- `layouts/index.html` and `layouts/_default/single.html`: These pages inherit
  from the base template above. They define the style for the root page ("/")
  and all other pages, respectively. (Both are necessary for Hugo to render
  these page types.) They are both identical, and both stubs.
- `content/*.html`: Various sample pages. These use HTML as the
  [content format](https://gohugo.io/content-management/formats/) because of
  their `.html` extension. Each contains a `menu` key if it should appear in
  the nav bar.
- `static/main.css`: A CSS file as an example of a
  [static file](https://gohugo.io/content-management/static-files/).

Here are the common Hugo features we're **not** using:

- We don't use a theme -- just the `layouts` directory.
- We don't make (significant) use of any Markdown formatting
- We don't define any list pages (which contain lists of all pages of a certain
  type).

### Notes

We _could_ avoid the use of a base template and just duplicate logic
`layouts/index.html` and `layouts/_default/single.html` -- that would simplify
things, but at the expense of duplicating things more.

## How to use this

- Install [Hugo](https://gohugo.io/)
- Run `hugo server` (or `hugo server --bind 0.0.0.0` if you want to expose the
  development server to other hosts)

## Where to go from here

This example is very, very minimal -- Hugo has many other features that help us
organize templates, or separate content from display logic:

- [Partial templates](https://gohugo.io/templates/partials/) can be used to
  extract common functionality (the menu bar is a prime candidate for this).
- [Shortcodes](https://gohugo.io/content-management/shortcodes/), particularly
  how to create your own [shortcode templates](https://gohugo.io/templates/shortcode-templates/).
- [Hugo pipelines](https://gohugo.io/hugo-pipes/), which are particularly
  useful for asset minification.
- [Front matter](https://gohugo.io/content-management/front-matter/), the top
  section of each page in `content`, can help separate page structure from
  rendering a bit more.
