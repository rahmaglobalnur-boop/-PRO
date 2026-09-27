# rahmaglobal.uz — design principles (read before any page work)

Owner's rule (2026-09-26): every inner page (SEO pages in `simptomy/`, product pages, new
landing pages) uses the SAME system as the main site. No "AI-looking" layouts.

Sources studied: `rahmaglobalnur-boop/A.LAGUTA` (Laguta references, GRID.png, OPERA AUSTRALIA),
`rahmaglobalnur-boop/Minimalizm` (`docs/NUR_DESIGN_SYSTEM.md` — Apple Monochrome × Laguta),
`rahmaglobalnur-boop/COMANDOS` (design-jury, verify-site, brief-interview skills),
`rahmaglobalnur-boop/Claude-Fonts-`. The NUR Design System's own colours/fonts belong to
FURSAN / TASLIM / NUR Mediaholding — for rahmaglobal.uz take its PRINCIPLES, keep the tokens below.

## Tokens (identical to index.html)
- Colours: `--ink #0A0A0A`, `--cream #EFEEE9` (page background), greys `#6E6B63 #9A968D #B9B5AC
  #D7D4CC #8E8A80 #C9C6BE`, white `#FFFFFF`. One warm accent at most: `#C9B389` / `#8A7550`
  for key numbers only. No other colours.
- Type pair: **Ammar** (display, H1, big numbers) + **Interphases** (everything else).
  - H1 — Ammar 400, `clamp(40px,9vw,70px)`, line-height 1.05, letter-spacing -.02em
  - H2 — Interphases 600, `clamp(28px,5vw,40px)`, line-height 1.15, letter-spacing -.02em
  - H3 — Interphases 600, 16px, line-height 1.3, letter-spacing .1em, UPPERCASE
  - Body — Interphases 16px, line-height 1.6–1.7
  - Section label — 13px, letter-spacing .14em, uppercase, grey
- Container: `max-width:1560px; padding:0 clamp(20px,4vw,64px)`. Section padding 80px (mobile 48px).
- Radius 0 everywhere. Borders 1px `rgba(10,10,10,.12–.16)`.

## SEO / inner pages palette — Apple neutrals (owner, 2026-09-26)
Owner: the cream `#EFEEE9` reads yellowish / "AI" on the SEO pages. Inner pages use Apple whites:
canvas `#FFFFFF`, alternate sections `#F5F5F7` (silver), text `#1D1D1F`, secondary `#6E6E73`,
lines `#D2D2D7`, final band `#000` with `#F5F5F7` / `#A1A1A6`. No accent hue: key numbers are
`#1D1D1F`, set apart by size only. (Main SPA index.html still cream — change only if owner asks.)

## Impeccable (anti-AI-slop skill, repo rahmaglobalnur-boop/Impeccable_-design-skill.)
Load its `reference/craft-floor.md` before editing UI. Hard rules adopted:
- NO eyebrow/kicker labels above headings; the heading carries itself.
- NO decorative section numbers (01/02/03) unless the order matters (recipe steps: OK).
- NO unicode arrows/emoji as icons: draw SVG (1.2px stroke).
- Max ~2 em-dashes per page body (AI cadence tell); prefer commas, colons, periods.
- Theme browser surfaces: `::selection`, `:focus-visible` outlines.
- After finishing, run `npx -y impeccable detect --json <file>` and fix real findings
  (known false positives: cramped-padding on full-bleed sections; the header radio pulse dot is a
  genuine live indicator; small-caps captions are brand).

## Laguta × Apple principles
1. **Swiss 4-column grid**, gap 32px. Everything aligns to the LEFT edge of the grid. No centred
   narrow article column, no random offsets. Text blocks sit in 1–2 columns, photos span 2.
2. **Extreme contrast of scale**: a huge element next to a tiny one (70px headline / 13px label;
   big Ammar number / small caption).
3. **Type as image**: the headline and numbers carry the page; decoration is minimal.
4. **One idea per section**, light/dark rhythm (cream sections, one ink band for the final CTA).
5. **Hick's law**: one primary CTA per screen (ink button), everything else ghost/border.
6. Motion ≤500ms, `cubic-bezier(.16,1,.3,1)`; hover barely visible.
7. Photos: owner-generated premium still life (cream / ink / muted gold, window light, no people,
   no text). Manhaj filter: no people/animals with faces.
8. Mobile: grid collapses to 1 column, photo first, 20px side padding, full-width buttons.

## Checklist before shipping a page
- [ ] Left edges of label, H1, text, numbers, cards line up on the grid?
- [ ] H1 70 / H2 40 / H3 16 caps, Ammar + Interphases only?
- [ ] One primary CTA per screen?
- [ ] Screenshot at 1440 and 390, no horizontal scroll?
- [ ] `npx impeccable detect` clean except the known false positives above?
- [ ] Facts only from the site (no invented numbers); health copy says "продукт питания, не лекарство".
