# tryglowgau.com — Static Site (Aurum Aesthetics Demo)

Demo aesthetic clinic website for **tryglowgau.com**, built to demonstrate **Glowgau's AI clinic assistant**.

This is a fictional clinic, clearly labelled as a demo, used by Glowgau to show prospective clinics what a Glowgau-powered website looks like in practice.

## What's here

| Path | Purpose |
|---|---|
| `index.html` | Home — hero, 6 treatment regions, team, locations, Glowgau widget |
| `treatments/index.html` | Treatments index (6 regions) |
| `treatments/forehead-eyes.html` | Forehead & Eyes service detail (Botox, Dysport, Xeomin) |
| `treatments/cheeks-jawline.html` | Cheeks & Jawline service detail (fillers, Kybella, masseter) |
| `treatments/lips.html` | Lips service detail (fillers, hydration, smoker's lines) |
| `treatments/skin.html` | Skin Rejuvenation (HydraFacial, Halo, MOXI, BBL, microneedling, Morpheus8) |
| `treatments/body.html` | Body & Waist (CoolSculpting, Emsculpt NEO, Emtone) |
| `treatments/men.html` | Men's Services |
| `about.html` | About the clinic + 4-person fictional team |
| `shop.html` | In-clinic retail line (6 fictional products) |
| `contact.html` | Contact form + Glowgau widget + 3 Chicago locations |
| `disclaimer.html` | Full demo disclaimer |
| `styles.css` | Design system stylesheet (1300+ lines) |
| `assets/` | Stock photos from Unsplash (heroes, portraits, products) |

## Demo Identity

**Aurum Aesthetics** — a fictional Chicago aesthetic clinic with three studios (Old Town, River North, Lincoln Park). 555-01XX phone numbers and the team members (Dr. Marisol Avila, Natasha Brennan, Eun-Ji Park, Sofia Reyes) are fictional — see `disclaimer.html` for the full list of what's not fabricated.

## Treatment Vocabulary

We use real, factual industry vocabulary (Botox, Dysport, Xeomin, Juvederm, Restylane, Kybella, HydraFacial, Halo, MOXI, Morpheus8, BBL, CoolSculpting, Emsculpt NEO, Emtone). These are category descriptors used across the medical-aesthetic industry — they describe what the treatments are, not endorsements.

## Demo vs. Production

The apex domain `tryglowgau.com` doesn't signal "demo" by URL, so we make the demo nature explicit in:
- Header (`Demo Clinic` pill next to the logo)
- Footer (persistent disclaimer banner)
- Footer (link to dedicated `disclaimer.html`)
- A dedicated `/disclaimer` page explaining everything in detail

The site has **no fake reviews, no fake before/after photos, no fake tier claims, no fake pricing** — all deliberately removed so the demo stays honest.

## Deployment

Deployed to **Cloudflare Workers + Pages** from this repo:
- Cloudflare watches `main` branch
- Pushes auto-deploy in ~30 seconds
- Custom domain: `tryglowgau.com` (DNS at Namecheap)

## How to update content

1. Edit HTML files directly (no build step)
2. Drop new images into `assets/`
3. Update `sitemap.xml` for any new pages
4. Commit + push to `main`
5. Cloudflare Pages deploys automatically

## Where the Glowgau widget goes

The Glowgau widget placeholder lives in `index.html` and `contact.html` at elements with `id="glowgau-widget-mount"`. When the COO/CTO profile provides the real snippet, replace each placeholder block with:

```html
<!-- BEGIN GLOWGAU WIDGET -->
<script src="..." async></script>
<!-- END GLOWGAU WIDGET -->
```

**Never invent widget IDs or tokens.** Always source from the COO/CTO profile.
