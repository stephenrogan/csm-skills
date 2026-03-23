---
name: stakeholder-research-prep
description: Prepares structured background research on a customer contact before a first meeting or engagement. Builds a profile including likely priorities, role-specific concerns, engagement approach, and conversation starters based on their title, function, and seniority level. Use when asked to prepare for a first meeting with a new contact, research a stakeholder, build a contact profile, prepare for an executive conversation, or when meeting someone at a customer account for the first time. Also triggers for questions about stakeholder preparation, first meeting research, contact profiling, or executive meeting prep with someone you have not met before.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Stakeholder Research Prep

Prepares you for a first conversation with a customer contact you have not met. Builds a profile of likely priorities, concerns, and communication style based on their role, function, seniority, and any context you provide.

This is not a dossier. It is a thinking framework that helps you walk into the meeting with a hypothesis about what this person cares about, so you can listen for confirmation or correction rather than starting from zero.

## How to Use

Provide what you know:
- Contact name and title
- Their function (engineering, product, finance, operations, executive)
- Seniority level (IC, manager, director, VP, C-suite)
- Company and account context (industry, size, your product, their use case)
- How this meeting came about (introduction from champion, they requested it, you reached out, new hire replacement)
- Anything your champion or other contacts have said about this person
- Any LinkedIn context you have gathered (background, career history, posts)

The more context you provide, the more specific the prep. But even with just a name and title, the skill produces a useful framework.

## What It Produces

### Role-Based Priority Profile

Based on the contact's function and seniority, the skill maps likely priorities:

**By function:**

| Function | Likely Priorities | Likely Concerns | What They Want From You |
|----------|-----------------|-----------------|----------------------|
| Engineering | Technical reliability, API quality, integration capabilities, developer experience | Downtime, breaking changes, tech debt, migration complexity | Technical competence, honest assessment of limitations, clear documentation |
| Product | Feature alignment with their roadmap, user feedback, competitive positioning | Feature gaps, slow release cycles, poor UX | Partnership on feature development, feedback loop, roadmap transparency |
| Finance | ROI, total cost of ownership, contract flexibility, predictable pricing | Hidden costs, scope creep, poor value realisation, vendor lock-in | Clear ROI evidence, pricing transparency, business case support |
| Operations | Process efficiency, adoption, training, change management | Low adoption, disruption to existing workflows, training burden | Implementation support, enablement resources, smooth transitions |
| Sales / Revenue | Revenue impact, competitive advantage, customer-facing capabilities | Tools that slow them down, poor reporting, integration with their stack | Quick wins, clear value narrative they can use with their customers |
| Executive (any function) | Strategic alignment, board-level metrics, competitive positioning, risk management | Vendor dependency, reputational risk, misaligned priorities | Strategic partnership, executive-to-executive relationship, business impact data |

**By seniority:**

| Level | Decision Scope | Time Horizon | Communication Preference |
|-------|---------------|-------------|------------------------|
| IC / Individual Contributor | Their own workflow, specific features | This week, this sprint | Detailed, technical, show-me-how |
| Manager | Team productivity, adoption, process | This quarter | Practical, outcome-focused, give-me-a-plan |
| Director | Department performance, budget, strategy | This half, this year | Results-oriented, data-driven, show-me-the-impact |
| VP | Cross-functional alignment, company goals, investment decisions | This year, next year | Strategic, high-level with option to drill down, executive summary |
| C-Suite | Company trajectory, board reporting, competitive position | Multi-year | Very concise, business impact only, relationship-first |

### Engagement Approach

Based on role and context, the skill recommends:

**Opening approach:**
- How to introduce yourself and frame the relationship
- What to lead with (and what not to lead with)
- How much product/technical context to provide upfront

**Questions to ask:**
- 3-5 role-appropriate questions that demonstrate you understand their world
- These should be genuine information-gathering, not leading questions
- Prioritise questions about their goals and challenges, not questions about your product

**Things to listen for:**
- Signals that indicate their disposition toward your product (positive, neutral, sceptical)
- Clues about the internal political landscape (who else matters, who they report to, who they influence)
- Indicators of their decision-making style (data-driven, relationship-driven, consensus-driven, top-down)

**What not to do:**
- Role-specific pitfalls (e.g., do not lead with ROI when talking to an engineer -- they care about technical quality first)
- Common mistakes for this stakeholder type
- Assumptions to avoid

### Context-Specific Adjustments

The prep adjusts based on how the meeting came about:

| Context | Adjustment |
|---------|-----------|
| Introduction from champion | Lead with the champion's endorsement. "Tom suggested we connect because..." Frame the meeting as a natural extension of an existing relationship |
| They requested the meeting | They have an agenda. Ask about it early. "I know you reached out about X -- I want to make sure I cover what matters to you" |
| You reached out cold | Earn the meeting in the first 30 seconds. Lead with relevance to their role and a specific observation, not a product pitch |
| New hire replacing someone | They are evaluating everything. Do not assume continuity. "I want to understand your priorities and how you would like to work together, rather than assume what worked with [predecessor] works for you" |
| Escalation-triggered | They are not happy. Acknowledge the situation before anything else. Do not try to reframe a problem as an opportunity |

## Output Format

```
## Stakeholder Prep: [Name] -- [Title]

### Profile Summary
Role: [function + seniority]
Likely priorities: [top 3]
Likely concerns: [top 3]
Communication style: [expected preference based on seniority]

### Engagement Approach
Opening: [How to start the conversation]
Lead with: [What to discuss first]
Do not lead with: [What to avoid early]

### Questions to Ask
1. [Role-appropriate question]
2. [Role-appropriate question]
3. [Role-appropriate question]

### Listen For
- [Signal to watch for]
- [Signal to watch for]
- [Signal to watch for]

### Pitfalls to Avoid
- [Common mistake for this stakeholder type]
- [Common mistake for this stakeholder type]

### Context Notes
[How the meeting came about and any specific adjustments]
```

## Quality Gates

- Are the priorities role-specific? If the priorities would apply to any title at any company, they are too generic. "Wants to be successful" is not a priority. "Wants to reduce engineering time spent on manual reporting" is
- Are the questions genuine? A question you already know the answer to is not a question -- it is a test. First meetings should build understanding, not demonstrate knowledge
- Does the approach match the context? Prepping for an escalation-triggered meeting with a "partnership" frame is tone-deaf
- Have you accounted for what you do not know? The prep is a hypothesis, not a profile. The purpose is to walk in with a framework and listen for whether it is right, not to assume it is right

## Principles

- First meetings are for listening, not presenting. The goal is to understand what this person cares about, not to convince them of anything. The prep helps you ask better questions, not deliver better pitches
- Role and seniority are useful proxies but they are not the person. A VP of Engineering who came up through product management thinks differently than one who came up through infrastructure. Use the role profile as a starting point, then update based on what you learn in the conversation
- The best first meetings end with the other person feeling understood, not impressed. If you leave the meeting knowing their top 3 priorities and they leave feeling you get their world, you have succeeded regardless of what you presented
