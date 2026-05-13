# Axovion.io — Complete Project Repository

This is the master backup repository for Axovion.io. It contains everything needed to rebuild, continue, or hand off the project.

## What is Inside

| Folder/File | Description |
|-------------|-------------|
| `mvp-code/` | Complete React frontend + Node.js backend (36 files, 2,600+ lines) |
| `MVP.md` | Detailed build prompt for Kimi K2.6 or any developer |
| `PROJECT-CONTEXT.md` | Full project summary — decisions, specs, env vars |
| `PAGE-*.md` | Instructions for building each post-MVP page |
| `FEATURE-*.md` | Instructions for building each post-MVP feature |

## Quick Start

### 1. MVP Code
```bash
cd mvp-code/client
npm install
npm run dev

cd ../server
npm install
# Add .env file (see PROJECT-CONTEXT.md)
npm run dev
```

### 2. Deploy to Production
- **Frontend:** Connect `mvp-code/client` to Vercel
- **Backend:** Connect `mvp-code/server` to Railway/Render
- **Database:** MongoDB Atlas (free tier)

## Post-MVP Roadmap

### Phase 1: Pages (Week 2)
- [ ] Services detail page
- [ ] Case Studies / Results page
- [ ] About page
- [ ] Team page (your face as founder)
- [ ] Blog / Resources page

### Phase 2: Features (Week 3-4)
- [ ] Full AI Audit automation (instant report generation)
- [ ] AI calling agent integration (Vapi/Retell)
- [ ] Email automation sequences (Resend/SendGrid)
- [ ] Advanced admin dashboard (task manager, analytics)
- [ ] SEO optimization

## Important Decisions

- **No instant AI report in MVP** — manual follow-up for first clients
- **Brand-first, no founder face yet** — team page comes post-MVP
- **Dark luxury + AI-native design** — black, silver, cyan, orange
- **6 signature animations max** — performance over quantity
- **English-speaking markets only**

## Environment Variables

See `PROJECT-CONTEXT.md` for full list.

## If You Need to Rebuild

1. Clone this repo
2. Read `PROJECT-CONTEXT.md` for full context
3. Use `MVP.md` with Kimi K2.6 to rebuild the MVP
4. Use `PAGE-*.md` and `FEATURE-*.md` for post-MVP expansion

## Contact

Axovion.io — Automate to Win
