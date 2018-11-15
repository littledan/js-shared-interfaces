Many JavaScript APIs, originally created for the Web Platform, are being implemented in other JavaScript environments. These shared interfaces assist the usage of the same JS code in various different places, sometimes called "isomorphic code". This repository attempts to document which JavaScript APIs are shared and on which platforms.

### Sections

- [Global object](https://github.com/littledan/js-shared-interfaces/blob/master/GLOBALS.md): Globals implemented in multiple environments
- [Built-in modules](https://github.com/littledan/js-shared-interfaces/blob/master/MODULES.md): Proposed built-in modules
- [import.meta](https://github.com/littledan/js-shared-interfaces/blob/master/IMPORTMETA.md): Shipping and proposed properties of the `import.meta` object

### Goals

- Help JavaScript programmers target multiple environments while using a broad range of APIs
- Enable more effective and rapid standards development by surfacing factors from non-Web environments early
- Expose and help prioritize opportunities for supporting shared interfaces to embedding environment maintainers
- Provide the underlying data which might be used some day to consider describing a standard JavaScript base library

### Non-goals

- Add any procedural requirements/blockers in standards development, or slow anything down (there's already enough paperwork! many APIs don't make sense in other environments, or people may be unavailable for feedback)
- List globals which are only implemented in a single environment (there are too many; use that environment's documentation)
- Document compatibility among browsers for global objects (see MDN, ChromeStatus, caniuse, etc.)
- Include any interfaces exposed by TC39 standards (which are already presumed to be cross-environment)
- Include polyfills (may make sense in the future, but keep scope minimal at first)

### Standards track

It's unclear whether this repository will evolve into any document which requires standardization as such. However, to encourage freely shared development, if there's interest, the intention is to pursue it in a [WICG](https://github.com/WICG), with the possibility to move into a W3C CG/WG structure if useful in the future.
