---
name: nps-response-analyser
description: Analyses an NPS score and verbatim response to produce a structured interpretation with recommended follow-up by score band. Goes beyond the number to extract actionable insight from the verbatim and match it to the account context. Use when asked to interpret an NPS response, analyse survey results, determine follow-up for a promoter or detractor, make sense of an NPS verbatim, or when an NPS score arrives and the CSM needs to decide what to do about it. Also triggers for questions about NPS follow-up strategy, survey response interpretation, promoter activation, detractor recovery, or what an NPS score means for a specific account.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# NPS Response Analyser

Takes an NPS score and verbatim response and produces an actionable interpretation matched to the account context. Most companies collect NPS and do nothing useful with individual responses. This skill ensures every response triggers the right follow-up.

## How to Use

Provide:
- NPS score (0-10)
- Verbatim response (the text the customer wrote)
- Who responded (name, role, contact classification if known)
- Account context (ARR, health, tenure, renewal date, recent events)
- Prior NPS scores from this account (if available -- trend matters more than the number)

## Score Band Framework

### Promoters (9-10)

**What it means:** The respondent is actively satisfied. They would recommend your product. This is not just a number -- it is permission to activate the relationship.

**Interpretation by verbatim quality:**

| Verbatim Type | Interpretation | Follow-Up |
|-------------|---------------|-----------|
| Specific and enthusiastic ("Your automation features have transformed how we work") | Strong advocacy candidate. The verbatim itself is testimonial material | Thank them within 48 hours. Ask what they value most. Assess advocacy readiness (ca-advocacy-tracker). The verbatim may be usable as a testimonial with permission |
| Brief and positive ("Good product") | Satisfied but not passionate. Will recommend if asked but will not advocate proactively | Thank them. Ask a follow-up question to deepen: "What specifically makes it work for your team?" |
| High score but no verbatim | Satisfaction is real but unexplored. You do not know what drives it | Thank them. Ask what they value most. This is an information gap you need to close |
| High score with a caveat ("Love it but wish you had X") | Satisfied with a specific improvement request | Thank them. Address the request: acknowledge, share roadmap status if relevant, log as product feedback |

**Timing:** Follow up within 48 hours. The goodwill from a promoter score has a half-life. Waiting a week signals you do not care about their feedback.

**What not to do:** Do not immediately ask for a G2 review or a reference call. Thank them and explore first. The advocacy ask comes later, once you understand what makes them a promoter.

### Passives (7-8)

**What it means:** Satisfied enough not to leave, not satisfied enough to advocate. The most underserved score band -- most companies ignore passives because they are not in crisis. But passives are one bad experience away from becoming detractors and one great experience away from becoming promoters.

**Interpretation by verbatim quality:**

| Verbatim Type | Interpretation | Follow-Up |
|-------------|---------------|-----------|
| Specific improvement suggestion ("Good but reporting could be better") | They know exactly what would make them a 9 or 10. This is a roadmap for earning their loyalty | Thank them. Ask: "If we improved [specific thing], would that change your experience materially?" Then act on the answer |
| Vague ("It is fine") | Satisfaction without enthusiasm. The product is meeting minimum expectations but not exceeding them | Thank them. Probe: "What would make this a 9 or 10 for you?" The answer reveals the gap between adequate and excellent |
| No verbatim | You know nothing except they are mildly satisfied. The most common and least useful response | Follow up in person: "I noticed your NPS response -- thank you. I want to make sure we are meeting your expectations. What could we be doing better?" |

**Timing:** Follow up within 72 hours. Passives are not urgent but are important.

**The opportunity:** Passives are the highest-leverage NPS band to influence. Moving a passive to a promoter (by addressing their specific gap) is more achievable than saving a detractor and has a direct impact on your NPS metric.

### Detractors (0-6)

**What it means:** The respondent is unhappy. The severity varies dramatically across the band -- a 6 may be mildly disappointed while a 0 may be actively hostile. The verbatim tells you which.

**Interpretation by verbatim quality:**

| Verbatim Type | Interpretation | Follow-Up |
|-------------|---------------|-----------|
| Specific, constructive criticism ("Support is too slow and we cannot get issues resolved") | They are frustrated but still communicating. The frustration is about a specific, addressable issue | Acknowledge within 24 hours. Address the specific issue. Do not defend -- fix. This customer may be saveable if you act fast |
| Angry or hostile ("This product is terrible and we regret buying it") | Deep dissatisfaction. This may or may not be saveable depending on the root cause | Acknowledge within 24 hours. Do not respond with data or defence -- respond with empathy and a commitment to investigate. Escalate to your manager. This is a churn risk |
| Brief and dismissive ("Not great" or just the score with no verbatim) | Disengaged. Not angry enough to explain why, which may be worse than anger -- it suggests they have stopped caring | Follow up in person, not by email. "I saw your survey response and I want to understand what is driving it. Can we talk?" |
| Score 0-3 with no verbatim | The lowest scores with no explanation are the most concerning. This person may have already made their decision | Immediate CSM follow-up. This is a risk signal equivalent to a competitive mention. Treat it with the same urgency |

**Timing:** Within 24 hours. Every hour without acknowledgement compounds the frustration.

**Critical rules for detractor follow-up:**
1. Do not email a defence of the product. Call them
2. Do not share their score with other contacts at the account. The response is confidential
3. Do not challenge their score ("We are surprised by your rating given that..."). Respect their perspective
4. Do not wait for a plan before acknowledging the feedback. Acknowledge first, plan second

## Trend Analysis

A single score is a data point. Multiple scores over time are a trend. The trend is more important than the number:

| Trend | Interpretation | Action |
|-------|---------------|--------|
| Improving (6 to 8 to 9) | Whatever you are doing is working. The customer is becoming more satisfied | Continue current approach. Ask what drove the improvement -- reinforce it |
| Stable promoter (9, 9, 10) | Strong, consistent satisfaction. Reliable advocacy candidate | Maintain the relationship. Activate for advocacy if not already |
| Stable passive (7, 7, 8) | Consistently adequate. Not growing into a promoter | Investigate the gap to 9. Something specific is holding them back |
| Declining (9 to 7 to 6) | Something is eroding satisfaction. The current score is less important than the direction | Urgent investigation. What changed between the periods? When did the decline start? |
| Volatile (6, 9, 5, 8) | Inconsistent experience. The product or service is unpredictable | Investigate what drives the highs and lows. Stabilise the experience before trying to improve the score |

## Output Format

```
## NPS Analysis: [Account Name]
**Score:** [0-10] | **Band:** [Promoter/Passive/Detractor]
**Respondent:** [Name, Role]
**Verbatim:** "[their response]"
**Date:** [date]

### Interpretation
[2-3 sentences: what this score and verbatim mean in the context of this account]

### Trend
[If prior scores available: trajectory and what it means]

### Recommended Follow-Up
- Action: [specific next step]
- Channel: [call/email/in-person]
- Timing: [within X hours/days]
- Framing: [how to approach the conversation]

### Account Implications
[What this means for the account's health, renewal, or relationship trajectory]

### Flags
[Risk flag if detractor / Advocacy opportunity if promoter / Improvement opportunity if passive]
```

## Quality Gates

- Is the follow-up specific to the verbatim, not generic to the score band? A promoter who praised automation and a promoter who praised support get different follow-ups. The score is the same; the insight is different
- Is the timing appropriate? Detractors within 24 hours. Promoters within 48 hours. Passives within 72 hours. Anything longer and the feedback feels ignored
- Does the follow-up avoid arguing with the score? The customer's perception is their reality. You do not get to tell them they are wrong
- Have you considered the respondent's role? A detractor score from an end user who had a bad support experience is different from a detractor score from the champion who controls the renewal decision. Both matter but the urgency and approach differ

## Principles

- NPS is a conversation starter, not a metric to manage. The number matters less than what you do with it. A company that responds to every NPS response with genuine follow-up outperforms a company that obsesses over the aggregate score
- The verbatim is the treasure. The score tells you the sentiment. The verbatim tells you why. If there is no verbatim, the follow-up must discover the why
- Detractor responses are gifts. A customer who tells you they are unhappy is giving you a chance to fix it. A customer who says nothing and quietly does not renew gave you no chance at all. Treat every detractor response as a second chance, not as a problem
- Never tie NPS follow-up to a commercial ask. The survey response is feedback, not a sales signal. The follow-up should serve the customer's interest, not yours. If the follow-up reveals an advocacy or expansion opportunity, pursue it separately -- not in the NPS follow-up conversation
