# HuskiesOfficial — Brand Guide
### v1.0 · An Arch Essentials brand · huskiesofficial.com

---

## 1. The idea

**Every husky page is a dog account. HuskiesOfficial is an expedition club — for people whose dog thinks every walk is one.**

The brand is not a picture of a husky. It's the *world the husky pulls you into*: the arctic night, the aurora, the treeline, the ridge. Some of our members live that literally — hikers, sledders, backcountry people. The rest live it in spirit, in a city apartment with a dog who screams at the vacuum. One identity holds both, because the feeling is the same.

**Brand line:** THE PACK RUNS NORTH

### Voice
Warm, direct, wry, in on the joke. We speak *as members of the pack*, never as a company addressing customers.

- Humor comes from shared experience — the screaming, the shedding, the escapes. Never from mocking the dogs or their owners.
- Be honest about the breed's difficulty. **Trust is the moat.** We never oversell husky ownership.
- Community first, monetization second. The sales voice never overrides the community voice.

**Avoid:** corporate jargon, generic pet-brand cheerfulness, clickbait, exclamation-mark spam.

---

## 2. Color

The brand lives in **dark mode**. Night is the default background, not an alternate theme.

| Token | Hex | Role |
|---|---|---|
| `night` | `#0A1322` | Arctic night — primary background |
| `night-2` | `#0E1B30` | Raised surface — cards, panels |
| `aurora-teal` | `#3EE6C4` | **Primary accent.** CTAs, highlights |
| `aurora-violet` | `#8B6CFF` | Secondary accent — aurora, "coming soon" |
| `husky-blue` | `#5FA8E6` | The blue eye. Links, gradients |
| `husky-amber` | `#E8A33D` | The amber eye. Always the blue's partner |
| `bone` | `#C8BEAF` | From the logo outline. Connective neutral |
| `ice` | `#EAF4F7` | Primary text on dark |
| `snow-gray` | `#93A7BC` | Muted text on dark |
| `ink` | `#132238` | Primary text on light |
| `paper` | `#F7FAFC` | Light background (print, PDF) |

### The signature pair
**Blue + amber = heterochromia.** This is the ownable detail. When both appear, they're equal partners. **Never use amber alone as an accent** — orphaned, it just looks like a warning color.

### Rules
- `aurora-teal` is the **only** color used for primary CTAs. Do not introduce new accents.
- `bone` is what ties the logo's outline into the interface. Without it, the logo reads as pasted-on. Use it for eyebrow text, hairline rules, and secondary borders.
- Contrast on night: `ice` 14.3:1 · `bone` 9.1:1 · `snow-gray` 6.4:1. For light backgrounds, use `teal-dark` (`#0E9C82`) and `bone-dark` (`#8A7F6D`) — the raw teal and bone fail on white.

---

## 3. Typography

| | Family | Use |
|---|---|---|
| **Display** | Bricolage Grotesque (400/600/800) | Headlines, section titles, stats, buttons |
| **Body** | Inter (400/500/600) | Body copy, labels, forms |

Bricolage is chosen deliberately: its slightly imperfect, wide-set grotesque character reads rugged rather than corporate. It's the typographic equivalent of a national-park sign.

**Gradient text** (teal → husky-blue → violet, via `background-clip:text`) is reserved for **one word** in the H1. Never more than once per page.

---

## 4. Logo

A heritage badge: a Siberian Husky head with heterochromatic eyes, flanked by the pack, under a mountain, above a pine treeline, encircled in bone.

### The assets

| Asset | Use |
|---|---|
| `huskiesofficial-badge.png` | Circular emblem, no text. Universal — any background |
| `huskiesofficial-mark.png` | Small badge for nav headers and footers |
| `huskiesofficial-lockup-DARK-BG.png` | Badge + **white** wordmark → **dark backgrounds only** |
| `huskiesofficial-lockup-LIGHT-BG.png` | Badge + **dark** wordmark → **light backgrounds only** |
| `avatar-facebook-instagram.png` | 512px, night bg. Circle-crop safe (0px loss) |
| `favicon.*` | 16 / 32 / 48 / 64 / 180 / 192 / 512 + `.ico` |
| `og-image.jpg` | 1200×630 link preview |

### Always
- **Choose the lockup by background, not by preference.** This is the single most-broken rule in any brand system.
- Keep clear space of at least 8% of the logo's width on all sides.
- Use the dedicated `avatar` asset for any circular crop. It's padded to survive it.

### Never
- Never recolor, stretch, or change the aspect ratio.
- **Never put the dark-wordmark lockup on a dark background.** It measures 2.1:1 contrast — effectively invisible.
- **Never crop the badge tighter.** The ears and chest ruff span the full circle; clipping them destroys breed recognition. (The erect triangular ears are a primary husky identifier.)
- Never use the badge below 48px. Use the favicon assets instead.

### Format note
Current assets are **raster PNG**. Fine for all digital use. **Vectorize before any print or merch run** — do not upscale the PNG.

---

## 5. Layout & components

- **Container:** max 1060px, 22px gutter
- **Section padding:** 72px vertical
- **Radius:** 14px cards, 10px inputs/buttons, 99px pills
- **No shadows on cards.** Use a 1px `line` border on `night-2`. Shadows are reserved for CTA hover only.

**Signature element — the aurora.** Blurred radial gradients (teal, violet, husky-blue) drifting slowly behind the hero, over a starfield, above a snow ridge. Two layers at 16s and 22s, alternating. This is the brand's motion signature and appears on the site, the PDF, and the OG image.

**Accessibility:** all motion must respect `prefers-reduced-motion`. Contrast minimum 4.5:1 body / 3:1 large.

---

## 6. Rules that aren't visual (but govern every asset)

These are strategy constraints baked into the design system. Anything built for this brand should honor them.

1. **Mobile first, Facebook in-app browser first.** 80%+ of traffic arrives there. It's the least forgiving environment on the internet. Test there before anything else.
2. **Lead with the lead magnet.** Email capture always offers the free *Husky Owner's Cheat Sheet* — never "subscribe to our newsletter."
3. **Tag every subscriber by source.** A hidden `source` field populated from `?utm_source=` (fbgroup / fbpage / ig). Channel attribution is how we learn where buyers come from.
4. **Build monetization dormant.** Revenue modules (e.g. the affiliate "Gear the Pack Trusts" section) are built and hidden behind a body-class flag (`affiliate-off` → `affiliate-on`). Build once, activate later, never rebuild.
5. **Reserved routes:** `/kit` · `/shop` · `/calendar` · `/rescue` · `/meetups` · `/partners`
6. **Revival precedes monetization.** Community trust is restored before anything is sold. This is a brand rule, not just a business one — it governs tone in every asset.

---

## 7. Extending the system (Arch Essentials)

HuskiesOfficial is the prototype, not the endgame. The badge composition, the aurora world, the token structure, and the light/dark lockup pair are all designed to be **re-skinned for other breed communities** under Arch Essentials. When extending:

- Keep the structure (badge, ridge, aurora, night).
- Swap the animal and the signature color pair.
- The heterochromia blue+amber is *specific to huskies* — each new brand needs its own ownable detail.
