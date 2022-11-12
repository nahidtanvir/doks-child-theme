---
title : "Theming Overview"
description: "Learn how to use our CMS"
lead: ""
date: 2020-10-06T08:48:23+00:00
lastmod: 2020-10-06T08:48:23+00:00
draft: false
images: []
menu:
  docs:
    parent: "create-theme"
weight: 700
toc: true
---

You can use any frontend library or framework to create theme for the CMS. We provide all api endpoints required to make
a theme. However, we provide template for a few frameworks to make to process easier.

## Project Structure

```
project
└───src
└───static
└───.env
└───.gitignore
```

### src

This folder should only contain layouts, pages and components. There are a number of page types and a theme can support
any number of them. Also, each page types can have their own layouts. The home page is generally always static type.
The dynamic catch-all route [..slug] takes care of all the other pages and their corresponding layouts.

```
src
│
└───lib
│   │   Commons
│   │   micro_views
│   │   pages
│   │   sections
│
└───routes
│   │   layout
│   │   page
│   │   [...slug]
```
