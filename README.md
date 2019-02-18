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
  inserting the page content.
- `layouts/_default/single.html`: Default template for all other pages. This is actually identical to `layouts/index.html`.
- `content/*.md`: Various sample pages. Each contains a `menu` key if it should
  appear in the nav bar.
- `layouts/partials/head.html`: Common header. This contains `<head>` and the
  opening `<body>` tag, plus common header elements -- we build the nav bar
  here.
- `layouts/partials/foot.html`: Common footer. This contains any common footer
  elements and the closing `</body>` tag.
- `static/main.css`: A CSS file as an example of static content.

The division between `layouts/index.html`/`layouts/_default/single.html` and
the partials `head.html` and `foot.html` is not particularly elegant, but it
allows for a lot of flexibility.

Here are the common Hugo features we're **not** using:

- We don't use a theme
- We don't make (significant) use of any Markdown formatting
- List pages (which contain lists of all pages of a certain type)

## How to use this

- Install [Hugo](https://gohugo.io/)
- Run `hugo server` (or `hugo server --bind 0.0.0.0` if you want to expose the
  development server to other hosts)

## Where to go from here

Other features of Hugo that are useful for a static website:

- [Shortcodes](https://gohugo.io/content-management/shortcodes/), particularly
  how to create your own [shortcode templates](https://gohugo.io/templates/shortcode-templates/).
- [Hugo pipelines](https://gohugo.io/hugo-pipes/), which are particularly
useful for asset minification.
