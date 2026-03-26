# GoHighLevel Reference Guide

> Defines how LMM uses GoHighLevel for every client.
> Load when building any automation, workflow, or CRM setup.

---

## Account Structure

```
LMM Agency Account (master)
├── Sub-account: Apex Roofing — Grand Rapids
├── Sub-account: Cool Air HVAC — Kalamazoo
├── Sub-account: Green Lawn Landscaping — Lansing
└── Sub-account: LMM — Internal (for LMM’s own leads)
```

Each client gets their own sub-account. LMM controls all accounts from the agency dashboard.

---

## Standard Pipeline: "{Client} — Leads"

| Stage | Definition | Automation Triggered |
|-------|-----------|---------------------|
| **New Lead** | Form submitted, not contacted | Immediate SMS + owner alert |
| **Contacted** | Outreach sent, awaiting reply | Day 1 SMS follow-up |
| **Appointment Set** | Call or visit scheduled | 24hr + 2hr reminders |
| **Estimate Given** | Quote delivered to prospect | 2-day follow-up email |
| **Won** | Job booked | Move to “Active Client” pipeline |
| **Lost** | Not moving forward | Log reason, add to 90-day nurture |
| **Nurture** | Not ready now | 14-day and 28-day re-engagement |

---

## Custom Contact Fields (Add to Every Sub-Account)

| Field Name | Type | Purpose |
|------------|------|--------|
| Service Requested | Text | What they asked about |
| Lead Source | Dropdown | Which landing page or ad |
| Estimated Job Value | Currency | For pipeline value tracking |
| Appointment Date | Date | For reminder workflows |
| Owner Called | Checkbox | Did the owner call within 5 min? |
| Lead Quality | Dropdown (Hot/Warm/Cold) | Owner rates after first contact |

---

## Standard Workflows Per Client

### 1. New Lead — Immediate Response
- **Trigger**: Form submission (webhook from landing page)
- **Actions**:
  1. Send SMS to contact (< 2 min)
  2. Send email notification to business owner
  3. Create opportunity in “New Lead” stage
  4. Wait 1 hour → if no stage change → send Email 1
  5. Wait to Day 1 6pm → if no reply → send SMS 2
  6. Wait to Day 2 → send Email 2
  7. Wait to Day 4 → send SMS 3
  8. Wait to Day 7 → send SMS 4 + Email 3
- **Stop condition**: Contact replies OR stage moves to Appointment Set or Won

### 2. Appointment Reminders
- **Trigger**: Opportunity moves to “Appointment Set” stage
- **Actions**:
  1. Wait until 24 hours before appointment time → SMS reminder
  2. Wait until 2 hours before → SMS with address confirmation

### 3. Post-Estimate Follow-Up
- **Trigger**: Opportunity moves to “Estimate Given” stage
- **Actions**:
  1. Wait 2 days → SMS: “Hey {name}, just checking in on the estimate we sent. Any questions?”
  2. Wait 5 days → Email: “Still thinking it over?” with a review or case study

### 4. Long-Term Nurture
- **Trigger**: Opportunity moved to “Nurture” stage
- **Actions**:
  1. Wait 14 days → SMS check-in
  2. Wait 14 more days → Email re-engagement
  3. Continue every 30 days until opt-out or conversion

---

## GHL → Google Ads Conversion Tracking

For every client:
1. Create a GHL phone number (call tracking)
2. Add to Google Ads as a call extension
3. Track calls >= 60 seconds as conversions in Google Ads
4. Connect landing page form to GHL via webhook
5. Fire a Google Ads conversion event on form submission

This gives us two conversion signals:
- Form submissions (via webhook → GHL → Google tag)
- Phone calls (via GHL call tracking number → Google Ads)

---

## Reporting Setup

For each client, configure a GHL dashboard with:
- Total leads this month
- Leads by source (which campaign / landing page)
- Pipeline value by stage
- Appointment show rate
- Won / Lost ratio

Share dashboard link with client so they have live visibility.

---

## Day 1 Setup Order

When a new client signs:

```
1. Create GHL sub-account
2. Add custom fields
3. Create pipeline stages
4. Set up call tracking number
5. Connect landing page form via webhook
6. Build New Lead workflow
7. Build Appointment Reminder workflow
8. Submit test lead — verify all steps fire
9. Add client as user (view access)
10. Brief owner: "You must call leads within 5 minutes of getting the alert"
```

---

## GHL Variables Reference

Use these in all workflow copy:

| Variable | What It Inserts |
|----------|----------------|
| `{{contact.first_name}}` | Lead’s first name |
| `{{contact.full_name}}` | Full name |
| `{{contact.phone}}` | Lead’s phone number |
| `{{contact.email}}` | Lead’s email |
| `{{contact.service_requested}}` | Custom field: service type |
| `{{opportunity.name}}` | Opportunity name |
| `{{appointment_time}}` | Scheduled appointment time |
| `{{business_name}}` | Set in sub-account settings |
| `{{business_phone}}` | Set in sub-account settings |
| `{{owner_name}}` | Set as a custom value in the sub-account |
