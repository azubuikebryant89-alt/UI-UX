# Marketplace Screenshot Guide

## Why this file exists instead of finished screenshots

The build environment used for this project has no real browser (Chrome/Firefox/Safari)
and no network access to download one — Playwright MCP was requested in the brief but is
not available in this environment, and the only local rendering engine (`wkhtmltoimage`)
is built on a frozen ~2013-era WebKit fork that predates CSS Grid, the Popover API, and
the `<dialog>` element. Screenshots taken with it (kept in `/qa/renders/` for structural
QA only — not included here) show single-column layouts where the real product renders
proper 3–4 column grids, and show dropdown menus stuck open where real browsers keep them
correctly hidden. Using those renders as marketplace screenshots would misrepresent the
product, so they were deliberately excluded from this folder.

Every page has been verified for correctness by other means: HTML5 validation (zero real
errors — see `/qa/final-audit.md`), a full internal/asset link audit, JS syntax
verification, and manual source review of the CSS Grid/Popover/dialog implementations
against MDN's current specification and compatibility data (see
`/research/mdn-decisions.md`). The layouts are correct; they simply couldn't be
photographed correctly in this sandbox.

## What's already in this folder

- `icon-200x200.png` — marketplace icon (original graphic, not a page render)
- `preview-800x400.png` — marketplace preview card (original graphic, not a page render)

## What to capture before submitting (5–10 minutes in any real browser)

Open each URL below in Chrome or Firefox at the given width, and save a screenshot
(browser DevTools device toolbar → "Capture screenshot," or any screenshot extension).
Codester requires 3–9 images; this list gives you 6 good candidates.

| # | Page | Width | Notes |
|---|---|---|---|
| 1 | `index.html` | 1440px | Hero + workflow section |
| 2 | `dashboard.html` | 1440px | Scroll so all 4 stat cards are visible in one row |
| 3 | `clients.html` | 1440px | Table view with the status chips visible |
| 4 | `tasks.html` | 1440px | The 4-column board — this is the strongest differentiator shot |
| 5 | `pricing.html` | 1440px | Three-tier pricing grid |
| 6 | `dashboard.html` | 390px | Mobile view, sidebar collapsed |

Crop each to roughly 1280×800 (desktop) or the natural mobile viewport, matching the
16:10-ish aspect ratio Codester's examples use — no browser chrome, no address bar.
