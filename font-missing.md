# Font Extraction Report

All fonts used by https://zelophi.com/ were successfully identified and extracted as real font files. **Nothing is missing.** This file exists to document that the check was performed, per the extraction workflow.

| Family | Weights/styles used on-site | License | Source | Extracted? |
|---|---|---|---|---|
| DM Sans | 400, 400 italic, 500, 600 | SIL Open Font License (Google Fonts) | fonts.gstatic.com | ✅ `/assets/fonts/DMSans-*.woff2` |
| DM Mono | 400, 500 | SIL Open Font License (Google Fonts) | fonts.gstatic.com | ✅ `/assets/fonts/DMMono-*.woff2` |
| Faculty Glyphic | 400 | SIL Open Font License (Google Fonts) | fonts.gstatic.com | ✅ `/assets/fonts/FacultyGlyphic-400.woff2` |
| Inter | 400, 400 italic, 500, 700, 700 italic | SIL Open Font License (Google Fonts, self-hosted by Framer) | framerusercontent.com | ✅ `/assets/fonts/Inter-*.woff2` (7 unicode-range subset files per weight, matching the original's exact subsetting) |
| Switzer | 400, 500 | Fontshare Free License | framerusercontent.com (Fontshare CDN passthrough) | ✅ `/assets/fonts/Switzer-400.woff2`, `Switzer-500.woff2` |

All `@font-face` declarations, including original `unicode-range` values, were preserved and rewritten to point at the local files in [css/fonts.css](css/fonts.css).

No commercial/licensed foundry fonts (e.g. Klim, Commercial Type, custom GT faces) are used anywhere on the site, so no substitution was ever required.
