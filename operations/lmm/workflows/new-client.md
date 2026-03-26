# New Client Workflow

> Run every time a new client signs with LMM.
> Goal: campaign live within 7 days of signing.

## Overview

```
Intake → Strategy → Build Ads → Build Landing Page → Build Follow-Up → Launch → Week 1 Review
```

---

## Phase 1: Intake

- **Owner**: strategist
- **Duration**: Day 1 (within 24 hours of signing)
- **Evidence gate**: All 10 intake fields complete

### Checklist
- [ ] Business name and owner name
- [ ] Service type and primary service to advertise
- [ ] Service area (cities, zip codes, or radius)
- [ ] Average job value ($)
- [ ] Monthly ad budget
- [ ] Current lead sources
- [ ] Top 3 local competitors
- [ ] Phone number and preferred contact method
- [ ] Existing Google Ads history + account access (if any)
- [ ] Google Business Profile URL + review count

### Deliverable
Completed intake doc — all 10 fields populated. Passed to strategist to begin Phase 2.

---

## Phase 2: Strategy

- **Owner**: strategist
- **Duration**: Day 1–2
- **Evidence gate**: Strategy brief reviewed and approved by LMM owner

### Process
1. Run `/lead-gen-plan <client_name>` to generate full strategy
2. Review 30-day projections and adjust budget allocation if needed
3. Finalize offer and CTA to use across ads and landing page
4. Get client confirmation on offer and budget before building

### Deliverable
`client-strategy-brief.md` — campaign structure, daily budgets, offer, landing page direction, follow-up summary

---

## Phase 3: Build Ads

- **Owner**: ad-creator
- **Duration**: Day 2–3
- **Evidence gate**: Campaign built in Google Ads, reviewed by strategist

### Process
1. Run `/google-ads <client_name>` to generate campaign spec
2. Build campaigns in Google Ads Manager using spec
3. Implement all ad groups, keywords, RSAs, and extensions
4. Add negative keyword list from day 1
5. Set bidding strategy per strategist direction
6. Strategist reviews structure before launch

### Deliverable
Campaign built in Google Ads. Screenshot of structure sent to client.

---

## Phase 4: Build Landing Page

- **Owner**: funnel-builder
- **Duration**: Day 2–4
- **Evidence gate**: Page live, mobile-tested, conversion tracking confirmed

### Process
1. Run `/landing-page <client_name>` to generate page copy spec
2. Build page in client’s builder or LMM template
3. Connect form to CRM and notification system
4. Install Google Ads conversion tracking pixel
5. Mobile test: CTA above fold, phone number clickable, loads < 3 seconds
6. Strategist reviews before connecting to ad campaign

### Deliverable
Live landing page URL. Conversion tracking confirmed firing.

---

## Phase 5: Build Follow-Up System

- **Owner**: automation
- **Duration**: Day 3–5
- **Evidence gate**: Test lead submitted and full sequence triggers correctly

### Process
1. Run `/follow-up-sequence <client_name>` to generate sequence spec
2. Set up automation in client’s CRM (GoHighLevel / HubSpot / Jobber)
3. Configure immediate SMS trigger (< 2 min from form submission)
4. Build full SMS + email sequence with correct timing
5. Set up 24hr and 2hr appointment reminders
6. Submit test lead — verify every message fires correctly
7. Brief owner: "You need to call leads within 5 minutes"

### Deliverable
Working follow-up automation. Test lead proof. Client briefed on their role.

---

## Phase 6: Launch

- **Owner**: strategist
- **Duration**: Day 5–7
- **Evidence gate**: First click received within 24 hours of launch

### Launch Checklist
- [ ] Landing page URL connected to all ad campaigns
- [ ] Conversion tracking firing on form submissions and call clicks
- [ ] Google Ads campaigns set to Enabled
- [ ] Follow-up automation confirmed working
- [ ] Client notified: “We’re live — expect first leads within 24–48 hours”
- [ ] Week 1 review scheduled for Day 7

### Deliverable
Campaigns live. Client notified. Week 1 review on the calendar.

---

## Phase 7: Week 1 Review

- **Owner**: strategist
- **Duration**: Day 7–8
- **Evidence gate**: Report delivered to client

### Process
1. Pull data: impressions, clicks, CTR, conversions, CPL, spend
2. Review search terms report — add negatives for irrelevant queries
3. Check landing page CVR — if < 5%, flag to funnel-builder immediately
4. Check ad performance — pause ads with 0 clicks after 200+ impressions
5. Deliver Week 1 report to client

### Deliverable
Week 1 performance report. Any early optimizations implemented.
