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
Malabar, FL · hello@reelsteel.com  
Woman-Owned (WOSB), Veteran-Owned (SDVOSB), VBE, WBE, SAM.gov registered  
Tagline: *"Your Problem is MY Business — Big or Small, We Take Care of Them All."*  
Faith anchor: Joshua 24:15

## Pending Assets

Images will arrive from client. When they do:
- Logo → place in `/assets/logo/` and replace `.nav-logo` text with `<img>` tag
- Hero photo → add as a low-opacity layer behind `.hero-content`
- Product shots → add inside `.prod-card` elements above the icon

## Form Backend

The quote form has no backend yet. To activate Netlify Forms:
1. Add `name="quote-request" netlify` attributes to the `<form>` tag
2. Add a hidden `<input type="hidden" name="form-name" value="quote-request">`
3. Netlify will auto-detect and route submissions to the dashboard

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
