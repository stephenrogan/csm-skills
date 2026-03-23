---
name: quarterly-planning-builder
description: Helps a CSM build their quarterly plan with portfolio priorities, measurable targets, focus areas, capacity allocation, and development goals. Produces a structured plan that can be shared with management and reviewed at quarter-end. Use when asked to build a quarterly plan, set Q1-Q4 goals, create a portfolio strategy for the quarter, plan the next 90 days, or when a CSM needs to move from reactive week-to-week management to proactive quarterly strategy. Also triggers for questions about quarterly planning, goal setting for a period, portfolio prioritisation for the quarter, or structuring a 90-day plan.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Quarterly Planning Builder

Structures the CSM's quarter with clear priorities, measurable targets, and a plan for how to allocate time across a portfolio. The difference between CSMs who grow and CSMs who plateau is often the presence or absence of this kind of intentional planning.

## How to Use

Provide:
- Your portfolio (account count, total ARR, health distribution)
- Renewals this quarter (which accounts, ARR, risk level)
- Expansion opportunities (which accounts, estimated value, stage)
- At-risk accounts (which accounts, ARR, what is happening)
- Strategic priorities from your manager or leadership (if any)
- Your own development goals (if any)
- Capacity constraints (PTO, internal projects, ramp -- anything that reduces your available weeks)

## Plan Structure

### 1. Portfolio Snapshot

| Metric | Value | Trend |
|--------|-------|-------|
| Accounts | [count] | [+/- from last quarter] |
| ARR | [total] | [+/- from last quarter] |
| Health distribution | Strong: [n], Healthy: [n], At Risk: [n], Critical: [n] | [changes from last quarter] |
| Renewals this quarter | [count], EUR [ARR] | [risk breakdown] |
| Expansion pipeline | [count], EUR [estimated value] | [stage breakdown] |

### 2. Quarterly Objectives (Maximum 4)

For each objective:

| Element | Content |
|---------|---------|
| Objective | What you will achieve, stated specifically |
| Why it matters | How it connects to retention, growth, or your development |
| Success metric | How you will know you achieved it (must be measurable at quarter-end) |
| Target | The specific number or outcome |
| Key actions | The 3-5 things you will do to achieve this |

**Example objectives:**
- "Retain 95%+ of renewing ARR this quarter (EUR 1.2M renewing, target EUR 1.14M retained)"
- "Close EUR 45k in expansion across 3 accounts"
- "Move 3 accounts from At Risk to Healthy"
- "Establish executive sponsor relationships at top 5 accounts by ARR"

### 3. Account Priorities

Classify your accounts into four management tiers for the quarter:

| Tier | Accounts | Time Allocation | Management Approach |
|------|----------|----------------|-------------------|
| Strategic | Top 5-8 by ARR + risk | 40% of time | Full strategic plans (account-strategy-builder). Proactive. Multi-threaded |
| Managed | Next 10-15 by ARR | 30% of time | Regular cadence. Reactive + proactive. Standard engagement |
| Scaled | Next 10-15 | 20% of time | Lighter cadence. Reactive primarily. Digital touchpoints |
| Monitoring | Remaining | 10% of time | Automated checks. Engage only on signals |

### 4. Key Dates and Milestones

| Date | Event | Account(s) | Preparation Needed |
|------|-------|-----------|-------------------|
| [date] | [renewal, QBR, executive meeting, etc.] | [account] | [what to prepare before this date] |

### 5. Risk Register

| Risk | Probability | ARR Impact | Mitigation | Status |
|------|-----------|-----------|-----------|--------|
| [risk] | [H/M/L] | [EUR] | [what you are doing] | [active/monitoring] |

### 6. Development Focus

One professional development goal for the quarter. Not "get better at everything" -- one specific skill or capability:

| Goal | Why | How | Measure |
|------|-----|-----|---------|
| [specific development goal] | [how it improves your effectiveness] | [specific actions -- course, practice, mentoring] | [how you know you improved] |

### 7. Quarter-End Review Criteria

Define now what success looks like at the end of the quarter:

| Criteria | Target | Measurement |
|----------|--------|-------------|
| ARR retained | [EUR] of [EUR] renewing (%) | CRM renewal data |
| Expansion closed | [EUR] | CRM opportunity data |
| Health improvement | [n] accounts moved to higher band | Health score comparison start vs. end |
| Engagement compliance | [%] touchpoints completed vs. planned | Activity log |
| Objective achievement | [n] of [n] objectives met | Self-assessment + manager review |

## Output Format

```
## Quarterly Plan: [CSM Name] -- [Quarter Year]
**Portfolio:** [n] accounts | EUR [ARR] | [health summary]

### Objectives
[2-4 objectives with metrics and targets]

### Account Tiers
[Tier classification table]

### Key Dates
[Timeline of critical events]

### Risk Register
[Top risks with mitigation]

### Development Goal
[One specific development focus]

### Review Criteria
[Quarter-end success definition]
```

## Quality Gates

- Are the objectives measurable? "Improve retention" fails. "Retain 95%+ of EUR 1.2M renewing ARR" succeeds
- Is the time allocation realistic? If 40% goes to Strategic accounts and you also have 12 QBRs, 5 renewals, and 3 escalations, the math may not work. Check capacity before committing
- Does the risk register include at least one risk? If you see zero risks in your portfolio for the next 90 days, you are not looking hard enough
- Would your manager approve this plan? If the plan does not align with what leadership cares about, it will create friction regardless of execution quality
- Can you review this plan in 5 minutes at the end of the quarter and know whether you succeeded? If the review criteria are vague, the plan is vague

## Principles

- A plan you review weekly is 10x more valuable than a plan you write once. Schedule 15 minutes every Friday to check progress against the plan. Adjust as reality evolves
- Four objectives maximum. More than four means none get full attention. Pick the four that matter most and execute them well
- The plan should make you slightly uncomfortable. If every objective is easily achievable with your current approach, the plan is not ambitious enough. Growth happens when you stretch
- Share the plan with your manager. It aligns expectations, creates accountability, and gives them the context to support you. A manager who knows your plan can help you when things go sideways. A manager who does not know your plan can only react
