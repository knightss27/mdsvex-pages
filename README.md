# mdsvex-pages

Markdown-based documentation/blog generator built with [MDsveX](https://mdsvex.com/).
<br>
Currently supports [svelte-spa-router](https://github.com/ItalyPaleAle/svelte-spa-router) and [Sapper](https://sapper.svelte.dev/) (coming soon).
<br>
This is a sort of template repo, if you want to try implementing the rollup plugin yourself, see [rollup-plugin-mdsvex-pages](https://github.com/knightss27/rollup-plugin-mdsvex-pages).

---
# How it works

Assuming your svelte project tree looks similar to:

```
├─── /src
│   ├─── main.js
│   ├─── App.svelte
│   ├─── mdp.config.json
│   ├─── /docs
│   │   └─── page1.md
│   │   └─── page2.md
│   
├─── rollup.config.js
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

Look at [Setup](https://github.com/knightss27/rollup-plugin-mdsvex-pages#setup) for setting options and routes.
(Currently keeping this information there so I don't have to worry about keeping two very similar pages up to date)

