---
name: internal-status-update-writer
description: Compiles account portfolio status into formatted internal updates for leadership, cross-functional teams, or manager reviews. Adapts detail and framing by audience. Use when asked to write a status update, compile a portfolio summary for leadership, create a weekly report for your manager, draft a cross-functional update on key accounts, or when any internal audience needs a structured view of account status. Also triggers for questions about internal reporting, portfolio status updates, manager updates, leadership summaries, or how to communicate account status to internal stakeholders.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Internal Status Update Writer

Compiles your account portfolio status into a formatted update for internal consumption. The skill adapts the content, detail level, and framing based on who is reading it and what they need to know.

The core problem this solves: CSMs spend 30-60 minutes each week compiling status updates from memory and CRM notes. This skill structures the process and produces a consistent format that leadership can actually scan and act on.

## How to Use

Provide:
- Who the update is for (your manager, CS leadership, CRO, cross-functional team)
- What cadence (weekly, monthly, ad hoc)
- Your portfolio status: for each account that warrants mention, provide the current state, any changes, risks, opportunities, and open items
- Any specific topics leadership has asked about
- What you need from the audience (awareness, decisions, resources, nothing -- just informing)

## Update Formats by Audience

### Weekly Manager Update

**Purpose:** Keep your manager informed on your portfolio so they are never surprised in a leadership meeting.

**Structure:**
```
## Weekly Update: [CSM Name] -- Week of [Date]

### Portfolio Health
[Total accounts] | [Strong]: [n] | [Healthy]: [n] | [At Risk]: [n] | [Critical]: [n]
Change from last week: [+/- movements between bands]

### Accounts to Discuss
[2-3 accounts that need manager attention or input]

**[Account Name]** (EUR [ARR] | [Health] | Renewal: [date])
Situation: [2-3 sentences]
Action: [what you are doing]
Need: [what you need from the manager, if anything]

### Wins This Week
[1-2 positive developments worth noting]

### Open Items
[Commitments or actions pending from prior weeks]

### Asks
[Specific requests, or "None this week"]
```

**Rules:**
- Under 1 page. If your manager needs more than 5 minutes to read it, it is too long
- Lead with what changed, not with what is stable. Stable accounts do not need weekly airtime
- Every account mentioned should have a clear reason for being mentioned (risk, opportunity, decision needed) and a clear "need" (even if the need is "awareness only")

### Monthly Leadership Summary

**Purpose:** Give CS leadership a view of your portfolio's trajectory for their own reporting and decision-making.

**Structure:**
```
## Monthly Summary: [CSM Name] -- [Month Year]

### Portfolio Overview
Accounts: [n] | ARR: [total] | Avg Health: [score/band]
NRR (trailing 30 days): [if calculable]

### Key Developments
[3-5 most significant events this month, ranked by impact]

### Renewal Pipeline (Next 90 Days)
| Account | ARR | Renewal Date | Status | Risk Level |
|---------|-----|-------------|--------|-----------|
| [account] | [ARR] | [date] | [status] | [H/M/L] |

### Expansion Pipeline
| Account | Opportunity | Estimated Value | Stage |
|---------|-----------|----------------|-------|
| [account] | [what] | [EUR] | [early/active/closing] |

### Churn / Contraction This Month
[Any losses or downsells with root cause]

### Resource Needs
[What you need from leadership: headcount, tooling, executive engagement, policy change]
```

### Cross-Functional Update

**Purpose:** Keep product, engineering, sales, or support informed on accounts relevant to their work.

**Structure:** Tailored to the audience:

| Audience | Include | Exclude |
|----------|---------|---------|
| Product team | Feature feedback themes, adoption blockers, product-correlated issues, competitive intelligence | Revenue data, relationship dynamics, commercial strategy |
| Sales team | Expansion opportunities, at-risk renewals that need sales support, cross-sell candidates | Internal CS metrics, process details, support history |
| Support leadership | Escalation status, accounts with support-driven risk, CSAT trends | Commercial data, relationship details beyond what is relevant to support |
| Engineering | Active technical issues, integration problems, performance complaints | Everything non-technical |

### Ad Hoc Account Update

**Purpose:** When someone asks "what is going on with Account X?" and you need to respond quickly.

**Structure:** 5 lines maximum.
```
[Account Name] | EUR [ARR] | [Health band] | Renewal: [date]
Status: [one sentence]
Risk: [one sentence, or "none"]
Action: [what is happening]
Need: [what you need, or "awareness only"]
```

## What to Include vs. Exclude

| Always Include | Never Include |
|---------------|-------------- |
| Accounts with status changes this period | Stable accounts with nothing to report |
| Risks with ARR impact | Routine touchpoints that went as expected |
| Wins worth celebrating (closed expansion, save, milestone) | Activities without outcomes (calls made, emails sent) |
| Specific asks with rationale | Vague requests without context |
| Honest assessments (including bad news) | Optimistic spin on deteriorating situations |

## Quality Gates

- Does the update answer the question "what do I need to know?" for the reader? If you are not sure what they need to know, ask them
- Is every account mentioned for a reason? Status updates are not a log of everything that happened. They are a curated view of what matters
- Are your asks specific? "I need help with Acme" is not an ask. "I need your help getting a VP-to-VP call with Acme's CFO before March 30 to discuss the renewal" is
- Is the length appropriate? Weekly updates: under 1 page. Monthly: under 2 pages. Ad hoc: under 5 lines. Anything longer will not be read
- Would your leadership be surprised by anything in their next meeting that is not in this update? If yes, the update is incomplete

## Principles

- No surprises is the goal. Leadership should never learn about a risk, a churn, or a competitive threat for the first time in someone else's meeting. The status update is your insurance against that
- Write for skimming, not for reading. Bold the account names. Lead with the numbers. Put the ask in its own section. Your reader will spend 60 seconds on this, not 5 minutes
- Bad news early, good news often. If an account is deteriorating, surface it in the first update you write after detecting the change. Waiting until it becomes a crisis makes you look unaware, not optimistic
- The status update is a trust-building tool. Consistent, honest updates build your manager's and leadership's confidence in you. Inconsistent or spin-heavy updates erode it. The update itself is part of your professional reputation
