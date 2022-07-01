---
layout: ~/layouts/MainLayout.astro
title: Why Astro?
description: DESCRIPTION
i18nReady: true
---

Astro is a **web framework** for building **fast**, **content-focused** websites. 

When or why do you need Astro? 

1. [You need to get content in front of users](#content-focused).

1. [You don't want decisions you make now to limit you later](#zero-lock-in).

<!-- alternative, positively-worded versions: 
You want to make low-consequence choices, with the flexibility to easily change direction.

You want the flexibility to try new things, without starting over from scratch.

You want to take advantage of a framework you know, but also have the option to experiment with something new.

-->

1. [You want to get started quickly, without a huge learning curve](#easy-to-learn-easy-to-use).

1. [You want your site to be fast, by default](#fast-by-default).

1. [You want control over what and how you build, but don't want to have to build everything yourself](#fully-featured-but-flexible). 


Here are five things that only Astro can give you.


## Content-focused

Astro was designed and optimized around a single use-case: content. This includes marketing sites, publishing sites, blogs, portfolios, most ecommerce sites... any website that exists to get content in front of its users.

This focus on content is surprisingly unique in modern web development. Most frameworks tend to focus on the other side of the spectrum: dynamic web applications. This includes dashboards, inboxes, social networks, todo lists, and even full applications like Figma and Ping. But, by thinking of every website as an entire application to be run, these frameworks can't separate out the concern (solved problem?) of simply displaying your content, something that HTML and CSS have been doing effectively and efficiently for decades.


<!--The theory is that if you think of every website as an application, then your framework is the right pick for every website. Unfortunately, in practice, this is incorrect. -->

By prioritizing for content, Astro is able to make better tradeoffs where other frameworks can't. Astro features like Selective Hydration and Zero Lock-in don't make sense in rich web applications. But, they make a ton of sense in most sites that, when you really look closely, only require sprinkles of interactivity. Astro focuses on the latter to deliver a better user experience with a great developer experience as well.

:::note
There's nothing wrong with those other frameworks! If you are building a rich web application or dealing with a lot of dynamic or interactive data, then a more traditional web framework like Next.js, Nuxt, or SvelteKit would probably be a great pick. However, after learning about Astro, many people realize they are in the other camp --- the "content" camp --- and Astro was designed for that!
:::


## Zero lock-in

Most web frameworks will lock you into a single UI framework. Next.js only works with React, SvelteKit only works with Svelte, Nuxt only works with Vue, etc. This creates **UI Framework Lock-in,** where the only way to try a different framework is to rewrite your entire project from scratch. Next.js users, for example, aren't able to experiment with adding Solid.js (the latest JSX framework) to their existing project.

Astro lets you **Bring Your Own Framework (BYOF).** React, Preact, Solid, Svelte, Vue, and LitHTML are all supported as official, first-class UI frameworks in Astro. Use your favorite with Astro, or mix-and-match across different sites, routes, or teams. You can even choose your UI framework component-by-component on each individual page for maximum flexibility with minimal committment. Astro also gives you a "Get out of (framework) jail free!" card, allowing you to convert your entire project incrementally, with no interruption to your site.

This has an added benefit for larger organizations: you can scale up the number of supported UI frameworks at your company without increasing the complexity of the server-side code. Every Astro site ships the same server runtime code, regardless of which UI frameworks you use. This greatly reduces the production complexity vs. running different sites built with Next.js, SvelteKit, and Nuxt.

- Link to Multi-framework support?

## Easy to learn, easy to use

Astro was designed to be **easy to learn** and **easy to use**. Our philosophy is that Astro should feel familiar to every web developer, regardless of skill or past experience using React, Vue, PHP, Rails, or just plain old HTML and CSS. 

To accomplish this, Astro ships its own file type: `.astro`. And we'll let you in on a little secret: it's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags.

One of our favorite sayings is: **opt in to complexity.** We designed Astro to remove as much "required complexity" as possible from the developer experience. Instead, you opt in to complexity over time, as you need it, with the extra functionality `.astro` files give you on top of HTML. 

For example:
- If you need to run some code in your Astro template, you can add a block of code to the top of the file (similar to a `<script>` tag in Svelte or Vue!). 
- If you need to map over some data in your template, you can add JSX-like template expressions right in your HTML (just like React, Preact, and Solid.js).
- If you need to fetch some data from an external API or a database, you can do it right in your template (no `loader()` or `<Suspense>` or `{#await}` boilerplate required).
- If you need a server, you can flip your Astro build output from a static site to an SSR-ready server deployment.


## Fast by default

Every web framework claims to be fast, but very few can actually deliver on this promise at scale. Astro takes this idea to the extreme, so that you don't even need to think about performance to build a fast site. Our goal was simple: **It should be incredibly difficult to build a slow website with Astro.**

To start, Astro strips all unused JavaScript from your website automatically, using a process called Selective Hydration. By default, your Astro website won't ship a single byte of JavaScript. Instead, you opt in, on a per-component basis, to the interactive bits of your site. The result? You only pay the performance cost to load what's absolutely needed. Most other web frameworks do the exact opposite: ship all of the JavaScript you wrote to the client, even if most of it is never used by the client.

This idea of fast-by-default has inspired plenty of other Astro design choices and default behaviors as well. Your JavaScript and CSS are bundled by default. Your deployed server supports streaming HTML by default. THIRD THING??? DON"T FORGET TO DELETE THIS, FRED. (//`@astrojs/prefetch` maybe?//) As you build with Astro, you'll see how these design decisions shape how you work "in Astro." 

(// my thinking with this last line here is re: stated goal of priming the reader for thinking about how things work in Astro. With little nudges like this, the reader is more primed for THIS WORKS DIFFERENTLY AND I MIGHT HAVE TO ADJUST MY EXPECTATIONS //)


## Fully-featured, but flexible

We are unapologetically opinionated about the things we care about: site performance, ease-of-use, reducing lock-in. We want Astro to handle all of the important bits of infrastructure for you, and then stay out of your way so that you can focus on building awesome sites.

Astro controls the essentials like routing, data fetching, and HTML rendering all out-of-the-box. But Astro is unopinionated and flexible when it comes to how you build your project. 

- Bring your own database, or make calls to an API! 
- Use GraphQL and TypeScript, or don't!
- Use Tailwind or any other favorite CSS library, or write `<style>` tags!
- Use your favorite UI framework(s), or just write `.astro`!
- Use your favorite npm packages, astro-specific integrations and more!

  

