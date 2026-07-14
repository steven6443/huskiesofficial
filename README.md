# HuskiesOfficial

The world's largest Siberian Husky community. An Arch Essentials brand.
**Live:** https://www.huskiesofficial.com

---

## Design system

This repo is the source of truth for the HuskiesOfficial brand.

| File | What it is |
|---|---|
| `design-system-spec.json` | Machine-readable spec — tokens, components, logo rules, voice |
| `tokens.css` | CSS custom properties. Import before any other stylesheet |
| `BRAND-GUIDE.md` | Human-readable guide — the idea, the rules, the reasoning |
| `index.html` | Landing page. Reference implementation of every pattern |

### Importing into Claude Design

1. Push this repo to GitHub.
2. In Claude Design, connect this repository as a design system source.
3. Claude reads `tokens.css` and `design-system-spec.json` and builds with the real system — colors, type, components, and logo rules — checking its own output against the spec.

Every new project then inherits HuskiesOfficial automatically. Don't route through Figma; Claude Design can't read Figma files directly.

---

## Brand assets

| File | Use |
|---|---|
| `huskiesofficial-badge.png` | Circular emblem, no text. Any background |
| `huskiesofficial-mark.png` | Small badge — nav header, footer |
| `huskiesofficial-lockup-DARK-BG.png` | Badge + white wordmark → **dark backgrounds only** |
| `huskiesofficial-lockup-LIGHT-BG.png` | Badge + dark wordmark → **light backgrounds only** |
| `avatar-facebook-instagram.png` | Social avatar. Circle-crop safe |
| `favicon.*` | 16 / 32 / 48 / 64 / 180 / 192 / 512 + `.ico` |
| `og-image.jpg` | 1200×630 link preview |

**The one rule people break:** choose the lockup by *background*, not by preference. The dark-wordmark lockup on a dark background measures 2.1:1 contrast — effectively invisible.

---

## The three colors that matter

- `#0A1322` **night** — the brand lives in dark mode by default
- `#3EE6C4` **aurora-teal** — the only primary CTA color
- `#5FA8E6` + `#E8A33D` **blue + amber** — heterochromia, the ownable detail. Always partners, never amber alone

---

## Deploy

Static site on GitHub Pages. No build step.

Before going live, fill in the `TODO` markers in `index.html`:
- Kit form ID (and create a custom field named `source`)
- Meta Pixel ID
- GA4 Measurement ID
- Facebook Group, Facebook Page, and Instagram URLs

Then point DNS at GitHub Pages, enable HTTPS, and run the URL through Facebook's Sharing Debugger once so the OG image caches correctly.

### Channel-tagged links
Use these in each platform's bio so subscribers are attributed to a source:
```
huskiesofficial.com/?utm_source=fbgroup
huskiesofficial.com/?utm_source=fbpage
huskiesofficial.com/?utm_source=ig
```

### Reserved routes
`/kit` · `/shop` · `/calendar` · `/rescue` · `/meetups` · `/partners`

---

## Principles

1. **Revival precedes monetization.** Community trust is restored before anything is sold.
2. **Mobile first, Facebook in-app browser first.** That's where 80%+ of traffic lands.
3. **Build monetization dormant.** Revenue modules ship hidden behind a CSS flag, then activate. Build once, never rebuild.
4. **Lead with the lead magnet**, never "subscribe to our newsletter."
