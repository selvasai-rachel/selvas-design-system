# SELVAS AI — Design System

The shared visual language for **SELVAS AI** (셀바스 AI) — a Korean enterprise AI company building voice intelligence (음성지능), handwriting intelligence (필기지능), and image intelligence (영상지능) products.

The system is rooted in **Tailwind v4** + **shadcn/ui** scaffolding, retuned around two house colors:

| Role | Hex | Use |
|---|---|---|
| **Primary** lime green | `#87C82F` | Primary actions, focus, brand marks |
| **Secondary** dark slate-blue | `#384F5E` | Secondary actions, dark chrome |

Pretendard is the primary typeface so Korean and English copy share rhythm; Inter steps in for English-only chrome and Geist Mono for code.

---

## Files

- `colors_and_type.css` — single source of truth for color, typography, spacing, radius, shadow, and motion tokens. Drop into any prototype with `<link rel="stylesheet" href="colors_and_type.css">`.
- `previews/Type.html` — type ramp card.
- `previews/Colors.html` — full palette swatch sheet.
- `previews/Spacing.html` — spacing, radius, shadow tokens.
- `previews/Components.html` — button, input, switch, tabs, badge, card.
- `previews/Brand.html` — logo, semantic palette, voice + tone.
- `Index.html` — entry point linking everything.
- `SKILL.md` — drop-in reference for designers/agents using the system.

---

## Token quick-reference

### Brand colors

```
--primary       #87C82F   (lime — base 500)
--primary-text  #6CA823   (text on light surfaces — 600)
--secondary     #384F5E   (slate-blue — 700)
--destructive   #DC2626
--warning       #FACC15
--success       #22C55E
--info          #2563EB
```

### Type scale (PC)

| Token | Size / Line | Tracking |
|---|---|---|
| display-lg | 64 / 74 | -0.02em |
| display-md | 48 / 58 | -0.02em |
| display-sm | 44 / 53 | -0.02em |
| heading-lg | 32 / 42 | -0.01em |
| heading-md | 24 / 32 | -0.01em |
| heading-sm | 20 / 28 | -0.01em |
| heading-xs | 18 / 26 | 0 |
| heading-xxs | 16 / 24 | 0 |
| body-lg | 18 / 28 | 0 |
| body-md | 16 / 24 | 0 |
| body-sm | 14 / 21 | 0 |
| body-xs | 12 / 17 | 0 |

Mobile drops display sizes by ~50% and trims heading-lg → 24, heading-md → 22.

### Spacing

`2px / 4px / 8px / 12px / 16px / 20px / 24px / 32px / 48px / 64px` — t-shirt named `2xs` → `5xl`.

### Radius

`2 / 4 / 6 / 8 / 12 / 16 / 24 / pill`.  Default for buttons + inputs is `6px`.

---

## Editorial principles

1. **Information grouping.** Layouts should help users perceive grouping at a glance — clear surfaces, generous gaps between groups, tight gaps within them.
2. **Modern and clear.** No decorative gradients, no skeuomorphic shadows. The lime accent does the work — keep everything else neutral.
3. **Korean-first typography.** Pretendard renders Hangul, Hanja, and Latin from one family, so don't switch fonts mid-line.  Use Inter only when the surface is English-only chrome (a developer dashboard, an English console, etc.).
4. **Two anchors.** Lime green (#87C82F) for forward motion. Slate-blue (#384F5E) for ground / authority. Avoid introducing a third "brand" hue.
5. **Slate, not pure gray.** Body copy and chrome use the slate ramp (cool bias). Pure neutral gray is reserved for muted utility states.
