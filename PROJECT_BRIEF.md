# Think Small, Start Horribly — Full Project Brief
> For use with AI agents. This document contains everything needed to understand, work on, and extend the project.

---

## 1. Project Overview

**Brand:** Think Small, Start Horribly  
**Creator:** Alex Cooper  
**Product:** Life Circuitry — a 7-module interactive self-development programme  
**Price:** $297 (one-time, lifetime access)  
**Target audience:** Highly capable adults who keep getting stuck despite repeated effort — people who understand the problem intellectually but can't break the cycle  
**Core mechanism:** Reactive Adaptation — the pattern where capable people rebuild after collapse without fixing the underlying circuit, causing the same drop to repeat  

---

## 2. Live URLs

| Page | Live URL |
|------|----------|
| Sales page (v1 — original) | https://thinksmallstarthorribly.github.io/foundation-circuit/ |
| Sales page (v2 — influence-engineered, $297) | https://thinksmallstarthorribly.github.io/foundation-circuit/v2/ |
| Access gate | https://thinksmallstarthorribly.github.io/foundation-circuit/access.html |
| Student portal / dashboard | https://thinksmallstarthorribly.github.io/foundation-circuit/portal.html |
| Document library | https://thinksmallstarthorribly.github.io/foundation-circuit/library.html |
| Module 1 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-1.html |
| Module 2 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-2.html |
| Module 3 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-3.html |
| Module 4 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-4.html |
| Module 5 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-5.html |
| Module 6 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-6.html |
| Module 7 | https://thinksmallstarthorribly.github.io/foundation-circuit/module-7.html |
| Admin panel | https://thinksmallstarthorribly.github.io/foundation-circuit/admin.html |
| Ecosystem roadmap | https://thinksmallstarthorribly.github.io/foundation-circuit/roadmap.html |
| System overview (infographic) | https://thinksmallstarthorribly.github.io/foundation-circuit/overview.html |
| Original workbook (HTML) | https://thinksmallstarthorribly.github.io/foundation-circuit/foundation-circuit-workbook-v10.html |

**Pending custom domains (DNS in progress):**
- lifecircuitry.com → will point to v2 sales page
- lifecircuitry.com.au → redirect to lifecircuitry.com
- thinksmallstarthorribly.com → brand hub / creator site
- thinksmallstarthorribly.com.au → redirect to .com

---

## 3. GitHub Repository

**Repo:** https://github.com/thinksmallstarthorribly/foundation-circuit  
**GitHub Pages branch:** main (root)  
**Dev branch:** genspark_ai_developer  
**Hosting:** GitHub Pages (free, HTTPS enforced)  

### Key files in repo root

| File | Purpose |
|------|---------|
| `index.html` | v1 sales page (original, $97 price, keep untouched) |
| `v2/index.html` | v2 sales page (influence-engineered, $297) |
| `access.html` | Code-gated access page — students enter their access code here |
| `portal.html` | Student dashboard after login |
| `library.html` | Source PDFs and reference documents |
| `module-1.html` through `module-7.html` | The 7 interactive programme modules |
| `admin.html` | Admin code manager — add/revoke access codes |
| `roadmap.html` | Full ecosystem roadmap (internal/sales use) |
| `overview.html` | Single-page infographic overview of the system |
| `foundation-circuit-workbook-v10.html` | Original workbook in HTML format |
| `manifest.json` | PWA manifest — app can be installed on home screen |
| `sw.js` | Service worker — offline support |
| `CNAME` | Custom domain file (currently: lifecircuitry.com) |
| `assets/alex-photo.jpg` | Alex Cooper headshot (used on portal/modules) |
| `v2/alex-photo.jpg` | Alex Cooper headshot (used on v2 sales page) |

---

## 4. Programme Structure

### The 7 Modules

| # | Title | Type | Description |
|---|-------|------|-------------|
| 1 | The Momentum Formula | Foundation | How momentum is built and why it collapses — introduces the Reactive Adaptation cycle |
| 2 | The Stuck Framework | Diagnostic | Maps the specific pattern keeping the student stuck |
| 3 | The Conceptual Landscape | Diagnostic | Identifies the mental models and assumptions driving behaviour |
| 4 | Foundation Circuit | Core System | The central framework — rewiring the underlying circuit |
| 5 | Version of Self | Identity | Identity work — who you are versus who you're performing as |
| 6 | The Marketplace | Positioning | How your value is perceived and communicated externally |
| 7 | Re-Entering the Early Learning Phase | Integration | Sustainable re-entry — staying functional through uncertainty |

- Each module: 45-90 minutes of interactive work
- Total programme time: 6-8 hours
- Format: interactive web portal (not video), with diagnostics and reflection tools
- PDF export available
- No account required — access via code, data stored locally in browser
- Works as a Progressive Web App (installable on any device)

---

## 5. Sales Page v2 — Influence Framework

The v2 sales page (`/v2/index.html`) was built using Chase Hughes' persuasion architecture. The following techniques are embedded:

| Technique | Where used |
|-----------|-----------|
| **Identity Installation** | Hero section, module descriptions, closing CTA — describes "a type of person" without directly addressing the reader |
| **Negative Dissociation** | "Two Types of Stuck" section — separates "most people" from "a certain kind of person" |
| **Deviance Escalation (D1-D3)** | Opening line (D1 — slightly honest), "Two Types of Stuck" (D2 — shared social criticism), About Alex (D3 — personal truth admission) |
| **Emotional Ignition Trigger** | Reactive Adaptation cycle diagram — creates physical recognition and relief |
| **Scarcity Whispers** | Testimonials intro (unprompted messages), pricing note (early-access language, future price hint) |
| **Embedded Commands** | Closing CTA — "a person like this feels something settle" |
| **Permission Bridge** | How It Works section — lowers resistance before the ask |

### v2 Hero tagline
```
HIGHLY CAPABLE.
STUCK AGAIN.
READY TO GIVE UP.
```

### v2 Pricing
$297 — one-time. Lifetime access. 7 interactive modules. No videos. No fluff.

---

## 6. About Alex Cooper

- Creator and author of the programme
- Personal story: repeated cycles of collapse and rebuild, eventually diagnosed the pattern structurally
- Background: no formal credentials — the programme is built from lived experience and applied frameworks
- Tone: direct, no-fluff, treats the audience as intelligent adults
- Contact: hello@thinksmallstarthorribly.com
- Personal guarantee: if the first 3 modules deliver no genuine value, Alex refunds personally — no forms

---

## 7. Testimonials

### Jase
> "I'd been going for a $80k IT role and failed 3 interviews. After working through the modules I landed the job. The tools are practical, not motivational."

### Kathryn
> "I finally understood why I kept stopping. Not a discipline problem. A structure problem. I stopped waiting for motivation and started working."

---

## 8. Guarantee

30-day unconditional guarantee.  
Complete the first 3 modules. If you get no genuine value, email Alex for a full refund.  
No forms. No questions. Personal refund from Alex.

---

## 9. Payment & Access Flow (Current — Manual)

1. Student clicks "Get the Programme" → purchase modal opens
2. Modal shows PayPal link and bank transfer details (BSB + account number)
3. Student pays $297
4. Alex manually emails access code within a few hours
5. Student visits access.html, enters code
6. Redirected to portal.html (dashboard)
7. Accesses modules from the portal

**Planned automation:** Stripe or Gumroad integration to automate payment → code delivery

---

## 10. Tech Stack

| Layer | Technology |
|-------|-----------|
| Hosting | GitHub Pages (free) |
| Frontend | Vanilla HTML, CSS, JavaScript — no frameworks |
| Fonts | Google Fonts — Barlow and Barlow Condensed |
| PDF export | Browser print / CSS @media print |
| Offline support | Service Worker (sw.js) |
| Installable | PWA via manifest.json |
| Data storage | localStorage (no server, no database) |
| Access control | JavaScript-based code gate (admin.html manages codes) |
| Analytics | None currently |
| Payment | Manual (PayPal / bank transfer) |

---

## 11. Design System

### Colour palette (CSS variables)

```css
--teal:    #00B4D8;
--yellow:  #FFD60A;
--red:     #FF4757;
--green:   #2ED573;
--purple:  #7B5EA7;
--orange:  #FF6B35;
--charcoal:#1A1A2E;
--dark:    #111111;
--light:   #F8F9FA;
--muted:   #6C757D;
```

### Typography
- Headlines: Barlow Condensed (bold, uppercase, condensed)
- Body: Barlow (regular/medium)

### Visual style
- Dark background (#111111 base)
- High contrast — white text on dark
- No emojis anywhere in copy
- No hyphens or dashes in visible copy
- Minimal, direct — no decorative elements

---

## 12. Ecosystem Gaps (Priority order)

| Gap | Status | Impact |
|-----|--------|--------|
| Payment automation | Not built | HIGH — every sale is manual right now |
| Traffic / marketing | Not built | HIGH — no consistent lead source |
| Custom domain | DNS in progress | MEDIUM — unprofessional URL affects trust |
| Analytics | Not built | MEDIUM — no conversion data |
| Email automation | Not built | LOW-MED — onboarding is manual |

---

## 13. Raw GitHub File URLs (for direct access)

All files are accessible at:  
`https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/[filename]`

### Key raw file links

| File | Raw URL |
|------|---------|
| v1 Sales page | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/index.html |
| v2 Sales page | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/v2/index.html |
| Portal | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/portal.html |
| Access gate | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/access.html |
| Admin | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/admin.html |
| Library | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/library.html |
| Module 1 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-1.html |
| Module 2 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-2.html |
| Module 3 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-3.html |
| Module 4 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-4.html |
| Module 5 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-5.html |
| Module 6 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-6.html |
| Module 7 | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/module-7.html |
| Roadmap | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/roadmap.html |
| Overview | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/overview.html |
| Alex photo (v2) | https://raw.githubusercontent.com/thinksmallstarthorribly/foundation-circuit/main/v2/alex-photo.jpg |

---

## 14. Suggested Next Tasks for an AI Agent

The following are known outstanding tasks, in priority order:

1. **Replace Alex photo** — the current photo on the v2 sales page (`v2/alex-photo.jpg`) needs to be updated to the correct headshot
2. **Fix www CNAME for lifecircuitry.com** — DNS record in VentraIP needs `www` CNAME pointing to `thinksmallstarthorribly.github.io`; currently failing with hostname format error
3. **Set up DNS for remaining 3 domains** — lifecircuitry.com.au, thinksmallstarthorribly.com, thinksmallstarthorribly.com.au (same A records + CNAME pattern)
4. **Build a marketing/landing page** for thinksmallstarthorribly.com (brand hub — separate from the product sales page)
5. **Stripe/Gumroad payment integration** — automate the purchase-to-access-code flow
6. **Add analytics** — Google Analytics or Plausible on v2 sales page for conversion tracking
7. **Email automation** — Automated welcome email with access code on purchase
8. **Mobile QA** — Full review of v2 on iPhone/Android, especially the two-column dissociation grid

---

## 15. Copy Rules (Important — apply to all future work)

- **No hyphens or dashes** in visible copy anywhere
- **No emojis** anywhere
- **No hedging language** — direct, confident tone only
- **Speak to the structural problem**, not the symptom
- **Treat the audience as intelligent** — no hand-holding, no over-explaining
- **Tagline is fixed:** HIGHLY CAPABLE. / STUCK AGAIN. / READY TO GIVE UP.
- **Price is fixed:** $297 (do not change without instruction)
- **Brand voice:** Alex Cooper — direct, honest, occasionally self-deprecating, no corporate language

---

*Last updated: March 2026*  
*Maintained by: Genspark AI agent*
