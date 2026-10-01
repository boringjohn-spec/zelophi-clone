# Assets Manifest

All assets below were downloaded directly from the live site's network payload (`framerusercontent.com` CDN) at full resolution — none are screenshots or recreations. Filenames are the original CDN hashes, preserved as-is for traceability.

## /assets/images

| Filename | Type | Dimensions | Format | Used for | Notes |
|---|---|---|---|---|---|
| `5Hz2NeVSn4NVNjMa4mvQ8OAxRxc.gif` | Hero headline | 2774×460 | GIF (animated) | **Hero H1** on desktop/tablet: "Raise children with values, [waving mascot] not just limits." | Text + icon are baked into the image; confirmed via DOM inspection that no live text exists for this headline. |
| `6jMNYCJTyor5GnSEt9WBh9g0qc.gif` | Hero headline (mobile) | 802×336 | GIF (animated) | **Hero H1** on mobile (≤767px): same copy, pre-wrapped to 3 lines | Separate asset per breakpoint, not a responsive crop of the same file. |
| `P6MhhPb6WOwVdYxcbDdrdhkN9X4.png` | Product UI mockup | 2081×1118 | PNG | Foreground "dashboard" screenshot layered into the hero visual | |
| `JFReNPnolHiKg4W4Wcn5VkMPs.png` | Illustrated background | 1590×1214 | PNG | Hero background scene (trees/park), one of 5 responsive-variant files Framer generates for this layer | |
| `i7vdFEe75UCZDnJJS4feHIATTg8.png` | Illustrated background (variant) | 1448×1086 | PNG | Same hero background scene, alternate responsive resolution | |
| `gFrhd5DLt2gMV7YW5PzP9URtzUQ.png` | Illustrated background (variant) | 1448×1086 | PNG | Same hero background scene, alternate responsive resolution | |
| `7HEt21XVzvgK278XZiWah1ZyOM.png` | Illustrated background (variant) | 1023×1537 | PNG | Same hero background scene, alternate responsive resolution | |
| `mol7G5szMyPGZjCXVYcuRWltrpc.png` | Illustrated background (variant) | 1023×1537 | PNG | Same hero background scene, alternate responsive resolution | |
| `CeIgaekHgAC8KlB1gPp0skYMw.jpg` | Photo | 1536×1024 | JPEG | Child on sofa with tablet — hero stat-card photo (alt="Feature Image") | |
| `O3bGavZNLFi4DPsvdOEKNEVoEY.png` | UI detail graphic | 936×855 | PNG | Small chart/card graphic inside dashboard mockup overlay (alt="Card Image") | |
| `NiL3nN4xKYzcDnlqlAdWSOZ3U1E.png` | UI detail graphic | 927×1011 | PNG | Small chart/card graphic inside dashboard mockup overlay (alt="Card Image") | |
| `i8UTEbRdcVoHv4dt4nvGjUPo68.png` | UI detail graphic | 1247×597 | PNG | Small chart/card graphic inside dashboard mockup overlay (alt="Card Image") | |
| `LjpZImK8Fc1rxhU6MG564MlGwNs.png` | UI detail graphic | 667×372 | PNG | Small chart/card graphic inside dashboard mockup overlay (alt="Card Image") | |
| `IewU2qyhvLPrGiVvbVVI1mHpOnk.png` | UI detail graphic | 719×225 | PNG | Small chart/card graphic inside dashboard mockup overlay (alt="Card Image") | |
| `vncpkvJQxmAlvaaQUrUonHCfNac.png` | Icon/badge | 122×133 | PNG | Small decorative icon near hero stat card | |
| `FCyWThHI0rWb04H2pKu3GCefxZg.png` | Icon/badge | 132×132 | PNG | Small rounded badge/avatar, mid-page card | |
| `VOrXQxGQqewdvqF4Ghn8FaeL2A.png` | Icon/badge | 117×132 | PNG | Small rounded badge/avatar, mid-page card | |
| `0ULNY1LLI9tjr22OoiBGrGqqAcM.png` | Icon/badge | 132×132 | PNG | Small rounded badge/avatar, mid-page card | |
| `HaLeB738mRi3vm7dLfC4guDzMA.png` | Photo/illustration | 1024×1024 | PNG | Supplementary square image (how-it-works / feature area) | |
| `IOCOPXibMLFhGrF0yVeofRGcs.jpg` | Photo | 1732×1155 | JPEG | Full-bleed family photo band | |
| `Ye9JziiYfLJmm2CBOEYzfCApOD0.png` | Favicon | 247×247 | PNG | `<link rel="icon">`, both light/dark scheme | |
| `ONuHK4Fpks9Pda7XhKL9gOOKog.svg` | Icon | 31×31 | SVG | Red "✗" chip — comparison table "Other Apps" column | Colors: bg `#FEF2F2`, stroke `#EF4444` |
| `SRQT3q4Df0P5GAQwU6nX6ki1TI.svg` | Icon | 31×31 | SVG | Green "✓" chip — comparison table "Zelophi" column | Colors: bg `#24AE79`, stroke `#FFFFFF` |
| `P6wqWrnljUSZOuEVQ9WG5H7S71k.svg` | Icon | 31×31 | SVG | Neutral gray "✓" chip — "Basic content blocking" / Other Apps row | Colors: bg `#F3F4F6`, stroke `#6E6E7A` |

## /assets/svg

| Filename | Type | Notes |
|---|---|---|
| `icon-sprite.html` | Inline SVG sprite fragment | The site's hidden `#svg-templates` container: 31 standalone `<svg id="...">` definitions referenced elsewhere in the page via `<use href="#id">`. Extracted verbatim from the server-rendered HTML and reused identically in the clone (same ids, same `<use>` technique) rather than re-drawn, per "do not redraw an icon that can be extracted directly." |

## /assets/fonts

50 `.woff2` files — see [font-missing.md](font-missing.md) for the full family/weight/style table. All real, extracted files (no recreations). Filenames follow the pattern `{Family}-{Weight}[Italic][-n].woff2`, e.g. `Inter-500.woff2`, `DMSans-400Italic.woff2`. Multiple numbered files per weight correspond to the original's Unicode-range subsetting (Latin, Latin-ext, Cyrillic, Greek, Vietnamese, etc.) — preserved as separate files with their original `unicode-range` in [css/fonts.css](css/fonts.css) rather than merged, so browser subsetting behavior matches the source exactly.

## /assets/colors

| File | Contents |
|---|---|
| `colors.json` | Machine-readable palette — every color documented in [design-system.md](design-system.md) §1, with hex/rgb and a usage label. |

## Not extracted / not applicable

- **Videos:** none found on the site.
- **Lottie/JSON animations:** none found (motion is Framer Motion DOM animation, not Lottie).
- **Illustrations folder:** the site's "illustrations" (hero park scene, mascot) are delivered as the raster PNGs/GIFs listed above, not as separate vector illustration source files — there is nothing additional to extract beyond what's listed.

## Open dependency — Community page imagery

The content doc for `/community` (Zelophi Kids Connect / Zelophi Kids Arise) marks an `[IMAGES]` placeholder for the hero but supplies no actual file, and no community/ministry-specific photography exists in `/assets/images`. v2 of the page reuses three existing lifestyle photos from Home/Contact instead of shipping photo-free:

| Image | Reused for | Also appears on |
|---|---|---|
| `IOCOPXibMLFhGrF0yVeofRGcs.jpg` | Community hero (split hero visual) | Home — full-bleed family photo band |
| `CeIgaekHgAC8KlB1gPp0skYMw.jpg` | Full-bleed photo band after the age-group grid | Home — hero stat-card photo |
| `HaLeB738mRi3vm7dLfC4guDzMA.png` | Photo-overlay transition into "Zelophi Kids Arise" | Contact — "Get in touch" side photo |

This is disclosed reuse of existing brand photography, not purpose-shot imagery — **a real photo/video asset for Zelophi Kids specifically (ideally depicting the in-person Connect/Arise program) is still a genuine open request**, not silently filled. See `design-system.md` §12 for the full note, including the new flat-SVG icon glyphs (heart/book/chat/compass/calendar/shield/flag) drawn for the age-group and activity cards since no matching icon assets existed either.
