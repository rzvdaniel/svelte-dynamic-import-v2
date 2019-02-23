# Dynamic Runtime Component Import Example in Svelte

This is a project template for [Svelte] showcasing dynamically component loading at runtime.

The real thing here is that the sample component is not bundled at buildtime, but is added at a post build/deployment time.

The author of implementation is Rich Harris and his answer to a question about loading components dynamically at runtime in Svelte was posted on Stack Overflow:

Is it possible to dynamically load a Svelte template at runtime?
https://stackoverflow.com/a/50300657/778863

## Technical Details

The Chatbox.js is a simple Svelte component precompiled as ESM. Below you can see the required Rollup configuration:

```javascript
{
	sourcemap: true,
	format: 'esm',
	name: 'Chatbox',
	dir: 'public',
	isDynamicEntry: true
}
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*

## Get started

Clone the repository

```bash
git clone https://github.com/rzvdaniel/svelte-dynamic-import.git
```

Install the dependencies...

```bash
cd svelte-dynamic-import
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000).

Clicking the Chat button will load the Chatbox component dynamically.


