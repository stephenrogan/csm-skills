---
name: stakeholder-map-builder
description: Builds a structured map of customer stakeholders with roles, influence levels, engagement status, and relationship strategy per contact. Identifies coverage gaps and single-thread risk. Use when asked to map stakeholders, build an org chart, assess relationship coverage, identify single-thread risk, plan stakeholder engagement, or when a CSM needs to understand who matters at an account and where the relationship gaps are. Also triggers for questions about stakeholder mapping, contact assessment, org chart analysis, relationship coverage, multi-threading assessment, or who to engage at a customer account.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Stakeholder Map Builder

Builds a structured view of who matters at a customer account, how strong your relationship is with each person, and where the gaps are. The most common preventable churn pattern is single-threaded accounts where the champion leaves. This skill makes that risk visible before it materialises.

## How to Use

Provide for each known contact:
- Name, title, function
- Their relationship to the product (champion, user, economic buyer, decision-maker, blocker)
- Your relationship strength (strong, adequate, weak, none)
- Last engagement (when you last spoke and through what channel)
- Their sentiment (advocate, supportive, neutral, sceptical, detractor)
- Any notes (political context, personal preferences, upcoming changes)

Also provide:
- Account ARR and segment
- Renewal date
- Any known gaps (people you know exist but have not engaged)

## Stakeholder Classification

| Type | Definition | Why They Matter | Priority |
|------|-----------|----------------|----------|
| Champion | Actively advocates for the product. Goes to bat for you internally | If they leave, the relationship is at immediate risk. Your most important contact | Critical -- always engaged |
| Economic Buyer | Controls or directly influences the budget decision | If not engaged, the renewal is decided by someone you have never spoken to | Critical -- engage before renewal |
| Decision Maker | Has final authority on the renewal or expansion decision | May be the same as Economic Buyer or may be different (CEO, board, procurement) | High -- at least one touchpoint before any commercial conversation |
| Technical Lead | Owns the implementation and day-to-day technical relationship | If frustrated with the product, technical issues escalate and adoption stalls | Medium -- engage on product-related topics |
| End User Champion | Uses the product daily and advocates to their peers | Their enthusiasm drives organic adoption. Their frustration spreads just as fast | Medium -- recognise and support |
| Executive Sponsor | Senior leader who provides strategic air cover for the investment | If unaware of value being delivered, the budget is vulnerable in prioritisation discussions | High -- quarterly engagement minimum |
| Influencer | Does not decide but shapes opinions | An unmanaged negative influencer can poison the relationship without the CSM knowing | Varies -- identify and monitor |
| Detractor | Actively opposed to the product or the relationship | Must be identified and addressed, not ignored. Detractors who are unmanaged become the voice the buyer hears | High -- engage deliberately |

## The Map

```
## Stakeholder Map: [Account Name]
**Date:** [date] | **ARR:** EUR [amount] | **Renewal:** [date]

### Active Contacts
| Name | Title | Type | Relationship | Last Touch | Sentiment | Notes |
|------|-------|------|-------------|-----------|-----------|-------|
| Tom Chen | VP Engineering | Champion | Strong | Mar 1 (call) | Advocate | Primary relationship. Drives internal adoption |
| Sarah Kim | CFO | Economic Buyer | Weak | Dec 15 (QBR) | Neutral | Met once. Has not engaged since. Critical gap |
| Lisa Park | Eng Manager | Technical Lead | Adequate | Mar 5 (email) | Supportive | Responsive. Handles day-to-day |

### Known But Not Engaged
| Name/Role | Type | Why Not Engaged | Priority |
|-----------|------|----------------|----------|
| CTO (name unknown) | Executive Sponsor | Never identified or introduced | High -- need executive coverage |
| Operations Manager | Potential user | Product is used in Engineering only. Operations could benefit | Medium -- expansion opportunity |

### Coverage Assessment
| Coverage Dimension | Status | Risk |
|-------------------|--------|------|
| Champion | ✓ Active (Tom) | Low -- but single-threaded to one champion |
| Economic Buyer | ⚠ Gap (Sarah not engaged) | High -- renewal decision at risk |
| Executive Sponsor | ✗ Missing | Medium -- no strategic air cover |
| Breadth (departments) | ⚠ Narrow (Engineering only) | Medium -- a reorg in Engineering could sever the entire relationship |
| Depth (levels) | ⚠ Thin (VP + Manager, no C-level) | Medium -- no board-level awareness of value |

### Single-Thread Risk
[Assessment: is this account dependent on one person? If yes, what is the mitigation plan?]

### Multi-Threading Plan
| Target Contact | Path to Engagement | First Action | Timeline |
|---------------|-------------------|-------------|---------|
| Sarah Kim (CFO) | Through Tom (champion introduction) | Ask Tom to facilitate a brief ROI discussion | This month |
| CTO | Through Tom or Sarah | Identify name and role first. Then propose executive alignment meeting | This quarter |
```

## Risk Scoring

| Factor | Score | Rationale |
|--------|-------|-----------|
| Only 1 active contact | High risk | Any disruption to that person strands the relationship |
| No economic buyer engaged | High risk | Renewal will be decided without your input |
| No executive sponsor | Medium risk | Investment lacks strategic protection |
| All contacts in one department | Medium risk | Departmental reorg could sever the entire relationship |
| Active detractor exists with no engagement strategy | Medium risk | Unmanaged detractors become louder over time |
| 3+ active contacts across levels and functions | Low risk | Relationship is broad and resilient |

## Quality Gates

- Is every contact classified by type (not just by title)? A VP can be a champion, an economic buyer, or a detractor. The title tells you their level. The type tells you their role in the relationship
- Is the economic buyer identified? If you do not know who controls the budget, the most critical gap is finding out
- Is the single-thread risk assessed honestly? If losing one person would put the account at risk, that risk needs to be documented and addressed
- Does the multi-threading plan have specific actions with timelines? "Engage more people" is not a plan. "Ask Tom to introduce me to Sarah at the next QBR on April 15" is

## Principles

- The stakeholder map is a living document, not a one-time exercise. Contacts change roles, leave, and shift sentiment. Review the map quarterly and update it after any significant change
- Your champion is not your only relationship. They are your most important relationship and the bridge to every other relationship at the account. Use the champion to build breadth, not as a substitute for it
- The economic buyer is always the highest-priority gap. You can survive without an executive sponsor. You can manage without broad departmental coverage. You cannot renew without the person who controls the budget
- Every gap in the map is a bet. You are betting that the person you have not engaged will not become the decisive voice in the next renewal, escalation, or competitive evaluation. Sometimes that bet pays off. Often it does not
