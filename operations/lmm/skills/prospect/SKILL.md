# Prospect

## Command
`/prospect <city> <vertical> [--limit 10|20|30]`

## Purpose
Search the web to find local service businesses in a target city and vertical.
Score each one against the LMM ICP. Return a ranked, ready-to-action prospect list
with outreach angles. Output goes directly to the outreach agent.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| city | string | Yes | Target city (e.g., "Grand Rapids") |
| vertical | string | Yes | roofing / hvac / landscaping / gym |
| --limit | integer | No | Max prospects to return. Default: 10 |

## Output
Genre: prospect-list | Format: Markdown

1. **Tier 1 Prospects** — ICP score 7-8, flagged for immediate outreach
2. **Tier 2 Prospects** — ICP score 5-6, outreach this week
3. **Next Steps** — which prospects to run `/outreach-message` for first

## Agent Activation
1. **prospector** (wave 1): Web search, data collection, ICP scoring, list output
2. **outreach** (wave 2): Generates messages for all Tier 1 prospects

## Process
```
1. Prospector runs web search queries for city + vertical combination
2. Collects: name, owner, phone, email, website, reviews, ads status, social
3. Scores each business against 8-point ICP rubric
4. Ranks into Tier 1 / Tier 2 / Tier 3
5. Flags Tier 1 prospects to outreach agent immediately
6. Outreach agent generates a personalized message for each Tier 1 prospect
7. Delivers combined output: prospect list + ready-to-send messages
```

## Examples
```
/prospect "Grand Rapids" roofing
/prospect "Kalamazoo" hvac --limit 20
/prospect "Lansing" landscaping
/prospect "Muskegon" gym --limit 5
```

## Notes
- Cross-check against existing pipeline before adding any prospect
- Tier 1 prospects get an outreach message generated automatically
- Run this weekly per city/vertical to keep the pipeline full
