# Built-in modules

Support for built-in modules is a proposed feature of various JavaScript runtimes, via mechanisms such as the [JavaScript standard library](http://github.com/tc39/proposal-javascript-standard-library/) TC39 proposal, the [Web IDL modules](https://github.com/heycam/webidl/pull/675) proposal, or various Node.js TSC discussions.

## Conventions

- Current proposals share an idea of a shared module specifier prefix, so far tentatively `std:`. This document omits the module prefix, on the assumption that a common prefix will be used by all JS shared built-in modules. If multiple prefixes are used, then split this into separate documents for each namespace.
- Include built-in modules from all runtimes and standards bodies which wish to coordinate in the shared namespace.
- Alphabetize modules within their lists

## Provisional

The following modules have been proposed in a provisional fashion. To be on this list, they need to have:

- Standards track (e.g. have an explainer in a standards organization)
- Implementer interest (from any runtime)

Discussion of these names is encouraged in their respective GitHub repositories. A proposal which does not progress can have its name be re-allocated.

### `kv-storage`

- Standards group: WICG, hoping to graduate to W3C IndexedDB specification
- [GitHub repo](https://github.com/wicg/kv-storage)
- [Explainer](https://github.com/WICG/kv-storage/blob/master/README.md)
- [Specification](https://wicg.github.io/kv-storage/)
- [Tests](https://github.com/web-platform-tests/wpt/tree/master/kv-storage)
- Implementer interest: Blink, Gecko

### `temporal`

- Standards group: Ecma TC39
- [GitHub repo](https://github.com/tc39/proposal-temporal)
- [Explainer](https://github.com/tc39/proposal-temporal/blob/master/README.md)
- [Specification](https://tc39.es/proposal-temporal/spec-rendered)
- Implementer interest: ?

### `virtual-scroller`

- Standards group: WICG, hoping to graduate to the WHATWG HTML Standard
- [GitHub repo](https://github.com/wicg/virtual-scroller)
- [Explainer](https://github.com/wicg/virtual-scroller/blob/master/README.md)
- Implementer interest: Blink

## Allocated

The following modules have become stabilized and the corresonding names should be considered permanently allocated. To be on this list, a module needs to have:

- A full standard
- A test suite
- Multi-implementer commitment

(No modules have yet reached this stage.)
