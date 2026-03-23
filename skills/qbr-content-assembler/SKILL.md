---
name: qbr-content-assembler
description: Builds structured QBR deck content from manually provided account data including usage metrics, health indicators, support history, value evidence, and customer goals. Produces slide-by-slide content organised by segment template. Use when asked to build a QBR deck, prepare quarterly business review content, assemble QBR slides from data, create a customer review presentation, or when a CSM has data and needs it structured for a QBR. Also triggers for questions about QBR preparation, business review content, customer presentation assembly, or quarterly review slide creation.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# QBR Content Assembler

Builds QBR deck content from account data you provide. Give it the metrics, health indicators, support history, and goals -- it produces structured slide content ready to drop into a presentation template.

Distinct from the pre-call prep builder (which is a brief for you) -- this produces content for the customer. Every data point should be something you are comfortable presenting to the room.

## How to Use

Provide as much of the following as you have:

**Account basics:**
- Account name, ARR, product tier, contract tenure
- Primary contacts attending the QBR (names, roles)
- Customer's stated goals (from the success plan, onboarding, or prior QBRs)

**Usage and adoption data:**
- Active users and trend (growing, stable, declining)
- Key features used and not used
- Workflow completions or core use-case metrics
- Licence utilisation (active users vs. purchased seats)

**Health and engagement:**
- Overall health assessment (strong, healthy, at risk, critical)
- Recent touchpoints (calls, emails, meetings)
- Open items or outstanding commitments from either side

**Support history:**
- Ticket count, resolution time, open issues
- CSAT score if available
- Any escalations or notable support events

**Value evidence:**
- Time saved, productivity gains, or ROI metrics
- Customer-confirmed outcomes ("they told us X")
- Estimated value if no confirmed metrics exist

**Looking ahead:**
- Product roadmap items relevant to this customer
- Adoption opportunities (features they should be using but are not)
- Expansion signals or commercial context
- Risks or concerns to address

## Deck Templates by Segment

### Enterprise QBR (10-15 slides, 45-60 minutes)

| Slide | Content | What You Provide | What the Skill Produces |
|-------|---------|-----------------|----------------------|
| 1 | Title and agenda | Meeting details, attendees | Formatted title slide and agenda structure |
| 2 | Executive summary | Your top 3-5 points | Structured summary with headline metric, health status, and key discussion topic |
| 3 | Relationship timeline | Key milestones since last QBR | Chronological milestone view with dates and outcomes |
| 4-5 | Usage and adoption | Usage metrics, feature data | Charts-ready data with period-over-period comparison and adoption heatmap |
| 6 | Value delivered | ROI metrics, outcomes | Headline metric with supporting evidence and benchmark context if available |
| 7 | Support summary | Ticket data, CSAT | Formatted support review with trend indicators |
| 8 | Product roadmap | Relevant upcoming features | Feature list with relevance framing for this customer |
| 9 | Strategic recommendations | **You write this** | Placeholder with suggested structure (the most important slide -- cannot be generated from data alone) |
| 10 | Discussion | Topics for open discussion | Suggested discussion questions based on account context |
| 11 | Action items | Captured live | Template for capturing commitments with owner and deadline columns |

### Mid-Market QBR (8-10 slides, 30-45 minutes)

Same structure with slides 3 and 8 consolidated. Less granular data, more narrative. Usage section is 1 slide, not 2.

### SMB Business Review (5-6 slides or email format, 20-30 minutes)

| Slide | Content |
|-------|---------|
| 1 | Usage snapshot (key metrics, trend, headline) |
| 2 | Value highlights (top 2-3 outcomes) |
| 3 | Tips and recommendations (adoption opportunities) |
| 4 | What is coming (product updates, next steps) |
| 5 | Action items |

For SMB accounts, the skill also offers an email-format alternative -- same content structured as a concise email rather than a deck, for reviews done async instead of in a meeting.

## Comparison Views

For every data slide, the skill produces comparison context:

| Comparison | What It Shows | When to Use |
|-----------|-------------|------------|
| Period-over-period | This quarter vs. last quarter | Every data slide -- shows trajectory |
| Year-over-year | Same quarter last year (if data exists) | Value slide -- shows long-term trend |
| Plan vs. actual | Success plan targets vs. current metrics | If a success plan exists with measurable milestones |
| Peer benchmark | Account vs. similar companies | If you have benchmark data (from your knowledge of the segment) |

You do not need to provide all comparisons. The skill uses whatever prior-period data you provide and labels what is current vs. historical.

## Output Format

The skill produces slide-by-slide content in a structured format:

```
## Slide 1: Title and Agenda

**Quarterly Business Review: Acme Corp**
Q1 2026 | April 15, 2026

Attendees: Tom Chen (VP Engineering), Lisa Park (Eng Manager), Jane Doe (CSM)

Agenda:
1. Usage and adoption review (10 min)
2. Value delivered this quarter (10 min)
3. Support summary (5 min)
4. Looking ahead: roadmap and adoption opportunities (10 min)
5. Discussion (15 min)
6. Action items (5 min)

---

## Slide 2: Executive Summary

**Health: Improving** | Score equivalent: ~74 (up from ~68 last quarter)

Headlines:
- Usage growing: 42% DAU/MAU ratio, up from 38% last quarter
- Value: estimated 340 hours saved through automated workflows this quarter
- Support: clean quarter -- 12 tickets, 4.2-hour average resolution, 4.6/5 CSAT
- Discussion topic: Advanced Reporting adoption -- your analytics team could save additional time

---

## Slide 4: Usage and Adoption

**Active Users:** 47 of 60 seats (78% utilisation, up from 72%)
**Feature Adoption:** 18 of 24 available features used (75% breadth)

Features driving value:
- Workflow Automation: 2,847 executions this quarter (+22% QoQ)
- Team Dashboards: Daily use by 35 users
- API Integration: 12 active connections

Adoption opportunities:
- Advanced Reporting: untouched. 78% of companies your size use this feature
- Custom Alerts: explored but not adopted. Could replace manual monitoring

[Continue for all slides...]
```

## Quality Gates

Before delivering the content:

- **Customer-safe**: No internal terminology, risk scores, or CSM assessments visible. This is a customer-facing deck -- only include data the customer should see
- **Data-backed**: Every claim has a number. "Usage is growing" is weak. "DAU/MAU increased from 38% to 42% quarter-over-quarter" is strong
- **Balanced**: Do not present only good news. If there are support issues or adoption gaps, address them honestly. Customers respect transparency and distrust decks that only highlight positives
- **Action-oriented**: Every section should lead somewhere. Usage data leads to adoption recommendations. Value evidence leads to renewal confidence. Support history leads to resolution commitment or acknowledgement
- **Scannable**: Each slide should be readable in 30 seconds. If a slide requires narration to make sense, it has too much text or unclear charts
- **Strategic recommendation slide is a placeholder**: Mark it clearly. Do not generate generic recommendations -- this slide requires your judgment about the account's future direction and is the highest-value part of the QBR

## Principles

- The QBR exists to demonstrate value and align on direction. If the customer walks out feeling the product is worth the investment and knowing what comes next, the QBR succeeded. Every slide should contribute to one of those two outcomes
- Lead with value, not with usage. Usage is an input; value is the output the customer cares about. "340 hours saved" matters more than "2,847 workflow executions"
- The best QBR decks start a conversation, not deliver a monologue. Build in discussion points and questions. A QBR where the customer talks more than the CSM is a better QBR
- If you do not have data for a slide, skip the slide rather than presenting vague content. A concise 7-slide deck with strong data beats a 12-slide deck with filler
