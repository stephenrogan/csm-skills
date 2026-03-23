---
name: cs-investment-case-builder
description: Builds the business case for CS investment -- headcount, tooling, programmes, or operational improvements. Structures the argument in CFO-ready language with ROI projection, risk quantification, and evidence from portfolio data. Use when asked to build a business case for CS resources, justify headcount, make the case for a CS tool, propose a programme investment, or when a CS leader needs to secure budget or approval from finance or executive leadership. Also triggers for questions about CS headcount justification, tooling business cases, CS ROI for leadership, budget requests, or how to make the financial case for investing in customer success.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# CS Investment Case Builder

Builds business cases for CS investments in the language executives and CFOs understand: revenue impact, risk reduction, and return on investment. The most common failure in CS resource requests is framing the ask in CS language instead of finance language.

## How to Use

Provide:
- What you are requesting (headcount, tooling, programme, process improvement)
- The cost of the investment (salary, licence cost, implementation cost, ongoing cost)
- The problem the investment solves (expressed as revenue risk, capacity gap, or efficiency opportunity)
- Evidence from your portfolio (capacity data, churn correlated to gaps, time analysis)
- The alternative: what happens if the investment is not made

## Business Case Structure

### The One-Line Summary

Every business case needs a headline that a CFO can read in 5 seconds:

"Investing EUR [X] in [what] will protect EUR [Y] in at-risk ARR and create capacity for EUR [Z] in expansion -- a [N]x return in the first year."

If you cannot write this sentence, the business case is not ready.

### The Problem (in Revenue Terms)

Translate the operational problem into financial impact:

| CS Problem | Revenue Translation |
|-----------|-------------------|
| CSMs are overloaded | "At current capacity utilisation (108%), proactive retention work (save plays, adoption planning, multi-threading) is deferred. EUR [X] in ARR is managed reactively instead of strategically, increasing churn risk by [estimated %]" |
| No CS tooling | "CSMs spend [X] hours/week on manual data gathering and reporting. At [loaded cost], that is EUR [Y]/year in labour on work that could be automated. That time could be redirected to EUR [Z] in expansion pipeline" |
| No onboarding programme | "New customers reach first value in [X] weeks. Industry benchmark is [Y] weeks. The [gap] weeks of delay correlate with [estimated %] higher 12-month churn in our portfolio" |
| No executive engagement | "[N] accounts (EUR [X] ARR) have no executive sponsor relationship. Accounts without executive coverage churn at [Y]% vs. [Z]% for covered accounts" |

### The Investment

State clearly what you are asking for:

| Element | Content |
|---------|---------|
| What | Specific investment: 2 additional CSMs, a CS platform, an enablement programme |
| Cost | Total cost: annual salary + benefits, licence cost, implementation, training |
| Timeline | When the investment starts producing returns (ramp time for headcount, implementation time for tooling) |
| Dependencies | What else needs to happen (hiring timeline, integration work, training) |

### The Return

Quantify the expected impact:

| Return Type | How to Estimate | Example |
|-------------|----------------|---------|
| Revenue protected | Identify at-risk ARR that the investment directly addresses. Apply estimated save rate improvement | "2 additional CSMs would reduce average book size from 50 to 35 accounts, enabling proactive management of the 8 at-risk accounts (EUR 340k ARR) currently receiving only reactive support. At a conservative 20% save rate improvement, that protects EUR 68k in ARR" |
| Revenue generated | Identify expansion pipeline capacity that the investment enables | "Reduced book size frees an estimated 6 hours/week per CSM for expansion conversations. Based on current conversion rates, this produces an estimated EUR 120k in expansion ARR in the first year" |
| Cost avoided | Calculate the cost of the problem continuing | "Without additional capacity, churn is projected to increase by [X]%, costing EUR [Y] in lost ARR. The investment cost is EUR [Z] -- [fraction] of the revenue at risk" |
| Efficiency gained | Calculate time saved * loaded cost | "The CS platform automates [X] hours/week of manual work across the team. At a loaded cost of EUR [Y]/hour, that is EUR [Z]/year in recovered capacity" |

### The Risk of Inaction

What happens if the investment is not made:

| Dimension | Without Investment | With Investment |
|-----------|-------------------|----------------|
| Churn rate | [projected without intervention] | [projected with intervention] |
| NRR | [projected without] | [projected with] |
| CSM capacity utilisation | [current/projected] | [target] |
| Time to first value (new customers) | [current] | [target] |
| Expansion pipeline | [current] | [projected with capacity] |

### The Ask

End with a specific, time-bound request:

"I am requesting approval for [specific investment] at a cost of EUR [X] per year, starting [date]. The projected first-year return is EUR [Y] in protected and expanded revenue, representing a [N]x ROI. I would like to discuss this in our [next meeting/budget review/planning session]."

## Output Format

```
## CS Investment Case: [Title]
**Prepared by:** [name] | **Date:** [date]
**Investment:** [what] | **Cost:** EUR [amount]/year
**Projected return:** EUR [amount] (first year) | **ROI:** [X]x

### Summary
[One-line headline]

### The Problem
[Revenue-framed description of the gap]

### The Investment
[What, cost, timeline, dependencies]

### The Return
[Revenue protected + generated + cost avoided]

### Risk of Inaction
[What happens without the investment]

### The Ask
[Specific request with timeline]
```

## Quality Gates

- Is every number evidence-based? "Revenue at risk" should be traceable to specific accounts or portfolio data, not guesswork
- Is the ROI calculation conservative? An investment case with aggressive assumptions gets challenged. A case with conservative assumptions gets approved. Use the lower end of your estimates
- Is the "risk of inaction" specific? "Things will get worse" is not compelling. "Churn is projected to increase by 3 percentage points, costing EUR 180k in ARR based on our current renewal pipeline" is
- Would a CFO understand this without CS context? If the document uses health scores, NPS, or QBR frequency as arguments without translating to revenue, it is written for the wrong audience

## Principles

- CFOs think in revenue, risk, and return. Every argument must connect to one of these three. "Our team is overwhelmed" is a staffing observation. "Our team's capacity gap puts EUR 340k in ARR at risk" is a business case
- Conservative estimates build credibility. If you project 5x ROI and deliver 3x, you exceeded expectations. If you project 10x and deliver 5x, you missed by half -- even though 5x is excellent. Underpromise
- The comparison to inaction is your strongest argument. The investment cost is not being evaluated in isolation -- it is being compared to the cost of not investing. Make that comparison explicit and quantified
- One strong business case builds a pattern. If you get a CS tool approved with a solid business case and demonstrate the ROI, your next request (headcount, programme, expansion) starts from a position of credibility. The first case is the hardest
