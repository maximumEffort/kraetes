# Kraetes — Amr Sarhan's Consulting Portfolio

Personal portfolio and consulting site for **Amr Sarhan** — Digital Transformation & AI Automation Consultant based in Dubai, UAE.

## About

Kraetes showcases Amr's 12+ years of enterprise systems experience, covering Oracle Fusion Cloud HCM, ERP implementations, and AI-powered automation solutions. The site is a single-page application serving clients across the UAE, Saudi Arabia, Egypt, and the wider MENA region.

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | [Astro 6](https://astro.build) |
| Styling | [Tailwind CSS 4](https://tailwindcss.com) (via Vite plugin) |
| Language | TypeScript |
| Contact | [Formspree](https://formspree.io) |
| Sitemap | `@astrojs/sitemap` |

## Local Development

**Prerequisites:** Node.js >= 22.12.0

```bash
# Install dependencies
npm install

# Start dev server (http://localhost:4321)
npm run dev

# Type-check
npx astro check

# Production build
npm run build

# Preview production build
npm run preview
```

## Deployment

The site outputs a fully static build to `dist/`. Deploy to any static host:

- **Netlify / Vercel** — connect the repo and set the build command to `npm run build` with publish directory `dist`.
- **GitHub Pages** — use the provided `.github/workflows/build.yml` as a base and add a deploy step.
- **Any CDN / object storage** — upload the contents of `dist/` after running `npm run build`.

## Project Structure

```
kraetes/
├── public/              # Static assets (favicon, robots.txt, manifest.json)
├── src/
│   ├── components/      # Section components
│   │   ├── Nav.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── Services.astro
│   │   ├── Projects.astro
│   │   ├── Blog.astro
│   │   ├── Resume.astro
│   │   ├── Contact.astro
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro  # Base HTML shell (SEO, JSON-LD, meta tags)
│   ├── pages/
│   │   └── index.astro   # Single-page entry point
│   └── styles/
│       └── global.css    # Tailwind + custom properties
├── .github/workflows/
│   └── build.yml         # CI: type-check + build on push/PR
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## Contact Form

The contact form submits to [Formspree](https://formspree.io). To use your own endpoint, update the `FORMSPREE_ENDPOINT` constant in `src/components/Contact.astro`.
