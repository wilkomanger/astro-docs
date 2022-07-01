---
layout: ~/layouts/MainLayout.astro
title: Why Astro
description: DESCRIPTION
i18nReady: true
---

Astro is a **web framework** for building **fast**, **content-focused** websites. 

Curious to learn when or why you need Astro? Here are six things that make Astro unique and possibly well-suited to your next project.


## Content-focused

Astro was designed and optimized around a single use-case: content. This includes marketing sites, publishing sites, blogs, portfolios, most ecommerce sites, and basically any website that exists to get content in front of its users.

This focus on content is surprisingly unique compared to other web frameworks. Most frameworks tend to focus on the other side of the spectrum: dynamic web applications. This includes dashboards, inboxes, social networks, todo lists, and even full applications like Figma and Ping. The theory is that if you think of every website as an application, then your framework is the right pick for every website. Unfortunately, in practice, this is incorrect.

By prioritizing for content, Astro is able to make better tradeoffs where other frameworks can't. Astro features like Selective Hydration and Zero Lock-in don't make sense in rich web applications, but they make a ton of sense in more straightforward website. Astro focuses on the latter to deliver a better user experience with a great developer experience as well.

:::note
There's nothing wrong with those other frameworks! If you are building a rich web application or dealing with a lot of dynamic or interactive data, then a more traditional web framework like Next.js, Nuxt, or SvelteKit would probably be a great pick. However, if you're in the other camp, the "content" camp, then Astro is definitely worth checking out.
:::


## Zero lock-in

Most web frameworks will lock you into a single UI framework. Next.js only works with React, SvelteKit only works with Svelte, Nuxt only works with Vue, etc. etc. This creates **UI Framework Lock-in,** where the only way to try a different framework is to rewrite your entire project from scratch. Next.js users, for example, aren't able to try out Solid.js (the latest JSX framework) without starting a new project.

Astro lets you **Bring Your Own Framework (BYOF).** React, Preact, Solid, Svelte, Vue, and LitHTML are all supported as official, first-class UI frameworks in Astro. Not only can you use your favorite with Astro, but you can even mix-and-match across different sites, routes, and even individually on each page. 

This has an added benefit for larger organizations: you can scale up the number of supported UI frameworks at your company without increasing the complexity of the server-side code. Every Astro site ships the same server runtime code, regardless of which UI frameworks you use. This greatly reduces the production complexity vs. running different sites built with Next.js, SvelteKit, and Nuxt.

- Link to Multi-framework support?

## Easy to learn, easy to use

Astro was designed to be **easy to learn** and **easy to use**. Our philosophy is that Astro should feel familiar to every web developer, regardless of skill or past experience using React, Vue, PHP, Rails, or just plain old HTML and CSS. 

To accomplish this, Astro ships its own file type: `.astro`. This may feel unfamiliar, until you realize the most important thing about Astro files: It's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags.

One of our favorite sayings is: **opt-in to complexity.** We designed Astro to remove as much "required complexity" as possible from the developer experience. Instead, you opt-in to complexity over time, as you need it. 

For example:
- If you need to run some code in your Astro template, you can add a block of code to the top of the file (similar to a `<script>` tag in Svelte or Vue!). 
- If you need to map over some data in your template, you can add JSX-like template expressions right in your HTML (just like React, Preact, and Solid.js).
- If you need to fetch some data from an external API or a database, you can do it right in your template (no `loader()` or `<Suspense>` or `{#await}` boilerplate required).
- If you need a server, you can flip from your Astro build output from a static site to an SSR-ready server deployment.


## Fast by default

Every web framework claims to be fast, but very few can actually deliver on this promise at scale. Astro takes this idea to the extreme, so that you don't even need to think about performance to build a fast site. Our goal was simple: **It should be incredibly difficult to build a slow website with Astro.**

To start, Astro strips all unused JavaScript from your website automatically, using a process called Selective Hydration. By default, your Astro website won't ship a single byte of JavaScript. Instead, you opt-in the interactive bits of your site and only pay the performance cost to load what's absolutely needed. Most other web frameworks do the exact opposite: ship all of the JavaScript you wrote to the client, even if most of it is never used.

This idea of fast-by-default has inspired plenty of other Astro design choices and default behaviors as well. Your JavaScript and CSS are bundled by default. Your deployed server supports streaming HTML by default. THIRD THING??? DON"T FORGET TO DELETE THIS, FRED.


## Fully-featured, but flexible

As you can see from the above, we are unapologetically opinionated about the things we care about: site performance, ease-of-use, reducing lock-in. We want Astro to handle all of the important bits of infrastructure for you, and then stay out of your way so that you can focus on building awesome things.

Astro controls the essential things like routing, data fetching, and HTML rendering all out-of-the-box. But Astro is unopinionated and flexible when it comes to how you build your website. 

- Bring your own database, or make calls to an API! 
- Use GraphQL and TypeScript, or don't!
- Use Tailwind or any other favorite CSS library.
- Use your favorite UI frameworks (see above).
- Use your favorite npm packages.

  

