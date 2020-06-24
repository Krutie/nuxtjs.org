---
title: Routing francais
description: Most websites have more than just one page. For example a home page, about page, contact page etc. In order to show these pages we need a Router.
position: 2
category: Get Started
categoryPosition: 1
---
## Automatic Routes

Most websites have more than just one page. For example a home page, about page, contact page etc. In order to show these pages we need a Router. That's where `vue-router` comes in. Normally you would have to set up a configuration file and add all your routes manually to it. However, Nuxt.js automatically generates the `vue-router` configuration based on your provided Vue files inside the `pages` directory. That means you never have to write a router config again! Nuxt.js also gives you automatic code splitting for all your routes. 

In other words, all you have to do to have routing in your application is to create `.vue` files in the `pages` folder. 

➡️Learn more about Routing

## Navigation

To navigate between pages of your app, you should use the  `[<NuxtLink>](https://nuxtjs.org/api/components-nuxt-link)`  component. This component is included with Nuxt.js and therefore you don't have to import it like you do with other components. It is similar to the HTML `<a>` tag except that instead of using a `href="/about"` we use `to="/about"`.  If you have used `vue-router` before, you can think of the `<NuxtLink>` as a replacement for `<RouterLink>`

A simple link to the `index.vue` page in your `pages` folder:

```html
<template>
  <NuxtLink to="/">Home page</NuxtLink>
</template>
```

The `<NuxtLink>` component should be used for all internal links. That means for all links to the pages within your site you should use `<NuxtLink>`. The `<a>` tag should be used for all external links. That means if you have links to other websites you should use the `<a>` tag for those.

```html
<template>
  <main>
    <h1>Home page</h1>
    <NuxtLink to="/about">About (internal link that belongs to the Nuxt App)</NuxtLink>
    <a href="https://nuxtjs.org">External Link to another page</a>
  </main>
</template>
```

➡️Learn more about the `<NuxtLink>` component