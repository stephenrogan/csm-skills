---
name: expansion-opportunity-scorer
description: Scores expansion readiness for a customer account by assessing adoption depth, value realisation, stakeholder alignment, commercial signals, and timing. Produces a readiness classification with the recommended expansion approach and the specific signal that triggered the assessment. Use when asked to assess expansion potential, evaluate upsell readiness, score an account for growth, determine whether a customer is ready for a commercial conversation about expansion, or when a CSM detects expansion signals and needs to decide whether and how to pursue them. Also triggers for questions about expansion timing, upsell assessment, growth readiness, when to start an expansion conversation, or evaluating whether a customer is ready to buy more.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Expansion Opportunity Scorer

Scores whether a customer account is ready for an expansion conversation and what type of expansion is most likely. The critical distinction: expansion readiness is not the same as expansion interest. A customer who mentions growth is interested. A customer with deep adoption, proven value, executive engagement, and budget availability is ready.

## How to Use

Provide:
- Account name, current ARR, product tier, tenure
- The expansion signal (what triggered this assessment -- seat limit, feature request, new team interest, customer-initiated conversation)
- Adoption depth (feature breadth, usage intensity, active users vs. licensed seats)
- Value evidence (ROI confirmed, outcomes measured, customer-confirmed value)
- Stakeholder alignment (is the expansion champion the same as the economic buyer? Is the decision-maker engaged?)
- Health status (strong, healthy, at risk)
- Commercial context (budget cycle timing, pricing history, contract terms)
- Any blockers (open issues, unresolved concerns, competitive evaluation)

## Expansion Types

| Type | Signal | Typical Value | Complexity |
|------|--------|-------------|-----------|
| Seat expansion | Licence utilisation >85%, new team forming, credential sharing | 10-30% ARR increase | Low -- straightforward addition |
| Tier upgrade | Using features at the ceiling of current tier, requesting capabilities in higher tier | 20-50% ARR increase | Medium -- requires value justification for the price delta |
| Cross-sell (new product) | Customer using one product and expressing needs addressed by another | 30-100% ARR increase | High -- requires new discovery, demo, and business case |
| Usage expansion | Volume-based pricing and usage growing beyond current band | 10-25% ARR increase | Low-Medium -- data-driven conversation |

## Readiness Scoring

Score each dimension 1-5:

| Dimension | 1 (Not Ready) | 3 (Developing) | 5 (Ready) | Weight |
|-----------|-------------|----------------|----------|--------|
| Adoption depth | Shallow usage, low feature breadth, many unused capabilities | Moderate usage, growing adoption | Deep usage, high breadth, users dependent on the product | 25% |
| Value evidence | No ROI measured, value unproven | Data-derived value, not confirmed by customer | Customer-confirmed ROI, quantifiable outcomes | 25% |
| Signal strength | No signal -- CSM-initiated assessment | Indirect signals (usage growth, feature requests) | Direct signal (customer asked about expansion, new team expressed interest) | 20% |
| Stakeholder readiness | Decision-maker not engaged, no commercial relationship | Champion supportive, decision-maker aware but not engaged | Champion actively sponsoring, decision-maker engaged and budget-aware | 20% |
| Health | At risk or declining | Healthy and stable | Strong and improving | 10% |

**Composite readiness score** = weighted sum (1.0-5.0)

| Score | Classification | Meaning | Action |
|-------|---------------|---------|--------|
| 1.0-2.0 | Not ready | Focus on adoption and value realisation before commercial conversations | Deepen adoption. Build value evidence. Revisit in 60-90 days |
| 2.1-3.0 | Developing | Signals exist but foundation is not strong enough for a commercial conversation | Strengthen the weakest dimension. Prepare the ground over the next 30-60 days |
| 3.1-4.0 | Ready | Foundation is strong. Time to initiate the expansion conversation | Build the commercial case. Engage the decision-maker. Propose the expansion |
| 4.1-5.0 | High confidence | Customer is essentially asking for expansion. Execution risk only | Act this week. The conversation is warm. Delaying risks losing momentum or timing |

## The Expansion Conversation Sequence

When readiness score is 3.1+:

### Step 1: Confirm the Need (Consultative, Not Sales)

"I have noticed your team is approaching the seat limit / using features at the ceiling of your tier / expressing interest in [capability]. Can you tell me more about what is driving that?"

**Why consultative:** The CSM who listens to the need first and proposes second builds trust. The CSM who jumps to the upsell proposal loses the advisory position.

### Step 2: Build the Case

Connect the expansion to the customer's stated goals, not to your revenue target.

| Frame | For the Champion | For the CFO |
|-------|-----------------|-------------|
| Seat expansion | "Your team has outgrown the current licence. 15 people sharing 10 seats means queuing and workarounds" | "At current usage, the cost per active user drops with additional seats. The productivity gain per seat exceeds the incremental cost" |
| Tier upgrade | "The advanced features you have been requesting are available in the next tier and would address [specific workflow gap]" | "The tier upgrade adds [specific capabilities] at a [X]% price increase. Based on current usage, the ROI on the upgrade is [X]x" |

### Step 3: Propose and Close

Specific, tied to their timeline, with a clear next step.

"Based on what you have shared, I recommend [specific expansion]. The annual cost would be EUR [X], bringing your total to EUR [Y]. Given your Q2 team growth, I would suggest we aim to have this in place by [date]. Can I put together a formal proposal?"

## Blockers That Kill Expansion

| Blocker | Impact | Resolution Before Proposing |
|---------|--------|---------------------------|
| Unresolved support issue | Customer will not buy more from a vendor that has not fixed what they already bought | Resolve the issue first. Expansion after resolution feels earned |
| Low adoption on current purchase | "Why would we buy more when we do not fully use what we have?" | Drive adoption first. Show them the value of what they already own |
| No value evidence | The CFO will ask "what did we get from the last purchase?" and you cannot answer | Build the value case before the commercial case |
| Decision-maker not engaged | The champion is ready but the person who approves the budget has never heard from you | Engage the decision-maker with value evidence before proposing expansion |
| Competitive evaluation underway | The customer is evaluating whether to stay, not whether to grow | Resolve the competitive situation first. Expansion during evaluation is tone-deaf |

## Output Format

```
## Expansion Assessment: [Account Name]
**Current ARR:** EUR [amount] | **Expansion type:** [type] | **Estimated value:** EUR [amount]

### Readiness Scores
| Dimension | Score | Evidence |
|-----------|-------|---------|
| Adoption depth | [1-5] | [data] |
| Value evidence | [1-5] | [data] |
| Signal strength | [1-5] | [data] |
| Stakeholder readiness | [1-5] | [data] |
| Health | [1-5] | [data] |

### Composite: [X.X] -- [Classification]

### Blockers
[Any blockers and resolution plan, or "None identified"]

### Recommended Approach
[Specific next action based on readiness level]
```

## Quality Gates

- Is the signal real? A CSM projecting expansion hope onto a neutral account wastes commercial effort and risks the relationship. Verify the signal: did the customer indicate interest or are you interpreting usage data optimistically?
- Are blockers identified and addressed? Proposing expansion with an unresolved P1 ticket is self-sabotage
- Is the decision-maker identified and at least aware? An expansion proposal that reaches the champion but never reaches the budget holder stalls indefinitely
- Is the value case built? The expansion conversation is dramatically easier when you can say "your team saved X hours this quarter and the expansion would multiply that"

## Principles

- Expansion is earned, not sold. A customer who sees deep value, has broad adoption, and trusts the CSM will expand naturally. A customer who is pushed to expand before value is proven will resist and resent
- Timing matters as much as readiness. A customer who is ready but in the middle of budget freeze will say no regardless of the score. Align with their budget cycle, not your quarter-end
- The CSM is not a salesperson. The CSM identifies the opportunity, builds the case, and initiates the conversation. If the expansion requires commercial negotiation, involve your sales counterpart at the right moment
- A customer who says "not now" is not saying "never." Document the signal, note the timing constraint, and revisit. The groundwork you laid makes the next conversation easier
