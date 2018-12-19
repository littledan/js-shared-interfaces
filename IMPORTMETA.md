## `import.meta` properties

The TC39 [import.meta](https://github.com/tc39/proposal-import-meta) 

### `url`

[From the HTML specification](https://html.spec.whatwg.org/#hostgetimportmetaproperties),
> the module script's base URL, serialized
At a high level, roughly, this means: the directory where the running module came from.

Environment support:
- [Shipping on the Web](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import.meta#Browser_compatibility)
- [Shipping in Node.js](https://nodejs.org/api/esm.html#esm_import_meta)

### `resolveURL`

Status: [Proposed](https://github.com/whatwg/html/issues/3871) for the web

### `require`

Status: Proposed for Node.js (TODO: link?)
