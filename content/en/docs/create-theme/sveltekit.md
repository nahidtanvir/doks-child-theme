---
title: SvelteKit
description: Create Theme Using SvelteKit
lead: ''
date: 2020-10-06T08:48:23.000Z
lastmod: 2020-10-06T08:48:23.000Z
draft: false
images: []
menu: {docs: {parent: create-theme}}
weight: 770
toc: true
---

### src

```bash
src
│
├───lib
│   │
│   ├───Commons
│   │   │
│   │   ├───breadcrumbs
│   │   │   │   DefBreadcrumb.svelte
│   │   │   │   BreadcrumbTwo.svelte
│   │   │       ...
│   │   │
│   │   │   footer_menus
│   │   │   loaders
│   │   │   main_menus
│   │   │   sidebars
│   │   │   top_menus
│   │   │   back_to_top
│   │   │   error
│   │
│   ├───micro_views
│   │   │   buttons
│   │   │   form_fields
│   │   │   social_links
│   │   │   address_links
│   │   │   sections_headers
│   │       ...
│   │
│   ├───pages
│   │   ├───blog_pages
│   │   │   │   DefBlogPage.svelte
│   │   │       ...
│   │   │
│   │   │   post_pages
│   │   │   static_pages
│   │   │   ecommerce_pages
│   │   │   product_pages
│   │   │   category_pages
│   │   │   form_pages
│   │   │   poll_pages
│   │   │   survey_pages
│   │   │   survey_pages
│   │
│   ├───sections
│   │   │   SectionRender.svelte
│   │   │   heading
│   │   │   │   DefHeading.svelte
│   │   │       ...
│   │   │
│   │   │   content_slider
│   │   │   hero_section
│   │   │   left_right_image_section
│   │   │   fns_section
│   │   │   about_section
│   │   │   count_section
│   │   │   clients_section
│   │   │   testimonials_sections
│   │       ...
│
├───routes
│   │   +layout.js
│   │   +layout.svelte
│   │   +page.js
│   │   +page.svelte
│   │
│   ├───[...slug]
│   │   │   +page.js
│   │   │   +page.svelte
```

### static

```bash
static
│
└───assets
│   │
│   ├───css
│   ├───image
│   ├───vendor
│
├───designs
│   │
│   ├───sections
│   │   ├───about_sections.json
│   │   └───gallery_sections.json
│   │       ...
│   │
│   ├───pages
│   │   ├───blog_pages.json
│   │   └───post_pages.json
│   │       ...
│   │
```

#### json file structure

```json
{
  "DefFeatures": "Default Features Section",
  "DefServices": "Default Services Section",
  "ServicesTabs": "Services Section with Tabs"
}
```

### .env

```dotenv
PUBLIC_SECRET_KEY = 'your-api-key'
PUBLIC_DATA_SERVER = 'backend-api-route'
PUBLIC_APP_SERVER = 'deployment-url'
PUBLIC_DATA_MODE = 'dev-or-prod'
```

### .gitignore

```gitignore
.env
```
