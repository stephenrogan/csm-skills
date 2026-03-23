---
name: escalation-decision-framework
description: Helps a CSM decide whether to escalate an issue, when to escalate, to whom, at what severity, and how to frame it. Distinct from the escalation-brief-writer (which structures the escalation document) -- this skill helps with the judgment call of whether escalation is the right move. Use when asked to decide whether to escalate, determine the right escalation level, assess whether an issue warrants internal attention beyond the CSM, or when a CSM is unsure whether a customer issue is "bad enough" to escalate. Also triggers for questions about escalation judgment, severity assessment, when to involve leadership, whether to escalate or handle it yourself, or how to decide the right escalation level.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Escalation Decision Framework

Helps with the judgment call: should I escalate this, and if so, to whom? The skill addresses the decision, not the documentation. Most CSMs either escalate too late (waiting until the situation is critical) or too rarely (absorbing issues they should not be absorbing alone).

## How to Use

Provide:
- The issue (what is happening)
- The customer impact (how it affects their business)
- What you have tried (your resolution attempts so far)
- The account context (ARR, health, renewal proximity, strategic importance)
- Your gut feel (do you think you can resolve this, or do you need help?)

## The Escalation Decision Matrix

Score the situation on four dimensions:

| Dimension | 1 (Low) | 3 (Medium) | 5 (High) |
|-----------|---------|-----------|----------|
| Customer impact | Inconvenience. Workaround exists. No business disruption | Moderate disruption. Workaround is painful. Some business impact | Severe disruption. No workaround. Direct business or revenue impact |
| Account value | <EUR 10k ARR, non-strategic | EUR 10-50k ARR or moderate strategic value | >EUR 50k ARR or high strategic value (logo, reference, board-level) |
| Time sensitivity | Can be addressed within normal cadence (1-2 weeks) | Needs resolution within days | Needs resolution today. Delay creates compounding damage |
| CSM capability | You can resolve this with existing resources and authority | You need input or resources you do not have, but the issue is defined | The issue is beyond your expertise, authority, or access. You cannot resolve it alone |

**Decision logic:**

| Score Range | Decision |
|------------|---------|
| 4-8 | Handle it yourself. Standard CSM resolution. No escalation needed |
| 9-13 | Escalate for support. You need resources, not rescue. Route to the appropriate team with a clear ask |
| 14-17 | Escalate with urgency. This requires attention beyond your level. Route to CS leadership and the relevant functional team |
| 18-20 | Escalate immediately. Executive-level attention. Same-day routing to CS leadership and potentially CRO |

## Escalation Routing Guide

| Issue Type | Route To | When |
|-----------|---------|------|
| Product defect (technical) | Engineering via support platform | When the issue cannot be resolved through standard support channels within SLA |
| Feature gap blocking the customer | Product management | When the gap is affecting retention and there is no workaround |
| Service failure (SLA breach, repeated issues) | CS leadership + support leadership | When the pattern indicates a systemic problem, not a one-off |
| Commercial dispute (billing, contract, pricing) | CS leadership + finance | When the customer disputes terms the CSM cannot resolve |
| Relationship at risk (trust damage, champion frustration) | CS leadership | When the relationship damage exceeds what the CSM can repair alone |
| Executive intervention needed | CRO or CEO office (via CS leadership) | When the situation requires a peer-level response from your leadership |
| Cross-functional coordination | Relevant team leads | When the resolution requires coordinated action across teams the CSM does not control |

## Common Escalation Mistakes

| Mistake | Why It Happens | How to Avoid |
|---------|---------------|-------------|
| Escalating too late | CSM tries to handle everything themselves. By the time they escalate, the customer is furious and the issue is entrenched | Set a personal "if I cannot resolve this in [X] days, I escalate" rule. The threshold depends on severity |
| Escalating too broadly | CSM panics and involves everyone. Leadership, engineering, product, support -- all get the same message | Route to one team with a specific ask. Others can be informed later if needed |
| Escalating without context | CSM says "customer is unhappy, please help" without providing the history, the ask, or the commercial context | Use the escalation-brief-writer skill to structure the brief before routing |
| Escalating instead of communicating | CSM escalates internally but does not tell the customer what is happening. The customer feels ignored | Always communicate with the customer in parallel: "I have escalated this to [team] and expect an update by [date]" |
| Not escalating because "it is not that bad" | CSM underestimates the severity because they are too close to the situation | Ask yourself: "If my manager heard about this from the customer instead of from me, would they be surprised?" If yes, escalate |
| Escalating as a complaint, not an ask | CSM describes the problem but does not say what they need | Every escalation must include a specific ask: "I need engineering to investigate [X] and provide a fix or timeline by [date]" |

## Output Format

```
## Escalation Assessment: [Account Name]

### Situation
[2-3 sentences: what is happening]

### Scoring
| Dimension | Score | Rationale |
|-----------|-------|-----------|
| Customer impact | [1-5] | [why] |
| Account value | [1-5] | [why] |
| Time sensitivity | [1-5] | [why] |
| CSM capability | [1-5] | [why] |
| **Total** | **[4-20]** | |

### Decision
[Handle yourself / Escalate for support / Escalate with urgency / Escalate immediately]

### If Escalating
- Route to: [team/person]
- Specific ask: [what you need]
- By when: [deadline]
- Customer communication: [what the customer needs to hear, and when]
```

## Quality Gates

- Did you score all four dimensions honestly? The temptation is to underweight "CSM capability" because admitting you need help feels uncomfortable. Asking for help early is a sign of judgment, not weakness
- Is the specific ask clear? If you are escalating, the receiving team should know exactly what you need from them. "Help" is not an ask
- Have you communicated with the customer? An internal escalation without a customer communication is half an escalation. They need to know you are taking action

## Principles

- Escalation is a tool, not a failure. A CSM who escalates appropriately is demonstrating judgment. A CSM who never escalates is either handling everything (unlikely for a large portfolio) or absorbing issues they should not be
- The customer should never find out about an escalation before you tell them. If they hear from engineering before they hear from you, you have lost control of the narrative
- Speed of escalation matters more than perfection of documentation. A brief escalation today is better than a detailed escalation next week. You can supplement the brief once the escalation is in motion
- The "would my manager be surprised?" test is the best escalation heuristic. If the answer is yes, escalate. If the answer is "probably not, but I'm not sure," escalate. If the answer is definitely not, handle it yourself
