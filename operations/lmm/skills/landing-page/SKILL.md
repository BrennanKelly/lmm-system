# Landing Page

## Command
`/landing-page <client_name> [--service <service_type>]`

## Purpose
Generate complete landing page copy and structure for a specific client and service. All copy is written — no placeholders. Output hands directly to a web builder.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| client_name | string | Yes | Client business name |
| --service | string | No | Specific service. Uses primary service if omitted. |

## Output
Genre: page-copy | Format: Markdown

1. **Header** — phone number placement, trust badge
2. **Hero Section** — headline, sub-headline, CTA button, background photo direction
3. **Trust Bar** — 4 trust signals
4. **Benefits Section** — 3 named benefits with full copy
5. **Social Proof** — 3 customer review templates
6. **Lead Form** — fields, CTA copy, confirmation message
7. **Footer** — business info, service area, licensing

## Agent Activation
1. **strategist** (wave 1): Confirm offer, geography, and target audience from strategy brief
2. **funnel-builder** (wave 1): Write complete page copy per LMM landing page formula

## Process
```
1. Confirm strategy brief exists (offer, geography, audience)
2. Funnel builder writes all sections per LMM formula
3. Funnel builder adds mobile-first notes (CTA placement, form length)
4. Deliver complete page spec with copy + build instructions
```

## Examples
```
/landing-page "Apex Roofing"
/landing-page "Cool Air HVAC" --service "AC Repair"
/landing-page "Green Lawn Landscaping" --service "Lawn Maintenance"
```
