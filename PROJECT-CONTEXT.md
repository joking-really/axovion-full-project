# Axovion.io — Full Project Context

## Project Overview
- **Agency Name:** Axovion.io
- **Tagline:** Automate to Win
- **Positioning:** ROI-focused AI automation partner for high-ticket clients
- **Target:** E-commerce, clinics, sales/B2B agencies, startups/SaaS, real estate
- **Minimum Client:** $10K/month revenue, $1K budget
- **Tech Stack:** React + Node.js + MongoDB + Vercel

## 50-Question Discovery Summary

### Brand & Positioning
- Brand-first approach (no founder face yet, team page later)
- Dark luxury + AI-native design feel
- Colors: Black (#0A0A0F), Silver (#C0C0C8), Cyan (#00D4FF), Orange (#F97316), Amber (#FBBF24)
- English-speaking markets only

### Services
1. Free AI Audit
2. Customer Support Chatbots (Website, WhatsApp)
3. Lead Generation & Follow-Up
4. Booking Automation
5. E-Commerce Support
6. Abandoned Cart Recovery
7. CRM & Email Automation
8. AI Consulting & Strategy

### AI Audit Flow (MVP)
- Detailed questionnaire (all fields visible)
- No instant report — manual follow-up in 24h
- Data saved to MongoDB admin dashboard
- Customer sees: "Report ready in 24 hours, sent to email"

### Integrations
- Calendly for booking
- n8n for automation
- Groq for chatbot brain (Kimi K2.6)
- Vapi/Retell for calling agents (future)
- NextAuth.js + Google OAuth for admin

### Website Structure
**MVP Pages:**
- Home (killer landing page, all 10 sections)
- AI Audit (detailed form)
- Contact/Book a Call (Calendly embed)
- Admin Dashboard (protected, Google OAuth)

**Post-MVP Pages:**
- Services detail
- Case Studies/Results
- About
- Team (founder face here)
- Blog/Resources

**Post-MVP Features:**
- Full AI Audit automation (instant report generation)
- AI calling agent follow-up
- Email automation sequences
- Advanced admin dashboard (task manager, analytics)
- SEO optimization

### Key Decisions Log
- Primary CTA: "Start Free AI Audit"
- Secondary CTA: "Book a Call"
- Headline: "Automate Repetitive Workflows in Days, Not Quarters"
- Subheadline: Option A (full description)
- Top pain point: Slow customer support response time
- Cost of inaction: Competitors adopting AI while they don't
- Trust elements: AI agents in own business + Daily AI content system

### Design System
- Typography: Inter/Geist (headings), Inter (body), JetBrains Mono (code)
- Max width: 1280px
- Section padding: 120px desktop, 80px mobile
- Card radius: 16px, Button radius: 12px
- 6 signature animations: Aurora, SplitText, Bento hover, Flow diagram, Scroll reveal, CTA glow

### Timeline
- MVP launch: 1 week
- Post-MVP expansion: Weeks 2-4

## File Structure
```
axovion-full-project/
├── mvp-code/              # Complete React + Node.js MVP
│   ├── client/            # React frontend
│   └── server/            # Node.js backend
├── MVP.md                 # MVP build instructions
├── PAGE-*.md              # Post-MVP page instructions
├── FEATURE-*.md           # Post-MVP feature instructions
└── PROJECT-CONTEXT.md     # This file
```

## Environment Variables Needed
```
MONGODB_URI=
PORT=5000
KIMI_API_KEY=           # or GROQ_API_KEY
NEXTAUTH_SECRET=
NEXTAUTH_URL=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
ADMIN_EMAIL=
```

## Deployment Plan
1. Frontend: Vercel (from GitHub)
2. Backend: Railway/Render/Vercel Serverless
3. Database: MongoDB Atlas
4. Domain: axovion.io

## Notes
- MVP chatbot uses static responses (no live API)
- Admin dashboard has mock data (connect to real API for production)
- Placeholder testimonials — replace with real ones
- Calendly link needs to be added to Contact page
- Kimi K2.6 API integration needed for chatbot and audit automation
