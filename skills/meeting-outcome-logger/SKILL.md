---
name: meeting-outcome-logger
description: Structures what happened in a customer meeting into a CRM-ready activity record with outcome classification, sentiment assessment, next steps, and follow-up triggers. Bridges the gap between "the meeting happened" and "the system knows what happened." Use when asked to log a meeting outcome, create a CRM activity record, document what happened in a call, classify a meeting result, or when any customer interaction needs to be recorded in a structured format for downstream use. Also triggers for questions about meeting documentation, activity logging, CRM record creation, or structured meeting capture.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Meeting Outcome Logger

Structures a customer meeting into a CRM-ready record. Different from the call summary generator (which extracts discussion points and action items from notes) -- this skill classifies the meeting outcome, assesses sentiment, and produces a structured record optimised for CRM logging and downstream reporting.

The gap this fills: most CSMs either skip CRM logging entirely (too time-consuming) or write a sentence that does not capture enough for anyone else to act on. This skill makes logging take 2 minutes instead of 10 and produces a record that is genuinely useful.

## How to Use

After a customer meeting, provide:
- Account name and meeting type (check-in, QBR, escalation, onboarding, renewal, ad hoc)
- Attendees (customer and internal)
- Duration
- What happened (brief description -- a few sentences or bullet points)
- What was decided or agreed
- What actions were committed (by you and by them)
- How the customer seemed (positive, neutral, frustrated, disengaged, enthusiastic)
- Anything that changed about the account status (new risk, new opportunity, new stakeholder, resolved issue)

## Outcome Classification

Every meeting produces one of these outcomes. The classification drives downstream workflows:

| Outcome | Definition | Downstream Trigger |
|---------|-----------|-------------------|
| Positive progress | Meeting advanced the relationship or a specific initiative. Customer engaged, actions agreed | Log activity. Update health trajectory if warranted |
| Status quo | Routine touchpoint. No significant change in either direction | Log activity. Standard cadence continues |
| Concern surfaced | Customer raised an issue, frustration, or risk signal during the meeting | Log activity. Flag for risk assessment. CSM to investigate |
| Escalation needed | Issue identified that requires internal team involvement | Log activity. Trigger escalation workflow |
| Expansion signal | Customer expressed interest in growth (more users, higher tier, new use case) | Log activity. Flag expansion opportunity |
| Relationship repair | Meeting addressed a prior issue. Trust rebuilding in progress | Log activity. Update risk status if improving |
| Customer disengaged | Customer was present but minimally engaged. Short answers, low energy, delegation | Log activity. Flag as engagement risk. CSM to assess |
| Commitment made | Specific commercial or operational commitment from either side | Log activity. Create commitment record for tracking |
| No-show | Customer did not attend the scheduled meeting | Log no-show. Flag for CSM follow-up. If repeat pattern, flag as engagement risk |

## Sentiment Capture

Beyond the outcome classification, capture the emotional tone:

| Sentiment | Indicators | What It Means for the Account |
|-----------|-----------|------------------------------|
| Enthusiastic | Volunteered positive feedback, discussed expansion, asked about new features, forward-looking language | Strong health signal. Potential advocacy candidate. Look for expansion timing |
| Satisfied | Professional, engaged, answered questions fully, no complaints | Healthy baseline. Standard management |
| Neutral | Transactional, brief answers, no strong signal in either direction | Not a problem yet, but not building momentum either. Monitor for drift |
| Concerned | Raised specific issues, asked pointed questions about timelines or commitments, referenced alternatives | Early risk signal. Address the concerns before they become decisions |
| Frustrated | Expressed dissatisfaction directly, referenced prior failures, impatient with answers | Active risk signal. Escalate if not already addressed. Do not wait for the next meeting |
| Disengaged | Short meeting, minimal contribution, delegated to a junior person, cancelled or shortened the meeting | Relationship cooling signal. This is often a leading indicator of churn -- the customer stops caring before they stop paying |

## CRM Record Format

```
## Meeting Record: [Account Name]
**Date:** [date] | **Type:** [meeting type] | **Duration:** [minutes]

**Attendees:**
- Customer: [names, roles]
- Internal: [names, roles]

**Outcome:** [classification from above]
**Sentiment:** [assessment from above]

**Summary:** [2-4 sentences capturing what was discussed and concluded]

**Decisions Made:**
- [Decision 1]
- [Decision 2]

**Action Items:**
| Action | Owner | Deadline |
|--------|-------|----------|
| [action] | [owner] | [date] |

**Account Status Change:** [None / New risk: [detail] / New opportunity: [detail] / Issue resolved: [detail]]

**Next Touchpoint:** [Date and type]

**Internal Notes (not customer-visible):**
[Anything the CSM observed that should not be in the customer-facing record: political dynamics, competitor mentions, relationship concerns, stakeholder observations]
```

## What Makes This Different from Just Writing Notes

The structured format ensures:
1. **Outcome classification** drives downstream workflows automatically -- a "concern surfaced" outcome can trigger a risk review without the CSM manually flagging it
2. **Sentiment tracking** over time reveals trends invisible in individual meetings. A customer who moved from "enthusiastic" to "neutral" to "concerned" over three meetings is on a trajectory, even if each individual meeting seemed fine
3. **Action items with owners and deadlines** prevent the "we discussed it but nobody did it" pattern
4. **Internal notes** separate what the customer should see from what the CSM observed -- political dynamics, competitive mentions, and relationship assessments do not belong in a customer-visible record
5. **Consistency** makes reporting meaningful. If every CSM logs meetings the same way, portfolio-level reporting (engagement health, outcome distribution, sentiment trends) becomes reliable

## Quality Gates

- Is the outcome classification honest? "Positive progress" should mean actual progress, not just a pleasant conversation. If nothing advanced, it is "status quo" -- and that is fine
- Does the sentiment match what you observed, not what you hope? Optimistic sentiment logging is the most common data quality problem in CS. "Satisfied" should mean they expressed satisfaction, not that they did not complain
- Are action items specific with owners and deadlines? "Follow up" is not an action item. "Send API documentation to Lisa Park by Friday March 14" is
- Are internal notes genuinely useful? If you would not want your manager or successor to read them, they should not be there. If they contain context that would help your manager or successor, they should be there
- Would this record allow another CSM to understand what happened without asking you? That is the bar. If your notes are only useful to you, they are not CRM-ready

## Principles

- Log the meeting within 1 hour while the memory is fresh. Meeting records written the next day lose nuance and accuracy. Meeting records written a week later are fiction
- The outcome and sentiment classifications are more valuable than the narrative. Narratives are read once. Classifications aggregate into portfolio-level data that reveals patterns across hundreds of meetings
- Every no-show is a data point. Do not skip logging no-shows. They are engagement signals that compound -- one no-show is noise, three no-shows is a pattern, five no-shows is a risk
- Internal notes are for context, not for venting. "Customer was rude" is venting. "Customer was visibly frustrated about the unresolved API issue -- approached the conversation defensively and was not receptive to the adoption discussion I planned" is context that helps the next person engage effectively
