# Axovion.io — AI Calling Agent Integration Build Instructions

## Overview
Add voice AI calling to follow up with high-value leads after audit submission.

## Providers
Primary: **Vapi** or **Retell**
Fallback: **Go High Level** (if you want to keep everything in one ecosystem)

## Flow

### 1. Trigger Conditions
- Audit submitted with monthly revenue > $50K OR budget > $5K
- OR user explicitly requests a call in chatbot
- Delay: 2 hours after audit report delivery (or immediately if requested)

### 2. Call Script (Dynamic)
```
"Hi {name}, this is {agentName} from Axovion.io. 
I saw you submitted an AI Audit for {businessName}. 
Our analysis found that you could save approximately {monthlySavings} per month 
by automating {topOpportunity}. 
I'd love to walk you through the report and answer any questions. 
Do you have 15 minutes this week for a quick call?"
```

### 3. Call Outcomes
- **Booked**: Log to dashboard, send calendar invite
- **Not interested**: Log reason, stop follow-up
- **Voicemail**: Leave callback number, schedule retry
- **No answer**: Retry up to 2 times (24h, 72h)

### 4. Dashboard Integration
- New section: "Calling Campaigns"
- Table: lead, phone, status, call time, outcome, recording link
- Actions: trigger call, listen recording, mark as contacted

## Vapi Setup
1. Create account at vapi.ai
2. Create voice assistant with script template
3. Add variables: name, businessName, monthlySavings, topOpportunity
4. Connect phone number (buy via Vapi or bring your own)
5. API call to trigger outbound:
```js
const call = await vapi.calls.create({
  assistantId: 'your-assistant-id',
  customer: { number: '+1234567890', name: 'John' },
  assistantOverrides: {
    variableValues: {
      name: 'John',
      businessName: 'Acme Inc',
      monthlySavings: '$5,000',
      topOpportunity: 'customer support automation'
    }
  }
});
```

## Retell Setup
Similar flow. Retell has good dashboard for call analytics.

## Go High Level Setup
If using GHL:
- Build workflow in GHL
- Webhook from your backend triggers GHL workflow
- Pass variables via webhook
- GHL handles calling via its AI features

## Database
```js
// CallLog schema
{
  auditId: ObjectId,
  leadName: String,
  phone: String,
  provider: String, // 'vapi', 'retell', 'ghl'
  status: { type: String, enum: ['scheduled', 'in-progress', 'completed', 'failed', 'no-answer'] },
  outcome: String,
  recordingUrl: String,
  transcript: String,
  scheduledAt: Date,
  completedAt: Date,
  retryCount: Number
}
```

## API Endpoints
```
POST /api/calls/trigger      — Trigger outbound call
GET  /api/calls              — List call logs
GET  /api/calls/:id          — Get call details + recording
POST /api/calls/webhook      — Receive provider webhooks
```

## Webhook Handling
Providers send webhooks for call events:
- call.started
- call.completed
- call.failed

Update dashboard in real-time.

## Design
- Simple table in admin dashboard
- Play button for recordings
- Status badges (color-coded)

## Cost Note
- Vapi: ~$0.05/minute
- Retell: similar pricing
- Budget for ~100 calls/month initially
