# mdsvex-pages

Markdown-based documentation/blog generator built with [MDsveX](https://mdsvex.com/).
<br>
Currently supports [svelte-spa-router](https://github.com/ItalyPaleAle/svelte-spa-router) and [Sapper](https://sapper.svelte.dev/) (coming soon).
<br>
This is a template repo, if you want to try implementing the rollup plugin yourself, see [rollup-plugin-mdsvex-pages](https://github.com/knightss27/rollup-plugin-mdsvex-pages).

---
# How it works

Assuming your svelte project tree looks similar to:

```
├─── /src
│   ├─── main.js
│   ├─── App.svelte
│   ├─── /docs
│   │   └─── page1.md
│   │   └─── page2.md
```

mdsvex-pages will automatically generate [svelte-spa-router](https://github.com/ItalyPaleAle/svelte-spa-router) routes and convert the markdown files into parseable svelte files to be bundled. (using MDsveX's [compile](https://mdsvex.com/docs#use-it) function)

Because mdsvex-pages uses MDsveX, you can write valid Svelte code in the .md files. Additionally, I currently use .md files as the basis as that was what I wanted to parse for my own original usage, but options allow you to change this extension to `.svx` (as used by MDsveX in their docs) or `.anything`, so you can use whatever extension you prefer. 

---
# Setup

To start, clone this repo.

```bash
git clone https://github.com/knightss27/mdsvex-pages
cd mdsvex-pages
npm install
```  

In your `rollup.config.js` you can configure the options. Defaults are those listed below.

```js
export default {
...
plugins: [
  mdsvexPages({
    appName: 'App.svelte' // Path of the central svelte file, should include your Router component. Assumes you are in /src.
    docPath: 'docs' // Path of the .md pages folder. Assumes you are in /src.
    mdsvexOptions: { //You can configure any of the mdsvexOptions, and they will be passed to mdsvex.
      extensions: ['.md'] 
    }
  }),

  svelte({
  // Required for mdsvex-pages to work. Is already set in this repo. 
  extensions: [".svelte", ".md"],
  })
]};
```

In your App.svelte (or equivalent). Again, this is already set up in this repo.

```svelte
<script>
  import Router from 'svelte-spa-router'
  const routes = new Map();
</script>

<main>
  <h1>Hello world!</h1>
  <Router {routes} />
</main>
```
> ### NOTE: 
> You must be using the Map() version of svelte-spa-router, and it needs to be named `routes`.
> This allows you to make your own routes using the `routes.set(route, component)` syntax, and for mdsvex-pages to build on top.

Once this is set up, feel free to add as many .md pages to their folder as you'd like.
