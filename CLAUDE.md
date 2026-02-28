# CLAUDE.md — Foundation Circuit

## Project Overview

**Foundation Circuit** is a single-file Progressive Web App (PWA) implementing a personal development self-assessment workbook titled *"Think Small, Start Horribly."* It helps users assess their capability and capacity before taking action, using an interactive diagnostic framework developed by Alex Cooper.

The entire application lives in one HTML file with embedded CSS and JavaScript — no build step, no external dependencies beyond Google Fonts, no framework.

---

## Repository Structure

```
foundation-circuit/
├── CLAUDE.md                              # This file
├── README.md                              # Minimal placeholder
├── manifest.json                          # PWA manifest (app name, icons, colors)
├── sw.js                                  # Service worker (cache-first offline strategy)
└── foundation-circuit-workbook-v10.html  # The entire application (~2100 lines)
```

### File Roles

| File | Purpose |
|------|---------|
| `foundation-circuit-workbook-v10.html` | Complete app: markup, CSS, and JS in a single file |
| `manifest.json` | PWA configuration — display mode, theme colors, icon |
| `sw.js` | Caches the HTML and manifest for offline use |
| `README.md` | Minimal project name placeholder |

---

## Tech Stack

- **Language:** Vanilla HTML, CSS, JavaScript (ES6+) — no frameworks or libraries
- **Fonts:** Google Fonts — Barlow (300/400/600/700/800) and Barlow Condensed
- **Storage:** `localStorage` API for persisting user state (evidence log, commitments)
- **PWA:** Service Worker with cache-first strategy; `manifest.json` for installability
- **Browser APIs:** DOM API, localStorage, Service Worker API, SVG

---

## Architecture: Single-File Application

The entire app is `foundation-circuit-workbook-v10.html`. It is structured in three embedded sections:

### 1. `<style>` block — CSS

- Uses CSS custom properties (variables) for the color system:
  - `--teal: #5ec5cc` — primary accent
  - `--teal-dark: #3aabb3` — darker teal
  - `--red: #e05555` — warnings/low capacity
  - `--yellow: #f5c842` — caution/mid states
  - `--charcoal: #1e1e1e` — primary text
  - `--off: #f7f7f5` — background
- Max-width layout container at `700px`, mobile-first
- BEM-like naming: `.step-title`, `.step-num`, `.state-list`, `.teal-left`, `.red-left`, `.yellow-left`

### 2. `<body>` — HTML Content

Seven sequential content steps (plus cover and closing):
1. Have You Ever Felt Like This?
2. This Is Not A Motivation Problem
3. Capability vs. Capacity
4. Version 1 and Version 2
5. The Forecasting Error
6. The Two Phase Planning Model
7. Where Are You Right Now? *(the interactive assessment)*

### 3. `<script>` block — JavaScript

Vanilla JS, no modules. Key patterns:

**Naming conventions:**
- `camelCase` for functions and variables: `buildSliders()`, `runAudit()`, `makeCommitment()`
- `UPPER_SNAKE_CASE` for constant data arrays: `CAP_QS`, `CPC_QS`, `V1_OPTS`, `V2_OPTS`
- `kebab-case` for HTML element IDs: `cap-sliders`, `cpc-sliders`, `energy-tags`, `commit-input`

**Key functions:**
- `buildSliders(containerId, questions)` — renders 1-10 slider inputs
- `buildTags(containerId, options)` — renders multi-select tag buttons
- `buildChecks(containerId, options)` — renders checkbox lists
- `runAudit()` — calculates capability %, capacity %, generates diagnosis
- `makeCommitment()` — saves commitment to localStorage, renders evidence log

**Assessment scoring:**
- Capability % = `(sum of 3 slider values / 30) × 100`
- Capacity % = `(sum of 3 slider values / 30) × 100`
- Thresholds: Green ≥ 70%, Amber 40–69%, Red < 40%
- Diagnosis text is generated dynamically based on the capability/capacity combination

---

## Development Workflow

### Running the App

No build step required. Open directly in a browser:

```bash
# Option 1: open directly
open foundation-circuit-workbook-v10.html

# Option 2: serve locally (recommended for PWA/Service Worker testing)
python3 -m http.server 8080
# then visit http://localhost:8080/foundation-circuit-workbook-v10.html
```

> **Note:** Service Workers require a secure context (HTTPS or localhost). Use a local server for full PWA functionality.

### Making Changes

All code changes go into `foundation-circuit-workbook-v10.html`. There is no compilation or transpilation — edits are immediately visible on browser refresh.

1. Edit the HTML file
2. Reload the browser (hard reload: `Ctrl+Shift+R` / `Cmd+Shift+R` to bypass SW cache)
3. Test all assessment flows end-to-end

### No Tests

There is no automated test suite. Testing is manual:
- Verify slider interactions update scores
- Verify `runAudit()` produces correct % and diagnosis text
- Verify localStorage persistence across page reloads
- Verify offline functionality via DevTools → Application → Service Workers

---

## Service Worker & Caching

`sw.js` uses a **cache-first** strategy with cache name `foundation-circuit-v1`.

Files cached on install:
- `foundation-circuit-workbook-v10.html`
- `manifest.json`

**When updating the app**, if caching behavior needs to change, update the `CACHE_NAME` constant in `sw.js` (e.g., `foundation-circuit-v2`) to invalidate the old cache.

---

## PWA Configuration (`manifest.json`)

| Property | Value |
|----------|-------|
| `name` | Foundation Circuit |
| `short_name` | Foundation |
| `background_color` | `#1a1a1a` |
| `theme_color` | `#3aabb3` |
| `display` | `standalone` |
| `start_url` | `foundation-circuit-workbook-v10.html` |
| `scope` | `/` |

The icon is an inline SVG data URI of a circuit diagram aesthetic embedded directly in `manifest.json`.

---

## Conventions for AI Assistants

- **Do not introduce build tools, frameworks, or package managers** unless explicitly requested. This project's simplicity is intentional.
- **All changes go in the single HTML file.** Do not split into separate CSS/JS files without explicit instruction.
- **Preserve the vanilla JS approach** — no jQuery, React, Vue, or other libraries.
- **Follow existing naming conventions:** `camelCase` functions, `UPPER_SNAKE_CASE` constants, `kebab-case` IDs.
- **CSS changes** should use the existing custom property color variables rather than hardcoded hex values.
- **localStorage keys** should be namespaced (check existing keys in the script before adding new ones).
- **Test manually** — there are no automated tests; describe what to manually verify after any change.
- **Update `sw.js` cache version** if assets are renamed or added to ensure the service worker serves updated content.
- **Do not create a `package.json`** or any Node.js infrastructure unless the user explicitly requests it.

---

## Git Workflow

- Remote: `http://local_proxy@127.0.0.1:41000/git/thinksmallstarthorribly/foundation-circuit`
- Default branch: `master`
- Feature branches follow the pattern: `claude/<description>-<session-id>`

```bash
# Push to a feature branch
git push -u origin claude/<branch-name>
```

---

## Key Context

- The workbook is version 10 (`v10`), suggesting prior iterations exist outside this repo.
- The framework author is **Alex Cooper**, referenced within the HTML content.
- The app is designed for personal, reflective use — not a multi-user or backend system.
- Content is educational and motivational; changes to copy should preserve tone (direct, grounded, non-corporate).
