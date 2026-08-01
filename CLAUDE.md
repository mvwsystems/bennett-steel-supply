# CLAUDE.md — Bennett Steel Supply

## Critical Rules

- **Always read `index.html` before making any edits.** Never approximate from memory.
- All CSS lives inline in `index.html` inside the `<style>` block — do not create separate `.css` files unless explicitly asked.
- All JS lives inline in `index.html` inside the `<script>` block — do not create separate `.js` files unless explicitly asked.
- This is a **static site** — no framework, no build step, no npm.
- Never add `clip-path` polygon transitions between sections — use clean 1px rules instead.
- Never add a vertical decorative line inside the hero section.

## Brand Tokens (do not change without instruction)

```
--teal:       #1DA8C7
--teal-mid:   #2BBDD6
--gold:       #F5C842
--gold-dim:   #C9A020
--off-white:  #F4F1EB
--steel-gray: #8A9299
--charcoal:   #1A1C1E
--near-black: #0D0F10
```

## Fonts

- Display/headlines: `'Barlow Condensed'` — weight 800/900, uppercase
- Body: `'Barlow'` — weight 300/400/500
- Mono/labels: `'Space Mono'` — small caps, letter-spacing

## Client

**April Bennett** — Founder & Owner, Bennett Steel Supply  
Malabar, FL · abennett.reelsteel@gmail.com · 321-464-2283  
Woman-Owned (WOSB), Veteran-Owned (SDVOSB), VBE, WBE, SAM.gov registered  
Tagline: *"Your Problem is MY Business — Big or Small, We Take Care of Them All."*  
Faith anchor: Joshua 24:15

## Pending Assets

Images will arrive from client. When they do:
- Logo → place in `/assets/logo/` and replace `.nav-logo` text with `<img>` tag
- Hero photo → add as a low-opacity layer behind `.hero-content`
- Product shots → add inside `.prod-card` elements above the icon

## Form Backend

Netlify Forms is active. Two forms are wired up:
- `quote-request` — homepage quote form (`index.html`), plain HTML POST
- `spec-request` — spec sheet modal (`products/specifications.html`), AJAX POST via `handleSubmit()`

Both use `netlify-honeypot="bot-field"` with a matching hidden `bot-field` input for spam filtering.

Each `<form>` needs `method="POST"`, the `netlify` attribute, and a hidden
`<input type="hidden" name="form-name" value="...">` matching its `name`.
Omitting `method="POST"` silently breaks capture — the browser falls back to
GET and Netlify records nothing.

Submissions land in the Netlify dashboard and notify **abennett.reelsteel@gmail.com**
(set under Project configuration → Forms → Form submission notifications, not in the markup).

## Mobile Breakpoints

Not yet implemented. Priority order when building:
1. 768px — tablet: collapse nav links to hamburger, stack 2-col grids to 1-col
2. 480px — mobile: reduce hero font sizes, full-width buttons, single-col form

## Sections (in order)

1. `<nav>` — fixed top bar
2. `.hero` — full viewport
3. `.ticker-wrap` — infinite scroll trust bar
4. `.diff-section` — 6-card differentiators
5. `.products-section` — 4-col product cards
6. `.about-section` — 2-col stats + story
7. `.cta-section` — centered call to action
8. `.form-section` — 14-field quote form
9. `<footer>` — brand + certs + copy
