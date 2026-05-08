# SKILL.md — SELVAS AI Design System

> Drop-in reference for any agent or designer building inside the SELVAS AI
> visual language. Read this before producing any artifact for a SELVAS surface.

## What this system is

SELVAS AI (셀바스 AI) is a Korean enterprise AI company.  The system uses a
**Tailwind v4 + shadcn/ui** scaffold, retuned around two house colors:

| Role | Hex |
|---|---|
| Primary — lime green | `#87C82F` |
| Secondary — dark slate-blue | `#384F5E` |

Pretendard is the primary typeface (Korean + Latin), Inter handles
English-only chrome, Geist Mono carries code.

## Wiring it up

Always include the token sheet:

```html
<link rel="stylesheet" href="<path>/colors_and_type.css">
```

It declares every CSS custom property under `:root` and applies the default
font + color to `html`, `h1–h5`, `p`, `code`, `button`, and form controls.
Use the variables — never hand-paste hex values.

## Quick token cheatsheet

```css
/* Brand */
var(--primary)            /* #87C82F  CTAs, focus, brand */
var(--primary-text)       /* #6CA823  primary text on light */
var(--secondary)          /* #384F5E  secondary actions, dark chrome */

/* Surfaces */
var(--bg-canvas)          /* #FFFFFF */
var(--bg-subtle)          /* slate-50  — page tint */
var(--bg-muted)           /* slate-100 — toolbar/tab track */
var(--bg-inverse)         /* slate-950 — dark surface */

/* Text */
var(--fg-default)         /* slate-950 */
var(--fg-muted)           /* slate-600 */
var(--fg-subtle)          /* slate-500 */
var(--fg-on-primary)      /* #0A0A0A — text on lime */
var(--fg-inverse)         /* white */

/* Border */
var(--border-default)     /* slate-200 */
var(--border-strong)      /* slate-300 */
var(--border-subtle)      /* slate-100 */

/* Semantic */
var(--destructive) var(--warning) var(--success) var(--info)

/* Focus rings — set as box-shadow */
var(--ring-default)   /* lime, default */
var(--ring-error)     /* red */
var(--ring-sidebar)   /* slate-blue, for dark chrome */
```

Spacing: `--space-2xs` (2) → `--space-5xl` (64).
Radius: `--radius-xs` (2) → `--radius-3xl` (24) + `--radius-full`.  Default
is `--radius-md` (6).
Shadow: `--shadow-xs` → `--shadow-2xl`.
Motion: `--duration-fast` (150ms), `--duration-base` (200ms),
`--ease-standard`.

## Typography

Use the `t-*` utility classes or the matching headings:

```html
<h1 class="t-display-md">음성지능</h1>           <!-- 48 / 700 / -0.02em -->
<h1>큰 헤드라인</h1>                              <!-- = heading-lg, 32 -->
<p class="t-body-md">…</p>                       <!-- 16 / 400 -->
<p class="t-body-sm">…</p>                       <!-- 14 / 400, muted -->
```

PC sizes — display 64/48/44, heading 32/24/20/18/16, body 18/16/14/12.
On mobile drop displays to ~32/28 and heading-lg/md to 24/22.

**One font per line.** Pretendard renders both Hangul and Latin — don't
toggle to Inter mid-sentence. Use Inter only for English-only screens
(developer console chrome, English-only docs, etc.).

## Components — house style

- **Buttons**: 6 px corner, 36 px default height, 14 px font, `--ease-standard`
  150 ms transitions. Variants: `primary`, `secondary`, `tertiary`, `outline`,
  `ghost`, `ghost-muted`, `destructive`. Sizes: `lg/default/sm/mini`.
  A `--round` modifier swaps to a pill.
- **Inputs**: 36 px tall, 6 px corner, slate-200 border, white surface.
  On focus the border picks up `--primary` and adds `--ring-default`.
- **Switch**: 36×20 pill, slate-200 off, lime on, white knob with `shadow-xs`.
- **Tabs**: segmented control on a slate-100 track, white active pill with
  `shadow-xs`.
- **Badges**: pill, soft-tinted ramp 100 background + ramp 800 text.
- **Cards**: white surface, slate-200 border, `--radius-lg`, `--shadow-sm`.
  Dark variant uses `slate-950` background with slate-800 border.

The lime focus ring is shared across every interactive primitive — that's
the strongest cue that you're inside the SELVAS system.

## Editorial defaults

1. **Information grouping.** Generous gap between groups (`--space-3xl`),
   tight gap within (`--space-s` to `--space-md`).
2. **Modern and clear.** Skip decorative gradients and skeuomorphic shadows.
   Lime green does the highlighting.
3. **Korean first.** Korean text reads naturally in body-md (16/24).
   Display sizes work for both scripts.
4. **Slate, not gray.** Body copy + chrome use the slate ramp; pure gray is
   reserved for muted utility states.
5. **Two anchors only.** Lime and slate-blue. Reach for semantic ramps
   (red/yellow/green/blue) only when meaning warrants.

## When you're missing an asset

The official logo, icon set, and product imagery are not yet packaged.
Treat them as placeholders — see `previews/Brand.html` for the placeholder
mark.  Ask the user for the official lockup before shipping anything
external-facing.
