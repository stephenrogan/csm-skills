---
name: escalation-brief-writer
description: Writes structured escalation documents that get the right people to act on a customer issue. Includes the headline, timeline, customer impact, resolution attempts, specific ask, and commercial context. Use when asked to write an escalation brief, document an escalation, prepare an internal escalation report, structure a request for engineering or product help, or when a customer issue needs to be routed to a team that has no context on the account. Also triggers for questions about escalation documentation, internal issue briefs, cross-functional requests, or how to write an escalation that actually gets acted on.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Escalation Brief Writer

Writes escalation documents that get results. The difference between an escalation that is acted on in 4 hours and one that sits in a queue for a week is usually the quality of the brief -- not the severity of the issue.

Most escalation briefs fail because they describe the problem without giving the receiving team enough context to act. This skill produces briefs that are self-contained: anyone reading it for the first time can understand the situation, the impact, the urgency, and exactly what is needed.

## How to Use

Provide:
- What happened (the specific issue, not a category)
- When it started and what has happened since (timeline)
- What the customer impact is (in their terms, not in your terms)
- What you have already tried (every resolution attempt and its outcome)
- What you need from the receiving team (specific, not "please help")
- The commercial context (ARR, renewal proximity, strategic importance)
- What the customer knows and expects (their current understanding and timeline expectation)

## Brief Structure

### 1. Headline (5 Seconds to Understand)

One line that answers: what is happening, to whom, and what is at stake.

**Bad:** "Customer issue -- needs attention"
**Good:** "API latency affecting Acme Corp -- P1 open 12 days, EUR 85k ARR, renewal in 67 days"

The headline should be understandable by someone who has never heard of this account. If the recipient needs to read the entire brief to understand the headline, the headline failed.

### 2. Customer Impact (Their Language, Not Yours)

What this means for the customer's business. Not "the feature is broken" but "their analytics team cannot run reports, costing them an estimated 4 hours per week in manual workarounds."

| Bad Framing | Good Framing |
|------------|-------------|
| "API is slow" | "API latency >3s makes dashboard queries unusable. Their analytics team of 15 has reverted to manual reporting" |
| "Feature is not working as expected" | "The export function fails for files >50MB. Customer processes 200+ files/week at that size. They have no workaround" |
| "Customer is unhappy" | "Customer has raised this in 3 separate conversations over 10 days. Champion's patience is running out -- verbatim: 'If this is not fixed by end of week, we need to discuss alternatives'" |

### 3. Timeline (Chronological, Concise)

Every event from first occurrence to now. Each entry: date, what happened, outcome.

```
Feb 26: Customer reported API latency >3s on dashboard queries
Feb 27: Support ticket #4521 opened, classified P2. Initial investigation: no server-side issue found
Mar 01: Escalated to P1 after customer confirmed issue affects 15 users across the analytics team
Mar 05: Engineering identified potential database query optimisation. Fix estimated 3-5 days
Mar 10: Fix not yet deployed. Customer increasingly frustrated. CSM requested this escalation
```

### 4. Resolution Attempts (What Has Already Been Tried)

This prevents the receiving team from re-trying approaches that have already failed.

| Attempt | Date | Outcome |
|---------|------|---------|
| Server-side cache flush | Feb 27 | No improvement |
| Customer-side browser cache clear | Feb 28 | Temporary improvement, issue returned within hours |
| Database query review | Mar 05 | Root cause identified. Fix in development |

### 5. Specific Ask (Not "Please Help")

The single most important section. What exactly do you need, from whom, by when.

**Bad:** "Please help resolve this issue"
**Good:** "I need engineering to deploy the database query optimisation fix and confirm API response time returns to <500ms for dashboard queries. Target: March 14"

Include the definition of "resolved" from the customer's perspective -- not from your internal metrics.

### 6. Customer Communication Status

What the customer has been told, what they expect, and their current sentiment.

| Element | Content |
|---------|---------|
| What they know | "Engineering has identified the root cause and a fix is in development" |
| What they expect | "Resolution by end of this week" |
| Current sentiment | "Patient but firm. Champion said if not resolved by Friday, they will raise with their VP" |
| What they do not know | "That the fix has been delayed by 5 days. They need to be updated" |

### 7. Commercial Context

Why this matters beyond the immediate issue.

| Element | Data |
|---------|------|
| ARR | EUR 85,000 |
| Renewal date | May 16 (67 days) |
| Strategic importance | Mid-market reference account. Active case study in pipeline |
| Revenue at risk | Full ARR if unresolved before renewal conversation |
| Expansion context | Was discussing 15-seat expansion before this issue surfaced. Expansion is now paused |

## Routing Guidance

| Issue Type | Route To | Brief Emphasis |
|-----------|---------|---------------|
| Product defect | Engineering via support | Technical detail, reproduction steps, scope of impact |
| Feature gap | Product management | Business case, customer count affected, competitive context |
| Service failure | CS leadership + support leadership | Pattern evidence, SLA breach data, relationship impact |
| Commercial dispute | CS leadership + finance | Contract terms, customer's position, recommended resolution |
| Relationship crisis | CS leadership | Political context, stakeholder dynamics, recommended approach |

## Output Format

```
## Escalation Brief: [Account Name]
**Severity:** [P1/P2/P3] | **Route to:** [team]
**Headline:** [one line]

### Customer Impact
[2-3 sentences in the customer's terms]

### Timeline
[Chronological event list]

### Resolution Attempts
[What has been tried and outcome of each]

### Specific Ask
[What you need, from whom, by when, and definition of resolved]

### Customer Communication
[What they know, expect, and feel]

### Commercial Context
[ARR, renewal, strategic importance, revenue at risk]
```

## Quality Gates

- Does the headline tell the story in one line? Test: if the recipient only reads the headline, do they understand the urgency and scope?
- Is the customer impact described in business terms, not technical terms? The receiving team needs to understand why this matters, not just what is broken
- Is every resolution attempt documented? Duplication of failed attempts wastes time and frustrates the customer
- Is the ask specific with a deadline? "Please prioritise" is not an ask. A named action with a target date is
- Is the commercial context present? Engineering and product teams rarely see the revenue dimension. Providing it changes their prioritisation calculus

## Principles

- The escalation brief is an advocacy document. You are advocating for your customer to an internal team that has competing priorities. The brief must make the case for why this issue deserves their attention now
- Clarity is speed. A clear brief gets acted on faster than a vague one, regardless of severity. The 15 minutes you spend writing a good brief saves days of back-and-forth clarification
- Include everything the receiving team needs to act without asking you a single follow-up question. If they need to come back to you for the timeline, the reproduction steps, or the commercial context, the brief was incomplete
- Update the brief as the situation evolves. An escalation is not a single document -- it is a living record. Add entries to the timeline as new information emerges. The brief should always reflect the current state
