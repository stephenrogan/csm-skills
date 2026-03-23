---
name: customer-sentiment-decoder
description: Interprets mixed or contradictory signals from a customer by analysing the gap between what they say, what they do, and what the data shows. Produces a structured interpretation with investigation recommendations. Use when asked to decode customer sentiment, interpret mixed signals, make sense of contradictory behaviour, assess what a customer really thinks, or when a customer's words do not match their actions. Also triggers for questions about reading between the lines, interpreting customer behaviour, understanding contradictory signals, assessing true customer satisfaction, or when something feels off about an account but you cannot pinpoint why.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Customer Sentiment Decoder

Interprets the gap between what a customer says, what they do, and what the data shows. In CS, the most dangerous accounts are not the ones that complain -- they are the ones that say everything is fine while their usage declines and their engagement fades.

This skill helps you see through surface-level signals to the underlying dynamics.

## How to Use

Provide the mixed signals you are observing:
- What the customer says (in meetings, emails, surveys)
- What the customer does (usage, engagement, responsiveness, meeting attendance)
- What the data shows (health score, adoption trends, support history)
- What feels off (your intuition, even if you cannot articulate it -- intuition is pattern recognition)
- Timeline (when did you start noticing the disconnect?)

## The Signal Matrix

Every account produces signals across three channels. When they align, the sentiment is clear. When they diverge, you need to decode:

| Channel | Positive Signal | Negative Signal |
|---------|----------------|-----------------|
| **Says** (explicit statements) | Praises the product, discusses expansion, refers you to others | Complains, raises concerns, mentions alternatives, asks about contract flexibility |
| **Does** (observable behaviour) | Uses the product deeply, attends meetings, responds quickly, introduces new stakeholders | Usage declining, meetings cancelled, responses delayed, champions not available |
| **Data** (measurable metrics) | Health improving, adoption growing, support tickets declining, engagement broadening | Health declining, features abandoned, support escalating, engagement narrowing |

## Divergence Patterns

The interpretation depends on which channels diverge:

### Pattern 1: Says Positive, Does Negative

**Signal:** Customer says "everything is great" but usage is declining, meetings are being shortened or delegated, and response times are increasing.

**What it usually means:**
- The decision to leave has already been made internally and they are being polite while the transition is planned
- The champion is personally satisfied but knows their team is disengaging and does not want to address it
- The champion is conflict-avoidant and will not surface problems until asked directly
- Corporate culture: some organisations never give negative feedback to vendors. Silence and withdrawal are their "no"

**Investigation approach:**
- Ask a direct, specific question: "I have noticed your team's usage of [specific feature] has declined this month. What is driving that?" Do not ask "is everything okay?" -- that invites the polite response
- Talk to someone other than the champion. End users or technical leads may be more candid
- Check for competitive signals. A customer who says positive things while disengaging may be mid-evaluation

**Urgency:** High. This pattern frequently precedes churn by 60-90 days.

### Pattern 2: Says Negative, Does Positive

**Signal:** Customer complains frequently about specific issues, but usage is deep, feature adoption is growing, and they attend every meeting.

**What it usually means:**
- The product is sticky and valuable despite the issues. They complain because they care, not because they are leaving
- They are testing whether you will fix the issues. Complaints are a sign of investment in the relationship, not of departure
- The complainant may not be the decision-maker. They are frustrated as a user but the economic buyer sees the ROI
- In some cultures, direct feedback is how business relationships work. The complaints are data, not threats

**Investigation approach:**
- Take the complaints seriously. Resolve them. Responsive action on complaints strengthens the relationship more than any QBR
- Do not dismiss the negativity because the data is positive. Persistent unresolved complaints erode loyalty over time, even in deeply adopted accounts
- Ask: "If we fixed [specific complaint], what would that change for your team?" This reveals whether the issue is a dealbreaker or a frustration

**Urgency:** Medium. Not an immediate churn risk, but unresolved complaints compound into genuine dissatisfaction.

### Pattern 3: Says Positive, Data Negative

**Signal:** Customer says they are happy, NPS is high, but health score is declining -- usage down, support tickets up, engagement narrowing.

**What it usually means:**
- The champion is disconnected from the day-to-day reality. They think things are fine because nobody has told them otherwise
- The champion left and the replacement says positive things without deep product knowledge
- The product is being deprioritised organisationally even though the individuals you talk to like it. Budget review or reorg is happening in the background
- Seasonal variation: some industries have natural usage dips that look alarming on a dashboard but are normal

**Investigation approach:**
- Surface the data directly: "Your team's satisfaction is important to me, and I have noticed some changes in the usage patterns this quarter. Can we discuss what is driving that?"
- Check whether the champion has visibility into the team's actual usage. Sometimes they do not
- Look at the broader account context: reorg, budget cycle, competing initiatives

**Urgency:** Medium-High. The data is usually right. If the data says the account is declining, believe the data and investigate -- even if the customer says otherwise.

### Pattern 4: Says Negative, Data Positive, Does Positive

**Signal:** Customer has vocal complaints about specific issues, but usage is strong, adoption is growing, and they attend every meeting.

**What it usually means:**
- This is the healthiest "negative" pattern. They are invested enough to complain and engaged enough to keep using
- The complaints are likely actionable product feedback, not relationship signals
- If you fix the issues, this account becomes a strong advocate

**Investigation approach:**
- Prioritise resolving their complaints. This is a customer who tells you what is wrong instead of silently leaving
- Ask for their input on the solution: "If you were designing this feature, what would it look like?" Customers who give product feedback are customers who see a future with your product

**Urgency:** Low to Medium. Not a churn risk. A product improvement opportunity.

### Pattern 5: All Channels Negative

**Signal:** Customer is vocal about dissatisfaction, usage is declining, data is negative, engagement is fading.

**What it usually means:**
- The account is actively at risk. All signals are aligned on a negative trajectory
- This is the clearest signal -- and paradoxically, the most dangerous misread is assuming it is already lost. If they are still communicating, there is still a chance

**Investigation approach:**
- This is a save play, not a decoding exercise. Use the save-play-designer skill

**Urgency:** Critical.

## Output Format

```
## Sentiment Decode: [Account Name]
**Date:** [date]

### Signal Matrix
| Channel | Current Signal | Direction | Confidence |
|---------|---------------|-----------|-----------|
| Says | [Positive/Neutral/Negative] | [details] | [H/M/L] |
| Does | [Positive/Neutral/Negative] | [details] | [H/M/L] |
| Data | [Positive/Neutral/Negative] | [details] | [H/M/L] |

### Pattern Match
[Pattern number and name from above, or "Novel pattern -- does not match standard patterns"]

### Interpretation
[2-3 sentences: what you believe is actually happening based on the signal divergence]

### Investigation Recommendations
1. [Specific question to ask or action to take]
2. [Specific question to ask or action to take]
3. [Specific question to ask or action to take]

### Urgency
[Critical / High / Medium / Low]

### What to Watch Next
[Specific signals that would confirm or disprove your interpretation in the next 2-4 weeks]
```

## Quality Gates

- Are all three channels represented with specific evidence? "Says positive" without a specific quote or reference is too vague to decode
- Is the interpretation a hypothesis, not a conclusion? The decoder produces the most likely interpretation and tells you what to investigate. It does not claim to know the customer's true sentiment with certainty
- Are the investigation recommendations specific and actionable? "Talk to the customer" is not a recommendation. "Ask Tom directly about the usage decline in the Advanced Reporting module during your March 18 check-in" is
- Have you considered at least two possible explanations? The first interpretation that comes to mind is not always the right one. Mixed signals exist precisely because the situation is ambiguous

## Principles

- Behaviour is more honest than words. What the customer does (uses, attends, responds, adopts) is a more reliable signal than what they say. When words and actions diverge, trust the actions
- Data is more honest than behaviour. What the metrics show (usage trends, health trajectory, engagement frequency) is more reliable than any single observation. But data can miss context -- a usage decline during a holiday period is not a risk signal
- Your intuition is data. If something feels off about an account but you cannot point to a specific data point, that feeling is your pattern recognition seeing something the data has not captured yet. Document it, investigate it, and either confirm or disprove it. Do not ignore it
- Mixed signals are an invitation to investigate, not to assume. The worst CSM mistake is interpreting ambiguity in the direction you prefer rather than seeking the truth
