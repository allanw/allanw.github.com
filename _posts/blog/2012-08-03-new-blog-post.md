---
layout: article
published: true
categories:
- blog
---

# How does it work?

In order to get started with Prose Bootstrap, all you have to do is forking the [repository](http://github.com/prose/bootstrap) and make your own adjustments.

# Adjust Configuration

Make sure you setup `_config.yml` correctly.

If your page lives under `http://username.github.com/sitename` your config.yml looks like this:

    auto: true
    server: true
    permalink: none
    baseurl: "sitename"
    exclude:
    - .gitignore
    - README.md