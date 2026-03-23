---
name: week-planner
description: Structures the CSM's week based on their portfolio status, upcoming events, overdue items, and strategic priorities. Produces a time-blocked plan that balances reactive demands with proactive account management. Use when asked to plan a week, structure daily priorities, build a weekly schedule, allocate time across accounts, manage a busy week, or when a CSM feels overwhelmed and needs to determine where to focus. Also triggers for questions about time management, weekly planning, account prioritisation for the week, daily priority setting, or how to balance competing demands across a portfolio.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Week Planner

Structures your week by pulling together everything that needs your attention -- meetings, overdue items, risk accounts, proactive outreach, and administrative tasks -- and allocating time based on impact, not urgency.

The fundamental problem this skill solves: urgent things are visible. Important things are not. Without a plan, every week is consumed by what is loudest, not what matters most. The week planner makes the important things visible.

## How to Use

Provide:
- Your calendar for the week (meetings already scheduled)
- Your account list with current status (or the output from book-prioritisation)
- Overdue items (commitments, follow-ups, actions from prior weeks)
- Upcoming events (renewals in the next 30 days, QBRs, escalation check-ins)
- Proactive work you want to do but keep deferring (account strategy, multi-threading, adoption planning)
- Available hours (total working hours minus meetings already scheduled)
- Anything non-account-related (training, internal meetings, admin)

## Planning Framework

### Step 1: Categorise Everything

Sort all items into four buckets:

| Bucket | Definition | Time Allocation | Examples |
|--------|-----------|----------------|---------|
| Protect | Activities that prevent revenue loss or relationship damage | 40% of available time | At-risk accounts, escalations, renewal prep, overdue commitments |
| Grow | Activities that create new value or revenue | 25% of available time | Expansion conversations, adoption planning, QBR prep, success plan reviews |
| Maintain | Activities that sustain healthy relationships | 20% of available time | Scheduled check-ins, routine touchpoints, CRM updates |
| Build | Activities that invest in your long-term effectiveness | 15% of available time | Account strategy, multi-threading, internal development, process improvement |

**The 40/25/20/15 split is a guideline, not a rule.** A week with 3 at-risk accounts and an active escalation shifts to 60% Protect. A week with no fires shifts to 30% Protect and more Grow and Build. Adjust based on reality -- but if Protect is consistently >50%, your portfolio has a structural problem, not a time management problem.

### Step 2: Identify the Non-Negotiables

These happen regardless of what else is on the list:
- Meetings already on the calendar (customer calls, internal syncs)
- Commitments with deadlines this week (things you promised to deliver)
- Escalations requiring same-day attention
- Renewals in the next 14 days that need progress

List them, estimate time, and subtract from your available hours. What remains is your discretionary time.

### Step 3: Prioritise Discretionary Time

For everything that is not a non-negotiable, rank by impact:

**Impact scoring (quick assessment):**
- Will this prevent churn or protect ARR? (Protect -- high impact)
- Will this create expansion revenue? (Grow -- high impact)
- Will this strengthen a relationship that affects retention? (Maintain -- medium impact)
- Will this improve how I work in 30+ days? (Build -- medium impact long-term)
- Will this satisfy an internal request that does not affect customers? (Low impact -- deprioritise)

### Step 4: Time-Block the Week

Assign items to specific days and time blocks:

| Day | Focus | Why This Day |
|-----|-------|-------------|
| Monday | Protect + Plan | Start the week by addressing the most urgent items and reviewing the plan |
| Tuesday-Wednesday | Grow + Maintain | Mid-week has the most energy and the fewest interruptions. Use it for high-value work |
| Thursday | Maintain + Build | Customer check-ins, relationship maintenance, and investment in your own development |
| Friday | Build + Admin | Process improvement, CRM cleanup, next-week planning, reflection |

**Time-blocking rules:**
- Block 2-hour minimum for strategic work (account strategy, QBR prep). 30-minute fragments are not enough for deep thinking
- Cluster similar activities (all check-in calls in one block, all email drafting in another). Context-switching is expensive
- Leave 20% of the week unblocked for reactive demands. If you schedule 100% of your time, any unexpected escalation destroys the plan
- First thing Monday and last thing Friday are planning and reflection, not customer-facing work

### Step 5: End-of-Day Check

At the end of each day, take 5 minutes:
- What did I complete? (Update the plan)
- What moved to tomorrow? (Why? Was it deprioritised or blocked?)
- Did anything new emerge that changes the week? (Reprioritise if needed)

## Output Format

```
## Weekly Plan: [CSM Name]
**Week of:** [Date]
**Available hours:** [X] (after scheduled meetings)

### Non-Negotiables This Week
| Item | Day | Time | Bucket |
|------|-----|------|--------|
| Acme Corp renewal call | Tue | 1hr | Protect |
| Beta Inc escalation follow-up | Mon | 30min | Protect |
| Commitment: send API docs to Gamma Corp | Mon | 30min | Protect |
| QBR prep for Delta Corp (QBR Thursday) | Tue-Wed | 2hr | Grow |
| Manager 1:1 | Wed | 30min | Internal |

### Discretionary Priority List
| Priority | Item | Bucket | Est. Time | Scheduled |
|----------|------|--------|----------|-----------|
| 1 | Competitive response plan for Acme Corp | Protect | 1hr | Mon PM |
| 2 | Expansion proposal draft for Echo Corp | Grow | 1.5hr | Tue PM |
| 3 | Check-in calls: 4 mid-market accounts | Maintain | 2hr | Thu AM |
| 4 | Account strategy draft for top 3 accounts | Build | 2hr | Fri AM |
| 5 | Multi-threading outreach for Beta Inc | Build | 30min | Fri PM |

### Daily Breakdown
**Monday:** [Scheduled items + priority discretionary items]
**Tuesday:** [...]
**Wednesday:** [...]
**Thursday:** [...]
**Friday:** [...]

### Parked for Next Week
[Items that did not make the cut, with a note on why and when to revisit]
```

## Quality Gates

- Does the plan have a Protect item in the first 2 hours of Monday? The most urgent thing should be addressed first, not deferred
- Is there any Build time in the plan? If Build is zero every week, you are trapped in reactive mode. Even 2 hours of Build work per week compounds over a quarter
- Is the plan realistic? A plan with 50 hours of work in a 40-hour week is not a plan -- it is a wish list. Be honest about capacity. What does not fit gets parked with an explicit revisit date
- Does the plan leave buffer for the unexpected? If every hour is scheduled, the first unplanned escalation breaks the week. 20% buffer is the minimum
- Could you explain your priorities to your manager in 60 seconds? If the plan is too complex to articulate quickly, simplify. The plan should create clarity, not complexity

## Principles

- Planning is a weekly discipline, not a weekly event. The first time you plan your week it will take 30 minutes. By week four it takes 10 minutes. The ROI is in the hundreds of hours you do not waste on low-impact activities
- Your plan will not survive the week. That is fine. The value is in the intentional starting point, not in perfect execution. A plan that gets 60% executed is vastly better than no plan that gets 100% reactive
- Saying no to low-impact activities is the highest-leverage skill a CSM can develop. The week planner makes the trade-offs visible so you can make them consciously instead of by default
- Protect and Grow are where your value is measured. Maintain and Build are where your capability is developed. All four matter. A CSM who only Protects burns out. A CSM who only Builds never delivers
