# Trattoria Da Stefano — Design System

A single-page marketing site for an authentic Roman restaurant in Da Nang, Vietnam. The design blends Italian trattoria warmth with a modern, conversion-focused layout.

---

## Design Philosophy

The site must feel like stepping into a Roman trattoria — rich, dark, warm, and intimate — while remaining fast, accessible, and easy to navigate on any device. Every visual decision reinforces authenticity: the Italian tricolore runs through the logo, the checkered accent echoes tablecloths, and the dark sections evoke candlelit evenings.

---

## Colour Palette

| Token | Value | Role |
|---|---|---|
| `--primary` | `#cc2200` | CTA buttons, active states, prices |
| `--primary-dk` | `#a81a00` | Hover state for primary buttons |
| `--primary-lt` | `#ff3d1a` | Hover / highlight variant |
| `--accent` | `#f0b429` | Gold — TripAdvisor badge, section dividers, section labels |
| `--accent-lt` | `#ffd96a` | Light gold — nav hover, story badges |
| `--green` | `#2e7d32` | Italian flag green (logo "da") |
| `--green-lt` | `#43a047` | Lighter green variant |
| `--bg` | `#fffdf7` | Warm off-white page background |
| `--bg-alt` | `#fff5e6` | Slightly warmer tint for alternating sections |
| `--bg-dark` | `#1c0800` | Near-black footer and dark sections |
| `--bg-nav` | `#1c0800` | Fixed nav background |
| `--text` | `#1c0800` | Body copy on light backgrounds |
| `--text-muted` | `#6b3a1f` | Captions, form labels, secondary copy |
| `--white` | `#ffffff` | Text on dark backgrounds |
| `--border` | `rgba(204,34,0,.18)` | Subtle red-tinted borders |
| `--checkered` | `#cc2200` | Repeating tablecloth stripe accent |

### Section Rhythm

Alternating light/dark sections create contrast and pacing:

```
Hero (dark overlay) → Trust bar (dark) → Menu (light) →
Story (dark) → About (warm light) → Gallery (light) →
Reviews (dark) → Contact (warm light) → Footer (dark)
```

---

## Typography

Three typefaces, each with a specific role:

| Font | Usage |
|---|---|
| **Abril Fatface** | Display headlines, logo name, section titles, price labels |
| **Lora** (serif) | Body copy, menu item names & descriptions, review quotes |
| **Be Vietnam Pro** (sans-serif) | UI labels, nav links, buttons, form elements, Vietnamese text |

### Type Scale

| Element | Size | Weight | Notes |
|---|---|---|---|
| Hero title | `clamp(3.5rem, 9vw, 7rem)` | — | Abril Fatface |
| Hero sub-title | `clamp(2rem, 5vw, 3.5rem)` | — | Abril Fatface, gold |
| Hero subtitle | `clamp(1rem, 2.5vw, 1.3rem)` | — | Lora italic |
| Section title | `clamp(2rem, 5vw, 3.2rem)` | — | Abril Fatface |
| Section label | `0.7rem` | 600 | Be Vietnam Pro, uppercase, 0.4em tracking |
| Menu item name | `0.95rem` | 600 | Lora |
| Menu item desc | `0.8rem` | — | Lora italic |
| Nav link | `0.78rem` | 500 | Be Vietnam Pro, uppercase, 0.14em tracking |
| Button | `0.85rem` | 600 | Be Vietnam Pro, uppercase |

---

## Logo

The logo encodes the Italian tricolore directly:

```
Trattoria          ← small italic label, muted white
da Stefano         ← "da" in green (#4caf50), "Ste"+"fa" in white, "no" in red (#cc2200)
▓▓▓░░░▓▓▓          ← 3px tricolore bar: green / white / red
```

- "da" uses a smaller size (`1.1rem`) to sit at baseline next to the larger "Ste" (`2rem`)
- The bar is a flex row with three equal `flex:1` spans

---

## Layout & Grid

### Max Content Width
All section content is constrained to `max-width: 1200px` and centred with `margin: 0 auto`.

### Section Padding
`padding: 6rem 5%` on desktop, reduced to `4rem 5%` at `≤ 600px`.

### Key Grids

| Section | Grid |
|---|---|
| Story | `1fr 1fr`, gap `4rem` |
| About cards | `1fr 1fr 1fr` → `1fr 1fr` → `1fr` |
| Gallery | `repeat(3,1fr)` with `.tall` spanning 2 rows → `1fr 1fr` → `1fr` |
| Reviews | `repeat(3,1fr)` → `1fr` |
| Contact | `1fr 1fr` → `1fr` |
| Footer top | `2fr 1fr 1fr` → `1fr` |
| Menu items | `repeat(auto-fill, minmax(320px,1fr))` → `1fr` |

### Navigation
Fixed, `72px` tall (`--nav-h`). Always opaque (dark background). Shadow intensifies on scroll.

---

## Components

### Buttons

| Class | Style |
|---|---|
| `.btn-primary` | Solid red fill, white text; hover → transparent with white text |
| `.btn-outline` | Transparent, white border; hover → gold border, gold text |
| `.nav-cta` | Compact solid red; hover → transparent, gold |
| `.btn-submit` | Full-width solid red; hover → darker red |
| `.whatsapp-btn` | Full-width, `#25D366` green |

All buttons use `border-radius: 3–4px`, uppercase Be Vietnam Pro, and `letter-spacing`.

### Menu Tabs
Flat tab bar with a `3px` bottom border indicator in `--primary`. Tab panels use CSS `display: none / grid` toggled by JavaScript.

### Review Cards
`rgba(255,255,255,.05)` background with a faint gold border on the dark section — creates glass-like depth without using actual blur.

### Story Badges
Small pill labels with 15% gold background tint and 40% opacity gold border — convey key selling points without visual noise.

### Checkered Accent
```css
repeating-linear-gradient(90deg, #cc2200 0, #cc2200 10px, #fff 10px, #fff 20px)
```
8px tall horizontal stripe. Appears between major sections as a tablecloth nod.

---

## Scroll & Animation

### Reveal Animation
Elements with `.reveal` start hidden (`opacity: 0; transform: translateY(40px)`) and transition to visible once they enter the viewport (IntersectionObserver, threshold `0.12`). Observed once — observer disconnects after trigger.

### Hero Entrance
Staggered `fadeUp` keyframe animation (opacity 0 → 1, Y 30px → 0):
- Eyebrow: `0.3s` delay
- Title: `0.5s` delay
- Sub-title: `0.65s` delay
- Subtitle: `0.8s` delay
- Buttons: `1.0s` delay
- Scroll indicator: `1.3s` delay

### Hero Parallax
`hero-bg` translates on scroll: `translateY(scrollY × 0.3px)` with a base `scale(1.05)` to prevent edge gaps. Passive scroll listener.

### `prefers-reduced-motion`
All animations and parallax are disabled for users who opt out. The `hero-bg` transform is reset to `none`, and `.reveal` elements are shown immediately.

---

## Responsive Breakpoints

| Breakpoint | Changes |
|---|---|
| `≤ 900px` | Nav links and CTA hidden; hamburger shown. Grids collapse to 1–2 cols. Gallery tall items lose row-span. |
| `≤ 600px` | Section padding reduced. About, gallery, form row grids go single-column. Trust separators hidden. |

Mobile menu is a full-screen overlay (`position:fixed; inset:0`) with `display:flex` toggled via the `.open` class.

---

## Internationalisation (EN / VI)

All user-visible strings are dual-encoded as `data-en` and `data-vi` attributes. `setLang(lang)` iterates all elements with either attribute and sets `textContent` to the requested language. The `<html lang>` attribute is updated accordingly.

Vietnamese body copy uses **Be Vietnam Pro** (sans-serif) via the `:lang(vi)` and `[data-vi]` selectors to maintain readability.

---

## Images

All images live in `img/` and are referenced by filename. Required files:

| File | Used in |
|---|---|
| `img/hero.jpg` | Hero background |
| `img/interior.jpg` | Story (main), Gallery |
| `img/facade.jpg` | Story (side), Gallery (tall) |
| `img/amatriciana.jpg` | Story (side) |
| `img/carbonara.jpg` | Gallery |
| `img/vongole.jpg` | Gallery |
| `img/pizza.jpg` | Gallery |

All `<img>` tags include descriptive `alt` text for SEO and accessibility, and use `loading="lazy"` except where above the fold.

---

## SEO & Structured Data

- `<title>` and two `<meta name="description">` tags (EN and VI)
- `<link rel="canonical">` and `hreflang` alternates for `en`, `vi`, and `x-default`
- Open Graph tags (`og:type restaurant`, title, description, locale)
- JSON-LD `Restaurant` schema with address, opening hours, telephone, menu URL, price range, and `sameAs` social links

---

## Performance Notes

- Google Fonts loaded with `preconnect` and `crossorigin` hints
- `display=swap` on the font URL to prevent FOIT
- Images are `loading="lazy"` throughout (hero excluded — it is the LCP element)
- Scroll listeners are `{ passive: true }` to avoid blocking the main thread
- No external JS libraries; all interactivity is vanilla JS
