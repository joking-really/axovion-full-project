# Axovion.io — Full AI Audit Automation Build Instructions

## Overview
Upgrade the MVP audit form to a fully automated system that generates interactive reports instantly using Kimi K2.6.

## Current MVP State
- Form submits to database
- Manual follow-up in 24 hours
- Admin dashboard shows submissions

## Target State
- User submits form → AI analyzes instantly → Interactive report generated → Email sent → AI calling agent follows up

## Architecture

### 1. Audit Analysis Engine
- Trigger: Form submission
- Process:
  1. Parse form data
  2. Build analysis prompt for Kimi K2.6
  3. Call Kimi API with structured prompt
  4. Parse response into report sections
  5. Save report to database
  6. Send email with report link
  7. Trigger calling agent if high-value lead

### 2. Kimi K2.6 Prompt Template
```
You are an AI automation consultant for Axovion.io. Analyze this business and create a detailed automation audit report.

Business: {businessName}
Industry: {industry}
Website: {websiteUrl}
Monthly Revenue: {monthlyRevenue}
Employees: {employees}
Repetitive Tasks: {repetitiveTasks}
Tools: {tools}
Support Volume: {supportVolume}
Leads/Month: {leadsPerMonth}
Biggest Bottleneck: {bottleneck}
Budget: {budget}

Generate:
1. AUTOMATION_OPPORTUNITY_MAP: List 3-5 specific workflows that can be automated
2. ESTIMATED_ROI: Calculate potential savings (hours × hourly rate, or revenue recovery)
3. MONTHLY_SAVINGS: Dollar estimate
4. RECOMMENDED_AGENTS: Specific AI agents to build (chatbot, calling agent, etc.)
5. WORKFLOW_MAP: Step-by-step how each automation would work
6. IMPLEMENTATION_TIMELINE: Days to deploy each agent
7. PRIORITY_RANKING: Which automation to build first

Format as structured JSON.
```

### 3. Interactive Report Page (/audit-report/:id)
Sections:
- Header: Business name + audit date
- Executive Summary: Top 3 opportunities
- Automation Opportunity Map: Visual cards per workflow
- ROI Calculator: Editable inputs (hours saved, hourly rate, tool costs)
  - Real-time recalculation as user adjusts numbers
  - Show payback period
- Recommended Agents: Cards with description + estimated setup cost
- Workflow Map: Visual flow diagram (reuse homepage component)
- Implementation Timeline: Gantt-style or step list
- CTA: "Book Implementation Call" + "Download as PDF"

### 4. PDF Generation
- Library: Puppeteer or html2pdf.js
- Trigger: "Download as PDF" button
- Style: Print-optimized version of report

### 5. Email Delivery
- Service: Resend or SendGrid
- Trigger: Report ready
- Template: Branded email with report link + booking CTA

### 6. AI Calling Agent Follow-Up
- Trigger: High-value lead (revenue > $50K/month or budget > $5K)
- Delay: 2 hours after report delivery
- Provider: Vapi or Retell
- Script:
  - Intro: "Hi, this is [Name] from Axovion. I saw you submitted an AI Audit..."
  - Mention 1-2 top opportunities from their report
  - Push to book consultation
  - Handle objections
- Log call outcome to dashboard

## Database Updates
```js
// Add to Audit schema
report: {
  opportunities: [Object],
  roiEstimate: Number,
  monthlySavings: Number,
  recommendedAgents: [Object],
  workflowMap: Object,
  timeline: [Object],
  generatedAt: Date,
  status: { type: String, enum: ['pending', 'generated', 'delivered', 'viewed'], default: 'pending' }
}
```

## API Endpoints
```
POST /api/audit/analyze      — Trigger AI analysis
GET  /api/audit/report/:id   — Fetch report
POST /api/audit/pdf/:id      — Generate PDF
POST /api/audit/email/:id    — Send report email
POST /api/audit/call/:id     — Trigger calling agent
```

## Design
- Same dark luxury theme
- Report sections: card-based, scrollable
- ROI calculator: interactive sliders/inputs
- Workflow map: animated SVG

## Tech
- Kimi K2.6 API for analysis
- Puppeteer for PDF
- Resend/SendGrid for email
- Vapi/Retell API for calling
- Cron job or queue for delayed calling
