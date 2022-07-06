---
layout: ~/layouts/MainLayout.astro
title: Why Astro?
description: DESCRIPTION
i18nReady: true
---

Astro is an **all-in-one** **web framework** for building  **fast** **content-focused websites.**

Why choose Astro over another web framework? Here are five core design principles to help explain why we built Astro, the problems that it exists to solve, and why Astro may be the best choice for your project or team.

#### Astro is...

1. [Content-focused](#) -- Designed to build content-rich websites over not complex applications.
2. [Server-rendered](#) -- Websites work better when they do more work on the server.
3. [Extremely fast, always](#) -- It should be impossible to build a slow website in Astro.
4. [Easy to use](#) -- You don't need to be a JavaScript expert to build with Astro.
5. [Fully-featured, but flexible](#) -- Extend Astro with over 100+ integrations and UI frameworks.

<!-- 6. [Innovative](#) -- Astro is the leader in exploring a new islands-based site architecture. -->
<!-- 6. [Fast by default](#) -- It should be hard to build a slow website in Astro. -->
<!-- 4. [**Easy to learn, easy to use**](#) -- All youAstro was designed to support beginners and experts alike. -->

## Content-focused

**Astro excels at building content-rich websites.** We can proudly say that Astro is *the best framework* for building marketing sites, publishing sites, blogs, portfolios, and even some ecommerce sites. This is one of the most important things to understand about Astro because it influences so much of how Astro works. 

By contrast, most other web frameworks focus on the other side of the spectrum: building web applications. This includes things like interactive dashboards, inboxes, social networks, todo lists, and even full web apps running in your browser like Figma and Ping. 

If you are working with a ton of interactive data or long-lived logged-in experiences, then Astro probably isn't the right choice for your project. **And that's okay!** We are extremely proud of our laser-focus on content because it allows us to make unqiue tradeoffs for our users that other frameworks simply cannot. 



<!-- This focus on content over applications is surprisingly unique for a web framework. But it completely defines Astro as a framework, and is probably the most important thing to understand about Astro. By prioritizing for content, Astro is able to make tradeoffs and deliver features for this use-case where other frameworks cannot.  -->


<!-- Astro features like Selective Hydration and Zero Lock-in don't make sense in rich web applications. But, they make a ton of sense in most sites that, when you really look closely, only require sprinkles of interactivity. Astro focuses on the latter to deliver a better user experience with a great developer experience as well. -->

<!-- But, by thinking of every website as an entire application to be run, these frameworks can't separate out the concern (solved problem?) of simply displaying your content, something that HTML and CSS have been doing effectively and efficiently for decades. -->

<!--The theory is that if you think of every website as an application, then your framework is the right pick for every website. Unfortunately, in practice, this is incorrect. -->

<!-- :::note
There's nothing wrong with those other frameworks! If you are building a rich web application or dealing with a lot of dynamic or interactive data, then a more traditional web framework like Next.js, Nuxt, or SvelteKit would probably be a great pick. However, after learning about Astro, many people realize they are in the other camp --- the "content" camp --- and Astro was designed for that!
::: -->

## Server-rendered

Most web frameworks use an **SPA Architecture**, which stands for Single-Page Application. Next.js, SvelteKit, Nuxt, Remix, and other modern JavaScript frameworks use an SPA architecture because it supports building complex web applications with JavaScript. However, this power comes at the expense of complexity and performance tradeoffs that don't make much sense for content-focused websites.

Astro instead leverages an **MPA Architecture**, which stands for Multi-Page Application. This architecture is battle-tested and optimal for content-rich websites because it shifts work to the server and out of your users browser. 

Unlike an SPA like Next.js, Astro renders your JavaScript code to HTML on the server *without* also shipping the entire page's JavaScript code to your user's browser to render a second time. This improves page loading times, including the critical [Time to Interactive (TTI)](https://web.dev/interactive/) metric.

📚 [Read more about MPA Architecture and why Astro was built on it.](/en/concepts/mpa-vs-spa/)

<!-- We should use this somehow: https://youtu.be/2ZEMb_H-LYE?t=8163 -->

<!-- To start, Astro strips all unused JavaScript from your website automatically. When you build with Astro, you don't ship a single byte of unnecessary JavaScript to the user. Even if you use a JavaScript UI framework like React or Vue, your users will only ever see the fast, static, server-rendered HTML and CSS. -->

<!-- What happens when you need to add an interactive component to your page? Most web frameworks will be forced to download and run an entire page worth of JavaScript just for that one component. Astro websites only pay to load that one, interactive component.  -->

<!-- This process is called Selective Hydration, and very few web frameworks besides Astro support it today. -->



## Extremely fast, always

Having good performance is always important, but it is *especially critical* for content-focused websites. The data backs this up: poor performance leaves engagement, conversion, and money on the table:

- Every 100ms faster → 1% more conversions ([Mobify](https://web.dev/why-speed-matters/), earning +$380,000/yr)
- 50% faster → 12% more sales ([AutoAnything](https://www.digitalcommerce360.com/2010/08/19/web-accelerator-revs-conversion-and-sales-autoanything/))
- 20% faster → 10% more conversions ([Furniture Village](https://www.thinkwithgoogle.com/intl/en-gb/marketing-strategies/app-and-mobile/furniture-village-and-greenlight-slash-page-load-times-boosting-user-experience/))
- 40% faster → 15% more sign-ups ([Pinterest](https://medium.com/pinterest-engineering/driving-user-growth-with-performance-improvements-cfc50dafadd7))
- 850ms faster → 7% more conversions ([COOK](https://web.dev/why-speed-matters/))
- 1 seconds slowness → 10% less users ([BBC](https://www.creativebloq.com/features/how-the-bbc-builds-websites-that-scale))

Astro's magic is in how it combines the two points above -- a content focus with an MPA architecture -- to deliver features and performance unmatched by most other frameworks. An Astro website can [load 40% faster with 90% less JavaScript](https://twitter.com/t3dotgg/status/1437195415439360003) than the same site built with the most popular React web framework. This possible because Astro is able to make tradeoffs for performance that an SPA framework simply cannot.

But don't just take our word for it: Watch Astro's performance on a brutal benchmark leave Ryan Carniato (creator of Solid.js and Marko) [absolutely speechless](https://youtu.be/2ZEMb_H-LYE?t=8163).
<!-- ## Unapologetically server-rendered

Astro fully embraces the benefits (and tradeoffs) of server rendering.

If you are coming from a server language like PHP or Rails, Astro's server rendering will feel familiar. If you're coming from a JavaScript application framework like Next.js, then it may feel a bit unusual at first. 

Modern JavaScript application frameworks like Next.js are designed to run **isomorphically** on both the client and the server. When you build your website with one of these frameworks, you are essentially building an optimized Single Page Application, or SPA. EXPLAIN BENEFITS OF SPAs.

Astro isn't like other frameworks. Instead of building you an SPA, Astro builds you an MPA, or Multi Page Application. MPAs rely on server routing and rendering to do most of the work, with the user loading HTML from your site as they navigate from page to page.

MPAs have some serious benefits for the content-focused website (it's fast!) while SPAs are usually a better fit for more dynamic web applications. This is why Astro's content focus is so important to understand: MPAs are a better fit for Astro,  -->

<!-- and the tradeoffs that Astro can make happily.  -->

<!-- - It's fast.
- It's less complex: Make database reads and writes directly in your components.
- It's less boilerplate: With direct DB access, there's no need to create REST or GraphQL APIs. -->
## Easy to use

Early on, we decided to avoid Astro becoming an experts-only tool. We wanted Astro to feel familiar and approachable to every developer, regardless of skill or past experience. To do this, we created our own component syntax for server rendering HTML.

<!-- You should just get the amazing performance for free, on by default no matter what you do. -->

Astro's `.astro` component syntax takes inspiration from some of our favorite UI frameworks. Astro is a superset of HTML, meaning that any snippet of HTML can be a valid Astro component (just like Svelte and Vue). **If you know HTML, then you already know Astro!** When you need to render data in your template, you can use JSX-like template expressions (just like React).

Because Astro was designed for the server, it's incredibly simple by design.  You don't need to worry about hooks (React), stale closures (also React), refs (Vue), observables (Svelte), atoms, selectors, reactions, or derivations. All reactivity concerns disappear when you only care about server rendering your Astro components to HTML.

When you need an interactive component in the browser, you can still reach for your favorite UI framework. React, Svelte, Vue and others are all a great match with Astro when you need them.


<!-- borrowed our favorite features from JSX, Vue, Svelte, and even older server-side languages like PHP and Ruby. -->
<!-- The result was the Astro component syntax... aka the `.astro` filetype.  -->
<!-- https://indepth.dev/posts/1280/exploring-the-state-of-reactivity-patterns-in-2020 -->



<!-- shouldn't  easy for anyone to We design Astro should feel familiar to every web developer, regardless of skill or past experience using React, Vue, PHP, Rails, or just plain old HTML and CSS.  -->

<!-- 
To accomplish this, Astro ships its own file type: `.astro`. And we'll let you in on a little secret: it's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags. -->

<!-- One of our favorite sayings is: **opt in to complexity.** We designed Astro to remove as much "required complexity" as possible from the developer onboarding experience. You can build a "Hello World" example website in Astro with just HTML and a little CSS. -->

<!-- As you build with Astro, you opt in to complexity over time as you need it. To do this, Astro ships its own file type: `.astro`. It starts as HTML -- any HTML is valid `.astro` syntax! -- which makes Astro a great choice to learn the fundamentals of web development. Then, as you go, you can add features to your `.astro` file as needed: server-side code blocks, JSX-like template expressions, top-level async-await, data fetching, etc. -->

<!-- If you need a server that can run in production, you can flip Astro from building a static site to an SSR-ready server deployment. But until then, you can enjoy the simplicity of Astro's default simple static build output. -->


<!-- 
If you've never seen this file extension before, don't worry. And we'll let you in on a little secret: it's just HTML. Any valid HTML is valid Astro syntax. You could even build an entire Astro website with just HTML, CSS `<style>` tags and JavaScript `<script>` tags.

 Astro's 
For example:
- If you need to run some code in your Astro template, you can add a block of code to the top of the file (similar to a `<script>` tag in Svelte or Vue!). 
- If you need to map over some data in your template, you can add JSX-like template expressions right in your HTML (just like React, Preact, and Solid.js).
- If you need to fetch some data from an external API or a database, you can do it right in your template (no `loader()` or `<Suspense>` or `{#await}` boilerplate required).
- If you need a server, you can flip your Astro build output from a static site to an SSR-ready server deployment. -->

## Fully-featured, but flexible

Astro comes out-of-the-box with several features that you will need to build your website. Astro comes built-in with a component templating system, file-based routing, asset handling, bundling, build optimizations, data fetching and more. You can build a complete website without ever reaching outside of Astro.

Astro can also be extended further with over [100+ integrations](https://astro.build/integrations/) like [React](https://www.npmjs.com/package/@astrojs/react), [Svelte](https://www.npmjs.com/package/@astrojs/svelte), [Vue](https://www.npmjs.com/package/@astrojs/vue), [Tailwind CSS](https://www.npmjs.com/package/@astrojs/tailwind), [MDX](https://www.npmjs.com/package/@astrojs/mdx), [image optimizations](https://www.npmjs.com/package/@astrojs/images), and more. [Connect your favorite CMS](https://astro.build/integrations/) or [deploy to your favorite host](https://www.npmjs.com/package/@astrojs/netlify) with just a single command.

Where other SPA frameworks lock you into a single UI framework for your entire project, Astro lets you **Bring Your Own Framework (BYOF).** React, Preact, Solid, Svelte, Vue and Lit are all officially supported in Astro. You can even mix-and-match different frameworks on the same page, allowing for an easy migration in the future without framework lock-in.

<!-- Use your favorite UI framework with Astro, or mix-and-match UI components across different pages, websites, or even teams. You can even choose your UI framework component-by-component on each individual page for maximum flexibility with minimal committment. Astro also gives you a "Get out of (framework) jail free!" card, allowing you to convert your entire project incrementally, with no interruption to your site. -->

<!-- This has an added benefit for larger organizations: you can scale up the number of supported UI frameworks at your company without increasing the complexity of the server-side code. Every Astro site ships the same server runtime code, regardless of which UI frameworks you use. This greatly reduces the production complexity vs. running different sites built with Next.js, SvelteKit, and Nuxt. -->

📚 TODO: Link to Multi-framework support? 

<!-- ## Fast by default -->

<!-- As we mentioned above, Astro builds fast websites. But our focus on performance isn't just on what's *possible* with Astro. We want good performance to be an *automatic default.*  -->

<!-- When we built Astro, we were fed up with web frameworks that *could* be fast in the right hands, but that otherwise felt slow to the average user who didn't know every option or best practice. We had a wild idea: you shouldn't even need to think about performance to build a fast site. Our goal was simple: **It should be incredibly difficult to build a slow website with Astro.** -->

<!-- This idea of fast-by-default has inspired plenty of other Astro design choices and default behaviors, other than Selective Hydration which was mentioned above. Your JavaScript and CSS are bundled by default. Your deployed server supports streaming HTML by default. THIRD THING??? DON"T FORGET TO DELETE THIS, FRED. (//`@astrojs/prefetch` maybe?//) As you build with Astro, you'll see how these design decisions shape how you work "in Astro."  -->

<!-- (// my thinking with this last line here is re: stated goal of priming the reader for thinking about how things work in Astro. With little nudges like this, the reader is more primed for THIS WORKS DIFFERENTLY AND I MIGHT HAVE TO ADJUST MY EXPECTATIONS //) -->



