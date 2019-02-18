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

- `layouts/index.html`: Root template, for the main page only. It is very
  minimal, delegating mostly to common header and footer templates, and
  inserting the page content. This does a few things:
    - We build the skeleton of the HTML page
    - We build a common header
    - We build a [menu bar](https://gohugo.io/content-management/menus/)
    - We build a common footer
- `layouts/_default/single.html`: Default template for all other pages. **This
  is identical to `layouts/index.html`**, so all pages of the site will be
  built from the same template.
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

## How to use this

- Install [Hugo](https://gohugo.io/)
- Run `hugo server` (or `hugo server --bind 0.0.0.0` if you want to expose the
  development server to other hosts)

## Where to go from here

This example is very, very minimal -- Hugo has many other features that help us
organize templats, or separate content from display logic:

- [Base templates](https://gohugo.io/templates/base/) can be used to break up
  the main template.
- [Partial templates](https://gohugo.io/templates/partials/) can be used to
  extract common functionality (the menu bar is a prime candidate for this).
- [Shortcodes](https://gohugo.io/content-management/shortcodes/), particularly
  how to create your own [shortcode templates](https://gohugo.io/templates/shortcode-templates/).
- [Hugo pipelines](https://gohugo.io/hugo-pipes/), which are particularly
  useful for asset minification.
- [Front matter](https://gohugo.io/content-management/front-matter/), the top
  section of each page in `content`, can help separate page structure from
  rendering a bit more.
