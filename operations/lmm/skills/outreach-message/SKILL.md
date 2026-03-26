# Outreach Message

## Command
`/outreach-message <prospect_name> [--channel email|dm|linkedin] [--step 1|2|3|4|5]`

## Purpose
Generate a personalized outreach message for a local service business prospect using the SPOT framework (Specific → Problem → Outcome → Trigger). Every message references something real about their business. Output is ready to copy and send.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| prospect_name | string | Yes | Business name or owner name |
| --channel | string | No | Default: dm |
| --step | integer | No | Which step in the 12-day sequence. Default: 1 |

## Output
Genre: outreach-message | Format: Plain text

1. **Prospect Summary** — ICP score, key observations, recommended angle
2. **Message** — complete, ready-to-send for the specified channel and step
3. **Next Step** — what to do after sending (timing, follow-up channel)

## Agent Activation
1. **outreach** (wave 1): Research prospect, score ICP, write SPOT message

## Process
```
1. Outreach agent reviews available prospect info (business, vertical, location, online presence)
2. Score against 8-point ICP framework
3. Identify best outreach angle (what to observe, what gap to highlight)
4. Write SPOT message for specified channel and step
5. Deliver message + next step in sequence
```

## Examples
```
/outreach-message "Apex Roofing Grand Rapids"
/outreach-message "Cool Air HVAC" --channel email --step 2
/outreach-message "Green Lawn Landscaping" --channel linkedin
```
