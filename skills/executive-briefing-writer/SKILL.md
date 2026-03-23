---
name: executive-briefing-writer
description: Condenses account context into structured executive summaries of varying depth -- from a 30-second verbal brief to a one-page written summary. Formats for the specific executive audience (your leadership, the customer's leadership, or both). Use when asked to prepare an executive briefing, write an account summary for leadership, create a board-level overview, condense account information for a VP or CRO, or when a CSM needs to brief someone senior quickly. Also triggers for questions about executive summaries, leadership briefings, account snapshots for management, or condensing complex account situations into executive-ready formats.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Executive Briefing Writer

Condenses everything you know about an account into the format an executive needs to make a decision or have a conversation. The skill adjusts depth and framing based on who the executive is and what they need the briefing for.

The core discipline: executives do not have time for context. They need the answer first, then just enough context to trust the answer.

## How to Use

Provide:
1. Who is the executive? (Your VP, the customer's CRO, your CRO, a board member)
2. What is the briefing for? (Decision, awareness, preparation for a meeting, escalation)
3. Everything you know about the account (the skill will compress -- give it more than less)
4. What do you need from the executive? (If anything -- approval, resource, introduction, nothing)

## Briefing Formats

### The 30-Second Verbal Brief

For hallway conversations, the opening of a 1:1, or when asked "how is Account X doing?"

**Structure:**
1. **Status** (one word): Strong / Healthy / At Risk / Critical
2. **Why** (one sentence): The single most important thing about this account right now
3. **Ask** (one sentence, if applicable): What you need from this person

**Example:**
"Acme is at risk. Their champion left last month and usage is declining -- we have 67 days to renewal with no executive sponsor engaged. I need your help getting a VP-to-VP call set up before the end of the month."

**Rules:**
- Never open with background. The executive can ask for context if they want it
- Never hedge. "It is kind of at risk, but things might improve" is useless. Take a position
- If you have an ask, state it clearly. If you do not have an ask, say so: "No action needed -- just keeping you informed"

### The 5-Line Email Brief

For when leadership needs a written update they can scan on their phone.

**Structure:**
```
Subject: [Account Name] -- [Status] -- [One-line summary]

[Account Name] | [ARR] | [Health status] | Renewal: [date/days]

Situation: [2-3 sentences on what is happening]

[Ask or next step: 1 sentence]

[Your name]
```

**Rules:**
- Subject line must be scannable without opening the email
- Five lines maximum in the body. If you need more, attach the detail and keep the email itself to five lines
- ARR is always in the first line. Executives think in revenue

### The One-Page Written Brief

For leadership reviews, board preparation, or when the executive needs enough context to have a conversation about this account.

**Structure:**

| Section | Content | Length |
|---------|---------|--------|
| Headline | Account name, ARR, health, one-sentence status | 1 line |
| Context | Why this account matters (ARR, strategic value, logo value, reference potential) | 2-3 sentences |
| Current situation | What is happening now, with data | 3-5 sentences |
| Risk or opportunity | The primary risk or opportunity and its revenue impact | 2-3 sentences |
| What we are doing | Current intervention plan or growth strategy | 2-3 sentences |
| Ask (if any) | Specific request of the executive with rationale | 1-2 sentences |
| Timeline | Key dates: renewal, next touchpoint, decision deadline | 1-2 lines |

**Rules:**
- One page means one page. If you cannot fit the story in one page, you do not understand the story well enough yet
- Lead with the most important thing, not the background. The executive should know the answer before they know the question
- Every sentence must earn its place. If removing a sentence does not change the executive's understanding or decision, remove it

### The Board-Level Summary

For when your VP or CRO needs to include this account in a board deck or investor update.

**Structure:**
3-4 sentences maximum. Account name, ARR, one headline metric, one strategic note.

**Example:**
"Acme Corp (EUR 85k ARR, 18-month customer) achieved a 67% reduction in manual reporting time this quarter, putting them in our top quartile for value realisation. Renewal is in April and we expect expansion into their Marketing team (EUR 15k uplift). No risk signals."

**Rules:**
- Board members do not know your accounts. Do not assume context
- One number that proves value. One sentence on the outlook. That is the entire board contribution for most accounts
- Only include risk if it is material (large ARR, strategic account, or pattern-forming)

## Audience-Specific Framing

| Audience | Cares About | Frame As |
|----------|------------|---------|
| Your VP CS | Account health, team performance, resource needs | Operational: what is happening, what are you doing about it, what do you need |
| Your CRO | Revenue impact, pipeline, retention forecast | Financial: ARR at risk or in play, revenue impact of your ask |
| Customer's VP | Value delivered, strategic partnership, product direction | Partnership: what you have delivered, what comes next, how you will support their goals |
| Customer's CFO | ROI, cost of ownership, contract terms | Financial: return on their investment, value per seat, comparison to alternatives |
| Board members | NRR, strategic accounts, market position | Portfolio: representative example of customer success (positive) or lesson learned (negative) |

## Output for Each Format

The skill produces the briefing in the requested format with:
- The formatted content ready to send, say, or present
- A "context notes" section (for your eyes only) with supporting data that you might need if the executive asks follow-up questions
- A flag if any critical information was missing from your input: "Note: no renewal date provided -- add this before presenting"

## Quality Gates

- Does the headline answer the question the executive is going to ask? If they will ask "should I be worried about this account?" and your headline is about usage metrics, you have missed the point
- Is the ARR present? Executives anchor on revenue. An account brief without ARR is a brief without stakes
- Is the ask specific? "I need help" fails. "I need a VP-to-VP call with their CFO before March 30 to discuss the renewal" succeeds
- Have you removed all CS jargon? Health scores, NPS, QBR -- these are your language, not the executive's. Translate to their language: "the account is strong," "the customer is satisfied," "we have a scheduled business review"
- Is it the right length for the format? A 30-second brief that takes 2 minutes is a 2-minute brief. A one-pager that spills onto page two is not a one-pager
- Would you be comfortable if the customer saw this? Internal briefs sometimes get forwarded. Write accordingly

## Principles

- Executives do not need context to make decisions. They need a clear recommendation with enough evidence to trust it. Lead with the recommendation
- If you cannot summarise the account in one sentence, you do not understand it well enough. The briefing process itself forces clarity of thought
- The ask is the most important part. An executive briefing without a clear ask (or explicit "no ask -- awareness only") is a waste of their time and yours
- Match the medium to the message. Bad news in an email brief is acceptable. Bad news with a significant ask should be a conversation, not a document
