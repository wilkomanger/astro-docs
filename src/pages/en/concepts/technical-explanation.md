---
layout: ~/layouts/MainLayout.astro
title: Technical Explanation
description: DESCRIPTION
i18nReady: true
---

When we talk about Astro, we are really talking about a few different things:

- The Astro language (`.astro` files)
- The Astro compiler
- The Astro runtime
- The Astro ecosystem (integrations, themes, etc.)

Together, these four layers combine to form a larger piece of software that we refer to as **The Astro Platform**. Unless specified otherwise, the word "Astro" alone is usually referring to the larger platform.

## The Astro language

- `.astro` files
- components
- bedrock of your site, connecting to routing and allowing you to hook in islands

## The Astro compiler

- takes Astro files and turns them into a JS function that returns HTML  
- handles style scoping, style and script extraction for later bundling, island creation, etc. 

## The Astro runtime

- Takes the compiler output, and runs it
- provides the `Astro` global, with different APIs
- handles routing, request handling, response handling, etc.

## The Astro ecosystem

- Astro can be extended through its ecosystem
- add renderers that add new framework support
- add adapters that help with deployment configuration
- add integrations that new routes, new features, etc.
