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
├── robots.txt        # crawler directives + sitemap pointer
├── sitemap.xml       # XML sitemap with image entries
├── assets/           # logo, photography, favicon (currently empty)
├── docs/
│   ├── SETUP.md      # step-by-step: form, analytics, email, deploy
│   └── CONTENT.md    # copy that needs replacing with real trip details
├── netlify.toml      # Netlify build/deploy config
├── .gitignore
└── README.md
```

---

## SEO

The page is optimised around the primary query **"yoga retreat Rishikesh"** and
related long-tail variants.

What's in place:

- **Title + meta description** tuned for length (53 / 159 chars) and intent
- **Canonical URL**, robots directives, `geo.*` tags for local relevance
- **Open Graph + Twitter Card** tags with a 2000×1333 preview image
- **JSON-LD structured data** — an `@graph` containing `Organization`, `WebSite`,
  `WebPage`, `TouristTrip` (with a 4-stop itinerary), and `FAQPage`
- **Visible FAQ section** (`#faq`) — the 8 questions mirror the `FAQPage` schema
  one-for-one, which Google requires for FAQ rich results
- **Single `<h1>`** with a clean `h1 → h2 → h3` outline
- **`width`/`height` on every image** to prevent layout shift (CLS), plus
  `loading="lazy"` below the fold and `fetchpriority="high"` + preload on the hero
- **`robots.txt` / `sitemap.xml`** with image entries for Google Images
- **www → apex 301** in `netlify.toml` so ranking signals consolidate on one host

> The domain `antaraexperiences.com` is hard-coded in the canonical tag, Open Graph
> URLs, JSON-LD `@id`s, `sitemap.xml`, and `robots.txt`. If the domain changes,
> find-and-replace it across those files.

After deploying, submit the sitemap in
[Google Search Console](https://search.google.com/search-console) and validate the
structured data with the [Rich Results Test](https://search.google.com/test/rich-results).

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
