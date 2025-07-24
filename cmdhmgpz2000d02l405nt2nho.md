---
title: "Adding an APLOS Donate button to a managed WordPress site"
datePublished: Fri Jan 18 2019 00:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cmdhmgpz2000d02l405nt2nho
slug: adding-aplos-donate-button-to-managed-wordpress

---


# Adding an APLOS Donate button to a managed WordPress site
*January 18, 2019*

The blog post describes how to add an APLOS donate button to a managed WordPress site hosted by GoDaddy. The key challenges were:

1. WordPress strips out `<script>` tags from HTML widgets
2. The APLOS donate button requires a JavaScript snippet

## Solution Steps

- Used the "Scripts n Styles" WordPress plugin to globally add the JavaScript
- Added a link tag in the footer HTML widget 
- Bypassed WordPress's script stripping by using the plugin to insert the script

> "I occasionally help out with a website for a nonprofit, which is hosted by GoDaddy running on their managed WordPress platform."

The post provides a practical tutorial for web administrators dealing with restricted WordPress environments and third-party donation integration.