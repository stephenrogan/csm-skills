---
name: renewal-risk-scorer
description: Assesses renewal risk for a specific account by scoring across multiple dimensions including health, engagement, value evidence, stakeholder coverage, competitive signals, and commercial factors. Produces a risk classification with the primary risk driver and recommended intervention. Use when asked to assess renewal risk, evaluate whether a renewal is safe, score an account's likelihood of renewing, prepare for a renewal pipeline review, or when a CSM needs an objective assessment of whether a renewal is at risk. Also triggers for questions about renewal likelihood, churn risk assessment, retention risk scoring, or predicting whether a customer will renew.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Renewal Risk Scorer

Scores renewal risk across the dimensions that actually predict whether a customer will renew. Replaces gut-feel "I think they will renew" with a structured assessment that surfaces the specific risk drivers and tells you where to focus intervention effort.

## How to Use

Provide:
- Account name, ARR, renewal date, days to renewal
- Health status and trajectory (improving, stable, declining)
- Usage and adoption (growing, stable, declining, key features used/unused)
- Engagement (touchpoint recency, responsiveness, meeting attendance)
- Value evidence (ROI quantified, outcomes confirmed, or no evidence)
- Stakeholder coverage (multi-threaded or single-threaded, economic buyer engaged or not)
- Competitive signals (any mentions, evaluations, or indirect signals)
- Commercial factors (pricing concerns, discount history, contract terms)
- Sentiment (overall customer sentiment: positive, neutral, negative, unknown)
- Any other context (champion departure, reorg, budget pressure)

## Risk Scoring Model

Score each dimension 1-5:

| Dimension | 1 (Low Risk) | 3 (Moderate Risk) | 5 (High Risk) | Weight |
|-----------|-------------|-------------------|---------------|--------|
| Health and trajectory | Strong, improving | Healthy, stable | At risk or declining | 20% |
| Usage and adoption | Deep, growing | Adequate, stable | Shallow or declining | 15% |
| Engagement | Active, responsive, multi-channel | Regular but cooling | Disengaged, unresponsive, or dark | 15% |
| Value evidence | Customer-confirmed ROI | Data-derived, not confirmed | No evidence or negative | 15% |
| Stakeholder coverage | Multi-threaded, economic buyer engaged | Champion engaged, gaps elsewhere | Single-threaded or champion departed | 15% |
| Competitive signals | None detected | Indirect signals | Active evaluation | 10% |
| Commercial factors | No pricing concerns, clean history | Minor concerns raised | Active pricing objection or budget pressure | 10% |

**Composite risk score** = weighted sum (1.0-5.0)

| Score | Classification | Meaning | Action Urgency |
|-------|---------------|---------|---------------|
| 1.0-2.0 | Low risk | Renewal is expected. Standard process | Prepare value summary. Standard renewal conversation |
| 2.1-3.0 | Moderate risk | Some vulnerability. Not in danger but not certain | Proactive outreach. Address specific risk factors. Engage within 2 weeks |
| 3.1-4.0 | High risk | Renewal is uncertain. Specific intervention needed | Act this week. Build a dedicated save/retention plan |
| 4.1-5.0 | Critical risk | Renewal is unlikely without significant intervention | Act today. Executive engagement. Commercial flexibility. All-hands retention effort |

## Identifying the Primary Risk Driver

The composite score tells you overall risk. The dimension scores tell you where to focus.

**Primary risk driver** = the highest-scoring dimension. This is where intervention should concentrate.

| Primary Driver | Intervention Focus |
|---------------|-------------------|
| Health declining | Investigate root cause. Is it product, service, or relationship? Fix before commercial conversation |
| Adoption shallow | Enablement push. Show them what they are missing. Build the value case from usage depth |
| Engagement fading | Re-engage through a different channel or angle. Understand why they have disengaged |
| Value evidence missing | Build the ROI case urgently. You cannot defend the renewal without value evidence |
| Stakeholder gaps | Multi-thread now. Engage the economic buyer before the renewal conversation |
| Competitive active | Run the competitive-threat-assessor. Build a competitive response plan |
| Commercial friction | Understand the root of the pricing concern. Prepare for the negotiation |

## Output Format

```
## Renewal Risk Assessment: [Account Name]
**ARR:** EUR [amount] | **Renewal:** [date] ([days] days)
**Assessed by:** [CSM name] | **Date:** [date]

### Risk Scores
| Dimension | Score | Evidence |
|-----------|-------|---------|
| Health & trajectory | [1-5] | [specific data] |
| Usage & adoption | [1-5] | [specific data] |
| Engagement | [1-5] | [specific data] |
| Value evidence | [1-5] | [specific data] |
| Stakeholder coverage | [1-5] | [specific data] |
| Competitive signals | [1-5] | [specific data] |
| Commercial factors | [1-5] | [specific data] |

### Composite Score: [X.X] -- [Classification]

### Primary Risk Driver
[Dimension]: [Why this is the biggest risk, with evidence]

### Recommended Intervention
[Specific actions to address the primary risk driver, with timeline]

### Renewal Forecast
Probability: [%] (CSM assessment)
Confidence in forecast: [H/M/L]
Best case: [outcome]
Worst case: [outcome]
```

## Quality Gates

- Is every score backed by specific evidence? A score of "3" without explanation is a guess, not an assessment. "Engagement scored 4 because the champion has not responded to 3 emails in 14 days" is evidence
- Is the primary risk driver identified and the intervention specific? Knowing the overall score is not enough. Knowing that the specific vulnerability is "no economic buyer engaged with 45 days to renewal" tells you exactly what to do
- Is the forecast honest? Optimism bias is the biggest risk in renewal forecasting. If you score an account at 3.5 (high risk) but forecast 80% probability, the numbers are inconsistent
- Have you considered what you do not know? An account with "no competitive signals" may still be evaluating competitors -- you just have not heard about it. Score based on evidence but acknowledge blind spots

## Principles

- Renewal risk is a function of the entire relationship, not just the renewal conversation. By the time you enter the renewal discussion, the outcome is largely determined by what happened in the preceding 11 months. The risk scorer surfaces whether you did enough
- The score should change your behaviour. If the assessment reveals high risk and you continue with the same approach, the assessment was performative, not operational. Every high-risk score should produce a different plan than a low-risk score
- Forecast accuracy improves with practice. Track your predicted probabilities against actual outcomes. Over time, you will calibrate -- your "70% confident" will actually correspond to ~70% renewal rate. Without tracking, you are guessing every time
- The most dangerous renewal is the one you think is safe. A low-risk score should not mean no preparation. It should mean standard preparation. Accounts that churn from a "low risk" assessment are almost always accounts where the CSM stopped paying attention
