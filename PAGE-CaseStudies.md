# Axovion.io — Case Studies / Results Page Build Instructions

## Overview
Proof page. Real results from real clients. Essential for high-ticket conversion.

## Route
`/results` or `/case-studies`

## Sections

### Hero
- Heading: "Real Results, Real ROI"
- Sub: "See how businesses like yours are saving time and money with AI agents."

### Case Study Cards
Each case study:
- Client industry (tag)
- Challenge (1 sentence)
- Solution (1-2 sentences)
- Results (3 metrics with big numbers)
- Testimonial quote
- "Read Full Story" link (optional detail modal/page)

Placeholder case studies for MVP:
1. **E-Commerce Brand**
   - Challenge: 500+ support tickets daily, 24h response time
   - Solution: AI chatbot + WhatsApp agent
   - Results: 80% tickets automated, 2min response time, $12K/month saved

2. **Real Estate Agency**
   - Challenge: Leads not followed up, missed appointments
   - Solution: Lead capture bot + booking automation + follow-up sequences
   - Results: 3x lead response rate, 40% more bookings, 15 hours/week saved

3. **Clinic / Healthcare**
   - Challenge: Appointment scheduling chaos, no-shows
   - Solution: Booking bot + reminder system + rescheduling
   - Results: 60% reduction no-shows, staff saved 20h/week, happier patients

### Metrics Banner
- Big number stats across the page:
  - "500K+" — Customer interactions automated
  - "$2M+" — Client revenue recovered/saved
  - "100+" — AI agents deployed
  - "24/7" — Always-on availability

### CTA
- "Ready to be our next success story?"
- Button: "Start Free AI Audit"

## Design
- Cards with subtle gradient borders
- Metric numbers: large font (72px), orange accent
- Scroll-triggered number count-up animation

## Tech
- Reuse testimonial card component
- GSAP ScrollTrigger for count-up
