# Eidos Site — Project Specification

## Overview

Personal professional brand/portfolio site for technology readiness coordination and delivery advisory services. **Static HTML site** — no framework, no build step, no dependencies.

## Tech Stack

- **HTML5** — 4 static pages (`index.html`, `about.html`, `approach.html`, `experience.html`)
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) with inline config
- **Vanilla JavaScript** — dark mode toggle, mobile menu, dynamic footer year
- **No package.json, no Node.js, no bundler**

## Custom Tailwind Config (inline per page)

- **Primary (blue):** #3385f0 / #1967d2 / #1554b0
- **Secondary (gray):** neutral gray palette
- **Accent (teal):** #14b8a6 / #0d9488
- **Dark mode:** class-based (`<html class="dark">`), persisted to `localStorage`
- **Custom animations:** `fade-in`, `slide-up`, `slide-down`

## Pages & Content

| Page | Purpose |
|------|---------|
| `index.html` | Hero, value prop, 5 "Problems I Solve" blocks, contact info |
| `about.html` | What Eidos does, background, industry experience |
| `approach.html` | 4-stage methodology: Orientation, Specification, Coordination, Handoff |
| `experience.html` | 5 experience areas (integration, vendor coordination, readiness docs, regulatory, complex logic) |

## Layout Pattern (all pages)

- **Fixed header** — logo ("eidos" with gradient text), desktop nav, dark mode toggle, mobile hamburger
- **Footer** — copyright with dynamic year, dark background
- **Sections** alternate white/light backgrounds for visual rhythm
- **Max width:** `max-w-4xl` content, `max-w-7xl` header

## JavaScript (inline, ~2KB total)

1. **Dark mode** — toggle button, localStorage persistence, system preference fallback
2. **Mobile menu** — hamburger toggle with slide-down animation, aria-expanded
3. **Footer year** — `new Date().getFullYear()`

## SEO

Each page has unique `<title>` and `<meta name="description">`. Semantic HTML5, aria labels, sr-only text for accessibility.

## Brand Identity

- **Name:** Eidos
- **Tagline:** "Technology Readiness. Delivery Coordination. Regulated Environments."
- **Industries:** Healthcare, financial services, utility infrastructure
- **Location:** Tempe, Arizona
- **Contact:** avery@eidosadvisory.com, LinkedIn: averymckie

## Deployment

Pure static — deploy anywhere (GitHub Pages, Netlify, Vercel, S3). No build step required.

## Conventions

- Tailwind utility-first, no external CSS files
- Inline Tailwind config duplicated across all 4 HTML files (must update each when changing theme)
- kebab-case filenames
- SVG icons embedded inline
- Alternating section backgrounds for visual rhythm
- Consistent padding (4-6 units), bold headings, relaxed line-height
