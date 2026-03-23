---
name: objection-handler
description: Provides structured response frameworks for common CS objections including pricing challenges, feature gaps, competitive comparisons, adoption resistance, and value questioning. Produces multiple response options calibrated to the relationship context. Use when asked to handle an objection, respond to a customer pushback, prepare for a difficult commercial conversation, address a customer concern about pricing or features, or when a CSM faces pushback and needs a structured approach to responding. Also triggers for questions about objection handling, customer pushback, difficult questions from customers, or preparing responses to common CS challenges.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Objection Handler

Provides structured response frameworks for the objections every CSM faces. Not scripts -- frameworks that help you understand what the customer is actually saying, what is driving it, and how to respond in a way that addresses the real concern, not just the surface objection.

## How to Use

Provide:
- The objection (what the customer said)
- The context (when they said it, what was happening in the conversation)
- The account context (health, renewal proximity, relationship strength)
- What you think is really driving it (the stated reason is often not the real reason)

## The Objection Diagnosis Framework

Every objection has a surface statement and an underlying driver. The response must address the driver, not just the statement.

### Pricing Objections

**"It is too expensive"**

| Underlying Driver | Signal | Response Approach |
|------------------|--------|------------------|
| Budget constraint (real) | Budget cut announced, hiring freeze, cost reduction mandate | Empathise. Explore flexible terms (annual to quarterly, reduced scope, deferred payment). Frame as "how do we make this work within your constraints" not "here is why it is worth it" |
| Value perception gap | They cannot articulate what they get for the money | Value problem, not a pricing problem. Build the ROI case. "Let me show you what your team has achieved this quarter and what that is worth in terms of time and productivity" |
| Competitive benchmark | "Competitor X is 30% cheaper" | Do not panic. "What are you comparing? Same scope, same support, same capabilities?" Then reframe from price to total value |
| Negotiation tactic | No evidence of real budget pressure. Asking because it often works | Hold firm with confidence. "The pricing reflects the value we deliver. Let me make sure the value case is clear" |
| Anchor effect | They got a discount last time and expect it again | Address directly. "The initial pricing reflected an introductory incentive. Renewal pricing is based on the demonstrated value -- which has grown since you started" |

### Feature Gap Objections

**"You do not have X feature"**

| Underlying Driver | Signal | Response Approach |
|------------------|--------|------------------|
| Genuine blocker | The missing feature is preventing a critical workflow | Acknowledge honestly. If on the roadmap: share the timeline. If not: explore workarounds. If no workaround: be honest about the gap rather than overpromising |
| Leverage for negotiation | Feature mentioned during a pricing discussion | Separate the conversations. "Let me address the feature gap independently -- I want to make sure we solve that regardless of the commercial discussion" |
| Competitor comparison | "Competitor X has this" | "I understand they offer that capability. Can you help me understand how you would use it? I want to make sure I am comparing the right things" |
| Unfamiliarity | The feature exists but they do not know about it | "Actually, we do have that -- let me show you. It might be configured under a different name than you expected" |
| Aspirational | Nice to have, not a dealbreaker | Acknowledge. "That is on our radar. In the meantime, here is how teams in your segment solve that problem with our current capabilities" |

### Adoption Objections

**"My team is not using it"**

| Underlying Driver | Signal | Response Approach |
|------------------|--------|------------------|
| Training gap | Team does not know how to use the product effectively | Offer targeted enablement. "Let me run a session with the team on [specific workflow]. Most teams see adoption improve significantly after hands-on training" |
| Change resistance | Team prefers the old way. No management mandate to switch | This is a change management conversation, not a product conversation. "What would your team need to feel comfortable making the switch?" Help the champion build the internal case |
| Product friction | Team tried it and found it too complex, too slow, or too different from their existing workflow | Investigate the specific friction. "Can you tell me what they tried and where they got stuck? I want to understand whether this is a UX issue we can address or a workflow mismatch" |
| Wrong users | The people who have access are not the people who would benefit most | Reassess the user allocation. "Who on your team would benefit most from this? We may need to redirect the licences to the right people" |

### Value Objections

**"I am not sure we are getting enough value"**

| Underlying Driver | Signal | Response Approach |
|------------------|--------|------------------|
| No measurement | They genuinely do not know the value because nobody has measured it | Build the case together. "Let me pull the data and we can review it. I think you might be getting more value than you realise -- but let me prove it rather than claim it" |
| Comparison to expectation | They expected more based on the sales process | Acknowledge the gap honestly. "What were you expecting to achieve by now that has not happened? Let me understand the gap and we will build a plan to close it" |
| Champion cannot justify internally | They see the value but cannot articulate it to their CFO | Help them build the internal case. "I can prepare a value summary that you can share with your leadership. What format would be most useful?" |
| Value has actually declined | Product changes, team changes, or priority shifts have reduced the product's relevance | Honest conversation. "It sounds like the value equation has changed. Can we discuss what has shifted and whether we can realign?" |

### Relationship Objections

**"We do not feel supported"**

| Underlying Driver | Signal | Response Approach |
|------------------|--------|------------------|
| Service failure | Unresolved tickets, slow responses, dropped commitments | Own it. Do not defend. "I hear you. Let me review what happened and come back with a specific plan to address it" |
| Expectation mismatch | They expected enterprise-level service on a mid-market contract | Reset expectations while improving what you can. "Here is what our support model includes at your tier. Within that model, here is what I am committing to" |
| CSM turnover | Multiple CSM changes, loss of continuity | Acknowledge the disruption. "I understand the transitions have been frustrating. I am committed to being your CSM going forward and I want to earn your trust" |
| Feeling deprioritised | They sense they are not a top account | Show them they are valued. Increase cadence temporarily. Deliver something proactive. "I want to make sure you feel the level of support matches what you expect" |

## Response Structure

For every objection, the response follows three steps:

1. **Acknowledge** -- show you heard them. Do not argue, defend, or immediately counter. "I understand your concern about the pricing" or "That is fair feedback about the support experience"
2. **Diagnose** -- understand what is really driving it. Ask a question before responding. "Can you help me understand what is behind that?" or "What would need to be true for you to feel confident in the value?"
3. **Respond** -- address the underlying driver with a specific action. Not a promise, not a defence -- an action. "Let me build the ROI analysis and present it next week" or "I am going to review the support history and come back with a specific improvement plan by Friday"

## Output

For each objection, the skill produces:
- The objection diagnosed (what the customer said vs. what is likely driving it)
- 2-3 response options calibrated to the likely driver
- Questions to ask before responding (to confirm the diagnosis)
- What not to say (common mistakes for this objection type)
- Follow-up actions (what to do after the conversation)

## Quality Gates

- Did you diagnose before responding? Responding to the surface objection without understanding the driver addresses the wrong problem
- Is the response specific to this account? "The product delivers great value" is generic. "Your team saved 340 hours this quarter through workflow automation" is specific
- Does the response include an action, not just words? Every objection response should end with something you commit to doing -- not just something you said
- Did you avoid being defensive? The instinct when challenged is to defend. The effective response is to acknowledge and redirect

## Principles

- Objections are information, not attacks. A customer who raises a concern is telling you what matters to them. That is more valuable than a customer who says nothing and quietly leaves
- The first response to any objection is a question, not an answer. "Can you tell me more about that?" or "What would need to change?" gives you the information to respond effectively
- Never argue with the customer's perception. If they feel the product is too expensive, telling them they are wrong does not change their feeling. Showing them the value might
- The best objection handling happens before the objection. A customer with strong value evidence, deep adoption, and a multi-threaded relationship raises fewer objections. Prevention is more effective than response
