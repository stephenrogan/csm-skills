---
name: usage-pattern-interpreter
description: Takes raw usage data -- even a spreadsheet export or pasted metrics -- and identifies patterns, risks, and opportunities. Translates product analytics into account intelligence a CSM can act on. Use when asked to interpret usage data, analyse product metrics, make sense of a usage report, identify trends in customer behaviour, flag usage-based risks, or when a CSM has data but does not know what it means for the account. Also triggers for questions about usage analysis, product analytics interpretation, behavioural pattern detection, usage-based risk identification, or turning raw metrics into actionable insight.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Usage Pattern Interpreter

Translates raw usage data into account intelligence. Most CSMs have access to product analytics dashboards but struggle to move from "what is the data showing" to "what should I do about it." This skill bridges that gap.

## How to Use

Provide whatever usage data you have:
- Dashboard exports (active users, sessions, feature usage, workflow completions)
- Spreadsheet data (CSV or pasted tables)
- Screenshots of analytics with numbers you can describe
- Specific metrics you are trying to understand ("DAU dropped 30% this month -- what does it mean?")

Also provide:
- Account context (segment, product tier, tenure, number of licensed seats)
- Any known context for the data (did they just onboard a new team? Did they lose a key user? Is this a seasonal business?)
- What you are worried about or trying to understand

## Pattern Recognition Framework

### Step 1: Classify the Data

Organise whatever data you have into these categories:

| Category | Metrics | What They Measure |
|----------|---------|------------------|
| Volume | DAU, WAU, MAU, sessions, API calls | How much the product is being used overall |
| Breadth | Active users / total seats, features used / features available | How widely adoption has spread across the team and the product |
| Depth | Sessions per user, actions per session, workflow completions | How deeply each user engages when they use the product |
| Engagement | Login frequency, return rate, time in product | How habitually the product is part of their workflow |
| Trend | Period-over-period changes in any of the above | Direction of travel -- more important than any single number |

### Step 2: Identify Patterns

| Pattern | How to Detect | What It Usually Means | Risk or Opportunity |
|---------|-------------|---------------------|-------------------|
| Steady growth | Volume and breadth increasing 5-15% month-over-month | Healthy adoption. The product is spreading organically | Opportunity: expansion (seats, tier). The team is outgrowing the current configuration |
| Plateau | Metrics stable for 3+ months after initial growth | Adoption has reached its natural ceiling for the current setup | Risk if the ceiling is low (they are not using most of what they bought). Opportunity if the ceiling is high (time to deepen or expand) |
| Gradual decline | Volume or breadth decreasing 5-10% month-over-month for 2+ months | Something is changing. Could be seasonal, could be a team change, could be a competitive evaluation | Risk: investigate immediately. Gradual declines that go unaddressed become steep declines |
| Cliff drop | Volume or engagement drops >30% in a single period | Something happened. A key user left, a competing tool was adopted, an internal priority shifted, or there was a product issue | Risk: high urgency. Contact the customer within 48 hours. This is a potential churn trigger |
| Feature abandonment | A feature that was actively used has zero usage for 30+ days | The team found a better way, the feature broke, the person who used it left, or the use case disappeared | Risk if the feature was core to their value proposition. Investigate root cause |
| Broadening without deepening | More users logging in but each user does less | Adoption is spreading but without training or enablement. New users are exploring but not embedding the product in their workflow | Opportunity: targeted enablement for new users. Depth follows breadth if supported |
| Deepening without broadening | Fewer users but each user does more | Power users are getting more value but the broader team is not adopting | Risk: concentration. If 3 power users do everything and 40 licensed users do nothing, the account is vulnerable to any of those 3 leaving |
| Seasonal pattern | Usage dips and peaks that repeat annually (e.g., lower in December, higher in Q1 and Q3) | Normal business cycle. Not a risk signal unless the dip is deeper than prior years | No action needed -- but document the pattern so you do not misinterpret the next dip |
| Spike followed by return to baseline | Sudden increase (new feature launch, new team onboarding) that fades within 2-4 weeks | The initial interest did not convert to habitual usage. The feature or onboarding did not stick | Opportunity: investigate why the spike did not sustain. The interest was real; the follow-through failed |
| Credential sharing | Total active users exceed licensed seats, or login patterns suggest shared credentials | Demand exceeds the current licence. Users need access but cannot get their own seats | Opportunity: expansion conversation. "Your team has outgrown the current licence -- let us make sure everyone has proper access" |

### Step 3: Contextualise

Raw patterns become actionable when matched to account context:

| Pattern | Account Context | Interpretation |
|---------|----------------|---------------|
| Usage declining 15% | Customer's fiscal year just ended | Likely seasonal. Monitor but do not alarm. Compare to same period last year if data exists |
| Usage declining 15% | Champion left 3 weeks ago | Likely correlated to the departure. The champion may have been driving adoption personally. Urgent |
| Usage declining 15% | Customer mentioned budget review last month | Potentially deliberate reduction. May be an early signal of downsell or non-renewal |
| New user spike | Customer just hired 10 people | Expected. Provide onboarding resources for the new users |
| New user spike | No known headcount change | Investigate. Organic spread is a positive signal. But could also be a trial by a team evaluating alternatives |

### Step 4: Generate Insights and Recommendations

For each significant pattern detected:

```
## Usage Pattern Interpretation: [Account Name]
**Data period:** [date range]
**Prepared by:** [CSM name]

### Headline
[One sentence: the most important thing the data is telling you]

### Patterns Detected
| Pattern | Metric | Detail | Confidence | Urgency |
|---------|--------|--------|-----------|---------|
| [pattern] | [metric and values] | [what you observed] | [H/M/L] | [Immediate/This week/This month/Monitor] |

### Context Assessment
[How the account context (seasonal, personnel, strategic) affects the interpretation]

### Recommended Actions
1. [Action tied to a specific pattern]
2. [Action tied to a specific pattern]

### Questions for the Customer
[Specific questions to ask that would confirm or refute your interpretation]

### Watch Signals
[What to monitor in the next 2-4 weeks to see if the pattern continues, reverses, or accelerates]
```

## Common Misinterpretations to Avoid

| What the Data Shows | Common Misinterpretation | Better Interpretation |
|--------------------|-----------------------|---------------------|
| DAU/MAU ratio declining | "They are losing interest" | Could be that MAU grew (new users logged in once) while DAU stayed stable. The daily habit is fine; the new users need activation |
| Feature usage is zero | "They do not need that feature" | Could be they do not know it exists, cannot figure it out, or the feature requires configuration they have not done |
| Session duration declining | "They are less engaged" | Could mean they are more efficient. If they accomplish the same outcomes in less time, shorter sessions are a positive signal |
| API call volume declining | "They are using the product less" | Could be they optimised their integration to make fewer, more efficient calls. Check if outcomes are stable |
| Login frequency dropping but workflow completions stable | "They are disengaging" | They may be completing workflows via API or automation instead of the UI. The product is more embedded, not less |

## Quality Gates

- Are you interpreting patterns, not individual data points? A single day's DAU drop is noise. A 3-week declining trend is a signal. The distinction is critical
- Have you considered at least two explanations for each pattern? The first explanation is not always correct. Usage declining could be seasonal, personnel-related, competitive, or product-related. List the possibilities before concluding
- Are your recommendations specific to the pattern? "Schedule a check-in" is not a recommendation for a cliff drop. "Call the customer today to ask about the 40% usage decline and whether it correlates with the champion's departure last month" is
- Have you accounted for known context? A usage decline during December at a retail customer is expected. The same decline in March is not

## Principles

- Data tells you what happened. It does not tell you why. Your job as a CSM is to find the why. The data narrows the search space; the conversation with the customer provides the answer
- Trends matter more than snapshots. A health score of 65 is concerning. A health score of 65 that was 78 three months ago is alarming. A health score of 65 that was 52 three months ago is encouraging. The direction is more important than the position
- Not every change is a signal. Usage data is noisy. Holidays, vacations, product releases, and random variation all create fluctuations that look like trends but are not. Apply the "2+ consecutive periods" rule before classifying a change as a trend
- The most dangerous data pattern is the absence of data. An account with no usage data is not healthy by default -- it is invisible. The accounts you cannot see are the accounts you cannot save
