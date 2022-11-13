---
title: Static Page Data
description: Learn the structure of the data fetched from CMS
lead: Section components are fetche from the CMS as static page data.
date: 2022-11-12T08:48:23.000Z
lastmod: 2022-11-12T08:48:23.000Z
draft: false
images: []
menu: {docs: {parent: create-theme}}
weight: 740
toc: true
---

## Section Components

### Hero

```json
{
  "name": "Homepage Hero Section",
  "type": "hero_sections",
  "design": "DefHero",
  "content": {
    "type": "custom",
    "title": "Lorem ipsum dolor",
    "highlight_text": "amet, consectetur adipiscing elit, sed do eiusmod",
    "paragraph": "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    "bg_image": "path/to/bg",
    "image": "path/to/image",
    "button_text": "Duis aute",
    "button_link": "href/of/anchor/tag"
  }
}
```
