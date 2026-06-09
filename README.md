# Stand8 — Salesforce Leak Finder

An interactive, self-contained assessment tool that helps prospects discover
where their Salesforce org is leaking value, then routes them to schedule a
Salesforce Health Check with Stand8.

## What it is

`index.html` is a single, dependency-free page:

- All styles, scripts, fonts (Roobert / Hanken Grotesk), and the Stand8 logo
  are inlined — no build step and no external runtime dependencies.
- The flow walks the user through a series of questions, scores the answers,
  presents results, and offers two CTAs: **Schedule a Health Check** and
  **Send me my results**.
- It is currently a front-end prototype: the lead-capture actions are
  client-side only and not yet wired to a backend.

## Running locally

Because everything is inlined, you can just open the file:

```bash
open index.html        # macOS
xdg-open index.html    # Linux
```

Or serve it (useful for testing share/redirect behavior):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Project structure

```
.
├── index.html   # the entire app (markup + CSS + JS + embedded assets)
└── README.md
```

## Next steps / ideas

- Wire the "Send me my results" and "Request my Health Check" actions to a
  real backend (e.g. an email service or Salesforce lead endpoint).
- Add basic analytics on the funnel (start → complete → CTA click).
- Split the inlined CSS/JS into separate files if the app grows, or move to a
  small build setup.
