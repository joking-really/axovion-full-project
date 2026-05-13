# Axovion.io — Blog / Resources Page Build Instructions

## Overview
Content hub for SEO and authority building. Post-MVP priority.

## Route
`/blog`

## Sections

### Hero
- Heading: "AI Automation Insights"
- Sub: "Practical guides, case studies, and strategies for business owners."

### Featured Post
- Large card: latest/most important article
- Image, title, excerpt, date, read time

### Post Grid
- 3-column grid of article cards
- Each: thumbnail, category tag, title, excerpt, date
- Categories: Strategy, Case Studies, Tools, Trends

### Categories / Filters
- Horizontal filter bar: All, Strategy, Case Studies, Tools, Trends

### Newsletter Signup
- Heading: "Get AI Automation Tips Weekly"
- Email input + "Subscribe" button
- Stored in database or connected to Resend/SendGrid later

### Placeholder Posts (for design)
1. "How AI Chatbots Save E-Commerce Brands 20+ Hours a Week"
2. "The Real Cost of Slow Lead Response (And How to Fix It)"
3. "5 Workflows Every Clinic Should Automate in 2025"
4. "Why Most AI Projects Fail (And How We Avoid It)"
5. "Building a Daily AI Content Agent: Behind the Scenes"

## Design
- Clean, readable — content is king here
- Card hover: subtle lift + shadow
- Typography optimized for long-form reading

## Tech
- Markdown or CMS for posts (start with static MD files)
- React Router dynamic routes for posts: `/blog/:slug`
- SEO: react-helmet for meta tags
