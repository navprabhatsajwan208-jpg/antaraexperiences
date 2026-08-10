# Setup

Everything below is free tier. Total recurring cost of this stack is the domain
renewal only (~₹1,000–1,500/year).

---

## 1. Waitlist form (required)

The form currently posts to a placeholder and will not deliver anything until this is done.

1. Sign up at https://formspree.io (free plan: 50 submissions/month)
2. Create a new form, name it `Antara Waitlist`
3. Copy the form endpoint — it looks like `https://formspree.io/f/abcdwxyz`
4. In `index.html`, find:
   ```html
   <form class="waitlist" id="waitlistForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with your real ID.
5. Set the notification email to whichever inbox you'll actually check
6. Submit the form once yourself to confirm the email arrives

If you outgrow 50 submissions/month, https://tally.so has a more generous free tier
and can replace Formspree with a small markup change.

---

## 2. Deploy (required)

**Drag and drop**

1. https://app.netlify.com/drop
2. Drag this folder in
3. Live in seconds on a `*.netlify.app` URL

**Git-connected** (do this once you're making regular changes)

1. Create an empty repo on GitHub
2. From this folder:
   ```bash
   git remote add origin git@github.com:YOURNAME/antara-experiences.git
   git branch -M main
   git push -u origin main
   ```
3. Netlify → Add new site → Import an existing project → select the repo
4. Build command: *(leave empty)* · Publish directory: `.`

---

## 3. Custom domain

1. Register `antaraexperiences.com` (GoDaddy India or Namecheap)
2. Netlify → **Domain settings → Add a domain** → enter the domain
3. Netlify shows either nameservers or DNS records. Paste them into your registrar's
   DNS panel.
4. Wait for propagation (minutes to ~24h)
5. SSL is issued automatically once DNS resolves — confirm the padlock appears

---

## 4. Analytics (recommended)

You need this to know whether the demand test actually worked.

- **Google Analytics 4** — https://analytics.google.com — create a property, copy the
  `G-XXXXXXX` measurement ID, paste the gtag snippet just before `</head>` in `index.html`
- **Microsoft Clarity** — https://clarity.microsoft.com — free heatmaps and session
  recordings. Genuinely more useful than GA for a single landing page, because you can
  watch where people stop scrolling.

Run both. They don't conflict.

---

## 5. Branded email (recommended)

Free option: https://www.zoho.com/mail — free plan covers 1 domain and up to 5 users.

Set up `hello@antaraexperiences.com`. Add Zoho's MX records at your registrar. The
footer already links to this address, so it should exist before you drive traffic.

---

## 6. Drive traffic

The site is worthless without visitors. Cheapest sources first:

- Link in the Antara Experiences Instagram bio
- Cross-link from the Anandamaya Retreats and Sattva Journeys audiences
- Reddit: r/yoga, r/IndiaTravel, r/travel — participate genuinely, don't drop links cold
- A small Instagram/Meta ads test (₹500–1,000) targeting yoga interest in the US, UK,
  Germany, and Australia is enough to get a first read on cost per signup

---

## Reading the results

Rough benchmarks for a landing page like this:

| Signup rate | Read |
|---|---|
| under 2% | message or audience is off — revise the copy before spending more |
| 2–5% | normal; keep testing |
| above 5% | real demand — start locking dates and pricing |

Aim for at least 200–300 visitors before drawing any conclusion. Below that, the
numbers are noise.
