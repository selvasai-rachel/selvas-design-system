# Extracted from Figma (Obra shadcn_ui-based design system, Korean SELVAS AI)

## Core character
- Tailwind v4 base, shadcn_ui flavored
- Korean primary brand: 셀바스 — modern, clear, information grouping
- Description text: "색상은 사용자의 주의를 유도하고, 기능이나 메시지를 명확히 하여 직관적인 사용자 경험을 제공한다. 색상 체계는 셀바스 브랜드 이미지와 일관된 시각적 경험을 유지하기 위해 체계적으로 구성되며, 정보의 계층과 우선순위를 시각적으로 구분하는 역할을 한다."

## Top fonts (from METADATA)
- Pretendard (Regular/SemiBold/Bold/Medium/Light) — Korean primary
- Inter (Medium/Regular/SemiBold/Bold) — UI labels (chrome)
- Geist (Regular/Medium/SemiBold/Light) — used for some UI/mono
- Pretendard GOV (variant)

## Type scale (Pretendard)
- Display large/medium/small — sizes 64/?/44px PC; 32/.../28 mobile
- Heading large/medium/small/xsmall/xxsmall — 32/24/20/18/16 PC; 24/22/20/18/16 mobile (Bold)
- Body medium/small/xsmall — 16/14/12 PC same mobile (Bold variant; 140% line height)
- Body Bold variant
- Letter spacing -1px on display/heading

## Color palette signals
- Primary: PURPLE (rgb 151,71,255 = #9747FF) used 3383× — the brand purple
- Slate gray (rgb 71,85,105 = #475569) is dominant for fg/text/stroke (7330×)
- Tailwind slate scale visible (slate-50 through 950)
- Lime/green semantic: rgb(135,200,47), rgb(122,221,5) - success
- Red: rgb(220,38,38), rgb(239,68,68) - destructive/error
- Black bg: rgb(2,6,23) - slate-950
- Colors columns: Primary, Secondary, Slate Gray, Gray (cool), Error (red), Warning (yellow), Success (green), Info (blue)
- Primary 50 swatch: rgb(246,251,234) — light lime tint? Actually no, looking again — primary 50 is rgb(246,251,234) — that's lime/green. WAIT, but Primary uses purple (151,71,255). Let me reconcile: Primary swatch col uses 246,251,234 (50) -> 233,246,209 (100). This is GREEN. So Primary may actually be a LIME GREEN
- Secondary 50: rgb(246,255,229) — also lime/green
- Slate Gray 50: rgb(243,247,248) — neutral
- Gray 50: rgb(243,247,252) — cool gray

CONFIRMED FROM SCREENSHOT: Primary IS GREEN family.

## CONFIRMED COLOR LAYOUT (from screenshot)
주요 색상 (Main):
1. Primary (2 columns of green swatches) — 500 Base, 600 Text in col1; 200 Text in col2 (lime/olive green; brand)
2. Secondary color (2 columns of slate-blue swatches) — 700 Base, 800 text in col1; 800 Base in col2 (steel/slate blues)
3. Slate Gray (1 col) — bluish slate
4. CoolGray (1 col) — neutral cool gray

Semantic:
5. Gray (true neutral gray)
6. Red — 500 Base (destructive)
7. Yellow — 300 Base (warning, mid-orange)
8. Green — 500 Base (success)
9. Blue — 600 Base (info)

Tailwind v4 names — use Tailwind v4 default values for all 11-step scales (50,100,200,300,400,500,600,700,800,900,950).

## Spacing tokens
- Spacing-2xs / xs / s / md / lg / xl / 2xl / 3xl / 4xl / 5xl

## Radius tokens
- rounded-xs / sm / md / lg / xl / 2xl / 3xl / full

## Shadow tokens
- shadow-xs/sm/md/lg/xl/2xl
- focus ring (default / sidebar / error)

## Component coverage included
- Button (many variants), Input, Textarea, Field, Icon-Button
- Sidebar, Navigation-Menu, Pagination, Tabs, Drawer
- Switch, Checkbox, Radio, Select-Combobox
- Table, Data-Table, Tooltip
- Input-File
- Icons: Lucide-style icon system; FlagKr / FlagUs flags

## SELVAS AI context (from user)
- 음성지능 (Voice intelligence)
- 필기지능 (Handwriting intelligence)
- 영상지능 (Image intelligence)
- AI solutions provider, Korean enterprise

## Button system (from Figma /Button/Button)
- Variants: Primary, Secondary, Tertiary, Outline, Ghost, Destructive, Ghost Muted
- Sizes: Default, Large, Small, Mini
- Roundness: Default, Round
- States: Default (others likely Hover/Active/Disabled/Loading)
- Note: purple (rgb 151,71,255) appears as Figma annotation/bracket color (Inter 12px labels in figma chrome), NOT the brand color
- Default Mini button: 8px radius, padding 3px 8px, Inter 14/500, color rgb(51,65,85) (slate-700) for ghost label

## CONFIRMED button colors (from variant components)
- Primary bg: rgb(135,200,47) #87C82F (lime green) — text black
- Secondary bg: rgb(56,79,94) #384F5E (dark slate-blue) — text white
- Destructive bg: rgb(220,38,38) #DC2626 (red-600) — text white
- Outline: white/transparent bg, border rgb(203,213,225) #CBD5E1 (slate-300), text rgb(2,6,23) #020617 (slate-950)
- All buttons borderRadius: 6 default, "round" = pill

## Tone
- Modern, clear ("모던하고 명확함")
- Information grouping helps user perceive info ("정보의 그룹핑이 사용자에게 정보를 인식하는데 도움을 줌")
