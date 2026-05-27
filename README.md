# Bennett Steel Supply — Website

**Live site:** https://bennett-steel.netlify.app (update after deploy)
**Client:** April Bennett — Founder & Owner
**Built by:** 6 Signal (6signal.co)

---

## Project Overview

Static marketing website for Bennett Steel Supply — a woman-owned, veteran-owned steel sheet piling distributor based in Malabar, FL. The site is a single-page layout with smooth scroll navigation, a quote request form, and section animations.

---

## Tech Stack

- Pure HTML / CSS / Vanilla JS — no framework, no build step
- Google Fonts: Barlow Condensed (display), Barlow (body), Space Mono (mono/labels)
- Deployed via Netlify (drag-and-drop or GitHub CI)

---

## File Structure

```
bennett-steel/
├── index.html          # Full single-page site
├── netlify.toml        # Netlify config, headers, redirects
├── .gitignore
├── README.md
└── assets/             # Add client images/logos here
    ├── logo/
    │   └── bennett-steel-logo.png   (pending from client)
    ├── images/
    │   └── (job site photos, product shots — pending)
    └── certs/
        └── (certification badge PNGs — pending)
```

---

## Brand

| Token | Value |
|-------|-------|
| Primary teal | `#1DA8C7` |
| Gold accent | `#F5C842` |
| Off-white | `#F4F1EB` |
| Steel gray | `#8A9299` |
| Charcoal | `#1A1C1E` |
| Near black | `#0D0F10` |

---

## Certifications

- WOSB (Women-Owned Small Business)
- SDVOSB (Service-Disabled Veteran-Owned Small Business)
- VBE (Veteran Business Enterprise)
- WBE (Women Business Enterprise)
- SAM.gov Registered

---

## Sections

1. **Nav** — Fixed, frosted glass, centered links, teal CTA button
2. **Hero** — Full-viewport, grid texture, headline + sub + CTA buttons + cert pills
3. **Ticker Tape** — Infinite scroll trust bar
4. **Differentiators** — 6-card grid (01–06)
5. **Products** — 4-column: AZ/PZC, ZZ, H-Pile, Accessories
6. **About** — Stats + April's founding story + Joshua 24:15
7. **CTA** — Grid-texture call-to-action block
8. **Quote Form** — 14-field inquiry form
9. **Footer** — Brand + certs + copyright

---

## Quote Form Fields

Per client spec (from Typeform intake):
- Full name, Company name, Phone, Email
- Project type (dropdown), Rental or Purchase (dropdown)
- Est. footage or tonnage, Project location/state
- Material needed onsite by (date), Bidding or Awarded (dropdown)
- Domestic/Foreign steel preference, Set-aside requirement
- Additional details/specs (textarea)
- How did you hear about us

**Form currently has no backend.** Next step: connect to Netlify Forms (add `netlify` attribute to `<form>` tag) or wire to a service like Formspree / EmailJS.

---

## Pending Assets from Client

April confirmed sending within 24 hours:
- [ ] Bennett Steel Supply logo (high-res PNG/SVG)
- [ ] Job site photography
- [ ] Product shots (piling, equipment)
- [ ] Team photos
- [ ] Certification badge graphics
- [ ] Association logos

Once received, place in `/assets/` and update `index.html` to reference them.

---

## Deploy to Netlify

### Option A — Drag and Drop
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `bennett-steel/` folder onto the deploy zone

### Option B — GitHub CI (recommended)
1. `git init` in this folder
2. Create a new GitHub repo: `bennett-steel-supply`
3. Push: `git add . && git commit -m "initial" && git push`
4. In Netlify: New site → Import from GitHub → select repo → deploy

---

## To-Do / Claude Code Tasks

- [ ] Add real logo to nav (replace text logo)
- [ ] Add hero background image or photography layer
- [ ] Connect quote form to Netlify Forms or backend
- [ ] Add testimonials section (client to provide quotes)
- [ ] Add project gallery / past work section
- [ ] Mobile responsive pass (breakpoints at 768px and 480px)
- [ ] Add Open Graph / meta tags for SEO
- [ ] Add favicon
- [ ] Verify domain: reelsteel.com (client confirmed they have it)
