---
name: meeting-agenda-builder
description: Creates structured meeting agendas with time allocation, talking points, desired outcomes, and participant roles for any CS meeting type. Adapts format by meeting type and audience. Use when asked to build a meeting agenda, structure a customer call, plan a QBR agenda, prepare a kickoff meeting structure, or when a CSM needs to ensure a meeting has a clear purpose and structure before it happens. Also triggers for questions about meeting structure, agenda creation, time allocation for calls, QBR agendas, or how to run an effective customer meeting.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Meeting Agenda Builder

Creates structured agendas that ensure every meeting has a purpose, a plan, and a defined outcome. The difference between a productive 30-minute call and a wasted 30-minute call is almost always whether someone built an agenda.

## How to Use

Provide:
- Meeting type (check-in, QBR, kickoff, escalation review, renewal, executive, ad hoc)
- Duration (how long you have)
- Attendees (customer and internal, with roles)
- Objective (what success looks like when the meeting ends)
- Topics to cover (what needs to be discussed)
- Open items from prior meetings (commitments to close the loop on)

## Agenda Templates by Meeting Type

### Check-In Call (20-30 min)

| Block | Time | Content | Purpose |
|-------|------|---------|---------|
| Opening | 2 min | Brief rapport. Reference something specific from the last interaction | Show you remember. Set a human tone |
| Account observation | 5 min | One specific data point or observation about their account | Demonstrate you are paying attention. Open the conversation with value |
| Their update | 10 min | "What is on your mind? Anything changed since we last spoke?" | Let them set the direction. The most important insights come from the customer talking, not from you presenting |
| Your topics | 8 min | 1-2 items you need to cover (open items, upcoming events, specific questions) | Cover what you planned. Keep it focused -- 2 topics maximum |
| Next steps | 3 min | Confirm actions, set next touchpoint | Accountability. Nothing leaves the meeting without an owner and a date |

### QBR (45-60 min)

| Block | Time | Content | Purpose |
|-------|------|---------|---------|
| Agenda review | 2 min | Walk through the agenda. Ask if the customer wants to add anything | Alignment. The customer should feel ownership of the meeting |
| Value review | 10 min | Headline metrics, outcomes achieved, ROI evidence | Justify the investment. This is the most important section for renewals |
| Usage and adoption | 10 min | What they are using, what they are not, peer benchmarks | Identify adoption opportunities. Drive deeper engagement |
| Support summary | 5 min | Ticket activity, resolution times, open issues | Accountability. Address any service gaps before they raise them |
| Looking ahead | 10 min | Product roadmap (relevant items), adoption recommendations | Forward-looking. Show that the product is evolving in their direction |
| Strategic discussion | 15 min | Open floor. Their priorities, concerns, questions, feedback | The highest-value block. Insights from this discussion shape the next quarter's account strategy |
| Action items | 5 min | Capture every commitment with owner and deadline | Accountability. The QBR is only as valuable as the follow-through |

### Kickoff Meeting (45-60 min)

| Block | Time | Content | Purpose |
|-------|------|---------|---------|
| Introductions | 5 min | Everyone introduces themselves and their role | Establish the team on both sides |
| Customer goals | 15 min | "Why did you choose this product? What does success look like in 90 days?" | The most important block. Everything else builds on their stated goals |
| Product overview | 10 min | What they have access to and how it maps to their goals | Connect features to outcomes, not features to features |
| Onboarding roadmap | 10 min | The plan: phases, milestones, timeline, responsibilities | Set expectations. Both sides need to understand what is required |
| Roles and communication | 5 min | Who is responsible for what. Preferred communication channels. Meeting cadence | Prevent ambiguity. "Who do I call if X happens?" should be answered here |
| Questions and next steps | 5 min | Open floor, then confirm the first milestone and next touchpoint | Momentum. The kickoff should end with a clear first action |

### Escalation Review (20-30 min)

| Block | Time | Content | Purpose |
|-------|------|---------|---------|
| Status update | 5 min | Lead with what has been done since the last conversation. Do not make them ask | Accountability. Show progress before they ask about it |
| Current state | 5 min | Where things stand now. What is resolved, what is not | Transparency. Do not overstate progress or understate remaining work |
| Resolution plan | 10 min | What happens next, timeline, who is responsible | Commitment. Specific actions with dates |
| Customer concerns | 5 min | "Is there anything else we have not addressed?" | Space for them to raise what matters to them, not just what you planned to discuss |
| Next check-in | 2 min | When the next update will come. Do not make them chase | Proactive communication. They should never have to ask for an update |

### Executive Meeting (25-30 min)

| Block | Time | Content | Purpose |
|-------|------|---------|---------|
| Purpose | 2 min | Why this meeting is happening. One sentence | Executives have no patience for ambiguity |
| Your perspective | 5 min | Value delivered, partnership highlights, forward view | Establish the relationship's health and trajectory |
| Their perspective | 10 min | "What are your priorities? How does this investment fit?" | The most valuable block. Listen more than you talk |
| Alignment | 5 min | Connect your roadmap to their stated priorities | Strategic partnership, not vendor reporting |
| Next steps | 3 min | One specific follow-up. Not a list -- one thing | Executives commit to one thing. Make it count |

## Agenda Design Principles

| Principle | What It Means |
|-----------|-------------|
| Every block has a purpose | If you cannot state why a block exists in one sentence, cut it |
| Time allocation reflects priority | The block you care most about gets the most time. Do not give 15 minutes to status updates and 5 minutes to strategic discussion |
| Customer talk time > your talk time | Aim for 60/40 customer-to-CSM talk ratio. If you are talking more than them, you are presenting, not conversing |
| Open items are addressed, not avoided | If something was committed in the last meeting, it appears in this meeting. Skipping open items signals they were not important |
| The agenda is shared before the meeting | Send the agenda at least 24 hours in advance. Let the customer add topics. This signals respect and invites engagement |
| End with clear next steps | No meeting should end with "we will be in touch." Every meeting ends with: who does what by when, and when do we next speak |

## Output Format

```
## Meeting Agenda: [Account Name]
**Date:** [date] | **Duration:** [minutes] | **Type:** [type]
**Attendees:** [list]
**Objective:** [one sentence -- what success looks like]

| Block | Time | Content | Notes |
|-------|------|---------|-------|
| [block] | [min] | [content] | [prep needed or context] |

**Open items from prior meeting:**
- [item 1 -- status]
- [item 2 -- status]

**Desired outcome:**
[One sentence: what you want to walk away with]
```

## Quality Gates

- Does the agenda have a stated objective? "Check-in with Acme" is not an objective. "Confirm Tom supports the renewal and identify any outstanding concerns" is
- Is the time allocation realistic? A 30-minute meeting with 6 blocks of 10 minutes each does not work. Add up the minutes before sharing
- Is the customer's voice represented? If every block is you presenting and none are the customer talking, the agenda is a monologue plan, not a meeting plan
- Are open items from the prior meeting included? If you skip accountability, you train the customer that commitments are optional

## Principles

- An agenda is a hypothesis, not a script. The customer may take the conversation in a different direction. That is fine -- the agenda ensures you have a starting point and a fallback if the conversation stalls
- Shorter meetings with clear agendas outperform longer meetings without them. A focused 20-minute call with a 4-block agenda creates more value than an open-ended 60-minute call with no structure
- The agenda should be shared, not imposed. "Here is what I planned to cover -- what would you add?" signals partnership. "Here is the agenda" signals control
- Meeting preparation and agenda building are the same activity. If you build the agenda and realise you do not know what to talk about, you need more preparation, not less structure
