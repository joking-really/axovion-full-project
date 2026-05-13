# Axovion.io — Services Detail Page Build Instructions

## Overview
Dedicated page explaining each service in depth. Linked from homepage bento grid cards.

## Route
`/services`

## Sections

### Hero
- Heading: "AI Automation Services"
- Sub: "End-to-end AI agent development for businesses ready to scale."
- Background: subtle gradient (no heavy animation, keep load fast)

### Service Cards (Expanded)
Each service gets a full card with:
- Icon (larger than homepage)
- Service name
- 2-3 sentence description
- What you get (bullet list)
- Ideal for (industry tags)
- "Get AI Audit" CTA button

Services to detail:
1. **Free AI Audit**
   - Workflow automation map
   - Estimated ROI and savings
   - Recommended AI agents
   - Live demo agent

2. **Customer Support Chatbots**
   - Website chatbot
   - WhatsApp business agent
   - Custom channel integrations
   - 24/7 instant response

3. **Lead Generation & Follow-Up**
   - Capture leads from any channel
   - Automated qualification
   - Persistent follow-up sequences
   - CRM sync

4. **Booking Automation**
   - Calendar integration
   - Reminder sequences
   - Rescheduling handling
   - No-show reduction

5. **E-Commerce Support**
   - Order tracking
   - Return/refund handling
   - Product recommendations
   - Cart abandonment recovery

6. **Abandoned Cart Recovery**
   - Multi-channel follow-up
   - Personalized messages
   - Discount offer logic
   - Revenue recovery tracking

7. **CRM & Email Automation**
   - HubSpot/Salesforce sync
   - Segmented email flows
   - Lead scoring
   - Pipeline automation

8. **AI Consulting & Strategy**
   - AI readiness assessment
   - Custom agent architecture
   - Team training
   - Ongoing optimization

### Process Section
- Reuse homepage flow diagram but expanded
- Add timeline estimates per step

### CTA
- "Not sure which service? Start with a Free AI Audit."
- Primary button: "Start Free AI Audit"

## Design
- Same dark luxury + AI-native feel
- Cards: surface background `#12121A`, radius 16px
- Hover: cyan glow border
- Icons: Lucide React, 48px

## Tech
- React component reuse from homepage
- Data-driven service list (array mapped to cards)
