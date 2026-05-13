# Axovion.io — Email Automation Build Instructions

## Overview
Automated email sequences for lead nurturing, audit delivery, and follow-ups.

## Provider
**Resend** (recommended — simple, good deliverability, free tier)
Alternative: SendGrid, Mailgun, AWS SES

## Email Sequences

### 1. Welcome / Audit Submitted
**Trigger:** Audit form submitted
**Delay:** Immediate
**Subject:** "Your AI Audit is being prepared — Axovion.io"
```
Hi {name},

Thanks for submitting your AI Audit for {businessName}.

Our AI is analyzing your business right now. Your custom report will be ready within 24 hours.

In the meantime, here's what to expect:
- Automation Opportunity Map
- Estimated ROI & Monthly Savings
- Recommended AI Agents
- Implementation Timeline

Talk soon,
Axovion Team
```

### 2. Audit Report Ready
**Trigger:** Report generated
**Delay:** Immediate
**Subject:** "Your AI Audit Report is ready — {businessName}"
```
Hi {name},

Great news — your AI Audit report is ready.

[View Your Report] (link to interactive report)

Top finding: You could save approximately {monthlySavings}/month by automating {topOpportunity}.

Want to discuss implementation? Book a free call:
[Book Consultation] (Calendly link)

Best,
Axovion Team
```

### 3. No Report Open (Follow-up)
**Trigger:** Report delivered, not viewed after 24h
**Delay:** 24 hours
**Subject:** "Did you see your AI Audit results?"
```
Hi {name},

I sent your AI Audit report yesterday but noticed you haven't opened it yet.

Your top automation opportunity alone could save {monthlySavings}/month.

[View Report] — takes 2 minutes

Questions? Just reply to this email or book a call.
```

### 4. Post-Call Follow-Up
**Trigger:** Consultation call completed
**Delay:** 1 hour
**Subject:** "Next steps after our call — Axovion.io"
```
Hi {name},

Thanks for the call today. As discussed, here's what happens next:

[Custom next steps from call]

[Accept Proposal] or [Book Implementation Kickoff]

Excited to get started,
Axovion Team
```

### 5. Newsletter (Weekly)
**Trigger:** Manual or scheduled
**Content:** AI automation tips, case studies, new features

## Implementation

### Backend Setup
```js
// Using Resend
import { Resend } from 'resend';
const resend = new Resend(process.env.RESEND_API_KEY);

await resend.emails.send({
  from: 'Axovion <audit@axovion.io>',
  to: lead.email,
  subject: 'Your AI Audit Report is ready',
  html: generateEmailTemplate('report-ready', variables),
});
```

### Email Templates
- Build reusable template system
- Variables: name, businessName, monthlySavings, topOpportunity, reportLink, calendlyLink
- Branded with Axovion colors and logo

### Queue / Scheduler
- Use node-cron or bull queue for delayed emails
- Store scheduled emails in database
- Cancel sequences if user books call or replies

## Database
```js
// EmailLog schema
{
  auditId: ObjectId,
  template: String,
  subject: String,
  sentAt: Date,
  openedAt: Date,
  clickedAt: Date,
  status: String
}
```

## API Endpoints
```
POST /api/emails/send        — Send single email
POST /api/emails/sequence    — Start email sequence
GET  /api/emails/logs        — List email logs
```

## Admin Dashboard
- Email logs table
- Open/click rates per template
- Manual send option

## DNS Setup
- SPF, DKIM, DMARC records for axovion.io
- Improves deliverability
