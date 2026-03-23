---
name: churn-post-mortem
description: Structures a post-churn analysis to identify root causes, missed signals, intervention gaps, and systemic lessons. Produces a documented analysis that prevents the same failure pattern from repeating across the portfolio. Use when asked to analyse a churn, conduct a loss review, identify why an account left, build a post-mortem, or when a customer has churned and the CSM needs to understand what happened and what the team should learn from it. Also triggers for questions about churn analysis, loss review, retention failure investigation, or learning from customer departures.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Churn Post-Mortem

Structures the analysis of why an account churned. The post-mortem is not blame assignment -- it is pattern recognition. Every churn teaches the team something. The post-mortem captures that lesson so it does not have to be learned again on the next account.

## How to Use

Provide:
- Account name, ARR lost, contract tenure
- When they churned (date and renewal cycle context)
- The stated reason (what the customer told you)
- The actual reason (what you believe really drove the decision -- these are often different)
- Timeline of the decline (when did things start going wrong, what signals were visible)
- What interventions were attempted (save plays, escalations, executive engagement)
- What the outcome of each intervention was
- What you wish you had done differently

## Post-Mortem Framework

### 1. Summary

One paragraph: who churned, how much ARR, how long they were a customer, and the headline reason.

### 2. Root Cause Analysis

Most churns have multiple contributing factors. Identify the primary root cause and contributing factors:

| Category | Root Cause Question | Assessment |
|----------|-------------------|-----------|
| Product fit | Did the product solve their core problem? Did it stop solving it? | [Specific assessment with evidence] |
| Value realisation | Did they see measurable ROI? Could they articulate the value? | [Specific assessment] |
| Relationship | Was the relationship strong? Were we multi-threaded? Did we have executive coverage? | [Specific assessment] |
| Service | Did we deliver on our commitments? Was support responsive? Were escalations resolved? | [Specific assessment] |
| Competitive | Did a competitor win the business? What did they offer that we did not? | [Specific assessment] |
| Commercial | Was pricing the issue? Did we fail to demonstrate value relative to cost? | [Specific assessment] |
| Customer-side | Did their priorities change? Budget cut? Reorg? Champion departure? | [Specific assessment] |

**Primary root cause:** [The single most important factor]
**Contributing factors:** [Secondary factors that amplified the primary cause]

### 3. Signal Timeline

When did the warning signs appear, and were they detected?

| Date | Signal | Detected? | Action Taken | Outcome |
|------|--------|----------|-------------|---------|
| [date] | [signal -- usage decline, sentiment shift, competitive mention, etc.] | [Yes/No] | [What was done, or "none"] | [Result] |

**Key question:** What was the earliest signal that this account was at risk, and how long before churn did it appear?

### 4. Intervention Assessment

What was tried to save the account:

| Intervention | When | What Happened | Why It Worked / Failed |
|-------------|------|-------------|----------------------|
| [action] | [date -- how many days before churn] | [outcome] | [honest assessment of why] |

**Key question:** Were interventions early enough? Most save plays fail not because the play was wrong but because it started too late.

### 5. Preventability Assessment

| Classification | Definition | This Account |
|---------------|-----------|-------------|
| Preventable | We had the signals, the relationship, and the tools to save this account | [Was it preventable? Why or why not?] |
| Partially preventable | Some factors were within our control but the primary driver was not | [Assessment] |
| Non-preventable | External factors (acquisition, shutdown, strategic pivot) that no intervention could have changed | [Assessment] |

### 6. Systemic Lessons

The most important section. What does this churn teach us about our broader CS operation?

| Lesson | Evidence from This Churn | Portfolio Implication |
|--------|------------------------|---------------------|
| [lesson 1] | [what happened here] | [how many other accounts share this vulnerability] |
| [lesson 2] | [what happened here] | [what needs to change in our process, playbook, or coverage model] |

**Examples of systemic lessons:**
- "We detected the competitive signal 3 weeks before churn but had no competitive response playbook. This applies to at least 5 other accounts with similar signals"
- "The champion departed 60 days before renewal and we were single-threaded. We have 12 other accounts that are currently single-threaded with renewals in 90 days"
- "The customer never achieved measurable ROI. Our value reporting process does not cover accounts below EUR 50k ARR, which means 40% of our book has no value evidence"

## Output Format

```
## Churn Post-Mortem: [Account Name]
**ARR Lost:** EUR [amount] | **Tenure:** [months/years] | **Churn Date:** [date]
**Prepared by:** [CSM name] | **Date:** [date]

### Summary
[One paragraph]

### Root Cause
Primary: [root cause with evidence]
Contributing: [secondary factors]

### Signal Timeline
[Completed table]

### Interventions
[Completed table with assessment]

### Preventability
[Classification with rationale]

### Systemic Lessons
[Lessons with portfolio implications]

### Recommendations
1. [Specific change to prevent this pattern -- process, playbook, coverage, or tooling]
2. [Specific change]
```

## Quality Gates

- Is the root cause honest? "They did not see the value" is a symptom. Why did they not see the value? Was the product a poor fit, was enablement insufficient, or did we fail to measure and communicate ROI? Dig deeper
- Does the signal timeline go back far enough? The first signal is rarely close to the churn date. Look back 6-12 months for the early indicators
- Is the preventability assessment honest? The temptation is to classify everything as "non-preventable" to avoid accountability. The learning happens in the preventable and partially preventable categories
- Are the systemic lessons specific and actionable? "We need to do better at retention" is not a lesson. "We need to implement a competitive response playbook and run it on the 5 accounts currently showing competitive signals" is
- Would the CS leadership team learn something from reading this? If the post-mortem only documents what happened without extracting patterns, it is a report, not a learning tool

## Principles

- The post-mortem is for the team, not for the file. If the analysis is written and never discussed, the lesson is not learned. Present the findings. Discuss the systemic implications. Change the process
- Blame is the enemy of learning. A post-mortem that concludes "the CSM should have done X" misses the point. The question is: why did the system not surface X as the right action? What needs to change so the next CSM in the same situation does X automatically?
- Every preventable churn is a process failure, not a people failure. If the signals were there and the CSM did not act, the question is: were the signals visible? Was there a playbook? Did the CSM have the capacity? The system failed before the person did
- Non-preventable churns still teach. A customer who churned because they were acquired and the parent company standardised on a competitor tells you something about concentration risk in accounts owned by PE-backed companies. The lesson exists even when the outcome was inevitable
