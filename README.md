# mdsvex-pages

Markdown-based documentation/blog generator built with MDsveX.
<br>
Currently supports [svelte-spa-router](https://github.com/ItalyPaleAle/svelte-spa-router) and [Sapper](https://sapper.svelte.dev/) (coming soon).

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
  }),

  svelte({
  // Required for mdsvex-pages to work. Is already set in this repo. 
  extensions: [".svelte", ".md"],
  })
]};
```
