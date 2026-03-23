---
name: book-prioritisation
description: Prioritises a CSM's full book of accounts into action tiers using a weighted scoring model that considers ARR, health, renewal proximity, engagement status, and strategic importance. Produces a ranked list with recommended time allocation. Use when asked to prioritise accounts, rank a portfolio, determine where to focus, triage a book, decide which accounts need attention first, or when a CSM feels overwhelmed and does not know where to start. Also triggers for questions about account prioritisation, portfolio triage, book ranking, time allocation across accounts, or how to decide which accounts matter most this week.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Book Prioritisation

Ranks your entire book of accounts by where your time creates the most value. Replaces the default behaviour of responding to whoever is loudest with a structured assessment of where your attention matters most.

## How to Use

Provide your book of accounts with whatever data you have per account:
- Account name, ARR
- Health status (strong, healthy, at risk, critical)
- Renewal date (or days to renewal)
- Last touchpoint date
- Engagement status (active, cooling, gap, dark)
- Any flags (escalation, expansion opportunity, champion departure, competitive signal)
- Strategic importance (reference account, logo value, board-level visibility)

## Scoring Model

Score each account on 5 dimensions (1-5 scale):

| Dimension | 1 (Low Priority) | 3 (Medium) | 5 (High Priority) | Weight |
|-----------|-----------------|-----------|-------------------|--------|
| Revenue at risk | Low ARR, healthy, renewal distant | Mid ARR or moderate risk | High ARR, at risk, or renewal imminent | 30% |
| Health trajectory | Improving or stable/strong | Stable/adequate | Declining or critical | 25% |
| Renewal proximity | 180+ days | 90-180 days | <90 days | 20% |
| Engagement gap | Active and responsive | Adequate but cooling | Dark or disengaged | 15% |
| Strategic value | Standard account | Moderate (reference, logo) | High (board-level, marquee logo, major expansion) | 10% |

**Priority score** = weighted sum (1.0-5.0)

### Priority Tiers

| Score | Tier | Action | Time Allocation |
|-------|------|--------|----------------|
| 4.0-5.0 | Tier 1: Immediate | Act this week. These accounts have the highest combination of risk and value | 40% of available time |
| 3.0-3.9 | Tier 2: Active | Act this month. Regular engagement, proactive management | 30% of available time |
| 2.0-2.9 | Tier 3: Monitor | Standard cadence. Engage on schedule or on signal | 20% of available time |
| 1.0-1.9 | Tier 4: Maintain | Light touch. Digital engagement. Engage only on trigger events | 10% of available time |

## Prioritisation Overrides

Some situations override the scoring model:

| Override Condition | Automatic Tier | Rationale |
|-------------------|---------------|-----------|
| Active escalation | Tier 1 | An unresolved escalation is immediate risk regardless of other scores |
| Champion departed in last 30 days | Tier 1 | Relationship continuity is at immediate risk |
| Competitive signal (active evaluation) | Tier 1 | Delay increases the probability of loss |
| Customer contacted you with a concern | Tier 1 (temporary) | Responsive engagement builds trust. Delayed response erodes it |
| New customer in onboarding | Tier 2 minimum | First 90 days set the relationship trajectory |

## Output Format

```
## Book Prioritisation: [CSM Name]
**Date:** [date] | **Accounts:** [total] | **ARR:** EUR [total]

### Tier 1: Immediate ([n] accounts, EUR [ARR])
| Rank | Account | ARR | Health | Renewal | Primary Driver | Action This Week |
|------|---------|-----|--------|---------|---------------|-----------------|
| 1 | [account] | EUR [x] | [status] | [days] | [why this is Tier 1] | [specific action] |

### Tier 2: Active ([n] accounts, EUR [ARR])
| Rank | Account | ARR | Health | Renewal | Action This Month |
|------|---------|-----|--------|---------|------------------|
| [entries] |

### Tier 3: Monitor ([n] accounts, EUR [ARR])
[Summarised -- these accounts are on standard cadence]

### Tier 4: Maintain ([n] accounts, EUR [ARR])
[Summarised -- these accounts are light touch]

### Time Allocation
| Tier | Accounts | ARR | % of Time | Hours/Week (est.) |
|------|----------|-----|----------|------------------|
| Tier 1 | [n] | EUR [x] | 40% | [hours] |
| Tier 2 | [n] | EUR [x] | 30% | [hours] |
| Tier 3 | [n] | EUR [x] | 20% | [hours] |
| Tier 4 | [n] | EUR [x] | 10% | [hours] |
```

## Quality Gates

- Is the prioritisation based on where your time creates the most value, not on which customers are loudest? The loudest customer is not always the most important. The scoring model surfaces the accounts where your attention has the highest revenue impact
- Does Tier 1 have a manageable number of accounts? If 15 of your 40 accounts are Tier 1, either the scoring needs recalibration or your portfolio has a structural problem
- Does every Tier 1 account have a specific action for this week? Prioritisation without action is just a ranked list. The action is the point
- Is the time allocation realistic? 40% of a 40-hour week is 16 hours for Tier 1 accounts. If Tier 1 has 8 accounts, that is 2 hours per account per week. Is that enough?

## Principles

- Prioritisation is a decision about what not to do. Every hour you spend on a Tier 3 account is an hour not spent on a Tier 1 account. Make the trade-off consciously, not by default
- Re-prioritise weekly. The book changes constantly: new escalations, resolved issues, approaching renewals, competitive signals. A prioritisation that is a week old is already partially stale
- Your highest-ARR accounts are not automatically your highest-priority accounts. A EUR 200k account that is healthy, well-threaded, and renewing in 10 months is lower priority than a EUR 50k account that is at risk and renewing in 30 days. ARR matters, but risk and timing matter more
- The goal is not to spend equal time on every account. It is to spend the right amount of time on each account based on the value and risk. Some accounts need 4 hours this week. Some need 10 minutes. Both are appropriate if the prioritisation is right
