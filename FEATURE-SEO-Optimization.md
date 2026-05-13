# Axovion.io — SEO & Performance Optimization Build Instructions

## Overview
Make Axovion.io discoverable and fast. Post-MVP priority.

## Technical SEO

### Meta Tags (All Pages)
```html
<title>Axovion.io | AI Automation Agency — Automate to Win</title>
<meta name="description" content="Axovion.io builds ROI-focused AI agents that automate customer support, lead follow-up, booking, and repetitive business workflows. Get your free AI Audit.">
<meta name="keywords" content="AI automation, AI chatbot, business automation, AI agency, workflow automation">
<meta property="og:title" content="Axovion.io | AI Automation Agency">
<meta property="og:description" content="Automate repetitive workflows in days, not quarters.">
<meta property="og:image" content="/og-image.jpg">
<meta property="og:url" content="https://axovion.io">
<meta name="twitter:card" content="summary_large_image">
```

### Structured Data (JSON-LD)
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Axovion.io",
  "url": "https://axovion.io",
  "logo": "https://axovion.io/logo.png",
  "description": "AI automation agency building ROI-focused AI agents.",
  "sameAs": [
    "https://linkedin.com/company/axovion",
    "https://twitter.com/axovion"
  ]
}
```

### Sitemap & Robots
- `/sitemap.xml` — auto-generated
- `/robots.txt` — allow all, point to sitemap

### URL Structure
- `/` — Home
- `/services` — Services
- `/audit` — AI Audit
- `/results` — Case Studies
- `/about` — About
- `/team` — Team
- `/blog` — Blog
- `/contact` — Contact
- `/audit-report/:id` — Report (noindex)

## Performance

### Core Web Vitals Targets
- LCP < 2.5s
- FID < 100ms
- CLS < 0.1

### Optimizations
- Image optimization: WebP, lazy loading, responsive sizes
- Font loading: `font-display: swap`
- Code splitting: route-based lazy loading
- Minimize JS bundle: tree shaking, dynamic imports
- CDN: Cloudflare or Vercel Edge
- Caching: aggressive static asset caching

### Animation Performance
- Use `transform` and `opacity` only
- Avoid layout thrashing
- Pause animations when not in viewport
- Respect `prefers-reduced-motion`

## Content SEO

### Blog Strategy
- Target keywords:
  - "AI automation for small business"
  - "chatbot for customer support"
  - "automate lead follow up"
  - "AI agency pricing"
  - "workflow automation examples"
- Post 1-2 articles/week
- Internal linking between posts and service pages

### Local SEO (if targeting specific regions)
- Google Business Profile
- Local directory listings
- Location-specific landing pages

## Tools
- Google Search Console
- Google Analytics 4
- Ahrefs or SEMrush for keyword research
- PageSpeed Insights for performance monitoring

## Implementation
- Use react-helmet-async for meta tags
- Generate sitemap with sitemap npm package
- Add structured data in HTML head
- Set up 301 redirects if URLs change
