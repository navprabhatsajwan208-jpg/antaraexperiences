# Content to confirm

The copy on the page is written and ready, but several **figures are placeholders**.
Replace them with real numbers before driving traffic — inaccurate specifics are worse
than vague ones, because early signups will hold you to them.

---

## Placeholder figures

All of these live in the `.stat-strip` block in `index.html`.

| Currently says | Needs to be |
|---|---|
| `10` days, door to door | Actual trip length |
| `2` landscapes | Fine as-is |
| `~3,800m` peak altitude | Real summit altitude of the trek you'll run |
| `8–15` guests per batch | Your actual comfortable group cap |

Also check:

- **"Above 3,000 metres"** in the Alap section — should match your real route
- **"a week finding your breath on the ghats"** — adjust if the Rishikesh half isn't 7 days
- **Instagram handle** in the footer — currently `instagram.com/antaraexperiences`
- **Email** in the footer — currently `hello@antaraexperiences.com`

---

## Route decision

The page deliberately doesn't name a specific trek. That's fine for a demand test —
it keeps you flexible. But once you have signups, you'll need to commit. Garhwal
options that pair well with a Rishikesh-based yoga week:

- **Kedarkantha** — ~3,800m, runs in winter, very beginner-friendly
- **Nag Tibba** — ~3,000m, short, good for a lower-commitment version
- **Dayara Bugyal** — ~3,600m, meadows, gentle gradient
- **Kuari Pass** — ~3,650m, bigger views, slightly more demanding

Pick based on the season you want to run the first batch, then update the altitude
figure to match.

---

## Assets still needed

Drop these into `assets/` and wire them into `index.html`:

- **Logo** — the Antara Experiences mark, ideally SVG. Currently the header uses a
  text wordmark with a brass dot.
- **Favicon** — 32×32 PNG or SVG, add `<link rel="icon">` to `<head>`
- **OG image** — 1200×630 JPG for link previews when the URL is shared on WhatsApp,
  Instagram, or Slack. Add `<meta property="og:image">` to `<head>`. This matters more
  than it sounds; most of your early traffic will arrive via a shared link.
- **Photography** — the page currently runs entirely typographic with no photos. That's
  a deliberate choice and it holds up, but 2–3 strong images (a morning practice on the
  ghats, a ridge line, a camp at altitude) would strengthen the trek half considerably.

---

## Pricing

Intentionally absent. Don't add a price until the waitlist tells you demand exists —
naming a number too early anchors you and gives visitors a reason to bounce before
they've read the pitch. Once you have 20–30 signups, email them and ask directly what
they'd expect to pay. That answer is worth more than any competitor research.
