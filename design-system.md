# Zelophi — Design System

Reverse-engineered from the live site at https://zelophi.com/ (captured 2026-10-01). Zelophi is built and published with **Framer**. All values below were measured from rendered computed styles, the server-rendered HTML, and the live DOM — not estimated. Where a value could not be directly measured, that is stated explicitly.

---

## 1. Color System

### Base / Surface

| Name | HEX | RGB | Usage |
|---|---|---|---|
| `cream-bg` (primary page background) | `#F6F4EC` | 246, 244, 236 | Default `<body>` / page background |
| `cream-bg-light` | `#F9F7F1` | 249, 247, 241 | Lighter card / section surface |
| `cream-bg-muted` | `#E9E7DB` | 233, 231, 219 | Pricing section background, muted panels |
| `cream-bg-soft` | `#F2EFEA` | 242, 239, 234 | Secondary card surface |
| `white` | `#FFFFFF` | 255, 255, 255 | Card backgrounds (pricing "Monthly" card, FAQ open row) |
| `nav-pill-bg` | `rgba(216, 212, 195, 0.4)` | 216, 212, 195 @ 40% | Floating nav pill background |

### Dark / Ink

| Name | HEX | RGB | Usage |
|---|---|---|---|
| `ink-900` (primary dark panel) | `#1E1509` | 30, 21, 9 | "How it works" dark section bg, nav CTA button bg, footer bg |
| `ink-800` | `#2F210F` | 47, 33, 15 | Secondary dark panel variant (pricing "Annual" card bg) |
| `ink-black` | `#000000` | 0, 0, 0 | Default inherited text color on light backgrounds |
| `ink-soft-black` | `#191919` | 25, 25, 25 | Headings on light bg, FAQ question text |
| `ink-warm-black` | `#0D0503` | 13, 5, 3 | Large serif headline text color variant |

### Brand Accent

| Name | HEX | RGB | Usage |
|---|---|---|---|
| `brand-green` | `#24AE79` | 36, 174, 121 | Primary accent — buttons, check icons, links, "FEATURES"/"HOW IT WORKS" eyebrow labels, progress bars |
| `mint-bg` | `#EDFAF4` | — | Light success/check icon chip background |

### Status / Comparison-table chips

| Name | HEX | Usage |
|---|---|---|
| `success-bg` | `#EDFAF4` | Green check icon chip background |
| `success-icon` | `#24AE79` | Check icon fill |
| `error-bg` | `#FEF2F2` | Red "x" icon chip background |
| `error-icon` | `#EF4444` | X icon stroke |
| `neutral-bg` | `#F3F4F6` | Neutral/gray check (used once for "Basic content blocking" × Other apps) |
| `neutral-icon` | `#6E6E7A` | Neutral icon stroke, muted gray text |

### Text opacity tiers (on dark backgrounds)

| Token | Value | Usage |
|---|---|---|
| `text-on-dark-100` | `rgba(255,255,255,1)` | Primary heading text on dark panels |
| `text-on-dark-80` | `rgba(255,255,255,0.8)` | Secondary text on dark pricing card |
| `text-on-dark-51` | `rgba(255,255,255,0.51)` | Eyebrow / muted label on dark panel |
| `text-on-dark-45` | `rgba(255,255,255,0.45)` | Tertiary caption on dark card |
| `text-on-dark-40` | `rgba(255,255,255,0.4)` | Lowest-emphasis text ("/year") |
| `text-on-cream-51` | `rgba(246,244,236,0.51)` | Muted text on cream-on-dark footer blurb |

No CSS custom properties (`--*` tokens) are exposed on `:root` in the production build — Framer bakes literal values into generated class rules. The names above are **our own semantic labels** for documentation purposes, not site-native token names.

---

## 2. Typography System

### Font families (all self-hosted via `framerusercontent.com` or Google Fonts — see `font-missing.md` for licensing notes, though none are required here)

| Family | Role | Source | Weights used |
|---|---|---|---|
| **Faculty Glyphic** | Display / all headings (H2–H4 equivalents) | Google Fonts | 400 (only weight available) |
| **DM Sans** | Body copy, card text, stat numbers, footer | Google Fonts | 400, 500, 600 (700 loaded, unseen in current copy) |
| **DM Mono** | Eyebrow/overline labels ("HOW IT WORKS", "FEATURES", "PRODUCT") | Google Fonts | 500 (400 loaded, rarely used) |
| **Inter** | Navigation links, buttons, misc UI chrome | Google Fonts (self-hosted copy) | 400, 500, 700 |
| **Switzer** | FAQ question/answer text, "Try zelophi" button on quote/footer CTA | Fontshare (free license) | 400, 500 |

All five are freely licensed — **no substitution required**. Real font files were downloaded; see `assets-manifest.md` and `/assets/fonts`.

### Type scale — Desktop (≥1440px)

| Role | Font | Size | Weight | Line-height | Letter-spacing | Color |
|---|---|---|---|---|---|---|
| Hero headline | *(baked into image — see note below)* | — | — | — | — | — |
| H2 — section heading (dark bg) | Faculty Glyphic | 53.42px | 400 | 57.69px | -0.8px | `#F6F4EC` / `#0D0503` |
| H2 — quote / testimonial | Faculty Glyphic | 64.25px | 400 | 77.1px | -0.96px | `#0D0503` |
| H3 — card title | Faculty Glyphic | 22–25px | 400 | 57.69px | normal / -0.6px | `#000` |
| Price display | Faculty Glyphic | 43.9px | 400 | 43.9px | normal | `#1E1509` / `#FFF` |
| Overline / eyebrow | DM Mono | 12–15px | 500 | 14.66px | 1.43px | `#24AE79` / white |
| Body | DM Sans | 16px | 400 | 19.36px | normal | `#000` / `#1E1509` |
| Body small / stat label | DM Sans | 12.82–14px | 400–500 | 18.32–23.8px | normal | varies |
| Nav link | Inter | 18px | 500 | 25.2px | normal | `#000` |
| Button label | Inter-Medium / DM Sans | 13px | 500 | 18.2px | -0.26px | `#000` / `#FFF` |
| FAQ question | Switzer | 16px | 500 | 27.2px | normal | `#191919` |
| FAQ answer | Switzer | 16px | 400 | 27.2px | normal | `#191919` |

### Type scale — Tablet (1024px measured)

| Role | Size | Weight | Line-height |
|---|---|---|---|
| H2 (dark section) | 44px | 400 | 54.69px |
| Quote H2 | 48px | 400 | 57.6px |
| Body | 16px | 400 | 19.36px |
| Overline | 12px | 500 | 14.66px |

### Type scale — Mobile (375px measured)

| Role | Size | Weight | Line-height | Letter-spacing |
|---|---|---|---|---|
| H2 (dark section / "How it works") | 36–38px | 400 | 38.88–41.04px | -0.8px |
| Quote H2 | 36px | 400 | 41.4px | -0.96px |
| Card title | 24px | 400 | 57.69px | normal |
| Nav link (menu open, stacked) | 18px | 500 | 25.2px | normal |
| Body | 14–16px | 400 | 19.36–30.55px | normal |
| Footer "OTHER APPS" small-caps label | 12px | **700** | 24.44px | 0.92px, uppercase |

### Framer responsive breakpoint tiers (from live `__framer__breakpoints` data)

```
≥1920px        → "xl" desktop
1440–1919.98px → desktop (reference / most measurements above)
1200–1439.98px → small desktop
991–1199.98px  → tablet landscape
768–990.98px   → tablet portrait
≤767.98px      → mobile
```

### ⚠️ Important finding: the hero H1 is a baked image, not live text

The homepage's primary headline — *"Raise children with values, [mascot icon] not just limits."* — does **not exist as text in the DOM at any breakpoint**. It is rendered as a single `<img>` (desktop: `5Hz2NeVSn4NVNjMa4mvQ8OAxRxc.gif`, mobile: `6jMNYCJTyor5GnSEt9WBh9g0qc.gif`, 2 different pre-composed crops/line-breaks per breakpoint), including the inline waving-robot icon baked into the image itself. This was confirmed by querying `document.body.textContent` (phrase absent) and `elementFromPoint` (resolves to an `<img>` tag). The clone reproduces this literally — using the same two GIFs at the same breakpoints — rather than attempting to recreate the custom type/icon flow with live text, since that would not match kerning/line-break 1:1. This is documented, not hidden, per the replication skill's substitution-disclosure rule (though no substitution was actually needed — the real asset was extracted).

---

## 3. Spacing System

Measured from the box model at 1440px viewport:

| Context | Value |
|---|---|
| Outer page gutter (left/right margin to content) | 33px either side of a 1374px container (at 1440 viewport) / effectively ~2.3% |
| Header inner row padding | ~18px top, 18px bottom |
| Nav pill internal padding | 18.3px vertical, 22px horizontal |
| Nav pill item gap | 24.7px |
| Section vertical rhythm (dark panels, photo panels) | large, ~470–620px tall full sections, edge-to-edge (full-bleed) with ~18–30px outer corner radius |
| Card internal padding | ~24–32px |
| Card grid gap (How-it-works 4-card row, feature mini-cards) | ~16–24px |
| Comparison table row height | ~56px, row padding ~16–24px horizontal |
| Button padding | 12.8px × 20.2px (nav CTA reference) |

### Spacing scale (inferred, px)
`4, 8, 12, 16, 18, 20, 24, 28, 32, 40, 48, 56, 64, 80, 96, 120+`
Framer renders fluid/computed values rather than a discrete design-token scale, so most spacing is a direct px measurement, not a snapped token.

---

## 4. Layout System

- **Content container max-width:** ~1374px at 1440px viewport (≈33px gutter per side), full-bleed sections (dark panels, photo blocks) stretch edge-to-edge within a 16px outer page margin with large border-radius (~18–30px) corners.
- **Features comparison table width:** 1217px, centered.
- **Grid:** mostly flex-based single/two-column and 2–4 column card grids; no visible CSS grid with explicit track counts — Framer stacks flex rows.
- **Full-bleed sections:** hero photo, "How it works" dark panel, family photo, final CTA band, footer — all span (near) full viewport width with rounded top/bottom corners on the inset sections (dark panel, final CTA) and square-bleed on true full-width photos (family photo) and the footer.
- **Responsive behavior:**
  - Multi-column card rows (4-up "how it works" cards, pricing 2-up cards, comparison table) collapse to a single column / stacked layout on mobile (≤767.98px).
  - The hero headline swaps to a dedicated 3-line mobile image instead of reflowing the desktop 2-line image.
  - Nav collapses to a hamburger icon ≤ tablet; menu opens as an **inline push-down panel** (not an overlay/modal) — page content below is pushed down, it does not cover the page.
  - Pricing toggle (Monthly/Annual pill switch) persists across breakpoints, same component.

---

## 5. Button System

All buttons are fully pill-shaped (border-radius effectively 9999px / measured ~916px against their own box).

| Variant | Background | Text color | Font | Size/weight | Height | Hover (inferred) |
|---|---|---|---|---|---|---|
| **Primary dark pill** (Nav "Contact us", "Try zelophi") | `#1E1509` | `#FFFFFF` | Inter/Switzer-Medium, 13–18px, 500 | ~44px tall, padding 12.8×20px | Standard Framer tap/hover = slight opacity or scale shift (no drastic visible state change captured in static inspection) |
| **Primary green pill** ("Install Free") | `#24AE79` | `#000000`/`#0D0503` | DM Sans 600, 13.72px | ~48px tall | — |
| **Primary dark pill on dark card** ("Start Free Trial") | `#24AE79` (same green, on near-black card) | `#000` | DM Sans 600 | ~48px tall | — |
| **Pricing toggle pill** (segmented control) | Track: `rgba(216,212,195,.4)`-style muted; active segment: `#24AE79` | Active: white/black per segment | DM Sans | small, pill | Click swaps active segment |
| **Nav link (text button)** | transparent | `#000` | Inter 500, 18px | — | — |

No disabled-state button exists on the live site (no form elements that could be disabled were found).

---

## 6. Card System

| Card type | Background | Radius | Shadow | Padding | Notes |
|---|---|---|---|---|---|
| **How-it-works mini card** (4-up, on dark panel) | `#F6F4EC` (cream) | ~16px | none visible | ~24px | Icon (emoji-style illustration) + title (Faculty Glyphic) + body (DM Sans) |
| **Stat callout card** ("Positive Content 98%") | white/cream | ~16–18px | soft (`0 0.9px 3.7px rgba(0,0,0,.1)`) | ~20px | Overlaid on hero photo |
| **Feature mini-card** (Healthy Habits / Personalized) | `#F2EFEA` | ~16px | none | ~20px | Check icon + title + description |
| **Pricing card — Monthly** | `#FFFFFF` | ~18–19px | none | ~32px | Light card, green CTA button |
| **Pricing card — Annual** | `#2F210F` (dark) | ~18–19px | none | ~32px | Dark card, "BEST VALUE" badge in green, green CTA |
| **FAQ accordion row** | white when open / transparent-on-cream when closed | ~12px | none | ~20–24px | Single-open accordion; `+`/`–` icon toggle |
| **Comparison table row** | alternating white / `rgba(237,250,244,.5)` tint for Zelophi column | row dividers only | none | ~16–24px | Header row dark (`#1E1509`), Zelophi column tinted mint |

---

## 7. Form Elements

The production site has **no visible form inputs** at either `/` or `/contact`. The `/contact` page is a static "Get in touch" info panel (heading + paragraph + phone + email + photo) with no `<form>`, `<input>`, or `<textarea>` elements. This is documented rather than invented — the clone reproduces the same static info panel, not a fabricated form.

---

## 8. Borders, Radius & Elevation

| Radius token | px | Usage |
|---|---|---|
| `radius-sm` | 6px | small chip |
| `radius-md` | 10–12px | FAQ rows, small cards |
| `radius-lg` | 14–16px | feature/how-it-works cards |
| `radius-xl` | 18–19px | pricing cards |
| `radius-2xl` | 27–38px | large section corners |
| `radius-3xl` | 47–50px | hero image frame corners |
| `radius-pill` | 9999px (measured ~916px against element's own width) | buttons, nav pill, toggle |

**Shadow:** only one distinct shadow value observed: `0px 0.92px 3.66px rgba(0,0,0,0.1)` — a very soft, near-flat elevation used sparingly (stat callout card). Most surfaces rely on flat color contrast rather than shadow for separation.

**Borders:** no elements were found with a non-zero, non-`currentColor` border in the computed-style scan — separation is achieved via background-color contrast and spacing, not stroked borders.

---

## 9. Motion & Interaction

Framer ships a full spring-physics animation runtime (`motion` library) with the page. Exact internal easing math is proprietary/minified, so — per replication guidance — **behavior was measured, not the code ported**:

| Interaction | Trigger | Property | Feel |
|---|---|---|---|
| Hero element entrance | On page load | `opacity: 0.001→1`, `scale: 0.7→1` | Spring, `bounce: 0.2`, `duration: 1.4s` — a soft "pop-in" |
| Scroll-reveal headings (e.g. "The internet shouldn't raise your children.") | Element enters viewport | opacity/color fade from a muted/grey state to full color | Fade feels ~400–600ms, scroll-linked (ties to scroll position partway through, not a fixed timer) |
| FAQ accordion | Click | height auto + fade of answer | Single-open accordion; opening one closes any other open row |
| Mobile nav menu | Click hamburger | push-down reveal (not overlay) | content below shifts down; icon swaps hamburger ↔ close (×) |
| Pricing toggle | Click Monthly/Annual | active pill background slides/swaps | instant segment highlight swap |
| Nav pill / buttons | Hover | Framer's default is a subtle opacity/scale micro-interaction | Not strongly visible in static captures; clone applies a conservative `opacity .9` / `scale 0.98` on `:active` as a reasonable equivalent — labeled as an approximation |

**Recreation note:** the clone implements scroll-reveal via `IntersectionObserver` + CSS transitions (fade/translate), which reproduces the *visual effect* (trigger point, property animated, duration feel) without the proprietary Framer Motion spring engine. This is a declared, intentional simplification of implementation technique, not of visual outcome.

---

## 10. Component Inventory

| Component | Summary |
|---|---|
| **Header/Nav** | Fixed-at-top (scrolls with page, not position:sticky in observed capture) row: wordmark "Zelophi" (Faculty Glyphic-style logotype, left), floating pill nav (How it works / Features / Pricing, center, scrolls to in-page anchors), dark CTA pill "Contact us" (right, links to `/contact`). Collapses to hamburger ≤ tablet. |
| **Mobile nav panel** | Inline push-down list of nav links + full-width green "Contact us↗" pill button. |
| **Hero** | Baked-image headline + large rounded dashboard/illustration composite image + floating stat card + secondary heading/paragraph/CTA + two small feature cards. |
| **Quote block** | Centered large Faculty Glyphic pull-quote, no attribution shown. |
| **Photo-overlay heading** | Full-bleed photo with heading text overlaid bottom-left (white text on dark gradient/vignette). |
| **How-it-works section** | Full-bleed dark rounded panel: eyebrow + H2 + 4-up icon card row. |
| **Full-bleed photo band** | Plain edge-to-edge photograph, no text. |
| **Feature comparison table** | Eyebrow + H2 + subhead + 3-column table (Feature / Other Apps / Zelophi) with check/x icon chips, Zelophi column mint-tinted. |
| **Pricing section** | Eyebrow + H2 + Monthly/Annual toggle + 2 pricing cards (light "Monthly", dark "Annual" with best-value badge). |
| **FAQ accordion** | H2 "Your Questions Answered" + 4-row single-open accordion with `+`/`–` icon. |
| **Final CTA band** | Full-bleed painterly gradient background, H2 + "Try zelophi" button. |
| **Footer** | Dark panel: wordmark + blurb + 3 link columns (Product / Community / Support) + 4 social icons (X, Facebook, Instagram, LinkedIn) + copyright + email, all via the shared inline SVG icon sprite. |
| **Contact page hero** | "Get in touch" heading + paragraph + phone + email + photo, no form. |
| **Icon sprite** | 31 inline `<svg id="...">` definitions referenced elsewhere via `<use href="#id">` — used for comparison-table check/x icons and small decorative marks. Reproduced identically in the clone (`assets/svg/icon-sprite.html`). |

---

## 11. Declared substitutions / limitations

Per the replication skill's disclosure rule:

1. **None of the five fonts required substitution** — DM Sans, DM Mono, Faculty Glyphic, Inter, and Switzer are all freely licensed and were downloaded directly as real `.woff2` files (see `/assets/fonts` and `font-missing.md`, which is intentionally near-empty).
2. **Scroll-linked motion** is recreated with `IntersectionObserver`/CSS transitions rather than Framer's proprietary Motion spring engine — visual trigger points and easing feel are matched by eye, not by portable source code (none exists to port).
3. **Hero headline images** are the real extracted GIF assets, used as-is (not re-typeset) — this is the most faithful option since the originals are inline flowing text+icon compositions.
4. **No contact form exists on the source site** — the clone does not fabricate one.

---

## 12. Community page additions (extending the system, not replacing it)

Added when building `/community` (Zelophi Kids Connect / Zelophi Kids Arise), sourced from the supplied content doc rather than the original site (which has no community page). These are **additive tokens** layered onto the existing system — nothing above was changed.

### New color tokens — age-group accents

The content doc names a color per age group ("[ruby colour]", "[beryl colour]", "[amber colour]", "[emerald colour]") without supplying hex values, so these were chosen to read as natural siblings of the existing palette (same muted, warm-neutral saturation level as `--ink-900`/`--brand-green`, not saturated "brand-kit" colors):

| Token | Hex | Tint bg | Usage |
|---|---|---|---|
| `--ruby` | `#9C2B3A` | `--ruby-bg` `#FBEAEC` | "Rubies" (ages 0–2) age-card accent |
| `--beryl` | `#3E8E86` | `--beryl-bg` `#E9F5F3` | "Beryls" (ages 3–5) age-card accent |
| `--amber` | `#C77D1D` | `--amber-bg` `#FBF1DE` | "Crystals" (ages 6–8) age-card accent — doc explicitly specifies amber for this group |
| *(reused)* `--brand-green` / `--mint-bg` | `#24AE79` / `#EDFAF4` | — | "Emeralds" (ages 9–11) — reuses the existing brand green exactly rather than inventing a 4th new green, since "emerald" already *is* the site's brand color |

### New components (built from existing patterns, not new visual language)

| Component | Built from | Notes |
|---|---|---|
| `.community-hero` | `.section-head` typography scale, centered | Page intro: eyebrow + H1 + lede + mono caption + CTA |
| `.age-grid` / `.age-card` | `.how-grid` grid mechanics + `.feature-mini` card surface | 4-up card row, cream-soft surface, colored top border + pill chip per age group |
| `.activity-row` | `.feature-mini-row`, 3-column variant | Reuses `.feature-mini` card/icon exactly |
| `.inclusion-list` | `.price-card__list` checklist pattern | Same check-icon-in-circle SVG, standalone (not inside a pricing card) |
| `.program-section` | Same 140px/96px top-rhythm as `.features-section`/`.pricing-section` | Vertical pacing stays consistent with the rest of the site |

The quote block, final CTA band, header, mobile nav, and footer on the Community page are the **exact existing classes** (`.quote`, `.cta-band`, `.site-header`, `.mobile-nav`, `.site-footer`) — zero duplication, zero new variants needed for those.

### Declared content/asset gaps (Community page)

1. The source doc marks `[IMAGES]` for the Kids Connect intro but supplies no actual image. The existing asset library's photos (tablet/phone-in-hand lifestyle shots) visually contradict this program's "five days away from screens" message, so no existing asset was force-fitted — the section intentionally ships as a typography/color composition instead, matching how the Home page's own Pricing/FAQ/Features sections are built without photography. **A real photo for Zelophi Kids Connect/Arise is an open asset dependency**, not silently substituted.
2. The doc's `[sign-up form]` CTA target doesn't exist yet — both "Reserve your child's place" and "Save your child's place" route to `/contact` (the nearest existing equivalent) rather than a dead link. This is a disclosed placeholder, not a real form.
3. `[OUR SERVICE PAGE]` in the doc's closing CTA maps to `index.html` — the home page genuinely is "the product" in this site's structure, so this is a direct mapping, not a substitution.
