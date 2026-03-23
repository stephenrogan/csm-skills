---
name: manual-health-assessment
description: Guided diagnostic that scores account health through structured questions across five dimensions -- usage, engagement, support, sentiment, and commercial health. Produces a health classification with component breakdown and recommended actions. No automated data required -- the CSM's knowledge is the input. Use when asked to assess account health, evaluate a customer's risk level, score an account without a health scoring system, or when a CSM wants a structured way to evaluate where an account stands. Also triggers for questions about account risk, customer health, or portfolio assessment. The entry point to structured health thinking.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Manual Health Assessment

A structured diagnostic that turns your knowledge of an account into a scored health assessment. No CRM integration, no product analytics, no health scoring tool required -- just your answers to 12 questions.

## How to Use

Answer the 12 questions below for a specific account. Be honest -- optimistic assessments produce optimistic scores that miss real risk.

## The Diagnostic

### Usage (Weight: 35%)

**Q1: How actively is the customer using the product?**
- (5) Daily use by the majority of their team, deep feature adoption
- (4) Regular weekly use, good feature breadth
- (3) Moderate use, concentrated among a few users or features
- (2) Sporadic use, declining trend, or concentrated in a single user
- (1) Minimal or no meaningful usage

**Q2: Is usage growing, stable, or declining?**
- (5) Growing -- more users, more features, deeper engagement
- (4) Stable and healthy
- (3) Stable but below where it should be
- (2) Declining gradually
- (1) Declining sharply or collapsed

### Engagement (Weight: 25%)

**Q3: How responsive is your primary contact?**
- (5) Responds within a day, proactively reaches out, engaged partner
- (4) Responds within a few days, attends meetings, engaged
- (3) Responds eventually, attends most meetings
- (2) Slow to respond, misses meetings, hard to engage
- (1) Non-responsive, meetings declined or no-showed

**Q4: How broad is your relationship across the organisation?**
- (5) Multiple engaged contacts across different levels and departments
- (4) 2-3 engaged contacts including a senior stakeholder
- (3) Primarily one contact with occasional access to others
- (2) Single-threaded -- one contact only
- (1) Single-threaded and that contact is disengaging

### Support (Weight: 20%)

**Q5: What does the support experience look like?**
- (5) Minimal tickets, all resolved quickly, customer satisfied with support
- (4) Normal ticket volume, good resolution, no complaints
- (3) Some friction -- slow resolutions, moderate volume, or occasional dissatisfaction
- (2) Elevated tickets, unresolved issues, customer expressing frustration
- (1) Major open issues, support relationship strained, P1 tickets unresolved

**Q6: Are there any unresolved issues that affect the customer's trust?**
- (5) No unresolved issues
- (4) Minor issues that are being actively worked
- (3) One notable issue that has been open too long
- (2) Multiple unresolved issues creating cumulative frustration
- (1) A critical unresolved issue that is actively damaging the relationship

### Sentiment (Weight: 10%)

**Q7: What is the customer's overall attitude toward you and your product?**
- (5) Enthusiastic advocate -- would recommend without hesitation
- (4) Positive -- satisfied and sees value
- (3) Neutral -- neither positive nor negative, transactional
- (2) Negative -- dissatisfied with aspects of the product or service
- (1) Hostile -- actively unhappy, may be looking to leave

### Commercial (Weight: 10%)

**Q8: How does the customer view the ROI of your product?**
- (5) Clearly sees and can articulate the value -- ROI is obvious
- (4) Sees value, generally satisfied with the investment
- (3) Uncertain -- value is assumed but not proven
- (2) Questioning the value -- cost concerns raised
- (1) Believes they are overpaying or not getting value

**Q9: What is the renewal or commercial outlook?**
- (5) Will renew without question, possible expansion
- (4) Likely to renew, no significant concerns
- (3) Renewal is probable but not certain
- (2) Renewal is at risk -- concerns exist
- (1) Renewal is unlikely or customer has indicated intent to leave

### Bonus Modifiers

**Q10: Has there been a champion or sponsor change in the last 90 days?**
- Yes: -5 points from final score
- No: No adjustment

**Q11: Is there an active competitive evaluation?**
- Yes: -10 points from final score
- No: No adjustment

**Q12: Is the renewal within the next 90 days?**
- Yes and at risk: -5 points (urgency amplifier)
- Yes and healthy: No adjustment
- No: No adjustment

## Scoring

### Component Scores
For each component, average the question scores and multiply by 20 to get a 0-100 scale:
- Usage: average of Q1 and Q2, multiplied by 20
- Engagement: average of Q3 and Q4, multiplied by 20
- Support: average of Q5 and Q6, multiplied by 20
- Sentiment: Q7 multiplied by 20
- Commercial: average of Q8 and Q9, multiplied by 20

### Composite Score
Composite = (Usage * 0.35) + (Engagement * 0.25) + (Support * 0.20) + (Sentiment * 0.10) + (Commercial * 0.10) + modifiers from Q10-Q12

### Health Classification

| Score | Classification | Meaning |
|-------|---------------|---------|
| 81-100 | Strong | Healthy account. Maintain cadence, look for expansion |
| 66-80 | Healthy | Solid but watch for early risk signals. Standard management |
| 41-65 | At Risk | One or more components are weak. Investigate and intervene |
| 0-40 | Critical | Multiple components failing. Immediate attention required. Consider save play |

## Output Format

```
## Health Assessment: [Account Name]
**Date:** [date] | **Assessed by:** [CSM name]

**Composite Score:** [score] / 100 -- [Classification]

### Component Breakdown
| Component | Score | Trend | Key Driver |
|-----------|-------|-------|-----------|
| Usage (35%) | [score] | [your assessment] | [primary factor] |
| Engagement (25%) | [score] | [your assessment] | [primary factor] |
| Support (20%) | [score] | [your assessment] | [primary factor] |
| Sentiment (10%) | [score] | [your assessment] | [primary factor] |
| Commercial (10%) | [score] | [your assessment] | [primary factor] |

### Modifiers Applied
- [Champion change: -5 / Competitive eval: -10 / Renewal urgency: -5 / None]

### Recommended Actions
[Based on the weakest components and the overall classification]

### Reassessment Date
[When to re-run this diagnostic -- 30 days for At Risk, 90 days for Healthy, 14 days for Critical]
```

## Important Note

This is a subjective assessment based on your knowledge. It is valuable precisely because it captures what you know that automated systems cannot see. But it is not a substitute for data-driven health scoring when that is available. Use this when you need structure, not when you need precision.

## Quality Gates

- Did you answer every question honestly, including the ones where the honest answer is uncomfortable? The diagnostic only works if you resist the temptation to score optimistically. A health score of 52 that reflects reality is more useful than a score of 72 that reflects hope
- Can you point to specific evidence for each score? "I scored engagement at 6 because their champion responded to my last 3 emails within 24 hours and attended both scheduled calls" is evidence. "I scored it 6 because it feels fine" is not
- Did you apply modifiers where they apply? Champion departure and competitive signals are the two most commonly underweighted factors. If either is present and you did not apply the modifier, reconsider
- Does the overall score match your gut feel? If the math says 74 (Healthy) but your instinct says the account is at risk, trust your instinct and investigate the gap. The diagnostic may be missing something you sense but cannot yet quantify

## Principles

- A structured assessment beats an unstructured one every time. Even a subjective score based on your knowledge is more useful than no score at all -- because it forces you to evaluate each dimension rather than relying on a vague overall impression
- The value is in the component scores, not the composite. Knowing the account is "68" tells you the band. Knowing that usage is strong (82) but engagement is collapsing (35) tells you where to act
- Reassess on schedule. A health assessment that is 6 months old is fiction. At-risk accounts should be reassessed every 14 days. Healthy accounts every 90 days. The cadence matters because accounts change faster than your memory updates
- Use this assessment to challenge your own assumptions. If you score an account as Healthy and then the churn post-mortem reveals it was At Risk for months, the diagnostic shows you where your blind spots were. That is the learning opportunity
