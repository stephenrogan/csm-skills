---
name: competitive-threat-assessor
description: Evaluates the severity of a competitive threat on a specific account by assessing the evaluation stage, trigger, relationship strength, and switching cost. Produces a threat classification with a response framework. Use when asked to assess a competitive signal, evaluate a competitive threat, determine how serious a competitor situation is, prepare a competitive response, or when a customer has mentioned evaluating alternatives. Also triggers for questions about competitive analysis on a specific account, handling competitor mentions, responding to customer evaluations, or assessing the risk of losing an account to a competitor.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Competitive Threat Assessor

Evaluates how serious a competitive threat is on a specific account and produces a structured response framework. Turns "the customer mentioned a competitor" from a panic event into a assessed, actionable situation.

The key insight: competitive threats are symptoms, not causes. A customer evaluating alternatives has an unmet need. Your job is to find and address the need, not to fight the competitor.

## How to Use

Provide:
- Account name, ARR, renewal date
- What competitor was mentioned (or "unknown -- they said they are looking at alternatives")
- How you learned about it (customer told you directly, heard from champion, noticed in a support ticket, third-party intelligence)
- What triggered the evaluation (product gap, pricing, service failure, proactive competitor outreach, new leadership with a prior vendor preference)
- Your relationship strength (strong, adequate, thin, strained)
- Account health (strong, healthy, at risk, critical)
- How far you think the evaluation has progressed (early consideration, active evaluation, decision imminent)
- Any other relevant context (new stakeholder, budget pressure, reorg)

## Assessment Framework

### Step 1: Classify the Threat

Score each dimension on a 1-5 scale:

| Dimension | 1 (Low Threat) | 3 (Moderate) | 5 (High Threat) |
|-----------|----------------|--------------|-----------------|
| Evaluation stage | Casual mention, no active evaluation | Active comparison, demo scheduled or completed | Decision imminent, contract presented |
| Trigger severity | Proactive competitor outreach (customer was not looking) | Product gap or pricing concern (addressable) | Service failure or trust damage (relationship-based) |
| Competitor fit | Competitor is weaker for this use case | Competitor is comparable | Competitor is stronger for the specific need that triggered the evaluation |
| Relationship strength | Deep multi-threaded relationship with executive coverage | Adequate relationship, champion supportive | Thin or strained, single-threaded, champion departed |
| Switching cost | High (deep integrations, trained team, embedded workflows) | Moderate (some integrations, moderate training) | Low (standalone tool, minimal configuration, easy to replace) |
| Time pressure | Renewal 6+ months out | Renewal 60-180 days out | Renewal under 60 days |

**Composite threat score** = average of 6 dimensions.

| Score | Classification | Interpretation |
|-------|---------------|---------------|
| 1.0-2.0 | Low | Monitor. The customer is not actively pursuing alternatives. Reinforce value proactively |
| 2.1-3.0 | Moderate | Act within 2 weeks. Investigate the trigger, reinforce value, address the gap |
| 3.1-4.0 | High | Act this week. Dedicated save strategy required. Consider executive engagement |
| 4.1-5.0 | Critical | Act today. Executive involvement, commercial flexibility, and root cause intervention required |

### Step 2: Diagnose the Root Cause

The response depends on why they are evaluating, not who they are evaluating:

| Root Cause | Response Focus | What to Avoid |
|-----------|---------------|--------------|
| Product gap | Address the gap: roadmap if planned, workaround if possible, honest acknowledgement if neither | Do not dismiss the gap. "We are working on it" without a timeline is worse than "we do not have that today" |
| Pricing | Establish value first, then discuss pricing. Compete on ROI, not sticker price | Do not discount reflexively. Understand whether the issue is budget, value perception, or competitive pricing |
| Service failure | Acknowledge, recover, rebuild. The competitor did not win -- you lost. Win back by being better | Do not deflect blame or minimise the failure |
| Proactive competitor outreach | The customer was not looking. Reinforce the relationship and make the competitor's pitch irrelevant | Do not overreact. The customer took a meeting; they did not make a decision |
| New leadership with prior preferences | Build the relationship with the new person on your product's merits. Do not fight their history | Do not badmouth their prior vendor. Respect their experience and show what your product does for this team |
| Strategic priority shift | Reposition your value in the context of their new priorities. If it genuinely does not fit, be honest | Do not contort your product to fit a use case it does not serve. Honesty builds long-term credibility even in a loss |

### Step 3: Assess Your Competitive Position

For the specific capabilities the customer cares about (not a generic feature matrix):

| Dimension | Your Position | Competitor Position | Implication |
|-----------|--------------|-------------------|------------|
| [Capability 1] | [Your strength/weakness] | [Their strength/weakness] | [What this means for the customer] |
| [Capability 2] | [Your strength/weakness] | [Their strength/weakness] | [What this means for the customer] |

Be honest with yourself. If the competitor is stronger in the area that triggered the evaluation, saying "we are better overall" does not address the customer's specific need. Address the specific gap, not the general landscape.

### Step 4: Calculate Switching Cost

Not for sharing with the customer, but for your assessment:

| Factor | This Account |
|--------|-------------|
| Integrations to rebuild | [count and complexity] |
| Users to retrain | [count] |
| Workflows to reconstruct | [count and complexity] |
| Data to migrate | [volume and complexity] |
| Productivity loss during transition | [estimated weeks] |
| Total estimated switching cost | [time and money] |

High switching costs favour you -- the customer's perceived pain of leaving may exceed their perceived pain of staying. But never rely on switching costs as your retention strategy. They buy time, not loyalty.

### Step 5: Build Response Plan

Based on the assessment:

```
## Competitive Response Plan: [Account Name]

**Threat Classification:** [Low/Moderate/High/Critical]
**Root Cause:** [What triggered the evaluation]
**Competitor:** [Named or unknown]
**Evaluation Stage:** [Early/Active/Decision imminent]
**Renewal Date:** [Date] ([X] days)

### Response Strategy
[2-3 sentences on the overall approach based on root cause and stage]

### Immediate Actions (This Week)
1. [Specific action with owner]
2. [Specific action with owner]

### 30-Day Plan
1. [Action to address root cause]
2. [Action to reinforce value]
3. [Action to strengthen relationship]

### Executive Engagement
- Needed: [Yes/No]
- If yes: [Who from your side, who from their side, what framing]

### Commercial Flexibility
- Available without approval: [What you can offer]
- Requires approval: [What needs escalation]
- Do not offer preemptively: [Discounting before understanding the full situation weakens your position]

### Decision Criteria
- Win signal: [What would indicate the customer is staying]
- Loss signal: [What would indicate you are losing]
- Walk-away point: [When the cost of retention exceeds the value of the account]
```

## Quality Gates

- Did you diagnose the root cause before planning the response? Responding to a pricing threat with a product demo is a waste of everyone's time
- Is the competitive analysis specific to what this customer cares about? A generic feature comparison is not useful. A comparison on the 2-3 capabilities that triggered the evaluation is
- Are you being honest about where the competitor is stronger? Self-deception in competitive analysis leads to responses that miss the point
- Is the response plan actionable within the timeline? A 30-day plan on an account with 20 days to renewal is too slow
- Have you considered the possibility that you might lose? Not every account is saveable. If the switching cost is low, the competitor is stronger on the triggering need, and the relationship is thin, the honest assessment may be "invest time proportionally and prepare for the loss"

## Principles

- The customer is not the enemy. They are evaluating alternatives because they have a need. Your job is to address the need, not to prevent the evaluation. You cannot control whether they look at competitors. You can control whether they find what they are looking for in your product
- Never badmouth the competitor. It makes you look insecure and gives the competitor credibility. Instead: "I am not going to speak to what [competitor] does or does not do. What I can tell you is how we address [specific need]"
- Speed matters. The longer a competitive evaluation runs without your intervention, the more the customer invests in the alternative (sunk cost, relationship building, internal advocacy). Early engagement is higher-leverage than late engagement
- Some accounts are not worth saving at any cost. If the account is low-ARR, the relationship is thin, and the competitor is a better fit, the most strategic move may be a graceful exit that preserves the relationship for potential future return
