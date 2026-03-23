---
name: change-management-advisor
description: Provides a structured framework for helping customers drive internal adoption of your product within their organisation. Addresses resistance, stakeholder alignment, communication strategy, and phased rollout planning from the CSM's perspective as an external advisor. Use when asked to help a customer with change management, advise on internal adoption strategy, address resistance to product adoption, plan a team rollout, or when adoption is stalling not because of the product but because of the customer's organisational readiness. Also triggers for questions about customer change resistance, internal adoption blockers, rollout planning, or how to help customers get their teams to actually use the product.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Change Management Advisor

Provides a framework for helping customers overcome internal adoption resistance. The most valuable consultative skill in a CSM's toolkit -- and the one most CSMs lack because it requires understanding organisational psychology, not just product knowledge.

The insight: when adoption stalls, the problem is rarely the product. It is that the people who need to use the product have not been given a reason to change, a path to follow, or support along the way. The CSM's role is not to fix this for the customer -- it is to advise them on how to fix it themselves.

## How to Use

Provide:
- The adoption challenge: what should be happening that is not?
- Who is affected: which teams, roles, or individuals are not adopting?
- What you know about why: technical barriers, lack of training, resistance to change, competing tools, no mandate from leadership
- The customer's internal dynamics: who champions the product, who is indifferent, who is actively resistant
- What has been tried: training sessions, emails from leadership, incentives, mandates
- The customer's timeline and urgency

## The Adoption Blockers Framework

Adoption failures have five root causes. Most stalled rollouts involve 2-3 of these simultaneously:

| Blocker | Signal | What It Actually Means |
|---------|--------|----------------------|
| Awareness | "I did not know we had this tool" / "What does it do?" | The rollout communication failed. People cannot adopt what they do not know exists |
| Relevance | "This does not apply to my work" / "I do not see how this helps me" | The value proposition was not translated to this role's specific workflows. Generic "this tool is great" messaging does not drive adoption |
| Ability | "I tried it and could not figure it out" / "It is too complex" | Training was insufficient, the UX is too complex for this audience, or the product requires configuration they do not have |
| Motivation | "I have my own system" / "The old way works fine" | No compelling reason to change. The cost of switching (learning curve, disruption) exceeds the perceived benefit |
| Reinforcement | "I used it for a week but went back to the old way" / "Nobody else on my team uses it" | There is no accountability, no social proof, and no ongoing support. Behaviour change requires more than a one-time training |

## Diagnostic Process

### Step 1: Identify the Blocker(s)

Ask the customer (or help them ask their team):

| Question | What the Answer Reveals |
|----------|----------------------|
| "Does every target user know the product exists and what it does?" | Awareness |
| "Can each target user explain how it applies to their specific daily work?" | Relevance |
| "Has every target user completed the training and can they perform the core workflows independently?" | Ability |
| "What would each target user lose by not using it, or gain by using it?" | Motivation |
| "What happens if someone stops using it after the initial rollout?" | Reinforcement |

If the customer cannot answer these questions about their own team, that is the first gap to address.

### Step 2: Map the Stakeholder Landscape

Every adoption initiative has four stakeholder groups:

| Group | Their Role | What They Need |
|-------|----------|---------------|
| Sponsors | Leadership who approved the investment. They want adoption to succeed but are not driving it day-to-day | Visibility into adoption progress, evidence that the investment is paying off, and a plan that does not require their daily attention |
| Champions | Internal advocates who believe in the product and influence their peers | Tools and data to make the case to their colleagues. Recognition. A communication plan they can execute |
| Resistors | People who actively prefer the old way or oppose the change | Understanding of what they would gain (not what the company gains). Acknowledgement that their current process has value. A transition path that does not feel like starting over |
| Bystanders | People who will use whatever they are told to use but will not drive adoption independently | Clear instructions, a mandate from their manager, and a low-friction path to getting started |

The CSM's advisory role: help the customer's sponsor and champion develop a strategy that activates bystanders and addresses resistors. The CSM does not manage the customer's internal politics -- they provide the framework and the product expertise.

### Step 3: Build the Adoption Plan

For each blocker identified, recommend a specific intervention:

| Blocker | Intervention | CSM's Role | Customer's Role |
|---------|-------------|-----------|----------------|
| Awareness | Internal communication campaign -- email from sponsor, team meeting announcement, Slack channel | Provide the messaging framework and value narrative | Execute the communication through their internal channels |
| Relevance | Role-specific value mapping -- show each role how the product applies to their daily workflow | Help build the role-specific use cases and materials (pa-enablement-orchestrator content) | Present the materials to each team with their manager's endorsement |
| Ability | Targeted training by role, with hands-on practice, not just a demo | Deliver or support the training sessions. Provide self-serve resources | Ensure attendance. Provide time for training. Support post-training practice |
| Motivation | Visible quick wins, management accountability, and peer evidence | Surface usage data that shows early adopters getting results. Provide benchmarks | Have managers set expectations. Celebrate early wins publicly. Make adoption part of performance |
| Reinforcement | Ongoing support, regular check-ins, usage monitoring, and a feedback loop | Provide adoption tracking data. Flag regressions. Offer refresher sessions | Maintain the accountability structure. Address regressions through management, not through nagging |

### Step 4: Define the Rollout Phasing

Advise the customer against "big bang" rollouts (everyone starts on the same day) unless the product is trivially simple:

| Phase | Who | Duration | Purpose |
|-------|-----|----------|---------|
| Pilot | 5-10 enthusiastic users (champions and willing early adopters) | 2-4 weeks | Prove the value, identify friction, build internal case studies |
| Wave 1 | One full team or department | 2-4 weeks | Demonstrate team-level adoption, build playbook for subsequent waves |
| Wave 2+ | Additional teams, one at a time | 2-4 weeks each | Expand with the learnings from prior waves |
| Full rollout | Remaining users | 2-4 weeks | Complete with bystander activation and resistor conversion |

Each phase should produce:
- Usage data showing adoption and value
- Testimonials from adopters (internal social proof)
- A refined training approach based on what worked and what did not
- Identified issues to resolve before the next wave

### Step 5: Provide Ongoing Advisory

The CSM's advisory continues throughout the rollout:
- Share adoption data regularly (from pa-adoption-tracker or manually)
- Flag regressions early (users who adopted then stopped)
- Suggest adjustments to the plan based on what the data shows
- Help the champion prepare progress updates for the sponsor

## Output Format

```
## Adoption Advisory: [Account Name]

### Situation
[Description of the adoption challenge]

### Blocker Diagnosis
| Blocker | Present? | Evidence | Severity |
|---------|----------|----------|----------|
| Awareness | [Yes/No] | [Evidence] | [H/M/L] |
| Relevance | [Yes/No] | [Evidence] | [H/M/L] |
| Ability | [Yes/No] | [Evidence] | [H/M/L] |
| Motivation | [Yes/No] | [Evidence] | [H/M/L] |
| Reinforcement | [Yes/No] | [Evidence] | [H/M/L] |

### Stakeholder Map
[Sponsors, Champions, Resistors, Bystanders -- with names if known]

### Recommended Interventions
[Matched interventions per blocker with CSM and customer responsibilities]

### Rollout Plan
[Phased approach with timeline]

### CSM Advisory Cadence
[How often the CSM will check in on adoption progress and what data to review]
```

## Quality Gates

- Did you diagnose the blocker(s) before prescribing interventions? "Do more training" is the default prescription. It only works if the actual blocker is Ability. If the blocker is Motivation, more training is wasted effort
- Is the plan achievable by the customer, not just by you? The CSM advises. The customer executes. If the plan requires the CSM to manage the customer's internal communication, training, and accountability, it will not scale and it will not stick
- Does the plan address resistors specifically? Ignoring resistors does not make them neutral. It makes them quietly effective at undermining adoption
- Is there a phased approach? All-at-once rollouts fail more often than phased rollouts because there is no learning loop and no internal social proof
- Does the plan include reinforcement? Adoption without reinforcement decays. If there is no mechanism for ongoing accountability, adoption will revert within 90 days

## Principles

- Adoption is a change management problem, not a product problem. The product is a tool. People adopt tools when the cost of the old way exceeds the cost of the new way. Your job is to help make that calculus clear
- The CSM is an advisor, not a project manager. You do not manage the customer's internal rollout. You provide the framework, the data, and the product expertise. They provide the organisational authority, the internal communication, and the accountability
- Motivation is the hardest blocker to solve because it requires something the CSM cannot provide: internal leadership commitment. If the customer's leadership will not mandate or incentivise adoption, no amount of training or communication will drive sustained usage
- Quick wins create momentum. Do not design a 6-month adoption programme before showing value in week 2. Find the simplest, most visible win and build from there
