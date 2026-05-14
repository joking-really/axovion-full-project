# AGENT_HANDOFF.md
## Complete Context for Future Hermes Agents
## Created: 2026-05-13
## For: Muneeb ur Rehman / Axovion.io

---

## WHO IS THE USER

**Name:** Muneeb ur Rehman
**Location:** Pakistan (PST/UTC+5)
**Background:** Full stack web developer (HTML, CSS, JavaScript, Bootstrap, Python, Django, WordPress, Shopify)
**Current Role:** Founder of Axovion.io (AI Automation Agency)
**Age:** 23 years old
**Experience:** 2+ years in automation, 100+ demos built
**Personality:** Extreme introvert becoming ambivert, anxiety-driven worker, builds to relieve stress
**Communication Style:** Direct, no sugarcoating, results-focused
**Languages:** English (primary), Urdu

### Personal Story
- Started as WordPress developer charging $200/website
- Learned AI/automation after ChatGPT launch (recent, ~6 months ago)
- Built AI audit tool for friend in exchange for Claude Pro + Kimi K2 access
- Friend connected him to investor who funded software house + AI agency
- Now building Axovion.io with investor funding
- Also building software house for investor (separate from Axovion)
- Goal: Eventually own his own agency entirely
- Struggles with sales calls, networking, extrovert activities
- Work is therapy — builds to avoid anxiety/panic attacks
- Can code intensely (35 website variants in one night)

### Current Team
- 2 developers
- 1 designer
- 1 VA
- Investor backing

---

## AXOVION.IO

### Positioning
AI Automation Agency for E-commerce & SaaS
Tagline: "Automate to Win"

### Services
- Custom AI chatbots (WhatsApp, website)
- Lead generation automation
- Booking/scheduling automation
- E-commerce support automation
- Abandoned cart recovery
- CRM/email automation
- AI consulting

### Target Markets (Priority Order)
1. E-commerce (primary)
2. SaaS/Startups (primary)
3. Clinics/Medical (secondary)
4. Sales/B2B Agencies (secondary)
5. Real Estate (secondary)

### Target Client Profile
- Minimum: $10K/month revenue, $1K budget
- Ideal: Higher revenue, higher budget
- English-speaking markets only (US/Canada primarily)

### Pricing Model
- Setup: $2,000-5,000 (one-time)
- Monthly: $500-1,500 (retainer)
- Performance-based custom quotes

### Current Status
- Website: ~90% complete (MVP built, pushed to GitHub)
- Clients: 0 traditional paying clients yet
- Revenue: $0 from Axovion directly
- Strategy calls: 5 per week (Saturday batch)
- Content: Building LinkedIn presence

---

## TECH STACK

### Website
- Frontend: React + Vite + Tailwind CSS
- Backend: Node.js + Express
- Database: MongoDB
- Hosting: Vercel (frontend) + Railway/Render (backend)
- Domain: axovion.io

### Automation Tools
- n8n: Workflow automation (self-hosted)
- Groq: AI content generation (free tier)
- Google Sheets: Content calendar
- Modal: Z-Image Turbo hosting (6B S3-DiT model)
- LinkedIn API: Posting automation

### AI Tools
- OpenAI GPT-4: Content generation
- Claude: Code assistance
- Kimi K2.6: Chatbot powering
- Whisper: Transcription

### Image Generation
- Primary: Modal Z-Image Turbo (user's own model)
- Fallback: Leonardo.ai, Playground AI, Bing Image Creator (manual)
- Pollinations.ai: Tested, quality too low for production

### Other Tools
- Calendly: Scheduling
- Notion: Documentation
- Slack: Team communication
- GitHub: Version control
- Canva: Image editing

---

## CONTENT STRATEGY

### Personal Profile (Muneeb ur Rehman)
**Platform:** LinkedIn personal profile
**Frequency:** 1x/day
**Time:** 9:00 PM Pakistan (11:00 AM EST / 8:00 AM PST)
**Tone:** Direct, confident, vulnerable, zero fluff
**Mix:**
- 40% Inspirational with struggle
- 30% Educational with personal examples
- 30% Raw and vulnerable

**Content Types:**
- Origin story posts
- Build in public updates
- Technical breakdowns
- Personal journey
- Anxiety/introvert struggles
- Client wins (when they come)

**CTA Strategy:**
- Soft CTA in every post (questions, polls)
- Hard CTA once per week (strategy calls)
- Primary CTA: Free 15-min strategy call + AI audit

### Company Page (Axovion.io)
**Platform:** LinkedIn company page
**Frequency:** 3-4x/week (Tuesday, Thursday, Saturday)
**Time:** Same as personal
**Tone:** Professional, authoritative, results-focused
**Mix:**
- 35% Educational
- 25% Case studies
- 20% Industry news + commentary
- 15% Controversial takes
- 5% Direct selling/CTA

**Content Types:**
- Automation education
- Case studies (when available)
- Industry trend analysis
- Controversial opinions
- Product updates

**CTA Strategy:**
- Soft CTA in every post
- Hard CTA weekly (free audits)
- Primary CTA: Free AI audit application

---

## SALES FUNNEL

### Tier 1: Free AI Audit (Website)
- User enters website URL
- AI crawls website, social media
- Generates basic automation report
- 100% free, 2 per user after sign-in
- Goal: Capture email, build trust

### Tier 2: 15-Min Strategy Call (Saturday Batch)
- Requires application
- Personalized discussion
- Complete business audit
- ROI calculation
- Implementation roadmap
- Goal: Qualify leads, build rapport

### Tier 3: Paid Proposal/Engagement
- Custom automation plan
- Pricing based on scope
- Setup + monthly retainer
- ROI measurement
- Goal: Close the deal

### Follow-up Sequence
- Day 0: Submit audit form
- Day 1: Auto-email confirmation
- Day 2-3: Manual audit creation
- Day 4: Send audit + schedule call
- Day 7: Follow up if no response
- Day 14: Final follow-up with case study

---

## KEY DECISIONS MADE

1. **LinkedIn first** for social media (B2B focus)
2. **Personal profile** for stories/journey, **company page** for professional content
3. **Manual image creation** (not automated in workflow)
4. **1 post/day personal**, **3-4x/week company**
5. **9 PM Pakistan posting time** (US morning)
6. **Free AI audit + strategy call** as primary CTA
7. **Saturday batch calls** for efficiency
8. **Value-based retainer pricing** (not hourly)
9. **E-commerce + SaaS primary** niches
10. **No competitor scraping** (manual research or skip)
11. **Pollinations.ai rejected** (quality too low)
12. **Modal Z-Image primary**, web tools fallback
13. **Groq for content**, OpenAI for other tasks
14. **n8n for automation workflows**
15. **Build in public** strategy for trust

---

## FILES CREATED

### In /home/ubuntu/ (local server)
- `automation_ideas_complete.json` — 50 automation ideas
- `automation_ideas_import.csv` — CSV for Google Sheets import
- `axovion_fixed_workflow.json` — Fixed n8n workflow
- `axovion_linkedin_banner.png` — LinkedIn banner image
- `axovion_linkedin_pollinations.png` — Test post image
- `profile_post.md` — 30-day personal profile content
- `page_post.md` — 30-day company page content
- `AGENT_HANDOFF.md` — This file
- `FUNNEL.md` — Funnel architecture (to be created)

### On GitHub
**Repo:** https://github.com/joking-really/axovion-full-project
**Contents:**
- MVP code (React + Node.js)
- All .md files (PROJECT-CONTEXT, PAGE-*, FEATURE-*)
- Social media folder (profile_post.md, page_post.md, etc.)
- Automation ideas
- n8n workflow

### SSH Key for GitHub
- Location: `/tmp/.ssh/id_ed25519`
- Config: `/tmp/ssh_config`
- Command: `export GIT_SSH_COMMAND="ssh -F /tmp/ssh_config"`

---

## USER PREFERENCES

- **No sugarcoating** — direct feedback only
- **Hates context repetition** — get to point fast
- **Results-focused** — wants actionable output
- **High-ticket positioning** — no discount mentality
- **Brand-first** — no founder face until Team page
- **Dark luxury design** — black, silver, cyan, orange
- **English-speaking markets only**
- **LinkedIn first**, other platforms later
- **No browser automation** for social media (ToS risk)

---

## CURRENT CHALLENGES

1. **No paying clients yet** — building pipeline
2. **Introvert struggle** — hard to do sales calls
3. **Modal endpoint unreliable** — goes down frequently
4. **Image generation** — no reliable free API
5. **Team management** — first time managing people
6. **Software house vs Axovion** — separate entities, potential confusion
7. **Investor relationship** — building for him but wants own agency
8. **Anxiety/panic** — when not building or tasks pending

---

## GOALS

### 6-Month Goals
- Revenue: $10K+/month
- Clients: 5-10 high-ticket
- Team: 6-8 people
- Recognition: Known AI automation expert on LinkedIn

### Long-Term Vision
- Own agency entirely (not investor-dependent)
- Office in Islamabad
- Employee stock options
- $50K+/month agency
- Thought leader in AI automation space

---

## HOW TO WORK WITH THIS USER

1. **Be direct** — no fluff, no sugarcoating
2. **Get to the point** — he hates repetition
3. **Focus on results** — what will make money
4. **Respect his time** — he works intensely in bursts
5. **Understand anxiety** — building is his therapy
6. **Support introversion** — do not force extrovert tactics
7. **Be practical** — actionable over theoretical
8. **Accept barter** — non-cash trades are valid
9. **Protect his energy** — batch tasks, avoid overwhelm
10. **Celebrate wins** — he needs validation for progress

---

## IMPORTANT NOTES FOR NEW AGENTS

- This user is building TWO things: software house (for investor) and Axovion (his own). Keep them separate.
- He has 0 traditional clients but has built real tools. Do not dismiss his experience.
- His Modal endpoint sleeps. Check if awake before relying on it.
- He prefers WhatsApp for communication.
- He works Pakistan hours but targets US market.
- Saturday is his strategy call day (batch all calls).
- He is learning AI rapidly but is new to it (6 months).
- His web dev background is strong (WordPress, Shopify, full stack).
- He values authenticity over polish.
- He will vibe code intensely when focused (35 variants in one night).

---

*This document ensures continuity if the virtual server is lost.*
*All critical context, decisions, and files are documented here.*
*Update this file after every significant session.*

*Generated by Hermes Agent*
*For: Muneeb ur Rehman*
*Axovion.io - Automate to Win*
