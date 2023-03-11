# Awesome Tiny JS

A collection of tiny JS libraries to put your bundle on a diet. Curated by [Vladimir Klepov](https://blog.thoughtspile.tech) Rules:

- Size is under 2Kb-ish, min + gzip, with all deps, except where noted.
- For multi-purpose libraries, the size of a useful subset must be under 2Kb-ish.
- Second-level libraries only allowed for React, Vue, Angular, svelte. 
- Useful client-side. I haven't figured out participation rules for node-only libraries, and I'm not too worried about them.
- 100+ GitHub stars. Adding every obsure library will dilute the list.
- No zero-JS (CSS- or type-only) libraries. It's not awesome-css or something.

Disclaimers:

- I haven't used all these libraries personally. The ones I tried and enjoyed are marked with :star:
- Most framework-specific libraries are for React, because that's what I'm familiar with.

## Categories

- [UI frameworks](#ui-frameworks)
- [Event emitters](#event-emitters)
- [Reactive programming](#reactive-programming)
- [State managers](#state-managers)
- [Routers and URL utils](#routers-and-url-utils)
- [API Layer](#api-layer)
- [I18N](#i18n)
- [Generic utilities](#generic-utilities)
- [Unique ID generation](#unique-id-generation)
- [Colors](#colors)

The list is actively updated to include more categories and tools. 

- Want to help? [Contributing](#contributing)

## UI Frameworks

UI frameworks (libraries?) provide declarative templates, event bindings, and observable state to update the view. I've been generous and expanded the size limit for this category to 4Kb, but also increased the star limit to 3K. 

- [preact](https://github.com/preactjs/preact) :star: — React-like API (pre-hooks) in 4Kb. Cool ecosystem of similarly tiny tools and components. Highly recommended. ![](https://shields.io/github/stars/preactjs/preact?style=social)

The following libraries are small and cool, but note they're about [500x less popular than preact.](https://npmtrends.com/fre-vs-hyperapp-vs-million-vs-preact-vs-redom-vs-riot) Kudos for deconstrucing the very essence of a "framework":

- [million](https://github.com/aidenybai/million) — Marketed as a _drop-in replacement for React,_ but in under 2Kb. ![](https://shields.io/github/stars/aidenybai/million?style=social)
- [fre](https://github.com/frejs/fre) — React-like library with hooks and concurrency, 1–3Kb. ![](https://shields.io/github/stars/frejs/fre?style=social)
- [hyperapp](https://github.com/jorgebucaran/hyperapp) — Declarative UI with pure JS syntax and immutable state, under 2Kb. ![](https://shields.io/github/stars/jorgebucaran/hyperapp?style=social)
- [redom](https://github.com/redom/redom) — Hyperapp-style templates with _imperative_ event listeners and updates, around 2Kb. ![](https://shields.io/github/stars/redom/redom?style=social)

And if being declarative is not your thing:

- [umbrella](https://github.com/franciscop/umbrella) — jQuery-style DOM manipulation library in 3Kb. ![](https://shields.io/github/stars/franciscop/umbrella?style=social)

## Event emitters

Event emitter pattern is fairly easy to implement yourself, but why bother when you have these cool tools? With an arms race to build the smallest one, the limit is 0.5Kb.

- [mitt](https://github.com/developit/mitt) :star: — 200-byte emitter. I use it on most projects. ![](https://shields.io/github/stars/developit/mitt?style=social)
- [nanoevents](https://github.com/ai/nanoevents) — smaller and with nicer unsubscribe API, but no '*' event. ![](https://shields.io/github/stars/ai/nanoevents?style=social)
- [eev](https://github.com/chrisdavies/eev) — more of the same in 500b. ![](https://shields.io/github/stars/chrisdavies/eev?style=social)
- [onfire.js](https://github.com/hustcc/onfire.js) — 500b, but has `.once`. ![](https://shields.io/github/stars/hustcc/onfire.js?style=social)

## Reactive programming

A step up from a raw event emitter, reactive libraries can build chains of event transforms, filters, and side-effects. You can already use these to build UIs by manually updating DOM on state change:

- [flyd](https://github.com/paldepind/flyd) — rx-styled event streams in a 2Kb-ish package. ![](https://shields.io/github/stars/paldepind/flyd?style=social)
- [hyperactiv](https://github.com/elbywan/hyperactiv) — 4 functions to make objects observable and listen to changes, in 1Kb. ![](https://shields.io/github/stars/elbywan/hyperactiv?style=social)
- [flimsy](https://github.com/fabiospampinato/flimsy) — 1Kb reactive core of solid.js that _almost_ fit into UI frameworks category. Author warning: _is probably buggier._ ![](https://shields.io/github/stars/fabiospampinato/flimsy?style=social)

Honorable mentions: [callbag-basics](https://github.com/staltz/callbag-basics) ![](https://shields.io/github/stars/staltz/callbag-basics?style=social) and [oby](https://github.com/vobyjs/oby) ![](https://shields.io/github/stars/vobyjs/oby?style=social) _could_ make it _if_ they had tree-shaking, but otherwise are around 7Kb.

## State managers

State managers combine observable state with actions and framework bindings, intended for app-wide state.

- [zustand](https://github.com/pmndrs/zustand) :star: — ~1Kb store with pleasant actions and selectors. React / vanilla. ![](https://shields.io/github/stars/pmndrs/zustand?style=social)
- [nanostores](https://github.com/nanostores/nanostores) — modular store in sub-1Kb with lots of framework connectors. ![](https://shields.io/github/stars/nanostores/nanostores?style=social)
- [storeon](https://github.com/storeon/storeon) — minimal 400-byte redux-styled store. (p)react, has third-party connectors. ![](https://shields.io/github/stars/storeon/storeon?style=social)
- [unistore](https://github.com/developit/unistore) :star: — sub-1Kb store with actions from preact developers, (p)react support. ![](https://shields.io/github/stars/developit/unistore?style=social)
- [teaful](https://github.com/teafuljs/teaful) — (p)react store with useState-like API in 1Kb. ![](https://shields.io/github/stars/teafuljs/teaful?style=social)

## Routers and URL utils

Do stuff on URL / history changes, with path matching and parsing:

- [wouter](https://github.com/molefrog/wouter) — Declarative routes for (p)react in 1.5Kb, or a 400-byte hook. ![](https://shields.io/github/stars/molefrog/wouter?style=social)
- [@nanostores/router](https://github.com/nanostores/router) — routes as a nanostores store (framework-agnostic), sub-1Kb. ![](https://shields.io/github/stars/nanostores/router?style=social)
- [navaid](https://github.com/lukeed/navaid) — history-based observable router, sub-1Kb. ![](https://shields.io/github/stars/lukeed/navaid?style=social)
- [routie](https://github.com/jgallen23/routie) — hash-based observable router, sub-1Kb. ![](https://shields.io/github/stars/jgallen23/routie?style=social)

Just want to parse or match URL paths without observing them? Here you go:

- [matchit](https://github.com/lukeed/matchit) — route parser and matcher, sub-1Kb. ![](https://shields.io/github/stars/lukeed/matchit?style=social)
- [regexparam](https://github.com/lukeed/regexparam) — convert path to regexp in 400 bytes. ![](https://shields.io/github/stars/lukeed/regexparam?style=social)
- [qss](https://github.com/lukeed/qss) — parse querystrings in 300b. Not sure you need it, [URL API](https://developer.mozilla.org/en-US/docs/Web/API/URL) support is good. ![](https://shields.io/github/stars/lukeed/qss?style=social)

## API Layer

`fetch` API has some boilerplate associated with it: serialize & parse data, reject on non-200 response, etc. These tiny packages handle it for you:

- [redaxios](https://github.com/developit/redaxios) — drop-in axios replacement in 800 bytes. ![](https://shields.io/github/stars/developit/redaxios?style=social)
- [wretch](https://github.com/elbywan/wretch) — chainable API with error processing in 2Kb, and lots of extra plugins. ![](https://shields.io/github/stars/elbywan/wretch?style=social)
- [gretchen](https://github.com/truework/gretchen) — chainable API with type-safe errors in 2Kb. ![](https://shields.io/github/stars/truework/gretchen?style=social)

If for some reason you still need a fetch polyfill, try this one:

- [unfetch](https://github.com/developit/unfetch) :star: — loose fetch polyfill in 500 bytes. ![](https://shields.io/github/stars/developit/unfetch?style=social)

## I18N

A map of strings might seem enough to translate an app, but these tools also handle interpolation and some extra goodies:

- [@nanostores/i18n](https://github.com/nanostores/i18n) — detect locale, load dictionaries, format dates / numbers in sub-1Kb. ![](https://shields.io/github/stars/nanostores/i18n?style=social)
- [rosetta](https://github.com/lukeed/rosetta) — bare-bones interpolation in 300 bytes. ![](https://shields.io/github/stars/lukeed/rosetta?style=social)
- [lingui](https://github.com/lingui/js-lingui) — 1.7Kb core with template strings and optional react connector. babel-depenent. ![](https://shields.io/github/stars/lingui/js-lingui?style=social)
- [eo-locale](https://github.com/ibitcy/eo-locale) — interpolation & dates / numbers in under 2Kb, including react bindings. ![](https://shields.io/github/stars/ibitcy/eo-locale?style=social)

## Generic utilities

Something you'd find in lodash or ramda, but smaller. Most are pretty similar and very small, with minor differences in package structure (single / package-per-helper) and tree shaking vs direct helper import.

- [remeda](https://github.com/remeda/remeda) — 90 tree-shakable helpers. ![](https://shields.io/github/stars/remeda/remeda?style=social)
- [rambda](https://github.com/selfrefactor/rambda) — 187 tree-shakable helpers. ![](https://shields.io/github/stars/selfrefactor/rambda?style=social)
- [just](https://github.com/angus-c/just) :star: — 82 helpers in separate packages. ![](https://shields.io/github/stars/angus-c/just?style=social)
- [@tinkoff/utils](https://github.com/Tinkoff/utils.js) — 173 helpers, 1 import per helper. Conservative browser target. ![](https://shields.io/github/stars/Tinkoff/utils.js?style=social)
- [@fxts/core](https://github.com/marpple/FxTS) — 96 tree-shakable helpers. Lazy evaluation support. ![](https://shields.io/github/stars/marpple/FxTS?style=social)

Honorable mention: [underscore,](https://github.com/jashkenas/underscore) ![](https://shields.io/github/stars/jashkenas/underscore?style=social) outshined by lodash by chance, contains many sub-1Kb helpers. It does not tree-shake as well as the libraries above due to codebase structure.

Note: lodash itself is not tree-shakable, but has made many attempts at modulaity with `lodash.method` packages, imports from `lodash/method`, and `lodash-es`, none of which work well in practice. But yes, lodash does handle some corner cases.

Also note that much of the original lodash functionality comes built-in with modern ES. Prefer native versions over libraries as your browser target allows.

## Unique ID generation

Unique ID generation does not take a lot of code, but it's not someting I'd want to write myself. Limit is 500 bytes. Also note that the [native `crypto.randomUUID`](https://developer.mozilla.org/en-US/docs/Web/API/Crypto/randomUUID) has [OK support.](https://caniuse.com/mdn-api_crypto_randomuuid)

- [uuid](https://github.com/lukeed/uuid) :star: — real UUIDs in 240 bytes. ![](https://shields.io/github/stars/lukeed/uuid?style=social)
- [nanoid](https://github.com/ai/nanoid) :star: — random IDs with larger alphabet in 130 bytes. ![](https://shields.io/github/stars/ai/nanoid?style=social)
- [uid](https://github.com/lukeed/uid) — can do in in 130–205 bytes. ![](https://shields.io/github/stars/lukeed/uid?style=social)
- [hexoid](https://github.com/lukeed/hexoid) — hex IDs in 190 bytes. ![](https://shields.io/github/stars/lukeed/hexoid?style=social)

## Colors

Color manipulation is rare in pure UI development, but very helpful for data visualization, and uses [freaky math.](https://en.wikipedia.org/wiki/HSL_and_HSV#Color_conversion_formulae) Don't fry your brain, take these:

- [colord](https://github.com/omgovich/colord) — manipulate colors and convert formats. 1.7Kb, exotic color spaces as plugins. ![](https://shields.io/github/stars/omgovich/colord?style=social)
- [colr](https://github.com/stayradiated/colr) — fits more color spaces, but fewer manipulations than colord, into 1.9Kb. ![](https://shields.io/github/stars/stayradiated/colr?style=social)
- [randomcolor](https://github.com/davidmerfield/randomColor) — random attractive colors with configuration, just above 2Kb. ![](https://shields.io/github/stars/davidmerfield/randomColor?style=social)
- [polychrome](https://github.com/cdonohue/polychrome) — color manipulation in 2Kb. ![](https://shields.io/github/stars/cdonohue/polychrome?style=social)

## To be continued!

See [WIP.md](./WIP.md) for a list of small libraries I have found, but not yet analyzed deeply.

## Contributing

Suggestions welcome! Please check that the lib you're suggesting:

- Fits the [criteria.](#awesome-tiny-js)
- Is not already in [WIP.](./WIP.md) 

And drop a pull request or an [issue](https://github.com/thoughtspile/awesome-tiny-js/issues).

---

Collected and reviewed by [Vladimir Klepov](https://blog.thoughtspile.tech) in 2023. [CC0 license.](./LICENSE)
