---
name: contract-review-assistant
description: Walks through a customer contract to identify key commercial terms, renewal conditions, pricing structure, auto-renewal clauses, termination requirements, and negotiation leverage points. Produces an annotated summary the CSM can use for renewal preparation. Use when asked to review a contract, identify key terms, find renewal clauses, understand pricing structure, prepare for a commercial negotiation, check termination conditions, or when a CSM needs to understand what the contract actually says before a renewal or expansion conversation. Also triggers for questions about contract terms, commercial conditions, pricing clauses, auto-renewal provisions, termination notice periods, or preparing for a contract negotiation.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Contract Review Assistant

Walks through a customer contract and extracts the terms that matter for account management. Most CSMs do not read contracts. The contracts contain information that directly affects renewal strategy, expansion pricing, and the customer's negotiation leverage -- and the CSM is managing the account without this intelligence.

This is not legal advice. It is an operational summary of what the contract says so the CSM can make informed decisions about how to manage the commercial relationship.

## How to Use

Provide the contract content -- paste the relevant sections or describe the terms you know. Focus on:
- Pricing and payment terms
- Contract duration and renewal conditions
- Termination and notice requirements
- Auto-renewal provisions
- Usage or seat limits
- Discount or concession history
- Any special terms or custom clauses

Also provide:
- Account context (what are you preparing for -- renewal, expansion, renegotiation?)
- Any concerns (customer has mentioned pricing, you suspect they will ask for a discount, you want to know your leverage)

## What to Extract

### Section 1: Commercial Structure

| Term | What to Find | Why It Matters |
|------|-------------|---------------|
| Contract value | Total ARR, any variable components, payment terms (annual, quarterly, monthly) | Your baseline for any commercial conversation |
| Pricing model | Per-seat, per-usage, flat rate, tiered | Determines how expansion is priced and whether usage changes affect the commercial relationship |
| Seat/usage limits | Licensed seats, usage caps, overage provisions | If the customer is over their limit, you have expansion leverage. If under, they have reduction leverage |
| Discount history | Any discounts applied, their duration, conditions for renewal of the discount | Discounts that expire at renewal create pricing shock. Know this before the conversation |
| Price escalation clause | Annual price increase provisions (CPI-linked, fixed %, at company's discretion) | If the contract allows a price increase, you have leverage. If it locks pricing, you do not |

### Section 2: Renewal and Termination

| Term | What to Find | Why It Matters |
|------|-------------|---------------|
| Contract term | Initial term, renewal term | How long the customer is committed for |
| Auto-renewal | Does the contract auto-renew? What are the conditions? | If auto-renewal applies and the customer does not give notice, the contract continues. This is significant leverage |
| Notice period | How much notice must the customer give to not renew or terminate? (Typically 30-90 days) | If the notice period has passed without the customer giving notice, they may be contractually committed to the renewal. Know this |
| Termination for cause | What constitutes "cause" for early termination? What happens if the customer wants out early? | SLA breaches, material failures, or extended outages may give the customer grounds for early termination |
| Termination for convenience | Can the customer terminate without cause? What are the penalties? | Some contracts allow early termination with a cancellation fee. Know whether this exists and what it costs them |
| Renewal pricing | Is renewal pricing locked, negotiable, or at the company's discretion? | This determines your pricing flexibility at renewal |

### Section 3: Service Commitments

| Term | What to Find | Why It Matters |
|------|-------------|---------------|
| SLA provisions | Uptime guarantees, response time commitments, remedies for SLA breach | If you have breached SLAs, the customer has contractual leverage. Know this before they raise it |
| Support level | What support tier is included? Is premium support an add-on? | The customer may be expecting support that their contract does not include |
| Implementation commitments | Any commitments made during the sales process that were formalised in the contract | Unfulfilled implementation commitments are liabilities in a renewal conversation |

### Section 4: Negotiation Intelligence

Based on the contract review, the skill identifies:

**Your leverage:**
- Auto-renewal with passed notice period (customer may be contractually committed)
- Price escalation clause (you can increase pricing within the contract terms)
- High switching cost relative to contract value
- Customer exceeding usage/seat limits (they are getting more than they paid for)
- Strong ROI evidence (value exceeds cost)

**Their leverage:**
- Expiring discount (they expected the discount to continue)
- Active SLA breaches (you failed to meet commitments)
- Unfulfilled implementation promises
- Usage well below licensed capacity (paying for more than they use)
- Competitive alternatives available at lower price
- Termination for convenience clause with low penalties

**Neutral factors:**
- Standard terms (nothing unusual, no special leverage either way)
- Market-rate pricing (not significantly above or below alternatives)

## Output Format

```
## Contract Review: [Account Name]
**Reviewed by:** [CSM name] | **Date:** [date]
**Review purpose:** [Renewal prep / Expansion pricing / Renegotiation / General awareness]

### Commercial Structure
| Term | Details | Implication |
|------|---------|------------|
| ARR | EUR [amount] | [context] |
| Pricing model | [model] | [how expansion would be priced] |
| Licensed seats | [seats] vs. [actual usage] | [over/under and what that means] |
| Discounts | [details] | [expiry date and renewal impact] |
| Price escalation | [clause details] | [available increase and conditions] |

### Renewal and Termination
| Term | Details | Implication |
|------|---------|------------|
| Auto-renewal | [Yes/No] -- [conditions] | [whether customer has given notice] |
| Notice period | [days] -- [deadline date] | [has it passed?] |
| Renewal pricing | [terms] | [your flexibility] |
| Termination provisions | [details] | [customer's exit options] |

### Negotiation Position
**Your leverage:**
- [Point 1 with contract reference]
- [Point 2 with contract reference]

**Their leverage:**
- [Point 1 with contract reference]
- [Point 2 with contract reference]

### Recommended Approach
[Based on the contract terms and the negotiation position, what approach should the CSM take into the renewal or commercial conversation?]

### Items to Confirm
[Things in the contract that the CSM should verify with their finance or legal team before the conversation]
```

## Quality Gates

- Did you identify the auto-renewal and notice period? These are the two most commercially significant terms in any CS context. Missing them is like going into a negotiation without knowing the deadline
- Is the negotiation intelligence honest about both sides? If you only identified your leverage without acknowledging theirs, you will be surprised when they raise their points
- Are the implications specific to this renewal? "Standard terms" is not an implication. "Auto-renewal applies and the notice window passed on February 15, meaning the customer is contractually committed to the renewal unless they argue termination for cause" is
- Have you flagged items to confirm with legal or finance? The CSM should not make contractual commitments based solely on this review. Identify the items that need internal verification before the conversation

## Principles

- Read the contract before the renewal conversation, not during it. A CSM who does not know the contract terms is negotiating blind. The customer may know their contract better than you do
- Auto-renewal is your friend until it is your enemy. It provides leverage when the customer missed the notice window. But relying on auto-renewal to retain a dissatisfied customer is a short-term win that creates a long-term problem. The contract keeps them this year; the relationship keeps them next year
- Never lead with contractual leverage in a conversation. "You missed the notice period so you have to renew" is legally accurate and relationally destructive. Use the leverage as a safety net, not as a weapon. Lead with value
- Discount history is the most overlooked contract intelligence. If the customer received a 20% discount in the initial sale and the discount expires at renewal, the customer expects to pay 20% less than you expect. Address this early -- do not let pricing shock happen in the renewal meeting
