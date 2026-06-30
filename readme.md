# Carpet Guys — Design System

A clean, trustworthy, conversion-focused design system for **Carpet Guys**, a residential + commercial carpet cleaning company serving **Central Pennsylvania** (Harrisburg, Camp Hill, Mechanicsburg, Lemoyne, and surrounding areas).

This system supports two parallel customer journeys:
- **Residential** → flat per-area package pricing, easy to **Book Online**.
- **Commercial** → variable jobs that go through **Request a Quote**.

The unifying line is: **Flat prices for homes. Clear quotes for businesses. Easy booking for everyone.**

---

## Sources we worked from

The user provided this brief and a folder of real Carpet Guys assets (vans, before/after photos, gallery shots, the 2023 Best of Harrisburg award, real Google reviews, a logo icon).

- Brief: pasted into the project (full residential/commercial spec, page architecture, palette guidance, copy rules)
- Real photography: `assets/van.png`, `assets/van2.jpeg`, `assets/before*`, `assets/after*`, `assets/gallery*.jpg`, `assets/upholstery.jpg`, `assets/petstain*.jpg`, `assets/cleancarpet.jpg`, `assets/carpet.png`, `assets/tilegrout.png`
- Trust assets: `assets/award.png` (Voted Best of Harrisburg 2023), `assets/review1.png` … `assets/review3.png` (real Google reviews)
- Brand mark: `assets/logo.png` (the Carpet Guys mascot + green-on-black "CARPET GUYS" wordmark)

> The mark we have is a 192×192 favicon-sized PNG. **Ask the user for the high-res master logo (SVG ideally), and confirm the exact green hex.** We're using `#7ED321` derived visually from the mark and van decals.

---

## Index

| File | Purpose |
|---|---|
| `README.md` | This file — context, content rules, visual foundations, iconography. |
| `colors_and_type.css` | All design tokens: colors, type, spacing, radii, shadow, motion. |
| `SKILL.md` | Cross-compatible Agent Skill manifest for downloading. |
| `assets/` | Real photography, logo, award, review screenshots. |
| `preview/` | Cards rendered on the **Design System** tab (type, color, spacing, components, brand). |
| `ui_kits/website/` | High-fidelity recreation of the **Carpet Guys website** (home + 6 sub-pages) using all of the above. |

---

## Brand at a glance

| | |
|---|---|
| **Voice** | Local, practical, no-nonsense. The owner talking, not a marketing department. |
| **Wordmark** | "CARPET GUYS" set in a heavy condensed display, with a small standing-technician mascot to the left holding a wand and a bucket. |
| **Primary accent** | Lime green `#7ED321` — used for CTAs and the wordmark. |
| **Dark base** | Near-black `#0E1110` — used for headers, footers, the commercial page, and contrast sections. |
| **Light base** | Warm cream `#F7F5EE` — used for residential / approachable surfaces. |
| **Trust marks** | "Best of Harrisburg 2023" (gold), real Google review cards (do not fabricate). |
| **Tagline** | *Flat prices for homes. Clear quotes for businesses.* |

---

## Content fundamentals

### Tone
- **Direct, local, plain-spoken.** The site should read the way a contractor talks when they're confident in their pricing. Short sentences. No fluff. No "we are passionate about delivering exceptional carpet experiences."
- **You-not-we.** Headlines and CTAs address the customer ("your carpet," "book your cleaning"), not the company.
- **Trust through specifics, not adjectives.** Don't say "affordable" — say `$50/area, $150 minimum`. Don't say "fast drying" — say `Rapid Dry: 3 fans / 24 hours`.

### Casing
- **Display headlines (H1/H2):** ALL CAPS in the Anton display face. Tight letter-spacing. This is the loudest part of the brand.
- **Eyebrows:** ALL CAPS, tracked out (0.18em), small (12px). Always paired with a 24px green rule to the left.
- **Sub-headings (H3/H4):** Sentence case in Archivo (heavy sans). Never all caps.
- **Body:** Sentence case in Manrope. Never italic for emphasis — use weight.
- **Buttons:** ALL CAPS, tracked +0.04em, weight 800.

### Casing examples
- ✅ `CARPET CLEANING IN CENTRAL PA WITHOUT THE GUESSING.`
- ✅ `Choose your carpet cleaning package.`
- ✅ `BOOK ONLINE` / `REQUEST A QUOTE` / `CALL NOW`
- ❌ `Learn More`, `Submit`, `Click Here`, `Book Now to Start Your Journey!`

### CTA copy rules (CRITICAL)
- **Primary actions are verbs that match the booking model.**
  - Predictable residential service → `BOOK <PACKAGE>` (e.g. `BOOK STANDARD`)
  - Variable / commercial service → `REQUEST A QUOTE` or `REQUEST COMMERCIAL QUOTE`
- **Phone is always reachable** as a secondary CTA: `CALL NOW`.
- **Microcopy near pricing:** *"Know your package? Book online. Not sure what your carpet needs? Request a quote."*

### Pricing copy rules
- Always show the unit (`$50 / area`).
- Always show the minimum where it applies (`$150 minimum for up to 3 areas`).
- Never bury "per area" in fine print.
- Never lead with discounts or coupon energy.
- For variable services, write "**Starts at $X**" — never a single fixed price.

### Emoji & exclamation marks
- **No emoji** anywhere. The brand mascot does the warmth lifting. Emoji would cheapen it.
- **No exclamation marks** in body copy. One is allowed in a homepage hero CTA at most.

### Trust language
- Real review cards only — pulled from Google, attributed by first name + initial.
- Award badge ("Voted Best of Harrisburg 2023, Clipper Magazine") shown small, never as the hero of a section.
- "**Locally owned. Central PA only.**" — say it once, prominently, in About + footer.

---

## Visual foundations

### Color
A two-base system: **dark sections** for commercial credibility + contrast moments, **cream sections** for residential approachability. Green is a single accent, used **only** for primary CTAs and brand surfaces. Never used as a body text color or background field.

- `--cg-green: #7ED321` — primary accent (CTAs, brand mark, eyebrow rules)
- `--cg-green-deep: #5FA316` — hover/press
- `--cg-ink: #0E1110` — dark surface (header, footer, commercial hero, contrast bands)
- `--cg-cream: #F7F5EE` — default page background, residential surfaces
- `--cg-stone: #EFEDE6` — secondary card surface on light
- `--cg-gold: #B8924E` — reserved for award badges only
- `--cg-blue-trust: #1F6FA8` — used **only** to chrome real Google reviews (the Google "G")

**Rules:**
- No gradients on backgrounds. Solid fills only. (One exception: a faint cream→stone band can separate sections.)
- No drop-shadows on color blocks. Subtle shadows live only on cards.
- White (`#FFFFFF`) is used sparingly — for package cards on cream, and for the form field interior on dark.

### Type
- **Display: Anton** — for H1/H2. Heavy condensed, all caps, 0.95 line-height. This is the brand's "voice."
- **Headline: Archivo** — for H3/H4 and section titles. Strong but readable.
- **Body: Manrope** — for paragraphs and UI. Modern, clean, slightly geometric.
- **Pricing:** Anton at 64px+. Always larger than the surrounding heading. Always paired with a smaller `/ area` unit in Manrope.

> **Substitution flag:** all three families are loaded from Google Fonts (free + permissive). No proprietary type files were provided. If Carpet Guys has a specific licensed face for the wordmark, please share it.

### Spacing & rhythm
- 8-point base scale: `4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128`.
- Section vertical padding: **96px** desktop, **48px** mobile.
- Card interior padding: **32px** desktop, **20px** mobile.
- Max content width: **1240px**, gutters **24px**.

### Borders, radii, cards
- **Radius scale:** 4 / 8 / 12 / 14 / pill. Cards use **12px**, buttons use **10px**, badges use pills.
- **Border:** `1px solid rgba(14,17,16,0.10)` on light, `1px solid rgba(255,255,255,0.10)` on dark. Borders are the primary affordance — shadows are a quiet support.
- **Cards:** flat, bordered, optional `--cg-shadow-2` only on hover or on primary "Most Popular" card. No SaaS-style heavy lift shadows.
- **No left-border-only colored accent cards.** That's the carpet-cleaner-template trope we're explicitly fighting.

### Backgrounds & imagery
- **Real photos only** — every photo on the site is a real Carpet Guys job (vans, before/after, gallery, upholstery, pet stains).
- Photo treatment is **honest and minimal** — no heavy filters, no cyan-orange grading, no fake dramatic before/after color shifts.
- Hero compositions are **split** (image one side, words the other) or **full-bleed with a dark scrim** for legibility. Never a small inset image with a giant gradient behind it.
- No SVG illustrations. No cartoon mops. No stock cleaning families on couches.

### Animation & interaction
- **Entry:** 220ms fade + 8px translate-up, eased on `cubic-bezier(0.22, 0.61, 0.36, 1)`. One element at a time when stacked. Never a 6-card cascade.
- **Hover (buttons):** background goes from `--cg-green` → `--cg-green-deep`, no scale, no glow. 120ms.
- **Hover (cards):** border darkens slightly, shadow lifts to `--cg-shadow-2`, image inside scales 1.02 over 360ms. Card itself does **not** translate.
- **Press:** brief 50ms scale to 0.98, then back. No bounces.
- **Sticky mobile CTA bar:** fixed bottom, 60px tall, `Call Now | Book Online`. Slides up after 240px scroll.
- No parallax. No marquee that moves on its own (the trust strip is static).

### Transparency & blur
- Almost never. The header is solid (cream when on cream, ink when scrolled past hero, no glassmorphism).
- The only blurred surface is the dialog/quote-modal backdrop: `rgba(14,17,16,0.6)` with `backdrop-filter: blur(8px)`.

### Imagery color vibe
- Carpets photographed under warm natural light → tones lean warm beige / brown / cream. The cream page surface complements this; the dark sections give the photos contrast.
- **Do not** color-correct photos toward cool blue. Carpet cleaning is a warm-tone industry.

---

## Iconography

Carpet Guys does **not** ship a custom icon set. The brand's "iconography" is the **mascot character** + **real photography**.

- **Lucide** is our default icon set (loaded via CDN), used at 1.5px stroke. We use it sparingly:
  - Phone, MapPin, Clock, Check, ArrowRight, Star, ChevronDown — and that's about it.
  - Never on package cards (those use real photos + the price).
  - Never decoratively — every icon must label something.
- **Mascot:** the standing technician with wand + bucket from the wordmark. Used as a small (24–32px) accent on the footer, the favicon, and 404. Not in marketing surfaces.
- **No emoji. No flat illustrative icons. No gradient mesh icons. No outlined-cleaning-supply illustration sets.**
- **Trust icons:** the gold Best-of-Harrisburg badge and the Google "G" on review cards are the only colored marks allowed.

---

## File map

```
.
├── README.md                  ← you are here
├── SKILL.md                   ← agent-skill manifest
├── colors_and_type.css        ← all tokens
├── assets/
│   ├── logo.png
│   ├── award.png              ← Best of Harrisburg 2023
│   ├── van.png, van2.jpeg     ← branded vans
│   ├── before1/2.png/jpg
│   ├── after1/2.png/jpg
│   ├── cleancarpet.jpg
│   ├── carpet.png
│   ├── petstaina/b.jpg
│   ├── upholstery.jpg
│   ├── tilegrout.png
│   ├── gallery5..19.jpg
│   └── review1..3.png
├── preview/                   ← Design System tab cards
│   ├── colors-*.html
│   ├── type-*.html
│   ├── spacing-*.html
│   ├── components-*.html
│   └── brand-*.html
└── ui_kits/
    └── website/
        ├── README.md
        ├── index.html         ← /
        ├── carpet-cleaning.html
        ├── commercial.html
        ├── upholstery.html
        ├── results.html
        ├── about.html
        └── contact.html
```
# carpet-guys
