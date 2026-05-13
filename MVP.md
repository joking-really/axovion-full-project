# Axovion.io — MVP Build Prompt for Kimi K2.6

## Overview
Build a premium dark luxury AI agency landing page with AI-native fluid animations. This is a 1-week MVP. React frontend, Node.js backend, MongoDB database. Deploy to Vercel.

---

## Design System

### Colors
- Background: `#0A0A0F` (deep black)
- Surface: `#12121A` (cards, sections)
- Primary text: `#C0C0C8` (metallic silver)
- Heading text: `#FFFFFF` (pure white)
- Accent cyan: `#00D4FF` (glows, highlights)
- Accent blue: `#3B82F6` (gradients, links)
- CTA orange: `#F97316` (buttons, primary actions)
- CTA amber: `#FBBF24` (hover states, secondary highlights)
- Success: `#10B981`
- Error: `#EF4444`

### Typography
- Headings: Inter or Geist (weight 700-800)
- Body: Inter (weight 400-500)
- Mono: JetBrains Mono (for code/tech accents)
- Hero headline: 72px desktop, 40px mobile
- Section headings: 48px desktop, 32px mobile

### Spacing
- Max width: 1280px
- Section padding: 120px vertical desktop, 80px mobile
- Card radius: 16px
- Button radius: 12px

---

## Tech Stack
- Frontend: React 18 + Vite + Tailwind CSS
- Backend: Node.js + Express
- Database: MongoDB (Mongoose)
- Auth: NextAuth.js (Google OAuth) — admin only
- Animations: GSAP + ScrollTrigger, react-bits components
- Icons: Lucide React
- Forms: React Hook Form
- Deployment: Vercel (frontend), Vercel Serverless or Railway (backend)

---

## Pages & Routes

### 1. Home Page (/) — Killer Landing Page

#### Navigation
- Logo: Axovion.io (left)
- Links: Services, AI Audit, Contact
- CTA button: "Start Free AI Audit" (orange)
- Mobile: hamburger menu

#### Hero Section
- Background: Aurora animation (react-bits) — flowing cyan/blue gradient light beams on deep black
- Headline: "Automate Repetitive Workflows in Days, Not Quarters."
- Subheadline: "Axovion.io builds ROI-focused AI agents that automate customer support, lead follow-up, booking, e-commerce workflows, and repetitive business tasks."
- CTA: "Start Free AI Audit" (primary, orange) + "Book a Call" (secondary, outline)
- Headline animation: SplitText with stagger reveal
- Trust bar below: "Powered by Kimi K2.6" + "2+ Years Experience" + "100+ Demos Delivered"

#### Problem Section
- Heading: "Still Doing Work That AI Should Handle?"
- 4 pain points with icons:
  - Slow customer support response time
  - Leads slipping through manual follow-up
  - Repetitive tasks eating your team's hours
  - Competitors scaling with AI while you don't
- Visual: subtle gradient cards on hover

#### Services Section — Bento Grid
- Heading: "AI Agents That Run Your Business 24/7"
- Bento grid layout (mixed card sizes):
  - Large card (2x2): "Free AI Audit" — scan your business, get automation map + ROI
  - Medium card: "Customer Support Chatbots" — website, WhatsApp, custom
  - Medium card: "Lead Generation & Follow-Up" — never miss a lead again
  - Small card: "Booking Automation"
  - Small card: "E-Commerce Support"
  - Small card: "Abandoned Cart Recovery"
  - Small card: "CRM & Email Automation"
  - Medium card: "AI Consulting & Strategy"
- Hover: cyan glow border, 4px lift, subtle gradient rotation, 300ms transition
- Each card: icon, title, 1-line description, arrow link

#### How It Works — Visual Flow Diagram
- Heading: "From Manual to AI-Powered in 3 Steps"
- Vertical SVG flow diagram:
  - Node 1: "Submit AI Audit" (icon: clipboard)
  - Node 2: "AI Analysis" (icon: brain) — "Our AI scans your workflows"
  - Node 3: "Custom Report + Consultation" (icon: file-check)
- Central connecting line draws on scroll (IntersectionObserver)
- Nodes pulse/fade in as user scrolls
- Hover: node glows cyan, tooltip expands with detail

#### Social Proof — Testimonials
- Heading: "Trusted by Business Owners"
- 3 testimonial cards with placeholders:
  - "[Client Name], [Industry]" — "Axovion built us a chatbot that handles 80% of support. Game changer."
  - "[Client Name], [Industry]" — "We went from 24h response time to instant. Our customers love it."
  - "[Client Name], [Industry]" — "The AI Audit alone showed us $15K/month in savings we were missing."
- Design: quote marks, avatar placeholder, subtle card background

#### Trust Section
- Heading: "Why Axovion.io"
- 6 trust elements in 2 rows:
  - AI agents running in our own business
  - Daily AI automation content system
  - 2+ years building AI solutions
  - 100+ demos delivered
  - Powered by Kimi K2.6
  - ROI-focused, not just tech-for-tech

#### Final CTA Section
- Heading: "Ready to Stop Working Harder and Start Scaling?"
- Sub: "Get your free AI Audit. See exactly where AI can automate your business — with estimated ROI and savings."
- CTA: "Start Free AI Audit" (large orange button)
- Background: subtle Aurora or gradient glow

#### Footer
- 4 columns:
  - Brand: Axovion.io logo + "Automate to Win" tagline
  - Pages: Home, Services, AI Audit, Contact
  - Legal: Privacy Policy, Terms of Service
  - Social: LinkedIn, Facebook, Instagram, Twitter/X, YouTube (icons with links)
- Bottom bar: "© 2025 Axovion.io. All rights reserved."

---

### 2. AI Audit Page (/audit)

#### Hero
- Heading: "Free AI Business Audit"
- Sub: "Answer a few questions about your business. Our AI will analyze your workflows and build a custom automation report with ROI estimates."
- Background: subtle gradient, no heavy animation

#### Audit Form
- Multi-step or single long form (your choice, but keep it scannable)
- Fields (all visible, most optional):
  - Business Name (required)
  - Industry (required, dropdown)
  - Website URL (required)
  - Contact Email or WhatsApp (required)
  - Main Goal (required, textarea)
  - Monthly Revenue (optional)
  - Number of Employees (optional)
  - Repetitive Tasks You Do Daily (optional, textarea)
  - Tools You Use (optional, multi-select)
  - Customer Support Volume (optional)
  - Leads per Month (optional)
  - Biggest Bottleneck (optional, textarea)
  - Budget Range (optional)
  - Any Documents to Upload (optional, file)
- Submit button: "Submit for AI Audit"
- On submit: show success message — "Thank you! Your AI Audit report will be ready within 24 hours and sent to your email."
- Data saved to MongoDB

---

### 3. Contact/Book a Call Page (/contact)

#### Hero
- Heading: "Let's Talk AI Automation"
- Sub: "Book a free 15-30 minute consultation. We'll discuss your business and show you exactly where AI can help."

#### Calendly Embed
- Embed Calendly inline (or link to Calendly if embed not preferred)
- Alternative contact: email, WhatsApp number

---

### 4. Admin Dashboard (/admin) — Protected Route

#### Auth
- NextAuth.js with Google OAuth
- Only your email(s) allowed access

#### Dashboard Sections
1. **Audit Submissions**
   - Table: business name, industry, contact, date, status (New / In Progress / Delivered)
   - Click to view full submission details
   - Quick actions: mark as delivered, delete

2. **Chatbot Conversations**
   - List of recent chats
   - Click to view full transcript
   - Lead indicator (collected email/phone or not)

3. **Consultation Bookings**
   - From Calendly or chatbot
   - Name, contact, date, status

4. **Quick Stats**
   - Total audits submitted
   - Total chat conversations
   - Total bookings
   - Conversion rate (visits → audit)

#### Design
- Clean, functional, not overly styled
- Sidebar navigation
- Responsive table layout

---

## Global Components

### AI Chatbot (Floating)
- Position: bottom-right corner
- Trigger: chat bubble icon
- Open state:
  - Header: "Axovion AI" + close button
  - Message: "Hi, I'm Axovion AI. Ask me anything or pick a common question:"
  - FAQ chips (clickable):
    - "How long does implementation take?"
    - "What industries do you serve?"
    - "How much does it cost?"
    - "Is my data secure?"
    - "What is the AI Audit?"
  - Free-text input below
- Behavior:
  - Answers powered by Kimi K2.6 via API (Groq or direct Kimi)
  - Pushes to book consultation or submit AI Audit
  - Collects email/WhatsApp before deep answers
  - All chats saved to MongoDB
- Design: matches site dark theme, cyan accents

---

## Backend API Endpoints

```
POST /api/audit          — Submit AI Audit form
GET  /api/audits         — List all audits (admin)
GET  /api/audits/:id     — Get single audit (admin)
PUT  /api/audits/:id     — Update audit status (admin)
DELETE /api/audits/:id   — Delete audit (admin)

POST /api/chat           — Send message to AI chatbot
GET  /api/chats          — List all chats (admin)
GET  /api/chats/:id      — Get single chat transcript (admin)

POST /api/booking        — Log consultation booking
GET  /api/bookings       — List bookings (admin)

POST /api/auth/signin    — NextAuth.js Google signin
GET  /api/auth/session   — Check session
```

---

## MongoDB Schema

### Audit
```js
{
  businessName: String (required),
  industry: String (required),
  websiteUrl: String (required),
  contact: String (required),
  mainGoal: String (required),
  monthlyRevenue: String,
  employees: Number,
  repetitiveTasks: String,
  tools: [String],
  supportVolume: String,
  leadsPerMonth: String,
  bottleneck: String,
  budget: String,
  documents: [String], // file URLs
  status: { type: String, enum: ['new', 'in-progress', 'delivered'], default: 'new' },
  createdAt: Date,
  updatedAt: Date
}
```

### Chat
```js
{
  sessionId: String,
  messages: [
    { role: String, content: String, timestamp: Date }
  ],
  contactInfo: {
    email: String,
    whatsapp: String
  },
  leadScore: Number,
  createdAt: Date
}
```

### Booking
```js
{
  name: String,
  email: String,
  phone: String,
  source: String, // 'calendly' or 'chatbot'
  date: Date,
  status: String,
  createdAt: Date
}
```

---

## Animation Map (Max 6 Signature Animations)

1. **Aurora** — Hero background (react-bits)
2. **SplitText** — Hero headline stagger reveal
3. **Bento hover** — Custom CSS (glow, lift, gradient shift)
4. **Flow diagram** — SVG line draw + node fade-in on scroll
5. **Scroll reveal** — Sections fade/slide up as they enter viewport
6. **CTA glow** — Subtle pulse on primary buttons

---

## File Structure

```
axovion-mvp/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── AuroraBg.jsx
│   │   │   ├── SplitText.jsx
│   │   │   ├── BentoGrid.jsx
│   │   │   ├── FlowDiagram.jsx
│   │   │   ├── TestimonialCard.jsx
│   │   │   ├── AuditForm.jsx
│   │   │   ├── Chatbot.jsx
│   │   │   └── AdminLayout.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Audit.jsx
│   │   │   ├── Contact.jsx
│   │   │   └── Admin/
│   │   │       ├── Dashboard.jsx
│   │   │       ├── Audits.jsx
│   │   │       ├── Chats.jsx
│   │   │       └── Bookings.jsx
│   │   ├── hooks/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── public/
│   ├── index.html
│   ├── tailwind.config.js
│   └── vite.config.js
├── server/                 # Node.js backend
│   ├── models/
│   │   ├── Audit.js
│   │   ├── Chat.js
│   │   └── Booking.js
│   ├── routes/
│   │   ├── audits.js
│   │   ├── chats.js
│   │   └── bookings.js
│   ├── middleware/
│   │   └── auth.js
│   ├── config/
│   │   └── db.js
│   ├── server.js
│   └── package.json
└── README.md
```

---

## Environment Variables

```env
# Server
MONGODB_URI=
PORT=5000
KIMI_API_KEY=           # or GROQ_API_KEY for chatbot
NEXTAUTH_SECRET=
NEXTAUTH_URL=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
ADMIN_EMAIL=            # your email for dashboard access

# Client
VITE_API_URL=
VITE_CALENDLY_LINK=
```

---

## MVP Success Criteria
- [ ] All 3 public pages render correctly on desktop and mobile
- [ ] AI Audit form submits and saves to MongoDB
- [ ] Admin dashboard shows audit submissions
- [ ] Chatbot visible, clickable FAQs work, pushes to audit/booking
- [ ] Calendly embed works on Contact page
- [ ] All 6 signature animations present and performant
- [ ] Google OAuth protects /admin route
- [ ] Deployed to Vercel (frontend) + working backend

---

## Post-MVP Expansion (Separate .md files)
- Full AI Audit automation (instant report generation)
- AI calling agent integration (Vapi/Retell)
- Services detail page
- Case Studies / Results page
- About page
- Team page (with your face as founder)
- Blog / Resources page
- Advanced admin dashboard (task manager, analytics)
- Email automation (Resend/SendGrid)
- Stripe payment integration
- SEO optimization

---

## Notes for Kimi K2.6
- Use functional components + hooks
- Tailwind for all styling
- GSAP for complex animations, CSS for simple ones
- Mobile-first responsive design
- Accessible (ARIA labels, keyboard nav, focus states)
- Performance: lazy load below-fold sections, optimize images
