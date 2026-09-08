# Jay Lord Dela Cruz — Portfolio Site

Personal resume/portfolio site. Positioning: **Operations Architect | Customer Success Leader | CRM & Automation Specialist**.

## Status

- [x] Project folder created
- [x] Bio/timeline content captured (`content/bio-source.md`)
- [x] Draft About page copy written (`content/about.md`)
- [x] Structured experience data drafted (`content/experience.json`)
- [x] Design tokens extracted from BackendOperators brand guide, adapted for personal use (`brand/design-tokens.md`)
- [x] Node.js installed (v24.18.1)
- [x] Astro project scaffolded (minimal template, TypeScript strict)
- [x] Single-page site built (`src/pages/index.astro`) — Hero, About, What I've Built, Showcase carousel, Experience timeline, Core Expertise, Industries, Contact
- [x] Showcase carousel populated with 8 real screenshots: GHL custom menu links (Family Referral Network), Cycl Sales Tools (3), and 3 AI chatbots (Locked & Lawyered, BackendOperators, Family Referral Network knowledge base)
- [x] 9 real automation screenshots added from Jay's GHL/Make.com Google Drive folders (`assets/ghl-automations/`, `assets/make-automations/` — full sets of 13 + 7 kept there for reference; 9 curated ones copied to `public/` and used in the carousel). Showcase is now 18 slides total.
- [x] Cursor-follow teal glow (site-wide, disabled on touch devices and for `prefers-reduced-motion`)
- [x] Stats band (10+ yrs, 200+ customers, 100+ automations, 50+ AI bots, 20+ trained experts) with count-up animation on scroll into view, placed right after the hero
- [x] Showcase section kinetic-typography treatment: "Systems I've shipped" heading reveals word-by-word on scroll with a hand-drawn teal scribble that draws itself around "shipped"; each carousel slide's tag/caption fades and slides in when it becomes active
- [x] Contact channels: WhatsApp (`wa.me/639454360341`) + email button in the Contact section; site-wide contact email switched to `jay@backendoperators.com` (was a placeholder gmail)
- [x] Footer shows "Powered by BackendOperators" linking to backendoperators.com
- [x] Real photo added to hero (`public/jay-photo.png`)
- [ ] Resume PDF download link
- [ ] Deploy (Vercel/Netlify/GitHub Pages — not yet chosen)
- [ ] Further SEO pass (sitemap, OG image, favicon replacement, Lighthouse check)

## Tech stack decision

**Astro**, chosen for SEO and mobile performance (ships zero JS by default, fast static output). Content-collections pattern fits the timeline/experience data well.

## Commands

| Command | Action |
| :--- | :--- |
| `npm run dev` | Start local dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview the build locally |
| `npm run astro ...` | Run Astro CLI commands (`astro add`, `astro check`) |

**Note:** Node.js (`C:\Program Files\nodejs`) isn't yet on PATH for freshly spawned processes on this machine (PATH was updated in the registry by the installer, but running services/tools started before the install don't see it). `start-dev.bat` in this folder adds it to PATH before running `npm run dev` — the preview tool's `.claude/launch.json` (at the `C:\Users\Jay\Claude` root) points at that script rather than calling `npm` directly. If `npm`/`node` still aren't found in a plain terminal, prefix commands with the nodejs folder or restart the terminal.

## Brand relationship

This site is **not** the BackendOperators business site. The attached BackendOperators brand guide (`C:\Users\Jay\Downloads\BackendOperators-Brand-Guide.dc.html`) is used only as a **design reference** — color palette, type system, and voice rules — adapted here for Jay's personal brand. Copy and content are about Jay, not the BackendOperators agency offer.

## Next step

To add/replace Showcase slides: drop the screenshot into `public/`, then edit the `showcaseItems` array near the top of `src/pages/index.astro` (each item is `{ img, alt, tag, caption }`).

Source screenshots (originals) are kept in `assets/` at the project root for reference — not served by the site; the ones actually used are copied into `public/` with descriptive `showcase-*.png` names.
