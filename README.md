# nuxt-vuetify-storyblok-demo

A Storyblok + Nuxt + Vuetify demo.

## Get your Storyblok Space with components and first page entry

1. Before you start - click the link below to generate your space.

-> [Click here to generate your free space](https://app.storyblok.com/#!/build/60004)

2. Copy the `preview` token from the dashboard of that space into your `nuxt.config.js` (Line:43)

```
['storyblok-nuxt', { accessToken: 'YOUR_PREVIEW_TOKEN', cacheProvider: 'memory' }],
```

3. Execute the following commands to spin up your local environment

```
npm install && npm run dev
```

4. Exchange the "Location" in your Storyblok space with your local address, eg. localhost:3000
   
5. Click on "Content" and press on "Home"

6. Enjoy editing

## Build Setup

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).
