---
layout: ~/layouts/MainLayout.astro
title: MPAs vs. SPAs
description: TODO
i18nReady: true
---

Understanding Multi-Page Application (MPA) architecture is key to understanding what makes Astro different from other web frameworks. 

## Terminology

**A Multi-Page Application (MPA)** is a website consisting of multiple HTML pages, linking to each other. Considered the traditional or default website architecture. Astro is an example of an MPA framework along with Ruby on Rails, Wordpress, Python Django, and PHP Laravel. Static site builders like Eleventy and Hugo will also build MPA-style websites.


**A Single-Page Application (SPA)** is a website consisting of a single JavaScript application that runs in the user's browser to render HTML locally. Next.js, Nuxt, SvelteKit, Remix, Gatsby, and Create React App are all examples of SPA frameworks.


## MPAs vs. SPAs

MPA websites rely heavily on HTML and CSS with only sprinkles of JavaScript on the page as needed for interactivity. Therefore, MPA websites will almost always load faster than SPAs because there is so little code required to run them in the user's browser.

SPA websites rely heavily on JavaScript to create the HTML (and sometimes CSS) on the page. Therefore, SPA almost always load slower than MPA websites. SPAs run locally in the browser, which has both benefits (offline-first! nice data management!) and downsides (scroll position complexity, managing the browser history, SEO limitations).

SPA frameworks like Next.js mitigate some of these costs with built-in features like server-side rendering (SSR). But ultimately, the SPA JavaScript application needs to load, parse, and run in the browser before any part of the page can become interactive. 

## Are MPAs Better than SPAs?

When comparing MPAs vs SPAs, there is no "better" or "worse" choice. It all comes down to tradeoffs.

Astro prioritizes the performance and simplicity of MPAs because it makes the most sense for our usecase of content-focused websites. Other types of websites, like dynamic web applications, may prefer the app-like functionality that SPAs bring at the the expense of performance.

## Case Studies

Below are all of the public Astro comparisons that we are aware of:

- [Astro vs. SPA (Next.js)](https://twitter.com/t3dotgg/status/1437195415439360003) - 94% less JavaScript
- [Astro vs. SPA (Next.js)](https://twitter.com/jlengstorf/status/1442707241627385860?lang=en) - 34% faster load
- [Astro vs. SPA (Remix, SvelteKit)](https://www.youtube.com/watch?v=2ZEMb_H-LYE&t=8163s) - "That [Lighthouse score] is incredible."
- [Astro vs. Qwik](https://www.youtube.com/watch?v=2ZEMb_H-LYE&t=8504s) - 43% faster TTI

If you know a public migration or benchmark and don't see it listed here, please create a PR to add it!
## More Resources 

If you'd like to learn more, Surma (Google) and Jake Archibald (Google) recorded a great back-and-forth discussion [on this exact topic.](https://www.youtube.com/watch?v=ivLhf3hq7eM)
