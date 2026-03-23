---
name: onboarding-plan-builder
description: Creates a structured customer onboarding plan with phased milestones, success criteria, timeline, and responsibility assignments. Adapts by segment and complexity. Use when asked to build an onboarding plan, structure a customer kickoff, create an implementation timeline, design a go-live plan, or when a new customer needs a clear roadmap from contract signing to value realisation. Also triggers for questions about customer onboarding structure, implementation planning, kickoff preparation, time-to-value planning, or how to set up a new customer for success from day one.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Onboarding Plan Builder

Creates a phased onboarding plan that gets a new customer from contract signing to measurable value as fast as possible. The onboarding period is the highest-risk and highest-opportunity phase of the customer lifecycle -- the patterns set in the first 90 days predict the next 3 years.

## How to Use

Provide:
- Account name, ARR, product tier, segment
- What they bought (which products/modules, how many seats)
- Their goals (why they bought -- what outcomes they expect)
- Implementation complexity (integrations needed, data migration, custom configuration)
- Key contacts (champion, technical lead, executive sponsor, project manager on their side)
- Target go-live date (if committed) or desired timeline
- Any special circumstances (replacing a competitor, seasonal urgency, parallel initiatives)

## Onboarding Phases

### Phase 1: Kickoff and Planning (Days 1-7)

**Objective:** Align on goals, timeline, responsibilities, and success criteria before any implementation begins.

| Milestone | Deliverable | Owner | Success Criteria |
|-----------|-----------|-------|-----------------|
| Welcome and introduction | Welcome email sent, CSM introduced, expectations set | CSM | Customer confirms receipt and understanding |
| Kickoff call | 45-60 minute call covering goals, timeline, roles, success criteria | CSM + Customer | Goals and timeline documented and agreed by both sides |
| Onboarding plan shared | Written plan with milestones, dates, and owners | CSM | Customer approves the plan |
| Technical requirements gathered | Integration needs, data migration scope, configuration requirements documented | CSM + Technical Lead | All technical prerequisites identified |

**Kickoff call agenda:**
1. Introductions and roles (5 min)
2. Customer goals: what does success look like in 90 days? (10 min)
3. Product overview: what they have access to and how it maps to their goals (10 min)
4. Timeline and milestones: the onboarding roadmap (10 min)
5. Responsibilities: what you will do, what they need to do (5 min)
6. Next steps and questions (5 min)

### Phase 2: Technical Setup (Days 7-30)

**Objective:** Get the product technically ready for use -- integrations live, data migrated, configurations complete.

| Milestone | Deliverable | Owner | Success Criteria |
|-----------|-----------|-------|-----------------|
| Accounts and access provisioned | All users have access with correct permissions | CSM / Ops | All licensed users can log in |
| Integrations configured | CRM, email, calendar, or other integrations live and syncing | Technical Lead + Customer IT | Data flowing correctly between systems |
| Data migration complete | Historical data imported and validated | Technical Lead + Customer | Data is accurate and accessible in the product |
| Configuration complete | Workflows, templates, and settings configured for their use case | CSM + Customer | Configuration matches their stated requirements |
| Technical validation | Customer confirms the setup is correct and functional | Customer Technical Lead | Sign-off on technical readiness |

### Phase 3: Adoption and Training (Days 14-60)

**Objective:** Move from "the product is set up" to "the team is using it."

| Milestone | Deliverable | Owner | Success Criteria |
|-----------|-----------|-------|-----------------|
| Admin training | Product admin(s) trained on configuration and management | CSM / Enablement | Admin can manage settings, users, and configuration independently |
| End-user training | Core users trained on daily workflows | CSM / Enablement | Users can complete core workflows independently |
| First workflow completed | Team completes their first real workflow in the product (not a test) | Customer team | Real work is happening in the product |
| Adoption checkpoint | Usage review at Day 30: who is using it, who is not, what are the barriers | CSM | Adoption rate >50% of licensed users active. Barriers identified for non-adopters |

### Phase 4: Value Realisation (Days 30-90)

**Objective:** Demonstrate measurable value from the investment.

| Milestone | Deliverable | Owner | Success Criteria |
|-----------|-----------|-------|-----------------|
| First value metric | Measurable outcome the customer can point to | CSM + Customer | Customer confirms "yes, this is working" with evidence |
| 60-day review | Formal review of adoption, usage, value, and remaining goals | CSM + Customer | Customer satisfied with progress. Gaps identified and addressed |
| Onboarding close | Transition from onboarding to steady-state management | CSM | All onboarding milestones complete. Success criteria met. Cadence transitions to standard check-in rhythm |
| 90-day assessment | Full assessment: goals achieved, time-to-value, adoption depth, customer satisfaction | CSM | Customer would recommend the onboarding experience. All Phase 1 goals addressed |

## Segment Adaptations

| Segment | Timeline | Complexity | Engagement Level |
|---------|----------|-----------|-----------------|
| Enterprise | 60-120 days | Multiple integrations, data migration, custom configuration, change management | High: weekly calls, dedicated project management, executive check-ins |
| Mid-Market | 30-60 days | Standard integrations, moderate configuration | Medium: bi-weekly calls, milestone-driven check-ins |
| SMB | 14-30 days | Minimal configuration, self-serve setup | Low: kickoff call, 2-3 check-in emails, adoption checkpoint |
| PLG / Self-Serve | 7-14 days (or fully self-serve) | Zero configuration, in-app guidance | Minimal: automated emails, usage-triggered check-ins, human engagement only if the customer is stuck |

## Output Format

```
## Onboarding Plan: [Account Name]
**Start date:** [date] | **Target go-live:** [date]
**ARR:** EUR [amount] | **Segment:** [segment] | **Tier:** [product tier]

### Goals
1. [Customer goal 1 with success metric]
2. [Customer goal 2 with success metric]

### Timeline
| Phase | Dates | Key Milestones |
|-------|-------|---------------|
| Kickoff & Planning | [dates] | Kickoff call, plan agreed |
| Technical Setup | [dates] | Integrations, migration, config |
| Adoption & Training | [dates] | Training complete, first workflow |
| Value Realisation | [dates] | First value metric, onboarding close |

### Responsibilities
| Deliverable | Your Team | Their Team |
|------------|----------|-----------|
| [item] | [who] | [who] |

### Risk Register
| Risk | Mitigation |
|------|-----------|
| [risk] | [plan] |

### Success Criteria
[What "done" looks like for this onboarding]
```

## Common Onboarding Failures

| Failure | Root Cause | Prevention |
|---------|-----------|-----------|
| Technical setup stalls | Customer IT team is not prioritising the integration work | Set expectations in kickoff: "We need X from your team by [date]. If this slips, the timeline slips" |
| Training attendance is low | Users do not see the relevance or their manager did not mandate attendance | Get the champion or executive sponsor to mandate attendance. Frame training as "getting started with the tool that will save your team X hours" |
| No measurable value by Day 60 | Goals were not specific enough to measure | Define measurable success criteria in the kickoff. "You will know onboarding succeeded when [specific metric]" |
| Champion goes dark during onboarding | They are busy, distracted, or less engaged than expected | Set a weekly cadence. If they miss 2 scheduled touchpoints, escalate to their manager or executive sponsor |
| Scope creep | Customer wants more configuration, more integrations, more customisation than planned | Scope is defined in Phase 1. Additions are welcome but extend the timeline. Manage expectations explicitly |

## Quality Gates

- Does every milestone have a success criterion? "Training complete" is not a milestone -- "Users can complete core workflows independently" is
- Are responsibilities assigned to named people? "Their team will handle it" is not an assignment. "[Name] will configure the SSO integration by [date]" is
- Is the timeline realistic? An enterprise onboarding in 14 days is a fantasy. An SMB onboarding that takes 90 days is a failure. Match the timeline to the complexity
- Are the customer's goals captured and measurable? If you cannot measure whether the onboarding achieved its goals, you cannot demonstrate time-to-value -- and time-to-value is the single most important onboarding metric

## Principles

- Onboarding is not a project. It is the foundation of the relationship. The speed, quality, and experience of onboarding shape how the customer perceives every interaction that follows. Get it right
- Time-to-value is the metric that matters. Not time-to-go-live, not time-to-training-complete -- time-to-the-first-outcome-the-customer-cares-about. Everything in the plan should compress this number
- The customer's effort determines the timeline, not yours. The most common onboarding delay is waiting for the customer's team to complete their tasks (data migration, integration configuration, internal approvals). Set expectations early and follow up relentlessly
- A customer who finishes onboarding without a measurable value metric is a customer who enters steady-state management with unproven ROI. That makes every subsequent conversation -- especially the renewal -- harder than it needs to be
