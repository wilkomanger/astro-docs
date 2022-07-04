---
layout: ~/layouts/MainLayout.astro
title: Why Astro?
description: DESCRIPTION
i18nReady: true
---

Astro is an **all-in-one** **web framework** for building  **fast**, **content-focused websites.**

Why choose Astro over any other web framework? Here are six core design principles to help explain why Astro exists and when Astro may be the best choice for your project or team. 

<br />

1. [**Content-focused**](#) -- Designed to build fast websites, not complex applications.
2. [**Extremely fast**](#) -- Ships 0 bytes of JavaScript by default.
3. [**Unapologetically server-rendered**](#) -- Do as much work on the server as possible.
4. [**Easy to learn, easy to use**](#) -- Minimal API designed for easy onboarding.
5. [**Fully-featured, but flexible**](#) -- Extend Astro with over 100+ integrations and UI frameworks.
6. [**Fast by default**](#) -- It should be hard to build a slow website in Astro.

<br />

If any of these sound interesting to you, give Astro a try!

## Content-focused

Astro was designed and optimized around a single use-case: content. This includes marketing sites, publishing sites, blogs, portfolios, and most ecommerce sites. Basically, Astro is best at building websites that mainly exist to display content to the user for consumption and/or interaction.

Most web frameworks focus on the other side of the spectrum: web applications. This includes things like interactive dashboards, inboxes, social networks, todo lists, and even full web apps running in your browser like Figma and Ping. 

This focus on content over applications is surprisingly unique for a web framework. But it completely defines Astro as a framework, and is probably the most important thing to understand about Astro. By prioritizing for content, Astro is able to make tradeoffs and deliver features for this use-case where other frameworks cannot. 


<!-- Astro features like Selective Hydration and Zero Lock-in don't make sense in rich web applications. But, they make a ton of sense in most sites that, when you really look closely, only require sprinkles of interactivity. Astro focuses on the latter to deliver a better user experience with a great developer experience as well. -->

<!-- But, by thinking of every website as an entire application to be run, these frameworks can't separate out the concern (solved problem?) of simply displaying your content, something that HTML and CSS have been doing effectively and efficiently for decades. -->

<!--The theory is that if you think of every website as an application, then your framework is the right pick for every website. Unfortunately, in practice, this is incorrect. -->

<!-- :::note
There's nothing wrong with those other frameworks! If you are building a rich web application or dealing with a lot of dynamic or interactive data, then a more traditional web framework like Next.js, Nuxt, or SvelteKit would probably be a great pick. However, after learning about Astro, many people realize they are in the other camp --- the "content" camp --- and Astro was designed for that!
::: -->


## Extremely fast

Every web framework claims to be fast, but very few actually deliver on this point like Astro. 

To start, Astro strips all unused JavaScript from your website automatically. When you build with Astro, you don't ship a single byte of unnecessary JavaScript to the user. Even if you use a JavaScript UI framework like React or Vue, your users will only ever see the fast, static, server-rendered HTML and CSS.

What happens when you need to add an interactive component to your page? Most web frameworks will be forced to download and run an entire page worth of JavaScript just for that one component. Astro websites only pay to load that one, interactive component. 

The results speak for themselves: A website built in Astro can [load 40% faster with 90% less JavaScript](https://twitter.com/t3dotgg/status/1437195415439360003) than the same site built with the most popular React framework.

<!-- This process is called Selective Hydration, and very few web frameworks besides Astro support it today. -->



## Unapologetically server-rendered

Astro fully embraces the benefits (and tradeoffs) of server rendering.

If you are coming from a server language like PHP or Rails, Astro's server rendering will feel familiar. If you're coming from a JavaScript application framework like Next.js, then it may feel a bit unusual at first. 

Modern JavaScript application frameworks like Next.js are designed to run **isomorphically** on both the client and the server. When you build your website with one of these frameworks, you are essentially building an optimized Single Page Application, or SPA. EXPLAIN BENEFITS OF SPAs.

Astro isn't like other frameworks. Instead of building you an SPA, Astro builds you an MPA, or Multi Page Application. MPAs rely on server routing and rendering to do most of the work, with the user loading HTML from your site as they navigate from page to page.

MPAs have some serious benefits for the content-focused website (it's fast!) while SPAs are usually a better fit for more dynamic web applications. This is why Astro's content focus is so important to understand: MPAs are a better fit for Astro, 

<!-- and the tradeoffs that Astro can make happily.  -->

<!-- - It's fast.
- It's less complex: Make database reads and writes directly in your components.
- It's less boilerplate: With direct DB access, there's no need to create REST or GraphQL APIs. -->
## Easy to learn, easy to use

Astro was designed to be **easy to learn** and **easy to use**. Our philosophy is that Astro should feel familiar to every web developer, regardless of skill or past experience using React, Vue, PHP, Rails, or just plain old HTML and CSS. 

<!-- 
To accomplish this, Astro ships its own file type: `.astro`. And we'll let you in on a little secret: it's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags. -->

One of our favorite sayings is: **opt in to complexity.** We designed Astro to remove as much "required complexity" as possible from the developer onboarding experience. You can build a "Hello World" example website in Astro with just HTML and a little CSS.

As you build with Astro, you opt in to complexity over time as you need it. To do this, Astro ships its own file type: `.astro`. It starts as HTML -- any HTML is valid `.astro` syntax! -- which makes Astro a great choice to learn the fundamentals of web development. Then, as you go, you can add features to your `.astro` file as needed: server-side code blocks, JSX-like template expressions, top-level async-await, data fetching, etc.

If you need a server that can run in production, you can flip Astro from building a static site to an SSR-ready server deployment. But until then, you can enjoy the simplicity of Astro's default simple static build output.


<!-- 
If you've never seen this file extension before, don't worry. And we'll let you in on a little secret: it's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags.

 Astro's 
For example:
- If you need to run some code in your Astro template, you can add a block of code to the top of the file (similar to a `<script>` tag in Svelte or Vue!). 
- If you need to map over some data in your template, you can add JSX-like template expressions right in your HTML (just like React, Preact, and Solid.js).
- If you need to fetch some data from an external API or a database, you can do it right in your template (no `loader()` or `<Suspense>` or `{#await}` boilerplate required).
- If you need a server, you can flip your Astro build output from a static site to an SSR-ready server deployment. -->

## Fully-featured, but flexible

Astro comes out-of-the-box with everything that you need to build a fast, modern website. Extend Astro with over [100+ integrations](https://astro.build/integrations/) like [React](https://www.npmjs.com/package/@astrojs/react), [Svelte](https://www.npmjs.com/package/@astrojs/svelte), [Vue](https://www.npmjs.com/package/@astrojs/vue), [Tailwind CSS](https://www.npmjs.com/package/@astrojs/tailwind), [MDX](https://www.npmjs.com/package/@astrojs/mdx), [images](https://www.npmjs.com/package/@astrojs/images), and more. [Connect your favorite CMS](https://astro.build/integrations/) or [deploy to your favorite host](https://www.npmjs.com/package/@astrojs/netlify) with just a single command.

Most web frameworks will lock you into a single UI framework. Next.js only works with React, SvelteKit only works with Svelte, Nuxt only works with Vue, etc. Astro lets you **Bring Your Own Framework (BYOF).** React, Preact, Solid, Svelte, Vue, and LitHTML are all supported as official, first-class UI frameworks in Astro. 

Use your favorite UI framework with Astro, or mix-and-match UI components across different pages, websites, or even teams. You can even choose your UI framework component-by-component on each individual page for maximum flexibility with minimal committment. Astro also gives you a "Get out of (framework) jail free!" card, allowing you to convert your entire project incrementally, with no interruption to your site.

This has an added benefit for larger organizations: you can scale up the number of supported UI frameworks at your company without increasing the complexity of the server-side code. Every Astro site ships the same server runtime code, regardless of which UI frameworks you use. This greatly reduces the production complexity vs. running different sites built with Next.js, SvelteKit, and Nuxt.

- Link to Multi-framework support? 

## Fast by default

As we mentioned above, Astro builds fast websites. But our focus on performance isn't just on what's *possible* with Astro. We want good performance to be an *automatic default.* 

When we built Astro, we were fed up with web frameworks that *could* be fast in the right hands, but that otherwise felt slow to the average user who didn't know every option or best practice. We had a wild idea: you shouldn't even need to think about performance to build a fast site. Our goal was simple: **It should be incredibly difficult to build a slow website with Astro.**

This idea of fast-by-default has inspired plenty of other Astro design choices and default behaviors, other than Selective Hydration which was mentioned above. Your JavaScript and CSS are bundled by default. Your deployed server supports streaming HTML by default. THIRD THING??? DON"T FORGET TO DELETE THIS, FRED. (//`@astrojs/prefetch` maybe?//) As you build with Astro, you'll see how these design decisions shape how you work "in Astro." 

(// my thinking with this last line here is re: stated goal of priming the reader for thinking about how things work in Astro. With little nudges like this, the reader is more primed for THIS WORKS DIFFERENTLY AND I MIGHT HAVE TO ADJUST MY EXPECTATIONS //)



