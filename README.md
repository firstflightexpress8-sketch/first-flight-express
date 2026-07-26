# First Flight Express — Website

A premium, responsive marketing website for **First Flight Express**, an international courier & cargo company based in Chipledhunga, Pokhara, Nepal.

## ✈️ Pages

| File | Description |
|---|---|
| `index.html` | Home — hero, why-choose-us, services preview, animated stats, testimonials, CTA |
| `about.html` | Company story, mission/vision/values, milestone timeline, team |
| `services.html` | Full service catalog, indicative pricing, FAQ accordion |
| `tracking.html` | Interactive shipment tracking demo (client-side JavaScript) |
| `contact.html` | Contact form, contact details, map placeholder, WhatsApp link |

## 🎨 Brand system

- **Primary:** Royal Blue `#0B3D91` · White `#FFFFFF`
- **Accent:** Premium Gold `#D4AF37`
- **Type:** Poppins (display/headings) + Inter (body), via Google Fonts
- **Signature motif:** a dashed "flight path" line connecting Pokhara to the world, echoed in the hero, stats band, and the tracking page's boarding-pass-style shipment ticket.

## 🗂 Project structure

```
/
├── index.html
├── about.html
├── services.html
├── tracking.html
├── contact.html
├── style.css
├── script.js
├── README.md
└── images/
    ├── logo.svg
    ├── favicon.svg
    ├── hero-bg.svg
    ├── about-story.svg
    └── map-placeholder.svg
```

All images are hand-built SVG placeholders (no external image requests), so the site loads instantly and stays crisp at any resolution. Swap them for real photography/renders any time by keeping the same filenames, or updating the `src`/`background-image` references in the HTML/CSS.

## ⚙️ Features

- Sticky navigation with scroll-triggered background & mobile hamburger menu
- Full-screen hero with layered SVG illustration + gradient scrim
- Animated counters (Intersection Observer, no libraries)
- Scroll-reveal animations throughout
- Glassmorphism nav & badges, soft shadows, rounded cards, gradient CTA banner
- Functional FAQ accordion (services page)
- Demo shipment tracking timeline with sample tracking ID (tracking page)
- Contact form with client-side validation & success state (demo only — see below)
- Floating WhatsApp button + "back to top" button
- Page-load animation (logo loader)
- Fully responsive: mobile-first, tablet and desktop breakpoints
- Semantic HTML5, ARIA labels, visible focus states, `prefers-reduced-motion` support
- SEO: descriptive titles/meta descriptions, Open Graph tags, canonical URLs, `LocalBusiness` JSON-LD schema on the homepage

## 🔌 Connecting the contact form & tracking to real data

Both the contact form (`contact.html`) and tracking form (`tracking.html`) are **front-end demos** — they validate input and show a success/result state, but do not send data anywhere. To make them live:

- **Contact form:** point the `<form id="contactForm">` to a form backend (e.g. Formspree, Netlify Forms, or your own API) and update `script.js`'s `initContactForm()` to `fetch()` that endpoint instead of just toggling `.form-success`.
- **Tracking:** replace the sample data inside `initTracking()` in `script.js` with a call to your real shipment-tracking API, keyed by the tracking number entered.

## 🚀 Deploying to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Upload/commit **all files in this folder** to the repository root (keep the `images/` folder structure intact).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`, choose the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/` within a minute or two.
6. No build step, bundler, or config file is required — this is a static HTML/CSS/JS site.

### Optional: custom domain
Add a `CNAME` file (containing your domain, e.g. `firstflightexpress.com`) to the repo root and configure your DNS provider to point to GitHub Pages, then set the domain under **Settings → Pages → Custom domain**.

## 📝 Editing content

- **Company details** (phone, email, address) appear in the footer of every page and on `contact.html` — search for `061-580022` / `firstflightexpress8@gmail.com` to update everywhere at once.
- **Colors & fonts** are defined once as CSS custom properties at the top of `style.css` (`:root { ... }`) — change them there to restyle the whole site.
- **Navigation links** are duplicated in the `<header>` of each page; keep them in sync if you add/remove pages.

---

Built with clean, dependency-free HTML/CSS/JS — ready to upload directly to GitHub Pages.
