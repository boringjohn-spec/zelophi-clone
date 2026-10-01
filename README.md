# Zelophi — Site Clone

A pixel-faithful, responsive clone of [zelophi.com](https://zelophi.com/), built from a full reverse-engineering pass of the live site (a Framer-published site): real extracted fonts, images, icons, and a measured (not guessed) design system, rebuilt in plain HTML/CSS/JS.

## Run it locally

Any static file server works. For example:

```bash
python3 -m http.server 8743
```

Then open `http://localhost:8743/index.html`.

(A `.claude/launch.json` is included so the project also runs directly via Claude Code's preview tooling.)

## Pages

- `index.html` — homepage
- `contact.html` — contact page
- `community.html` — Community page (Zelophi Kids Connect / Zelophi Kids Arise) — added after the initial clone, not part of the original site; built from supplied copy using the existing design system end-to-end (see `design-system.md` §12)

## Documentation

This project was built research-first, per a reverse-engineering workflow. The research artifacts are included alongside the code:

- [`design-system.md`](design-system.md) — colors, typography, spacing, layout, components, and motion, all measured from the live site's computed styles
- [`website-structure.md`](website-structure.md) — full sitemap, section hierarchy, and copy for both pages
- [`assets-manifest.md`](assets-manifest.md) — every extracted asset, with source and usage notes
- [`font-missing.md`](font-missing.md) — font licensing/extraction notes (all 5 fonts used are freely licensed and were fully extracted)

## Structure

```
.
├── index.html
├── contact.html
├── css/
│   ├── styles.css       # main stylesheet (design tokens + components)
│   └── fonts.css        # @font-face declarations for all local fonts
├── js/
│   └── main.js          # mobile nav, FAQ accordion, pricing toggle, scroll reveal
└── assets/
    ├── fonts/           # real extracted .woff2 files
    ├── images/           # real extracted images, GIFs, icon SVGs
    ├── svg/              # the site's inline icon sprite
    └── colors/           # colors.json reference
```

## Notes

- All fonts (DM Sans, DM Mono, Faculty Glyphic, Inter, Switzer) are freely licensed and were extracted directly — no substitutions.
- The homepage's hero headline is a baked image (two breakpoint-specific GIFs), reproduced using the real extracted assets rather than retyped, since that's how the source site renders it.
- Scroll-reveal animations are implemented with `IntersectionObserver` + CSS transitions as a practical equivalent to the source site's proprietary Framer Motion engine — see `design-system.md` §9 for details.
