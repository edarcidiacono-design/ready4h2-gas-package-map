# Ready4H2 Gas Package Map

Interactive map of national approaches to implementing the EU Hydrogen and Decarbonised Gas Market Package (Directive (EU) 2024/1788 and Regulation (EU) 2024/1789).

**Live site:** https://edarcidiacono-design.github.io/ready4h2-gas-package-map/

- Ready4H2 national examples (distribution level), *Overview of National Approaches to Gas Package Implementation*, 30 September 2026
- ACER Opinion No 17/2026 on gas and hydrogen national network development plans (transmission level, EU-27)
- Norway (EEA EFTA state) and United Kingdom (non-EU) as comparators, with official sources in each country profile
- Eight languages; Explore, Compare and Briefing views; works on desktop and mobile

The application is a single self-contained `index.html` with no build step or backend. To update it, replace `index.html` and push to `main`; GitHub Pages republishes automatically.

Useful links: `#compare` and `#brief` open those views, `#framework` opens the legal-relationship view, `#acer` opens the ACER view.

## Versions
- `index.html` — V7.2: one set of themes with a transmission (TSO) / distribution (DSO) switch; distribution-level transposition data for all 27 Member States from official national sources (checked 19 October 2026).
- `archive/v7.1/index.html` — V7.1 (UX/UI redesign on V7 data).
- `archive/v7/index.html` — previous V7, kept for recovery (also recoverable from git commit `5950949`).

## Embedding (e.g. on ready4h2.com)
- Add `?embed=1` to the page URL inside an iframe: the page hides its own brand bar, uses the light theme (`&theme=auto` keeps the visitor's light/dark setting), removes sticky elements and reports its height to the parent window with `postMessage({type: "r4h2-map:height", height})`. On a view change it also sends `{type: "r4h2-map:scrollTop"}`.
- `embed-example.html` shows the iframe plus the few lines of parent-page script that resize it.
- Language can be preset with `&lang=de` (en, de, fr, es, it, nl, cs, sk).
- Fonts (IBM Plex Sans, Bricolage Grotesque; SIL Open Font License 1.1) are embedded in the file: the page makes no external requests.
