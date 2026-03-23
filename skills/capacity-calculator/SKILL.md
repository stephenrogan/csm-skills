---
name: capacity-calculator
description: Assesses whether a CSM's book of accounts is manageable given the mix of account tiers, health states, upcoming events, and strategic demands. Produces a capacity assessment with overload indicators, rebalancing suggestions, and evidence for headcount conversations. Use when asked to assess workload, evaluate book capacity, determine if a CSM is overloaded, justify additional headcount, plan account distribution, or when a CSM or manager needs to understand whether the portfolio is sustainable. Also triggers for questions about CSM capacity, workload management, account-to-CSM ratios, book balance, portfolio sizing, or when to hire.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Capacity Calculator

Assesses whether a CSM's portfolio is manageable by computing the weighted workload across all accounts. Raw account count is a poor measure of capacity -- a CSM with 30 enterprise at-risk accounts is more loaded than a CSM with 80 healthy SMB accounts. This skill computes the actual demand.

## How to Use

Provide:
- Your account list with: name, ARR, segment/tier, health status, renewal proximity, and any special circumstances (active escalation, expansion in progress, onboarding)
- Your available hours per week (typically 35-40 after internal meetings and admin)
- Any upcoming capacity constraints (PTO, projects, training)

## Capacity Model

### Step 1: Compute Per-Account Demand

Each account consumes a different amount of CSM time based on its characteristics:

**Base demand by segment:**

| Segment | Base Hours/Month | Rationale |
|---------|-----------------|-----------|
| Enterprise | 8-12 hours | Multi-stakeholder, strategic, deep engagement expected |
| Mid-Market | 3-5 hours | Regular cadence, moderate complexity |
| SMB | 1-2 hours | Light touch, digital-first with periodic check-ins |
| Scaled/Tech-Touch | 0.5 hours | Automated primarily, engage on signal only |

**Demand multipliers:**

| Factor | Multiplier | Rationale |
|--------|-----------|-----------|
| Health: Strong | 0.7x | Less intervention needed. Standard cadence |
| Health: Healthy | 1.0x | Baseline management |
| Health: At Risk | 1.5x | Additional investigation, intervention, monitoring |
| Health: Critical | 2.5x | Save play, frequent touchpoints, escalation management |
| Renewal in 90 days | 1.3x | Renewal preparation, commercial conversations, stakeholder engagement |
| Active escalation | 1.5x | Escalation management, internal coordination, customer communication |
| Onboarding (first 90 days) | 1.5x | Intensive engagement, training, milestone tracking |
| Expansion in progress | 1.2x | Commercial preparation, stakeholder engagement |

**Per-account demand** = Base hours * Product of applicable multipliers

### Step 2: Compute Total Portfolio Demand

Sum the per-account demand across all accounts. Compare to available capacity:

| Metric | Computation | What It Means |
|--------|------------|--------------|
| Total monthly demand | Sum of all per-account demands | How many hours your portfolio requires |
| Available monthly capacity | Available hours/week * 4.3 | How many hours you have |
| Capacity utilisation | Total demand / Available capacity | How loaded you are |
| Buffer | 1.0 - Capacity utilisation | How much room you have for the unexpected |

### Step 3: Classify Capacity Status

| Utilisation | Status | Interpretation |
|------------|--------|---------------|
| <70% | Underloaded | Room for more accounts or deeper strategic work on existing accounts |
| 70-85% | Healthy | Sustainable workload with buffer for surprises |
| 85-95% | Stretched | Manageable but no buffer. Any new escalation or at-risk account will push into overload |
| 95-110% | Overloaded | Not sustainable. Something is being dropped -- usually the proactive, strategic work that prevents future crises |
| >110% | Critical | Unsustainable. Active harm to accounts is occurring through neglect. Immediate rebalancing or support needed |

### Step 4: Identify Rebalancing Opportunities

If overloaded, the skill identifies:

| Lever | How | Trade-Off |
|-------|-----|----------|
| Move accounts to a peer CSM | Transfer lowest-ARR, healthiest accounts that require the least relationship continuity | Relationship disruption on the transferred accounts |
| Shift accounts to scaled/tech-touch | Move healthy low-ARR accounts to a lower-touch model | Reduced relationship depth. Monitor for health changes |
| Defer strategic work | Delay account strategy, multi-threading, and proactive initiatives | Short-term relief at the cost of long-term portfolio health |
| Request temporary support | Ask for a colleague to take on escalation management or QBR prep for specific accounts | Coordination overhead. Customer may interact with an unfamiliar CSM |
| Make the headcount case | Use the capacity data to justify additional hiring | Timeline: 2-6 months to hire, onboard, and ramp a new CSM. Not a quick fix |

## Output Format

```
## Capacity Assessment: [CSM Name]
**Date:** [date]

### Portfolio Summary
| Segment | Accounts | Base Demand (hrs/mo) |
|---------|----------|---------------------|
| Enterprise | [n] | [hours] |
| Mid-Market | [n] | [hours] |
| SMB | [n] | [hours] |

### Demand Modifiers
| Factor | Accounts Affected | Additional Demand (hrs/mo) |
|--------|------------------|--------------------------|
| At Risk | [n] accounts | +[hours] |
| Critical | [n] accounts | +[hours] |
| Renewal <90 days | [n] accounts | +[hours] |
| Onboarding | [n] accounts | +[hours] |
| Active escalation | [n] accounts | +[hours] |

### Capacity Status
- Total demand: [hours/month]
- Available capacity: [hours/month]
- Utilisation: [%]
- Status: [Underloaded / Healthy / Stretched / Overloaded / Critical]
- Buffer: [hours/month available for unplanned work]

### Top Demand Accounts
[5 accounts consuming the most CSM time, with demand breakdown]

### Recommendations
[Rebalancing suggestions if overloaded, or strategic opportunities if underloaded]
```

## Using This for Headcount Justification

The capacity model produces the evidence a CS leader needs to make a hiring case:

| Data Point | What It Shows |
|-----------|-------------|
| Utilisation >95% sustained for 2+ months | The team is structurally overloaded, not just having a busy month |
| At-risk accounts not getting intervention time | Revenue is being left unprotected because CSMs do not have capacity to run save plays |
| Proactive work at zero | Multi-threading, account strategy, and adoption planning are not happening because all time goes to reactive work. This is a leading indicator of future risk |
| New accounts cannot be properly onboarded | Growth is creating churn risk because new customers do not get the onboarding attention they need |

Frame the ask as: "At current utilisation, we are deferring [X hours/month] of proactive work that protects [EUR Y] in ARR. A new hire at [cost] would recover [Z] hours of capacity and reduce the unprotected ARR."

## Quality Gates

- Are the segment classifications accurate? An account labelled "SMB" that actually requires mid-market engagement will undercount demand
- Are the multipliers applied honestly? Tempting to downplay the demand of at-risk accounts to make the number look manageable. The model is only useful if it reflects reality
- Does the buffer account for realistic variability? A month with zero surprises is fiction. 15-20% buffer is the minimum for a sustainable portfolio
- If overloaded, is the rebalancing recommendation specific? "Reduce workload" is not a recommendation. "Transfer 5 SMB accounts (EUR 35k combined ARR, all healthy) to scaled motion to free 8 hours/month" is

## Principles

- Account count is a vanity metric. Capacity is a function of ARR-weighted, health-adjusted, event-modified demand -- not the number of logos on the list. 40 accounts is not a meaningful statement without knowing the mix
- Chronic overload is a management failure, not a CSM resilience test. A CSM operating at 110% utilisation for 3 months is not performing heroically -- they are being set up to fail. The capacity model makes this visible
- The capacity model is an argument, not a complaint. Presenting utilisation data with revenue impact and risk quantification is a business case. Saying "I am too busy" is a complaint. The model produces the former
- Underloaded CSMs are an opportunity, not a problem. If utilisation is below 70%, the CSM has room for deeper strategic work, more accounts, or both. Use the capacity data to make that case as well
