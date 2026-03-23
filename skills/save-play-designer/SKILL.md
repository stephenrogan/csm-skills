---
name: save-play-designer
description: Creates a structured intervention plan for an at-risk account by identifying the root cause of the risk, designing a targeted response, assigning actions with timelines, and defining what success looks like. Use when asked to build a save play, design a retention intervention, create a rescue plan for an at-risk account, plan a churn prevention strategy, or when an account has been classified as at-risk and needs a dedicated intervention plan. Also triggers for questions about save plays, retention interventions, at-risk account management, churn prevention planning, or how to save a customer who is thinking about leaving.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Save Play Designer

Designs a structured intervention plan for an at-risk account. A save play is not "try harder" -- it is a specific, time-bound plan that addresses the root cause of the risk with targeted actions, defined ownership, and measurable success criteria.

## How to Use

Provide:
- Account name, ARR, renewal date (days remaining)
- Why the account is at risk (the specific risk drivers, not just "at risk")
- How long the risk has been present
- What has been tried so far (if anything)
- Stakeholder landscape (who you know, relationship strength, coverage gaps)
- The customer's stated concerns (if they have told you)
- What you believe is actually driving the risk (which may differ from what they said)
- Your commercial authority (what you can offer: discounts, credits, extended terms)

## Save Play Framework

### Step 1: Diagnose the Root Cause

The intervention must match the cause. A product-fit save play on a relationship problem wastes time.

| Root Cause Category | Indicators | Save Play Focus |
|--------------------|-----------|----------------|
| Product fit | Customer's use case has evolved beyond what the product serves. Feature gaps are blocking critical workflows | Product: address the gap (roadmap, workaround, custom solution) or be honest that the fit is no longer there |
| Value gap | No measurable ROI. Customer cannot justify the investment. CFO asking "what do we get for this?" | Value: build and present the ROI case urgently. Show them what they are getting that they may not be measuring |
| Service failure | History of unresolved issues, SLA breaches, support frustration | Service: fix the outstanding issues. Assign a dedicated resource. Rebuild trust through accountable follow-through |
| Relationship erosion | Champion departed, contacts disengaged, single-threaded, no executive coverage | Relationship: multi-thread immediately. Build new relationships. Executive engagement if warranted |
| Competitive displacement | Active evaluation of alternatives, competitor demos completed, pricing comparison in progress | Competitive: understand what triggered the evaluation. Address the root need, not the competitor |
| Commercial friction | Pricing perceived as too high, discount expected, budget cut affecting vendor spend | Commercial: establish value before discussing price. Explore flexible terms if budget is genuinely constrained |
| Customer-side change | Reorg, new leadership, strategy pivot, acquisition | Adapt: understand the new context. Reposition the value proposition for the new reality |

### Step 2: Design the Intervention

For the identified root cause, build a phased response:

**Phase 1: Stabilise (Week 1)**
- Acknowledge the situation. Contact the customer directly -- do not wait for the scheduled touchpoint
- Gather intelligence. What do they actually want? What would change their mind? What is their timeline?
- Stop the bleeding. If there is an unresolved issue, fix it or commit to a specific resolution timeline

**Phase 2: Address (Weeks 2-4)**
- Execute the root cause intervention (see table above)
- Engage the decision-maker (if not already engaged)
- Present evidence of progress or commitment (do not wait until everything is fixed -- show movement)

**Phase 3: Rebuild (Weeks 4-8)**
- Demonstrate sustained improvement
- Rebuild the value narrative
- Secure the renewal commitment (verbal, then contractual)

### Step 3: Assign Actions

| Action | Owner | Deadline | Purpose |
|--------|-------|----------|---------|
| [specific action] | [named person] | [date] | [how this addresses the root cause] |

**Rules:**
- Every action connects to the root cause. If an action does not address the diagnosed issue, remove it
- Every action has a named owner and a specific date
- Include actions from the customer's side. "Tom to provide feedback on the proposed resolution by March 21" is a tracked commitment
- Include escalation actions if needed. "CSM manager to request executive outreach from VP CS by March 14"

### Step 4: Define Success Criteria

| Criteria | Metric | Target | Timeline |
|----------|--------|--------|----------|
| Customer re-engagement | Response to outreach, meeting scheduled | Customer actively engaged in the save conversation | Week 1 |
| Root cause addressed | Depends on the cause (issue resolved, value presented, relationship rebuilt) | Customer acknowledges progress | Week 4 |
| Renewal commitment | Verbal or written confirmation of intent to renew | Customer commits to renewal (verbal minimum) | Week 6-8 |

### Step 5: Define the Walk-Away Point

Not every account is saveable. Define in advance what constitutes a walk-away:

- The customer explicitly declines to engage in the save conversation
- The root cause is a fundamental product fit issue with no resolution on the roadmap
- The cost of the save (discount, dedicated resource, executive time) exceeds the account's long-term value
- The customer has signed with a competitor

**The walk-away is not failure.** It is the recognition that some resources are better spent on accounts where the intervention can succeed. A graceful exit preserves the relationship for a potential return.

## Output Format

```
## Save Play: [Account Name]
**ARR:** EUR [amount] | **Risk Level:** [High/Critical] | **Renewal:** [date] ([days])
**Created:** [date] | **Owner:** [CSM name]

### Root Cause
[Diagnosis with evidence]

### Intervention Plan
**Phase 1: Stabilise (Week 1)**
[Actions with owners and dates]

**Phase 2: Address (Weeks 2-4)**
[Actions with owners and dates]

**Phase 3: Rebuild (Weeks 4-8)**
[Actions with owners and dates]

### Success Criteria
[Table with metrics and targets]

### Walk-Away Criteria
[Defined conditions for disengaging]

### Review Cadence
Weekly status check: [day]
Manager review: [date]
Decision point: [date]
```

## Quality Gates

- Is the root cause diagnosed, not assumed? "They are at risk" is not a diagnosis. "Champion departed 30 days ago, no replacement identified, economic buyer unengaged, and usage is declining" is a diagnosis
- Does the intervention match the root cause? A save play that focuses on product demos when the root cause is relationship erosion addresses the wrong problem
- Is the timeline realistic given the renewal date? A 12-week save play on an account renewing in 4 weeks is too slow
- Is there a walk-away point defined? Save plays without an exit criteria become resource sinks. Know when to stop
- Are the success criteria measurable? "Things improve" is not a success criterion. "Customer re-engages and verbally commits to renewal by Week 6" is

## Principles

- Speed is the most important variable in a save play. The longer a risk persists without intervention, the harder it is to reverse. A decent save play executed today outperforms a perfect save play executed in two weeks
- The customer must be part of the save. A save play that happens entirely behind the scenes (internal escalation, product fixes, value reports) without engaging the customer directly is not a save play. It is hope. Talk to them
- Match the intensity of the response to the value of the account. A EUR 10k account does not warrant a 6-week save play with executive engagement and commercial concessions. A EUR 200k account does
- Sometimes the save is a conversation, not a project. Many at-risk accounts can be stabilised with a single honest conversation: "I know things have not been perfect. Here is what we are doing about it. What else would you need to feel confident going forward?" Do not over-engineer what can be resolved with directness
