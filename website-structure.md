# Website Structure — Zelophi

Source: https://zelophi.com/ (sitemap confirms exactly 2 routes). Built/published with Framer.

```
Zelophi (zelophi.com)
├── / (Home)
│   ├── Header (shared)
│   │   ├── Logo "Zelophi" (Faculty Glyphic wordmark, links to "/")
│   │   ├── Floating pill nav: How it works (#how-it-works) · Features (#FEATURES) · Pricing (#Pricing)
│   │   ├── CTA pill: "Contact us" → /contact
│   │   └── Mobile: hamburger icon → inline push-down menu (same 3 links + full-width "Contact us↗" button)
│   │
│   ├── Hero
│   │   ├── Headline (pre-rendered image, NOT live text): "Raise children with values, [mascot icon] not just limits."
│   │   │     — desktop/tablet asset: 5Hz2NeVSn4NVNjMa4mvQ8OAxRxc.gif (2-line layout)
│   │   │     — mobile asset: 6jMNYCJTyor5GnSEt9WBh9g0qc.gif (3-line layout)
│   │   ├── Dashboard/illustration composite image (rounded frame, forest background + product UI mockup)
│   │   ├── Floating stat card: "Positive Content — 98% — Age-appropriate" (progress bar)
│   │   ├── Heading: "The internet shouldn't raise your children."
│   │   ├── Paragraph: "The online world moves fast. Zelophi helps protect what matters while building healthy digital habits."
│   │   ├── CTA button: "Try zelophi"
│   │   └── 2 mini feature cards: "Healthy Habits — Build healthy digital habits through smart daily guidance" / "Personalized — Protection and recommendations tailored to your family"
│   │
│   ├── Quote block
│   │   └── "We've built a framework of what your children should be exposed to, not just what they should be protected from."
│   │
│   ├── Photo-overlay section
│   │   └── Full-bleed photo (child on couch with tablet) + overlay heading "Zelophi helps protect curious young minds online."
│   │
│   ├── How It Works (id="how-it-works") — dark full-bleed panel
│   │   ├── Eyebrow: "HOW IT WORKS"
│   │   ├── H2: "Simple to install. Profound in impact."
│   │   └── 4-up card row:
│   │       ├── 📥 Install in 30 seconds — "Add the Zelophi Chrome extension. No account needed to start. The product works immediately."
│   │       ├── 🔔 Scores appear instantly — "Open YouTube or any supported site and every thumbnail is already scored. No setup. No waiting."
│   │       ├── 🛡️ Harmful content blocked — "When a child clicks something harmful, Zelophi intercepts it before a single frame loads calmly, silently."
│   │       └── 📁 You receive your report — "Receive an email with key insights, blocked content, and practical conversation guides."
│   │
│   ├── Full-bleed family photo (no text overlay)
│   │
│   ├── Features (id="FEATURES")
│   │   ├── Eyebrow: "FEATURES"
│   │   ├── H2: "Not control. Guidance."
│   │   ├── Subhead: "Traditional parental control apps were built for a different era. Zelophi was built for the family you want to be."
│   │   └── Comparison table (Feature / Other Apps / Zelophi):
│   │       ├── Real-time AI content scoring — ✗ / ✓
│   │       ├── Silent operation — no warnings — ✗ / ✓
│   │       ├── Values alignment tracking — ✗ / ✓
│   │       ├── Weekly family insight reports — ✗ / ✓
│   │       ├── Teach Values conversation guides — ✗ / ✓
│   │       ├── Character development framework — ✗ / ✓
│   │       └── Basic content blocking — ✓ (neutral) / ✓
│   │
│   ├── Pricing (id="Pricing")
│   │   ├── Eyebrow: "PRICING"
│   │   ├── H2: "Simple pricing. One account. Whole family."
│   │   ├── Toggle: Monthly / Annual — save 33% (Annual selected by default)
│   │   └── 2 cards:
│   │       ├── Family Monthly — £4.99 — "Install and see Zelophi working immediately." — Full weekly report / Teach Values guide / Unlimited number of kids / All platforms & browsers — CTA "Install Free"
│   │       └── Family Annual — £39.99/year — "BEST VALUE — save 33%" / "That's just £3.33/month" — Everything in Monthly / Priority score updates / Values curriculum / Unlimited children / All platforms and browsers / Family dashboard — CTA "Start Free Trial"
│   │
│   ├── FAQ
│   │   ├── H2: "Your Questions Answered"
│   │   └── Accordion (single-open, first item open by default):
│   │       ├── How does Zelophi protect my child's privacy? → "Zelophi uses privacy-conscious safeguards and gives families clear visibility into activity without exposing unnecessary personal information."
│   │       ├── How does content blocking work? → "Potentially harmful content is identified and interrupted before it loads, while parents receive useful context for a calm follow-up conversation."
│   │       ├── Which platforms does Zelophi support? → "Zelophi is designed for supported browsers and online platforms used by families. The latest compatibility details are available during installation."
│   │       └── How are weekly reports delivered? → "A concise family report is delivered by email each week, summarising activity, blocked content, and useful conversation prompts."
│   │
│   ├── Final CTA band (painterly gradient background)
│   │   ├── H2: "The safer way for children to explore online."
│   │   └── CTA button: "Try zelophi"
│   │
│   └── Footer (shared)
│       ├── Logo "Zelophi"
│       ├── Blurb: "We ensure that the spaces, platforms, and experiences individuals engage with for learning and entertainment are safe, enriching, and built for their well-being."
│       ├── Column "Product": How It Works · Features · Pricing · Chrome Extension
│       ├── Column "Community": Conferences · Summer Camps · Schools · Faith Partners
│       ├── Column "Support": Help Centre · Privacy · Terms
│       ├── Social icons: X · Facebook · Instagram · LinkedIn
│       └── Bottom row: "© 2026 Zelophi. All rights reserved." · "hello@zelophi.com"
│
└── /contact (Contact)
    ├── Header (shared, identical to Home)
    ├── "Get in touch" section
    │   ├── H1: "Get in touch"
    │   ├── Paragraph: "We'd love to hear from you. Reach out using the contact details below and we'll be in touch soon."
    │   ├── Phone: "+001 347 5893"
    │   ├── Email: "hello@zelophi.com"
    │   └── Photo (child on couch with phone)
    ├── Final CTA band (shared, identical to Home: "The safer way for children to explore online.")
    └── Footer (shared, identical to Home)
```

## Navigation structure

- In-page anchors on Home: `#how-it-works`, `#FEATURES`, `#Pricing` (note the mixed casing — reproduced verbatim as anchor IDs for fidelity, though case is irrelevant for `id` matching in HTML).
- Cross-page link: nav CTA + mobile menu CTA → `/contact`.
- Footer "Product" column items point to the same in-page anchors as the main nav (How It Works, Features, Pricing) plus a non-functional "Chrome Extension" item (no target found — treated as a placeholder link, reproduced as `href="#"`).
- Footer "Community" and "Support" columns (Conferences, Summer Camps, Schools, Faith Partners, Help Centre, Privacy, Terms) have no discoverable destination routes on the live site (not in sitemap) — reproduced as placeholder `href="#"` links, consistent with the live site's apparent placeholder state.

## Responsive behavior summary

| Breakpoint | Nav | Hero headline asset | Cards |
|---|---|---|---|
| ≥991px | Full pill nav visible | Desktop 2-line GIF | Multi-column rows (4-up / 2-up) |
| 768–990px | Full pill nav (slightly compressed) | Desktop 2-line GIF | Multi-column, tighter gaps |
| ≤767px | Hamburger → inline push-down menu | Mobile 3-line GIF | Single column, stacked |

## Shared components

Header, mobile nav panel, Final CTA band, and Footer are identical across both routes — implemented once and reused in the clone (`partials` pattern via shared CSS classes + duplicated static markup, since this is a static HTML/CSS/JS build with no server templating).
