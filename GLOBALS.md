## Multi-environment properties of the global object

Properties of the global object are the entry-point to the Web's current JavaScript APIs, as built-in modules are not yet exposed. This page documents

### Conventions
- Only include APIs which have built-in support in at least two environments, at least one of which is the Web.
- Link to MDN for browser compatibility data (there is a multivendor effort to keep this data in good shape).
- Include at most a short note about compatibility inline, and use a separate Markdown file for more extensive notes.
- When possible, include information about support in the following embedding environments:
    - [Web](https://developer.mozilla.org/en-US/docs/Web/API)
    - [Node.js](https://nodejs.org/api/)
    - (please make PRs to add to this list! Should we add CloudFlare Workers, Windows Universal Apps, Moddable XS, etc?)

### URL

Spec: https://github.com/whatwg/url/

Environments supported:
- [Web](https://developer.mozilla.org/en-US/docs/Web/API/URL#Browser_compatibility)
- [Node.js](https://nodejs.org/api/url.html)

Compatibility: Node.js implements same interface, modulo brand checks and IDL mistakes in Node.js (TODO: be more specific)

### Encoding standard

Spec: https://github.com/whatwg/encoding

Environments supported:
- [Web](https://developer.mozilla.org/en-US/docs/Web/API/Encoding_API)
- Node.js: [TextEncoder](https://nodejs.org/api/util.html#util_class_util_textencoder) and [TextDecoder](https://nodejs.org/api/util.html#util_class_util_textdecoder)

Compatibility: Node.js does not support the `*Stream` encoding interfaces. The set of encoding supported by Node is dependent on compilation options; see Node documentation for more details.

### WebAssembly JS API

Spec: https://www.w3.org/TR/wasm-js-api-1/

Environments supported:
- [Web](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WebAssembly)
- Node.js: not documented yet
