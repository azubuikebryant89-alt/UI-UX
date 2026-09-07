# Product Freeze

Locked before implementation. Any change beyond this scope during the build was treated
as a deviation requiring justification (see "Deviations from freeze" at the bottom).

**A. Product name:** Portside (working title — flagged as needing a trademark/collision
check before real commercial launch; not verified in this pass).

**B. Product positioning:** A client-operations template pairing a marketing site with a
working application UI, for developers building agency/freelancer tools.

**C. Target audience:** Developers reselling/customizing for agencies, freelancers, and
small consultancies on Codester, Envato, and TemplateMonster.

**D. Core workflow:** Lead/Client → Proposal → Approval → Project → Tasks → Files →
Invoice → Delivery/Completion.

**E. Page architecture (17 pages, locked):**
Marketing/auth (6): index, features, pricing, login, register, 404.
Application (10): dashboard, clients, client-details, projects, project-details, tasks,
proposals, invoices, files, settings.
Documentation (1): documentation/index.html.
*(Calendar, Messages, and a real dark-mode toggle were explicitly deferred to a future
v1.1 per `product-strategy.md`, to avoid uncontrolled feature creep.)*

**F. Component architecture:** one shared stylesheet (`assets/css/styles.css`) and one
shared script (`assets/js/app.js`) across all pages; no per-page CSS/JS files, no
templating engine — each HTML file is a complete, self-contained document assembled from
shared partials at build time by an internal (non-shipped) Python script.

**G. Design system:** navy/"harbor teal" palette on CSS custom properties; system-font
typography; 4px-based spacing scale; 3-step border-radius scale; documented in full in
`documentation/index.html#design-system`.

**H. Interaction model:** native `<dialog>` for modals, native Popover API (with JS-
computed positioning, since CSS Anchor Positioning isn't cross-browser yet) for dropdown
menus, custom ARIA-pattern tabs/accordions, vanilla-JS table sort/filter, HTML5
drag-and-drop for the task board with a keyboard-operable "move to" fallback.

**I. Content model:** one fictional demo tenant ("Northline Studio") with 8 fictional
clients, 8 projects, 6 invoices, 5 proposals, 13 tasks across 4 board columns, and a
4-person fictional team — sized to make every page feel populated and realistic without
being arbitrary or padded.

**J. Technical architecture:** semantic HTML5, modern CSS, vanilla JavaScript, no build
step for the shipped product, no backend, no database, no real authentication, no real
payment processing, no external API dependency for the core demo — per the workflow's
default architecture, with no evidence surfaced in Phase 1 research compelling a framework.

## Deviations from freeze during build
None. The 16 content pages plus documentation page were built exactly as scoped above; no
additional pages or major features were added mid-build.
