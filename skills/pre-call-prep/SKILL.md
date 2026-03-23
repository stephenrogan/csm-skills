---
name: pre-call-prep
description: Builds a structured pre-call brief from manually provided account context. Produces talking points, questions to ask, risks to address, and a clear call objective. Use when asked to prepare for a customer call, build talking points, create a pre-meeting brief, structure a call agenda, or when a CSM has a call in 30 minutes and needs to walk in prepared. Also triggers for questions about call preparation, meeting readiness, talking point development, or structuring a productive customer conversation.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Pre-Call Prep

Builds a structured brief for any customer call. The 10 minutes you spend preparing determine whether the call advances the relationship or wastes everyone's time.

## How to Use

Provide whatever you know:
- Account name, ARR, health status
- Call type (check-in, QBR, escalation, renewal, first meeting, ad hoc)
- Who is attending (customer contacts and internal team)
- Last touchpoint (what was discussed, any open items)
- Current account situation (health, usage, engagement, open issues)
- What you want to accomplish (the objective of this specific call)
- Anything you are worried about (risk signals, difficult topics, relationship concerns)

## The 5-Minute Brief

For routine calls, the skill produces a 5-minute brief:

```
## Pre-Call Brief: [Account Name]
**Date:** [date] | **Type:** [type] | **Duration:** [expected]

### Call Objective
[One sentence: what does success look like when this call ends?]

### Context (30-Second Refresh)
[Account name] | EUR [ARR] | [Health] | [Renewal: date]
Last touch: [date, what happened]
Open items: [any commitments pending from either side]

### Talking Points (In Priority Order)
1. [Most important topic -- the one you must cover even if the call runs short]
2. [Second priority]
3. [Third priority -- cover if time allows]

### Questions to Ask
- [Question 1 -- genuine information-gathering, not leading]
- [Question 2]

### Watch For
- [Signal to listen for -- competitive mention, sentiment shift, new information]

### Do Not Forget
- [Open item to close, commitment to confirm, or follow-up to mention]
```

## Prep by Call Type

### Check-In Call

| Element | Content |
|---------|---------|
| Objective | Maintain the relationship. Surface any changes. Offer value |
| Lead with | Something specific to their account (usage observation, upcoming event, open item status) |
| Ask about | Their priorities this quarter, any changes, any concerns |
| Avoid | Running through a generic checklist. If you have nothing specific, reconsider whether this call should happen |

### QBR / Business Review

| Element | Content |
|---------|---------|
| Objective | Demonstrate value. Align on direction. Identify expansion or risk |
| Lead with | Value evidence (the headline number they should take away) |
| Prepare | Deck or data (from qbr-content-assembler), discussion questions, strategic recommendation |
| Avoid | Data dump without narrative. QBR is a conversation, not a presentation |

### Escalation / Issue Review

| Element | Content |
|---------|---------|
| Objective | Show accountability. Provide an update. Confirm resolution path |
| Lead with | The update -- what has been done since the last conversation. Do not make them ask |
| Prepare | Timeline, resolution status, next steps, any asks of the customer |
| Avoid | Defensive language. Do not explain why the issue is hard. Explain what is being done |

### Renewal Conversation

| Element | Content |
|---------|---------|
| Objective | Confirm value. Initiate the commercial conversation. Understand their position |
| Lead with | Value delivered (use the value-narrative-builder output) |
| Prepare | Renewal pricing, objection responses (from pricing-conversation-framework), competitive readiness |
| Avoid | Jumping to the commercial discussion before establishing value. Value first, then pricing |

### First Meeting with New Contact

| Element | Content |
|---------|---------|
| Objective | Build the relationship. Understand their priorities. Establish credibility |
| Lead with | A brief introduction and a genuine question about their priorities |
| Prepare | Research on their role and likely concerns (from stakeholder-research-prep) |
| Avoid | Presenting. First meetings should be 70% listening, 30% responding |

## The Call Objective Test

Before every call, write one sentence: "This call is successful if [specific outcome]."

| Good Objectives | Bad Objectives |
|----------------|---------------|
| "Confirm Tom supports the renewal and identify any blockers" | "Discuss the renewal" |
| "Understand Lisa's priorities for Q2 and identify one way our product supports them" | "Check in with Lisa" |
| "Get agreement to schedule a QBR for April" | "Talk about doing a QBR" |
| "Confirm the escalation is resolved from the customer's perspective" | "Follow up on the issue" |

If you cannot write a specific objective, either (a) you need more preparation or (b) the call does not need to happen.

## Output

The skill produces:
- The structured brief (5-minute or full depending on call complexity)
- The call objective (one sentence)
- Talking points in priority order (most important first)
- Questions to ask (genuine, not leading)
- Signals to watch for (competitive, sentiment, political)
- Post-call actions to plan (follow-up email, CRM update, internal debrief if warranted)

## Quality Gates

- Does the brief have a clear objective? Not a topic -- an objective with a definition of success
- Are the talking points prioritised? If the call runs short, will you have covered the most important item?
- Is there at least one genuine question? A call where you only talk and never ask is a presentation, not a conversation
- Are open items from the last touchpoint addressed? Walking into a call without knowing what was promised last time is a credibility failure
- Can you complete this prep in under 10 minutes? If the prep is longer than the call, the tool is not working

## Principles

- Preparation is respect for the customer's time. Walking into a call unprepared wastes 30 minutes of their day. 10 minutes of preparation creates 30 minutes of value
- The objective is the anchor. If the conversation drifts, the objective brings it back. If the customer takes the conversation in a new direction, the objective helps you assess whether that direction is more valuable than what you planned
- Priority order saves bad calls. If the internet drops at minute 15, you have covered the most important topic. If the customer takes the call in a different direction, you covered the critical item before the drift
- The best calls feel like a conversation, not a checklist. The prep provides structure. Your skill as a CSM provides the responsiveness, empathy, and judgment that make the conversation valuable
