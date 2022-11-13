---
title: Layout Data
description: Learn the structure of the data fetched from CMS
lead: Site settings and common components are layout data fetche from the CMS.
date: 2022-11-12T08:48:23.000Z
lastmod: 2022-11-12T08:48:23.000Z
draft: false
images: []
menu: {docs: {parent: create-theme}}
weight: 730
toc: true
---

## Site Settings

```json
{
  "site_name": "Lorem ipsum dolor",
  "site_moto": "Duis aute irure dolor in reprehenderit",
  "site_logo": "path/to/log",
  "site_favicon": "path/to/favicon",
  "top_menu": 1,
  "main_menu": 1,
  "footer_menu": 1,
  "sidebar": 1,
  "default_home": null,
  "maintenance_mode": false
}
```

## Common Components

### Top Menu

```json
{
  "name": "Default Top Menu",
  "design": "DefTopMenu",
  "full_width": false,
  "show_search": false,
  "show_social_links": true,
  "language_switch": true,
  "dark_mode_switch": false,
  "show_current_date": true,
  "show_phone" : true,
  "show_email" : true,
  "show_address" : false,
  "menu_items": [
    {
      "item": {
        "title": "Blog",
        "url": "/blog",
        "open_in_new_tab": false
      },
      "sub_menu_items": []
    }
  ]
}
```

### Main Menu

```json
{
  "name": "Default Main Menu",
  "design": "DefMainMenu",
  "show_search": false,
  "show_notifications": false,
  "language_switch": false,
  "dark_mode_switch": false,
  "sidebar_toggle": true,
  "menu_items": [
    {
      "level": 1,
      "type": "custom_link",
      "link_text": "Home",
      "link_url": "/",
      "open_in_new_tab": false,
      "icon": ""
    },
    {
      "level": 1,
      "type": "custom_link",
      "link_text": "About",
      "link_url": "/#about",
      "open_in_new_tab": false,
      "icon": ""
    },
    ...
  ]
}
```

### Footer Menu

```json
{
  {
    "name": "Default Footer Menu",
    "design": "DefFooterMenu",
    "full_width": false,
    "title": "Footer menu",
    "is_active": true,
    "newsletter": true,
    "items": [
      {
        "type": "one_column_row",
        "value": [
          [
            {
              "type": "footer_text",
              "value": {
                "show_site_logo_or_name": "only_name",
                "show_social_links": false,
                "about_text": "Door to door delivery, air & sea freight, product sourcing & indenting, warehousing, cross trade services and L/C & TT support provider."
              }
            }
          ],
          [
            {
              "type": "footer_links",
              "value": [
                ...
                {
                  "title": "Services",
                  "url": "/#services",
                  "open_in_new_tab": false
                },
                ...
              ]
            }
          ]
        ]
      }
    ],
    "copyright_section": [
      {
        "type": "show_site_name",
        "value": true
      },
      {
        "type": "copyright_text",
        "value": "All rights reserved."
      },
      {
        "type": "show_current_year",
        "value": true
      }
    ]
  }
}
```

### Sidebar
