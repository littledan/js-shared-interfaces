This document aims to list places where an API to address similar use cases is developed differently in different environments. These differences sometimes make it hard to write code which spans environments, and sometimes justify investigation into a shared solution.

This initial document includes Node and Web APIs, but PRs are welcome to document additional environments as well. Some of the entries here may be poor analogies--if so, please make a PR to clarify things!

For interfaces to be considered analogous, there should be some evidence that developers today are using them in a shared way today, e.g., a widely-used polyfill of one in terms of the other, or a widely-used higher-level API based on them both.

## Event handling

- **Purpose**: Register callbacks for certain events
- **Web API**: [EventTarget](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget)
- **Node.js API**: [EventEmitter](https://nodejs.org/api/events.html)
- **Mitigation strategies**: TODO (Observables? Polyfills? How do programmers write isomorphic code today?)

## Streams

- **Purpose**: Incremental access to binary data, e.g., from over the network
- **Web API**: [WHATWG Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API)
- **Node.js API**: [Node Streams](https://nodejs.org/api/stream.html)
- **Mitigation strategies**: [whatwg-stream](https://github.com/nodejs/whatwg-stream) effort to implement WHATWG Streams as a Node.js module; [`readable-stream`](https://www.npmjs.com/package/readable-stream) provides Node streams for the Web

## HTTP access

- **Purpose**: Open, read and write to an HTTP, HTTPS, HTTP2 connection
- **Web API**: [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- **Node.js API**: [http](https://nodejs.org/api/http.html), [https](https://nodejs.org/api/https.html), [http2](https://nodejs.org/api/http2.html)
- **Mitigation strategies**: [node-fetch](https://www.npmjs.com/package/node-fetch) polyfill to support fetch from Node.js, [stream-http](https://www.npmjs.com/package/stream-http) implementation of the Node HTTP module for browsers

## Cryptography

- **Purpose**: Basic cryptography algorithms, available as a standard library
- **Web API**: WebCrypto's [`crypto.subtle` SubtleCrypto](https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto)
- **Node.js API**: The [`crypto` module](https://nodejs.org/api/crypto.html)
- **Mitigation strategies**: npm packages like [uuid](https://www.npmjs.com/package/uuid) detect where they are running and use whatever APIs are available. There are various WebCrypto polyfills/shims in npm, but none seem to be very widely used.

## Filesystem access

- **Purpose**: Read and write files on the filesystem
- **Web API**: [File API](https://developer.mozilla.org/en-US/docs/Web/API/File), in-progress [WritableFile](https://github.com/WICG/writable-files/blob/master/EXPLAINER.md) proposal
- **Node.js API**: [`fs` module](https://nodejs.org/api/fs.html)
- **Mitigation strategies**: TODO (Unclear if these are analogous enough to actually ever be bridged in practice)

## Cancel[l]ation

- **Purpose**: Provide APIs which cancel asynchronous processes, asynchronous requests, promises, etc.
- **Web API**: [AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)
- **Node API**: ??
- **Mitigation strategies**: ??
