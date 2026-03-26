# Follow-Up Sequence

## Command
`/follow-up-sequence <client_name> [--type lead|appointment|reengagement]`

## Purpose
Build a complete SMS + email follow-up sequence for a client's leads. All copy is written and ready to load into GoHighLevel, HubSpot, or any CRM. No placeholders — every message is ready to send.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| client_name | string | Yes | Client business name |
| --type | string | No | Sequence type. Default: lead |

## Output
Genre: follow-up-sequence | Format: Markdown

1. **Immediate Response** (0–5 min) — SMS to lead + email alert to business owner
2. **SMS Sequence** — 4 messages with exact timing and copy
3. **Email Sequence** — 3 emails with subject lines and full body copy
4. **Appointment Reminders** — 24hr and 2hr SMS reminders
5. **Implementation Notes** — field variables, stop conditions, CRM setup steps

## Agent Activation
1. **strategist** (wave 1): Confirm client details (business name, owner, phone, service)
2. **automation** (wave 1): Write complete sequence with all copy

## Process
```
1. Confirm client intake data (business name, owner, phone, service type)
2. Automation writes all 4 SMS messages with timing
3. Automation writes all 3 emails with subjects and full copy
4. Automation writes appointment reminder messages
5. Automation adds implementation notes and stop conditions
6. Deliver complete sequence spec ready for CRM implementation
```

## Examples
```
/follow-up-sequence "Apex Roofing"
/follow-up-sequence "Cool Air HVAC" --type appointment
/follow-up-sequence "Green Lawn Landscaping" --type reengagement
```
