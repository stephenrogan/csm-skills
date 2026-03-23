---
name: internal-debrief-writer
description: Generates an internal-only post-meeting summary that includes context a CSM would never share with the customer -- political observations, relationship assessments, competitive intelligence, strategic notes, and honest sentiment reads. Distinct from follow-up emails (customer-facing) and meeting outcome logs (CRM-facing). Use when asked to write an internal debrief, document internal observations from a meeting, create a confidential post-meeting analysis, capture relationship intelligence, or when a CSM needs to record what they actually think happened versus what they would share externally. Also triggers for questions about internal meeting analysis, confidential account observations, political dynamics documentation, or candid post-meeting notes for the team.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Internal Debrief Writer

Generates the internal-only version of what happened in a meeting. This is where you document what you actually observed -- political dynamics, relationship reads, competitive signals, and the gap between what the customer said and what they meant.

Distinct from:
- **Follow-up email** (cc-email-drafter / follow-up-email-writer): what the customer sees
- **Meeting outcome log** (meeting-outcome-logger): what the CRM sees
- **This debrief**: what your team sees. The unfiltered analysis

## How to Use

After a significant customer meeting, provide:
- What happened (the factual summary -- can be brief since the CRM log captures this)
- What you observed that is not in the formal notes (body language, tone shifts, sidebar comments, things said off the record, the gap between what was said and what was meant)
- Your relationship read (how is the relationship really doing, not how the health score says it is doing)
- Political observations (who has influence, who is aligned, who is resistant, who was notably silent)
- Competitive intelligence (any mentions, hints, or signals about alternatives)
- Strategic assessment (what this meeting means for the account, for the renewal, for expansion)
- What you need from your team (help, resources, executive engagement, product escalation)

## Debrief Structure

### 1. Meeting Headline
One sentence: what was the most important thing that happened?

Not a summary of the agenda. The one insight that changes how you think about this account.

Example: "Tom is supportive but is not going to fight for the renewal without data he can show his CFO."

### 2. What the Customer Said vs. What They Meant

| They Said | What It Likely Means | Confidence | Implication |
|-----------|---------------------|-----------|------------|
| "We are happy with the product" (but did not elaborate) | Surface-level satisfaction. Not passionate enough to advocate. Not dissatisfied enough to leave | Medium | Do not mistake politeness for loyalty. Probe deeper in the next touchpoint |
| "We are looking at our tool stack" | May or may not include your product. Could be routine review or competitive signal | Low-Medium | Ask directly: "Is our product part of that review?" Better to know now |
| "Our priorities have shifted" | The use case you sold into may no longer be the use case they need you for | Medium | Investigate what the new priorities are. Can your product serve them? |
| "Let me think about it" | They have concerns they did not voice. Or they need to consult someone not in the room | Medium | Follow up in 48 hours with a specific question, not a generic "have you had a chance to think?" |

This is not a universal decoder. It is a framework for the CSM to document their specific read on what specific statements meant in the context of this specific relationship.

### 3. Political Landscape Update

Who matters and where they stand:

| Person | Observation | Change from Prior | Implication |
|--------|------------|------------------|------------|
| [name] | [what you observed -- energy, engagement, statements, body language] | [Better/Worse/Same/New] | [What this means for your strategy] |

Specific things to note:
- Who spoke the most? Who was notably silent?
- Who deferred to whom? (Reveals the real hierarchy, not the org chart)
- Did anyone disagree with the group consensus? (Even subtle disagreement is a signal)
- Was there a conversation before or after the meeting that was more revealing than the meeting itself?

### 4. Competitive Intelligence

Any competitive signal from the meeting, even indirect:

| Signal | Strength | Source | Recommended Action |
|--------|---------|--------|-------------------|
| [what you heard or observed] | [Strong/Moderate/Weak] | [Direct statement / Indirect hint / Inference] | [Investigate / Monitor / Prepare response] |

### 5. Strategic Assessment

Your honest read on the account's trajectory:

- **Health reality** (may differ from the health score): [your assessment]
- **Renewal outlook** (your gut, not the forecast model): [your read]
- **Expansion potential** (based on what you heard today): [your assessment]
- **Biggest risk right now**: [one sentence]
- **Biggest opportunity right now**: [one sentence]
- **What changed because of this meeting**: [one sentence]

### 6. Help Needed

What you need from your team, stated directly:

| Need | From Whom | Urgency | Context |
|------|----------|---------|---------|
| [specific ask] | [person or team] | [This week / This month / FYI] | [why you need it] |

## Output Format

```
## Internal Debrief: [Account Name]
**Meeting date:** [date] | **Type:** [type]
**Classification:** [Routine / Significant / Concerning / Urgent]

### Headline
[One sentence -- the most important takeaway]

### Said vs. Meant
[Completed table with your reads]

### Political Landscape
[Completed table with observations and implications]

### Competitive Intelligence
[Any signals, or "None detected"]

### Strategic Assessment
Health reality: [your read]
Renewal outlook: [your read]
Biggest risk: [one sentence]
Biggest opportunity: [one sentence]
What changed: [one sentence]

### Help Needed
[Specific asks with urgency]

### Distribution
[Who should read this -- manager only, manager + leadership, broader CS team]
```

## When to Write a Debrief (vs. Just Logging the Meeting)

Not every meeting needs a full debrief. The guideline:

| Meeting Type | Debrief? | Why |
|-------------|----------|-----|
| Routine check-in, no surprises | No -- meeting outcome log is sufficient | The formal record captures everything meaningful |
| Meeting where something shifted (new information, change in tone, unexpected topic) | Yes | The shift is the story. The formal record does not capture nuance |
| QBR or major business review | Yes | Too much happened to capture in a CRM log. The strategic read matters |
| Escalation or service recovery meeting | Yes | The political dynamics and relationship impact are as important as the resolution |
| First meeting with a new stakeholder | Yes | First impressions and relationship reads need to be documented while fresh |
| Meeting where you detected a competitive signal | Yes | Competitive intelligence decays rapidly. Document it immediately |
| Any meeting that changes your view of the account | Yes | If your assessment changed, document why. Your future self needs this context |

## Quality Gates

- Is the headline genuinely the most important takeaway? Not the first thing discussed -- the most important thing you learned. If the headline could apply to any account, it is too generic
- Is the "said vs. meant" analysis honest? Optimistic interpretation of ambiguous statements is the most common trap. If you are unsure, document the uncertainty rather than choosing the interpretation you prefer
- Is the distribution appropriate? Internal debriefs with sensitive political observations should go to your manager, not to the broader team Slack channel
- Would this debrief be useful to your successor if you left tomorrow? If so, it is well-written. If they would need to ask you to explain it, add more context
- Is there a specific ask in the "Help Needed" section, or is it empty? If you emerged from a significant meeting without needing anything from anyone, either the meeting was routine (and does not need a debrief) or you are not asking for help you should be asking for

## Principles

- Write the debrief within 2 hours. Political reads and relationship observations fade fast. What felt like a clear signal during the meeting becomes a vague impression by the next morning
- This document is for your team, not for you. Write it assuming someone who was not in the meeting needs to understand what happened and what it means. Your manager, your successor, your leadership -- they should be able to read this and act
- Honesty is the entire point. If you sugarcoat the internal debrief the same way you would a customer-facing note, you are defeating the purpose. "I think Tom is going to leave and take the relationship with him" is more useful than "Tom seemed a bit less engaged than usual"
- The debrief is a living document for the account's history. Six months from now, when you are preparing for the renewal and wondering "when did things start to shift?", the debrief trail is where you will find the answer
