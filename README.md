# Antara Experiences

Landing page for **Antara Experiences** — a yoga and Himalayan trek immersion based in
Rishikesh, Uttarakhand.

The site is a single self-contained HTML file. No build step, no dependencies, no
package manager. Open `index.html` in a browser and it works.

---

## Purpose

This is a **demand-validation landing page**, not a full booking site. Its one job is
to convert visitors into waitlist signups so we can measure interest before committing
to fixed dates, pricing, or inventory.

Success metric: waitlist signups per 100 visitors.

---

## Project structure

```
antara-experiences/
├── index.html        # the entire site — HTML, CSS, and JS in one file
├── assets/           # logo, photography, favicon (currently empty)
├── docs/
│   ├── SETUP.md      # step-by-step: form, analytics, email, deploy
│   └── CONTENT.md    # copy that needs replacing with real trip details
├── netlify.toml      # Netlify build/deploy config
├── .gitignore
└── README.md
```

---

## Running locally

Just open the file:

```bash
open index.html          # macOS
start index.html         # Windows
```

Or serve it over HTTP if you want to test the form properly:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Before going live

Two things are placeholders and must be replaced. Both are covered in `docs/SETUP.md`.

1. **Waitlist form** — `index.html` posts to `https://formspree.io/f/YOUR_FORM_ID`.
   Replace `YOUR_FORM_ID` with a real Formspree form ID or the form silently does nothing.
2. **Trip details** — day count, peak altitude, and batch size are placeholder figures.
   See `docs/CONTENT.md` for the full list of what to confirm.

---

## Deploying

Fastest path (drag and drop):

1. Go to https://app.netlify.com/drop
2. Drag this folder onto the page
3. Site is live on a temporary `*.netlify.app` address

Via git (recommended once you're iterating):

1. Push this repo to GitHub
2. In Netlify: **Add new site → Import an existing project** → pick the repo
3. Leave build command empty, publish directory `.`
4. Every `git push` now redeploys automatically

Then connect the custom domain under **Domain settings → Add a domain**. SSL is issued
free and automatically once DNS resolves.

---

## Design notes

The page structure follows the movements of a Hindustani classical composition —
*sthayi, alap, antara, vistar, tihai* — which is where the brand name comes from.
The *antara* is the rising second phrase of a raga, and it's the section that gives the
whole piece its identity. The section labels on the page are functional, not decorative:
each names what that part of the page is actually doing.

The hero line reads as both a mountain elevation profile and a melodic contour.

**Palette**

| Token | Hex | Use |
|---|---|---|
| `--ink` | `#15202B` | primary text, dark buttons |
| `--paper` | `#E8E2D2` | light section background |
| `--night-deep` | `#0A0F17` | dark section background |
| `--brass` | `#BD8A3B` | accent, contour line, CTA |
| `--mist` | `#C9D5D8` | body text on dark |

**Type** — Fraunces (display), Work Sans (body), JetBrains Mono (labels and figures).

---

## License

Private. All rights reserved.
