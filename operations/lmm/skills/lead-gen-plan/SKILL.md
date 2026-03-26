# Lead Gen Plan

## Command
`/lead-gen-plan <client_name> [--vertical roofing|hvac|landscaping|gym]`

## Purpose
Generate a complete lead generation strategy for a client: campaign structure, keyword direction, landing page direction, budget allocation, and follow-up plan. The output is the single source of truth before anything gets built.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| client_name | string | Yes | Client business name |
| --vertical | string | No | Business type. Auto-detected from intake if omitted. |

## Output
Genre: strategy-brief | Format: Markdown

1. **Market Analysis** — competitive landscape, search volume estimates, seasonal patterns
2. **Campaign Structure** — recommended campaigns, ad groups, keyword themes
3. **Budget Allocation** — daily split across campaigns
4. **Landing Page Direction** — headline, offer, CTA, trust signals
5. **Follow-Up System Summary** — lead response sequence overview
6. **30-Day Projections** — estimated clicks, leads, CPL

## Agent Activation
1. **strategist** (wave 1): Intake review, market analysis, strategy framework
2. **ad-creator** (wave 2): Campaign structure and keyword direction
3. **funnel-builder** (wave 2): Landing page direction
4. **automation** (wave 2): Follow-up sequence summary
5. **strategist** (wave 3): Compile into unified plan with projections

## Process
```
1. Confirm all 10 intake fields are complete (strategist requests if missing)
2. Strategist produces market analysis and strategy framework
3. Ad creator adds campaign structure + keyword direction
4. Funnel builder adds landing page direction
5. Automation adds follow-up sequence summary
6. Strategist compiles unified plan with 30-day projections
7. Deliver complete plan — ready to hand to the build team
```

## Examples
```
/lead-gen-plan "Apex Roofing"
/lead-gen-plan "Cool Air HVAC" --vertical hvac
/lead-gen-plan "Green Lawn Landscaping" --vertical landscaping
```
