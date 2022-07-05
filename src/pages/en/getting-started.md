---
setup: |
    import Button from '../../components/Button.astro'
    import ContributorList from '../../components/ContributorList.astro'
layout: ~/layouts/MainLayout.astro
title: Getting Started
description: A basic intro to Astro.
i18nReady: true
---

## What is Astro?

Astro is an **all-in-one** **web framework** for building **fast**, **content-focused** websites. 

#### Key Features

<br/>

- **Server runtime:** Astro runs on the server, generating fast HTML.
- **Use your favorite UI framework:** React, Preact, Vue, Svelte, Lit, and more.
- **No JavaScript runtime:** Astro includes zero bytes of JS, by default.
- **Selective hydration:** Individual components only load if needed.
- **Ultra-granular performance:** If a component is never visible, it never loads.
- **Filesystem routing:** Your codebase defines your routes.
- **Extensible:** Extend Astro with 100+ public integrations.

Considering Astro for your next project? Check out the [Why Astro](/en/concepts/why-astro/) breakdown to learn more. 


## Try Astro in your browser

Visit [astro.new](https://astro.new/) and choose from a variety of templates to get started. Play around with a full, working version of Astro right in your browser!

<div style="display: flex; flex-wrap: wrap; gap: 0.5rem;">
    <Button href="https://astro.new/basics?on=stackblitz">Quickstart!</Button>
    <Button variant="outline" href="https://astro.new/">View all templates →</Button>
</div>

## Start your first project

Get a new Astro project up and running locally in no time with our easy `create-astro` CLI wizard!

```bash
# create a new project with npm
npm create astro@latest

# or yarn
yarn create astro

# or pnpm
pnpm create astro@latest
```

Our [Installation Guide](/en/install/auto/) has full, step-by-step instructions for installing Astro using your favorite package manager.




## Learn Astro

See examples of some of the key concepts and patterns of an Astro site!

📚 [Add your first page](/en/core-concepts/astro-pages/) to your site.

📚 Read more about Astro’s [project structure](/en/core-concepts/project-structure/).

📚 Learn about Astro's [template directives](/en/reference/directives-reference/).

*... find more material under **Reference***


## Extend Astro

🧰 Start your next project with a [prebuilt theme](https://astro.build/themes/)

🧰 Customize your site with official and community [plugins and components](https://astro.build/integrations/).

🧰 Get inspired by visiting our [site showcase](https://astro.build/showcase/).

*... see our [guide to using integrations](/en/guides/integrations-guide/)*



## Join our Community

Join us in the [Astro Discord](https://astro.build/chat/) to share with and get help from an active, friendly community!

💬 Say hi in our `#introduce-yourself` channel!

💬 Ask our Support Squad a question in our `#support-threads` channel!

💬 Share what you've been working on in our `#showcase` channel!


## Learn More

[Astro Blog](https://astro.build/blog/)

[Astro changelog](https://github.com/withastro/astro/blob/main/packages/astro/CHANGELOG.md)

[Astro Migration guide](/en/migrate/)


## Contribute

These docs are brought to you by all these helpful people. [Join us on GitHub!](https://github.com/withastro/docs)

<ContributorList githubRepo="withastro/docs" />
