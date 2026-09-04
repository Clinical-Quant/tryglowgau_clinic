# tryglowgau.com — Static Site

This is the static demo clinic website for **tryglowgau.com**.

## What's here

| File | Purpose |
|------|---------|
| `index.html` | Home page |
| `treatments.html` | Treatments overview / index |
| `injectables.html` | Injectables service page |
| `skin-rejuvenation.html` | Skin Rejuvenation service page |
| `laser-devices.html` | Laser & Devices service page |
| `about.html` | About the clinic + team |
| `contact.html` | Contact form + Glowgau widget placeholder |
| `disclaimer.html` | Demo disclaimer page |
| `styles.css` | Design system stylesheet |
| `assets/` | Processed images (hero, cards, portraits) |

## Deployment

Deployed to **Cloudflare Workers + Pages** from this repo:

- Cloudflare watches `main` branch
- Pushes auto-deploy
- Custom domain: `tryglowgau.com`
- DNS at **Namecheap**

## How to update content

1. Edit HTML files directly (this is a flat static site, no build step)
2. Drop new images into `assets/`
3. Commit + push to `main`
4. Cloudflare Pages deploys within ~30 seconds

## Where the Glowgau widget goes

The Glowgau widget placeholder lives in `contact.html` at the `#glowgau-widget-mount` element. When the COO/CTO provides the snippet, replace the placeholder block with:

```html
<!-- BEGIN GLOWGAU WIDGET -->
<script src="..." async></script>
<!-- END GLOWGAU WIDGET -->
```

**Never invent widget IDs or tokens.** Always source from the COO/CTO profile.

## Demo vs. production

This **is** the production URL (`tryglowgau.com`). Because the apex domain itself doesn't signal "demo", we make the demo nature explicit in:

- Header (`Demo Clinic` tag next to the logo)
- Footer (persistent disclaimer banner)
- Footer (link to the dedicated `disclaimer.html` page)

The dedicated `disclaimer.html` page explains in plain language that this is not a real medical practice.
