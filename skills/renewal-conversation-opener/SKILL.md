---
name: renewal-conversation-opener
description: Frames the initial renewal conversation by leading with value delivered, transitioning to forward-looking partnership, and anticipating likely objections based on account context. Produces multiple opening approaches calibrated to the account's health, relationship, and commercial situation. Use when asked to prepare for a renewal discussion, draft a renewal email, frame a renewal conversation, open a retention dialogue, or when a CSM needs to move from relationship management to commercial conversation. Also triggers for questions about renewal preparation, retention conversation strategy, renewal email drafting, or how to start the renewal discussion with a customer.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Renewal Conversation Opener

Frames the opening of the renewal conversation. The goal is not to "close" the renewal in one interaction -- it is to set the right tone, lead with value, and create the conditions for a productive commercial discussion.

The renewal conversation starts the moment the CSM first mentions renewal. That moment shapes the customer's framing of the entire process. Lead with what they have gained, not with what you are asking for.

## How to Use

Provide:
- Account name, ARR, renewal date, days remaining
- Account health (strong, healthy, at risk, critical)
- Value delivered (metrics, outcomes, ROI -- whatever you have)
- Key stakeholders involved in the renewal decision
- Known risks or concerns (pricing, feature gaps, competitive signals, champion changes)
- Expansion opportunity (if any -- seat growth, tier upgrade, cross-sell)
- Prior renewal history (smooth renewals? Negotiated last time? First renewal?)

## Approach Selection

The skill produces 2-3 opening approaches because renewal conversations are not one-size-fits-all. The right approach depends on the relationship, the account health, and the commercial context.

### Approach 1: The Value-Led Opener

**Best for:** Healthy accounts with strong value evidence. The renewal should be straightforward.

**Structure:**
1. Open with the headline value metric (lead with what they gained, not what you want)
2. Briefly acknowledge the partnership and key milestones
3. Transition to the forward look: what value is available next
4. Introduce the renewal as the mechanism to continue and expand the value
5. Propose timing for the commercial discussion

**Tone:** Confident, consultative, forward-looking. The renewal is a natural continuation, not an event.

**Example framing:**
"Your team saved an estimated 340 hours this quarter through automated workflows -- up 22% from last quarter. As we approach [renewal date], I wanted to discuss how we build on that momentum next year and make sure you have everything you need. Can we set aside 30 minutes next week to talk through the renewal and what the next 12 months could look like?"

### Approach 2: The Partnership Opener

**Best for:** Accounts where the relationship is strong but value evidence is thin. Or accounts where the personal relationship matters more than the data.

**Structure:**
1. Acknowledge the relationship and history
2. Reference specific moments that demonstrate partnership (not generic "we value our partnership")
3. Frame the renewal as a checkpoint for alignment, not a transaction
4. Ask what their priorities are for the next period before presenting your view
5. Propose a conversation to align on the future

**Tone:** Warm, relationship-first, collaborative. The renewal is a conversation about where you go together.

**Example framing:**
"We have been working together for [X months/years] and I have genuinely valued the partnership -- especially [specific moment: launching the API integration, navigating the Q3 migration, supporting the team expansion]. With the renewal coming up in [X days], I would love to hear what your priorities look like for the next 12 months so we can make sure we are set up to support them. Can we schedule a conversation?"

### Approach 3: The Problem-Solving Opener

**Best for:** At-risk accounts, accounts with known concerns, or accounts where addressing the elephant in the room is more credible than ignoring it.

**Structure:**
1. Acknowledge the situation directly (do not pretend things are fine if they are not)
2. Reference what you have done to address concerns (specific actions, not promises)
3. Frame the renewal as an opportunity to reset and commit to improvement
4. Ask what would need to be true for them to feel confident renewing
5. Propose a conversation with that agenda

**Tone:** Honest, accountable, forward-looking. The renewal is a chance to get things right.

**Example framing:**
"I know the last quarter has not been smooth -- the API performance issues affected your team's workflow and I understand the frustration. We have [specific action: deployed the fix, restructured your support escalation path, brought in a dedicated technical resource]. With the renewal in [X days], I want to have an honest conversation about where we stand and what we need to commit to for you to feel confident going forward. What would that conversation need to cover?"

## Objection Anticipation

Based on the account context, the skill identifies likely objections and prepares responses:

| Likely Objection | Trigger Signal | Prepared Response Framework |
|-----------------|---------------|---------------------------|
| "It is too expensive" | Budget pressure, pricing mentioned in prior conversations | Lead with value delivered (ROI > cost). Then explore: is it a budget issue or a value perception issue? Each has a different path |
| "We are not using it enough" | Low adoption, underutilised features | Acknowledge the gap. Offer an adoption plan. Frame the renewal as the commitment to fix this, not a reward for the current state |
| "We are looking at alternatives" | Competitive signals, evaluation language | Do not panic. Understand the trigger. Address the root cause, not the competitor |
| "We need a discount" | Prior negotiation history, budget cycle timing | Establish value before discussing price. Ask what is driving the request. Never discount without understanding why |
| "The timing is not right" | Budget cycle mismatch, internal reorganisation | Offer flexibility on timing (if your contract allows). The goal is renewal, not renewal on your preferred date |
| "I need to involve [new person]" | Stakeholder change, champion departure | Good -- you want the decision-maker in the conversation. Ask for an introduction. Do not view this as a delay; view it as alignment |

## Channel Guidance

| Situation | Channel | Why |
|-----------|---------|-----|
| Healthy account, straightforward renewal | Email opener, then call | Email sets the frame. Call has the discussion |
| At-risk or complex renewal | Call first, then email to confirm | Difficult conversations should happen in real-time, not in writing |
| Expansion included with renewal | Meeting (not just a call) | Expansion requires a proper discussion with data. A phone call is too brief |
| Executive involved | Executive-to-executive outreach from your leadership, supported by your preparation | Executives respond to peers. Your prep arms your leader; their leader receives the outreach |

## Output

For each approach, the skill produces:
- The opening message (email or call script)
- Anticipated objections with response frameworks
- Suggested next steps after the opener
- A flag if any critical information was missing: "Note: no value metrics provided -- the value-led approach will be generic without data"

## Quality Gates

- Does the opener lead with value or acknowledgement, never with the ask? "Your renewal is coming up" as the first sentence is a negotiation opener, not a partnership conversation
- Is the approach honest about the account's situation? A value-led opener on an account with declining health is tone-deaf. A partnership opener on an account you barely touch is hollow
- Is there a specific ask at the end? "Let's talk" is vague. "Can we schedule 30 minutes next week to discuss the renewal and your Q2 priorities?" is actionable
- Does the objection preparation match the account's actual risk signals? Preparing for a discount negotiation on an account that has never raised pricing is wasted effort. Preparing for a competitive conversation on an account with active competitive signals is essential

## Principles

- The renewal conversation is not when you start demonstrating value. It is when you present the evidence you have been building all year. If you arrive at renewal without value evidence, the conversation will be harder regardless of the opener
- Renewals are not events. They are the last mile of a relationship that has been building (or eroding) since day one. The opener reflects the relationship -- it does not create one
- The customer knows the renewal is coming. They have been thinking about it. Your opener should acknowledge that shared awareness and frame the conversation as collaborative, not adversarial
- Silence from the customer approaching renewal is a risk signal, not a sign that everything is fine. If they are not engaging, the opener needs to address why, not pretend it is not happening
