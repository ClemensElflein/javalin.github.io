---
layout: default
title: JavalinVue Plugin
rightmenu: true
permalink: /plugins/javalinvite
---

<div id="spy-nav" class="right-menu" markdown="1">
- [Getting started](#getting-started)
- [Install and use npm packages](#install-and-use-npm-packages)
- [Build for production](#build-for-production)
</div>

<h1 class="no-margin-top">JavalinVite Plugin</h1>

The JavalinVite plugin allows us to rapidly build Javalin Apps while using any modern Javascript framework and any `npm` package.
It works by utilizing [Vite.js](https://vitejs.dev/) to supply a development server with hot-reloading and minified production builds.
When building for production, a single `.jar` file will be generated.

## Getting started
The easiest way to get started with JavalinVite is using the [template repository](https://github.com/javalin/javalin-vite-templates/tree/main).
- Hit the `Use this template` button.
- Check the `Include all branches` option.
- Merge the branch of the example you want to use into the main branch.
- Run the Main.kt file.

## Install and use npm packages
Install the npm package you want to install using `npm i -D hello-world-node-package`.
Run some code in `frontend/apps/app.js`
```javascript
import exports from 'hello-world-node-package'

exports.helloWorld()
```

## Build for production
Building for production is easy. Simply run

```
mvn package
```

to build the `.jar` file.

Now you can run your app by running

```
java -jar ./target/<artifactId>-<version>-jar-with-dependencies.jar PROD
```

Using the `PROD` argument makes sure that the prebuilt files from within the `jar` will be used.
