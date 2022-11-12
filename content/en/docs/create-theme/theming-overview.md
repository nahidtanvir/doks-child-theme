---
title: Theming Overview
description: Learn how to use our CMS
lead: ''
date: 2020-10-06T08:48:23.000Z
lastmod: 2020-10-06T08:48:23.000Z
draft: false
images: []
menu: {docs: {parent: create-theme}}
weight: 700
toc: true
---

You can use any frontend library or framework to create theme for the CMS. We provide all api endpoints required to make
a theme. However, we provide template for a few frameworks to make to process easier.

    project
    └───src
    └───static
    └───.env
    └───.gitignore

## Src

This folder should only contain layouts, pages and components. There are a number of page types and a theme can support
any number of them. Also, each page types can have their own layouts. The home page is generally always static type.
The dynamic catch-all route [..slug] takes care of all the other pages and their corresponding layouts.

    src
    │
    └───components
    │   │   Commons
    │   │   micro_views
    │   │   pages
    │   │   sections
    │
    └───routes
    │   │   layout
    │   │   page
    │   │   [...slug]

### Components

-   **Commons**: Contains components used in layouts.
-   **Sections**: Contains components used in pages.
-   **pages**: Contains components that is responsible for fetching section component data,
    calling section components and sometimes rendering the layout on top of that. Although in most cases rendering layout
    is done by layout of the framework.
-   **Micro Views**: Small component that are created to reduce the complexity of all the other components. These components
    are usually called from only components and not layouts or pages.

### Routes

-   **Layout**: Renders the layout of a page. It only contains common components. All the common/global settings are fetched from here.
-   **Page**: Responsible for fetching page data and pass them to the corresponding page type with section data fetch urls.

## Static

-   **Assets**: Contains all types of media files, documents and styles.
-   **Designs**: Contains component file name without extension and a name given by theme developer to be shown in CMS
    admin panel as key value pair. All these json files are used in order to render dropdowns in CMS admin panel as page
    type and section templates.

```bash
    static
    │
    └───assets
    │   │   media/doc
    │   │   style/vendor
    │
    └───designs
    │   │   pages
    │   │   sections
```

Json file example for `static/designs/sections/about_section.json`:

```json
{
  "DefFeatures": "Default Features Section",
  "DefServices": "Default Services Section",
  "ServicesTabs": "Services Section with Tabs"
}
```

Name of the json file need to exactly match the name of the corresponding section folder from `src/components/sections` or page folder from `src/components/pages`.

## .env

Add api keys, cms api root url, mode(dev/prod).

## .gitignore

Always add **.env** file here.
**Example**:

```gitignore
...
.env
.env.*
!.env.example
.DS_Store
node_modules
/build
/package
.vercel
.output
...
```

Any frontend Framework can be used for the CMS as long as the designs folder is provided inside the framework's static/public folder with exact json file names required by the CMS.
