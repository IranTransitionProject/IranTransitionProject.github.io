# IranTransitionProject.github.io

Organization landing page for the [Iran Transition Project](https://irantransitionproject.org).

Built with Jekyll and deployed via GitHub Pages.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000

## Structure

- `index.html` -- Landing page
- `briefs/` -- Convergence briefs listing
- `blog/` -- Project blog (posts in `_posts/`)
- `technology/` -- Technical infrastructure overview
- `community/` -- Discussion forums, issue trackers, contributing guides

## Adding a blog post

Create a file in `_posts/` with the naming convention:

```
_posts/YYYY-MM-DD-title-slug.md
```

With frontmatter:

```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD
author: Your Name
---
```
