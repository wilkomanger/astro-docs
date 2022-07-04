---
layout: ~/layouts/MainLayout.astro
title: Islands
description: TODO
i18nReady: true
setup: |
  import IslandsDiagram from '~/components/IslandsDiagram.astro';
---

**Islands architecture** is the idea of using selective hydration to build entire websites. Islands architecture is an alternative to the common process of building your website into a client-side JavaScript bundle that must be shipped to the user.

> The general idea of an “Islands” architecture is deceptively simple: render HTML pages on the server, and inject placeholders or slots around highly dynamic regions.
> <br/> -- [Islands Architecture: Jason Miller](https://jasonformat.com/islands-architecture/)

Besides the obvious performance benefits of sending less JavaScript down to the browser, there are two key benefits to islands architecture:

- **Components load individually.** A lightweight component (like a sidebar toggle) will load and render quickly without being blocked by the heavier components on the page.
- **Components render in isolation.** Each part of the page is an isolated unit, and a performance issue in one unit won't directly affect the others.

<IslandsDiagram>
    <Fragment slot="headerApp">Header "app"</Fragment>
    <Fragment slot="sidebarApp">Sidebar "app"</Fragment>
    <Fragment slot="main">
        Server-rendered HTML content like text, images, etc.
    </Fragment>
    <Fragment slot="carouselApp">Image carousel "app"</Fragment>
    <Fragment slot="advertisement">Advertisement<br/>(server-rendered)</Fragment>
    <Fragment slot="footer">Footer (server-rendered HTML)</Fragment>
</IslandsDiagram>

_Source: [Islands Architecture: Jason Miller](https://jasonformat.com/islands-architecture/)_
