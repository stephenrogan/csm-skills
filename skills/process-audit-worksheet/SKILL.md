---
name: process-audit-worksheet
description: Walks through auditing any CS process for agent-readiness by classifying each step as requiring human judgment (HUMAN) or suitable for agent execution (AGENT). Quantifies the production vs. judgment split and identifies the highest-value automation opportunities. Use when asked to audit a process, assess agent-readiness, classify workflow steps, evaluate what can be automated, or when a CS leader wants to understand how much of a process could be handled by agents. Also triggers for questions about process automation assessment, agent-human classification, workflow audit, operational efficiency analysis, or the agent-ready process model.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Process Audit Worksheet

Audits any CS process by classifying every step as AGENT (can be automated) or HUMAN (requires judgment). The most important operational assessment a CS team can run -- it reveals how much of the CSM's week is spent on work that does not require their expertise.

The governing insight: most CS processes were designed when the only execution engine was a person. Every step carries human time cost regardless of whether it requires human thinking. This audit separates the two.

## How to Use

Provide any CS process in step-by-step form:
- Onboarding workflow, renewal timeline, QBR preparation, escalation protocol, check-in cadence, health review, reporting cycle, handoff sequence -- any documented or undocumented process
- For each step: what happens, who does it, how long it takes, and what judgment (if any) is required

## The Classification Framework

### Step 1: List Every Step

Write out every step in the process, including the ones nobody documents because "everyone knows" them. The undocumented steps are often the most time-consuming.

### Step 2: Classify Each Step

For each step, apply the classification test:

**The test:** If an agent executed this step to a consistent standard using available data, would a senior CSM approve the output without modification?

| Classification | Criteria | Examples |
|---------------|----------|---------|
| AGENT | Step requires no judgment. Follows a defined rule, uses available data, produces a predictable output | Data pulls, CRM updates, email templates, scheduling, report formatting, status tracking, notification sending, field computation |
| HUMAN | Step requires expertise, relationship awareness, strategic thinking, or emotional intelligence | Customer diagnosis, strategic recommendations, escalation decisions, relationship judgment, negotiation, save play design, political navigation |
| HUMAN+ | Step is primarily human but agent-prepared context would significantly improve quality or speed | QBR recommendations (agent assembles data, human writes the strategy), health assessment (agent computes score, human validates and interprets) |

### Step 3: Apply the Pressure Test

The instinct is to classify too many steps as HUMAN. For each HUMAN classification, pressure-test:

| Pressure Test Question | If Yes | If No |
|----------------------|--------|-------|
| Could an agent do this with a clear rule and available data? | Reclassify as AGENT | Confirm as HUMAN |
| Is the "judgment" actually just pattern matching that could be encoded? | Reclassify as AGENT with rules | Confirm as HUMAN |
| Would a template with variable data fields produce an acceptable output? | Reclassify as AGENT | Confirm as HUMAN |
| Does the step require understanding the customer's emotional state, political dynamics, or relationship history? | Confirm as HUMAN | Consider AGENT with human review |
| Does the step involve deciding between options where the right answer depends on context an agent cannot access? | Confirm as HUMAN | Consider AGENT |

### Step 4: Quantify the Split

| Metric | Calculation |
|--------|------------|
| Total steps | Count of all steps in the process |
| AGENT steps | Count classified as AGENT |
| HUMAN steps | Count classified as HUMAN |
| HUMAN+ steps | Count classified as HUMAN+ |
| Agent density | (AGENT + 0.5 * HUMAN+) / Total steps |
| Time on AGENT steps | Sum of estimated time for all AGENT-classified steps |
| Time on HUMAN steps | Sum of estimated time for all HUMAN-classified steps |
| Time reclamation potential | Time currently spent by humans on AGENT-classified steps |

**Typical results:** Most CS processes are 60-80% AGENT-classifiable. That means 60-80% of the time a CSM spends on that process is on work that does not require their judgment.

## Output Format

```
## Process Audit: [Process Name]
**Audited by:** [name] | **Date:** [date]
**Total steps:** [n] | **Agent density:** [%]

### Step-by-Step Classification
| # | Step | Classification | Time (min) | Rationale |
|---|------|---------------|-----------|-----------|
| 1 | [step] | [AGENT/HUMAN/HUMAN+] | [minutes] | [why this classification] |
| 2 | [step] | [AGENT/HUMAN/HUMAN+] | [minutes] | [why] |

### Summary
| Category | Steps | Time/Cycle | % of Process |
|----------|-------|-----------|-------------|
| AGENT | [n] | [min] | [%] |
| HUMAN | [n] | [min] | [%] |
| HUMAN+ | [n] | [min] | [%] |

### Time Reclamation
If AGENT steps were automated: [hours/week] freed per CSM per cycle
Across a team of [n] CSMs: [hours/week] total

### Priority Automation Candidates
1. [Step X]: [time/cycle] * [frequency] = highest time recovery
2. [Step Y]: [rationale]
3. [Step Z]: [rationale]

### Human Decision Points
The [n] steps that must remain human:
1. [Step]: [why human judgment is required]
2. [Step]: [why]
```

## Quality Gates

- Did you list every step, including the undocumented ones? Most processes have 3-5 steps that "everyone just knows" but that consume significant time. If your audit has fewer than 10 steps for a major process, you are missing steps
- Did you pressure-test the HUMAN classifications? If more than 40% of steps are classified HUMAN, either the process involves unusually high judgment content or the classifications are too conservative. Pressure-test each one
- Is the time estimate per step realistic? CSMs often underestimate how long production steps take because the time is distributed across the day in small increments. 5 minutes of CRM updating * 20 accounts = 100 minutes, not "a few minutes"
- Are the priority automation candidates ranked by impact, not by ease? The highest-impact automation is often not the easiest. Rank by (time saved * frequency), not by implementation simplicity

## Principles

- The audit is a diagnostic, not a judgment. A process that is 80% AGENT-classifiable is not a bad process. It was a good process designed for the only execution engine available at the time: a person. The audit reveals the opportunity to upgrade the delivery mechanism
- HUMAN steps are where the CSM earns their seat. The 20-30% of steps that require judgment, relationship awareness, and strategic thinking are the most valuable activities a CSM performs. The audit protects these steps by freeing time from the 70-80% that do not require them
- Agent density is the business case metric. When a CS leader needs to justify an investment in automation, the audit provides the data: "Our QBR process has 24 steps. 18 are AGENT-classifiable, consuming 3.5 hours per cycle. Across 40 accounts per CSM, that is 140 hours per quarter of work that does not require judgment"
- Start with your highest-volume process. The audit has the most impact on processes that run frequently (check-in cadence, health reviews) or that consume the most time per cycle (QBR preparation, renewal workflows). Audit the expensive processes first
