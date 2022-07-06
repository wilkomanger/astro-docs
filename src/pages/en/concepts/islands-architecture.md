---
layout: ~/layouts/MainLayout.astro
title: Islands
description: TODO
i18nReady: true
setup: |
  import IslandsDiagram from '~/components/IslandsDiagram.astro';
---

**Islands** are a web architectural pattern pioneered by Astro. The term was first coined by Etsy's frontend architect [Katie Sylor-Miller](https://twitter.com/ksylor) in 2019, and expanded on in [a post](https://jasonformat.com/islands-architecture/) by Preact creator Jason Miller.

Several new frameworks have directly embraced or expanded on Astro's work in this field, including [Deno's Fresh](https://fresh.deno.dev/), [Isles](https://github.com/ElMassimo/iles), [Capri](https://capri.build/), and others.

## What is an Island?

An island refers to an interactive UI component on an otherwise static page of HTML. An island renders in isolation using your favorite UI framework of choice (React, Svelte, Vue).

Think of these components as isolated islands in a sea of static, non-interactive HTML.

<IslandsDiagram>
    <Fragment slot="headerApp">Header (interactive island)</Fragment>
    <Fragment slot="sidebarApp">Sidebar (static HTML)</Fragment>
    <Fragment slot="main">
        Static content like text, images, etc.
    </Fragment>
    <Fragment slot="carouselApp">Image carousel (interactive island)</Fragment>
    <Fragment slot="footer">Footer (static HTML)</Fragment>
</IslandsDiagram>

The technical act of rendering individual components on your page is also known as **partial** or **selective hydration.** Astro was designed to take advantage of this technique behind the scenes. 

TODO: Talk about `client:` directives here and tie it all back together.

## How Do Islands Work in Astro?

**Astro generates every website with zero client-side JavaScript, by default.** Use a frontend UI component built with [React](https://reactjs.org/), [Preact](https://preactjs.com/), [Svelte](https://svelte.dev/), [Vue](https://vuejs.org/), [SolidJS](https://www.solidjs.com/), [AlpineJS](https://alpinejs.dev/) or [Lit](https://lit.dev/) and Astro will automatically render it to HTML at build-time and strip away all JavaScript. This keeps every site fast by default.

```astro
---
// Example: Use a static React component on the page, without JavaScript.
import MyReactComponent from '../components/MyReactComponent.jsx';
---
<!-- 100% HTML, Zero JavaScript! -->
<MyReactComponent />
```

But sometimes, client-side JavaScript is required for creating interactive UIs. When you find yourself needing interactive UI on the page, Astro doesn't force you to go 100% JavaScript on the entire page. Instead, Astro uses a technique called **selective hydration** that lets you hydrate individual components on the page. This way, you only send down the absolutely essential JavaScript that you need to run your page. 

```astro
---
// Example: Use a dynamic React component on the page.
import MyReactComponent from '../components/MyReactComponent.jsx';
---
<!-- This component is now interactive on the page! 
     The rest of your website remains the same. -->
<MyReactComponent client:load />
```

The vast majority of your site remains pure, lightweight HTML and CSS, with isolated **islands of interactivity.**

There are plenty of cases where you need an interactive UI component to run in the browser:

- An image carousel
- An auto-complete search bar
- A mobile sidebar open/close button
- A "Buy Now" button

In Astro, it’s up to you as the developer to explicitly opt in any components on the page that need to run in the browser. Astro will only hydrate exactly what’s needed on the page and leave the rest of your site as static HTML. This technique is known as **selective hydration**.

**Selective hydration is the secret to Astro’s fast-by-default performance story.**


## TODO

- Talk about SPAs and why Islands are hard/impossible
- Talk about react server components idea
- Talk about...