# Axovion.io — Advanced Admin Dashboard Build Instructions

## Overview
Upgrade the MVP dashboard with full task management, analytics, and team collaboration features.

## New Sections

### 1. Task Manager
- Kanban board: To Do → In Progress → Review → Done
- Tasks linked to audits, chats, or general
- Assign tasks to team members
- Due dates, priorities, labels
- Drag-and-drop

### 2. Analytics
- Website traffic: visitors, unique visitors, bounce rate
- Conversion funnel: Visit → Audit → Report Open → Booking
- Top traffic sources
- Device breakdown
- Time on site

### 3. Lead Scoring
- Auto-score leads based on:
  - Monthly revenue (higher = better)
  - Budget
  - Industry match
  - Engagement (chat, email opens, report views)
- Color-coded: Hot (red), Warm (orange), Cold (blue)

### 4. Team Management
- Add team members
- Role-based access (admin, sales, developer)
- Activity logs per user

### 5. Settings
- Business info
- Email templates editor
- Chatbot behavior config
- Calling agent settings
- Integration configs (Calendly, Vapi, etc.)

### 6. Notifications
- Real-time alerts for new audits, bookings, high-value leads
- Browser push notifications
- Email digests (daily/weekly)

## Design
- Sidebar navigation with icons
- Top bar: search, notifications, profile
- Dashboard widgets: draggable, resizable
- Dark theme consistent with main site

## Tech
- React + Tailwind
- Recharts or Chart.js for analytics
- React DnD for kanban
- WebSockets or polling for real-time updates

## Database Updates
```js
// Task schema
{
  title: String,
  description: String,
  status: { type: String, enum: ['todo', 'in-progress', 'review', 'done'] },
  priority: { type: String, enum: ['low', 'medium', 'high', 'urgent'] },
  assignee: ObjectId,
  relatedAudit: ObjectId,
  dueDate: Date,
  labels: [String],
  createdAt: Date
}

// ActivityLog schema
{
  user: ObjectId,
  action: String,
  entity: String,
  entityId: ObjectId,
  details: Object,
  createdAt: Date
}
```

## API Endpoints
```
Tasks:
GET    /api/tasks
POST   /api/tasks
PUT    /api/tasks/:id
DELETE /api/tasks/:id

Analytics:
GET /api/analytics/traffic
GET /api/analytics/conversions
GET /api/analytics/sources

Team:
GET    /api/team
POST   /api/team
DELETE /api/team/:id

Settings:
GET  /api/settings
PUT  /api/settings
```
