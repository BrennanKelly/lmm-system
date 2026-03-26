# Google Ads Campaign

## Command
`/google-ads <client_name> [--campaign-type search|call-only]`

## Purpose
Build a complete, ready-to-implement Google Ads campaign spec: campaigns, ad groups, keywords, RSA ad copy, extensions, and negative keyword list. Output goes directly to a campaign manager to build in Google Ads.

## Arguments
| Arg | Type | Required | Description |
|-----|------|----------|-------------|
| client_name | string | Yes | Client business name |
| --campaign-type | string | No | Default: search |

## Output
Genre: campaign-spec | Format: Markdown

1. **Campaign Structure** — named campaigns with daily budgets and bidding strategies
2. **Ad Groups** — themed groupings with tight keyword sets
3. **Keywords** — exact and phrase match per ad group
4. **RSA Ad Copy** — 10-15 headlines + 4 descriptions per ad group (3 RSAs per group)
5. **Extensions** — call, location, sitelinks, callouts
6. **Negative Keyword List** — master list for the vertical

## Agent Activation
1. **strategist** (wave 1): Confirm strategy brief is complete
2. **ad-creator** (wave 1): Build full campaign spec

## Process
```
1. Confirm strategy brief exists (or request from strategist)
2. Ad creator builds campaign structure based on strategy brief
3. Ad creator writes all keyword lists (exact + phrase)
4. Ad creator writes RSA headlines and descriptions for each ad group
5. Ad creator adds extensions and negative keyword list
6. Deliver complete campaign spec ready for implementation
```

## Examples
```
/google-ads "Apex Roofing"
/google-ads "Cool Air HVAC" --campaign-type call-only
/google-ads "Premier Fitness Grand Rapids"
```
