---
name: qbr-action-tracker
description: Tracks and manages action items from QBRs and business reviews without requiring CRM integration. Maintains a structured register of commitments from both sides with owners, deadlines, and status, and generates follow-up reminders. Use when asked to track QBR actions, manage commitments from a business review, follow up on QBR deliverables, build an action item register, or when commitments made in QBRs are not being tracked systematically. Also triggers for questions about QBR follow-through, commitment tracking, action item management, meeting deliverables, or ensuring promises made in business reviews actually get delivered.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# QBR Action Tracker

Manages the commitments made during QBRs and business reviews. The gap this fills: QBRs generate 5-15 action items. Without structured tracking, half are forgotten within two weeks. This is where the credibility of the QBR process lives or dies.

## How to Use

After each QBR, provide:
- The action items agreed (what, who, by when)
- Context for each item (why it matters, what it enables)
- Prior QBR actions that are still open (carry forward)

Between QBRs, use the tracker to:
- Check status of open items
- Generate follow-up reminders
- Prepare the accountability section for the next QBR

## The Action Register

For each action item:

| Field | Content | Why |
|-------|---------|-----|
| ID | Unique identifier (QBR date + sequence number) | Reference in follow-ups |
| Action | What needs to happen, stated specifically | Clarity prevents ambiguity |
| Owner | Named person (not "their team" or "us") | Accountability requires a name |
| Deadline | Specific date | "Soon" is not a deadline |
| Priority | High / Medium / Low | Not everything is urgent |
| Status | Not started / In progress / Complete / Blocked / Overdue | Current state |
| Source QBR | Date of the QBR where this was agreed | Tracks how long items have been open |
| Notes | Updates, blockers, partial completion details | History of the item |
| Carry-forward count | Number of QBRs this item has been open | Items carried forward 3+ times need escalation or removal |

## Status Management

| Status | Definition | Trigger |
|--------|-----------|---------|
| Not started | Acknowledged but no work begun | Default after QBR |
| In progress | Work is underway | Owner confirms work has started |
| Complete | Deliverable is done and confirmed | Owner confirms. CSM validates with the other party |
| Blocked | Cannot proceed due to a dependency or blocker | Owner identifies the blocker. CSM assists in removing it |
| Overdue | Past the deadline with no completion | Automatic when deadline passes. Triggers follow-up |
| Cancelled | No longer relevant (context changed, superseded by a different action) | Both parties agree. Log the reason |

## Follow-Up Cadence

| Timeline | Action |
|----------|--------|
| T+3 days | Quick pulse check: are all items understood and being actioned? (Email or Slack, not a call) |
| T+14 days | Midpoint check: formal status update on all items. Flag any at risk of missing deadline |
| T-7 days before deadline | Reminder to owner: "[Action] is due in 7 days. Are you on track?" |
| Deadline day | If not complete: escalate to the CSM. CSM decides whether to follow up or grant extension |
| T+7 days past deadline | If still not complete: include in next touchpoint agenda. Do not let overdue items become invisible |

## Accountability Between QBRs

The action tracker feeds into three touchpoints:

**Mid-quarter check-in:** Surface all open items. Update status. Address any that are blocked. This is not a QBR -- it is a 15-minute accountability check

**Pre-QBR preparation:** Generate the accountability section for the next QBR deck:
- Items completed since last QBR (with outcomes)
- Items still in progress (with current status and expected completion)
- Items overdue (with explanation and revised timeline)
- Items cancelled (with reason)

**The QBR itself:** Open with the accountability section. Demonstrate that commitments are tracked and taken seriously. This is what builds trust over time -- not the data slides, but the follow-through

## Output Format

```
## QBR Action Register: [Account Name]

### Active Items
| ID | Action | Owner | Deadline | Priority | Status | Source QBR | Carry-Forward |
|----|--------|-------|----------|----------|--------|-----------|--------------|
| Q1-01 | Send Advanced Reporting documentation to analytics team | Jane (CSM) | 2026-03-14 | High | In progress | 2026-03-10 | 0 |
| Q1-02 | Provide headcount plan for April engineering onboarding | Tom (Customer) | 2026-03-21 | Medium | Not started | 2026-03-10 | 0 |
| Q4-03 | Resolve API latency issue on customer instance | Engineering | 2026-03-17 | High | In progress | 2025-12-15 | 1 |

### Completed Since Last QBR
| ID | Action | Owner | Completed | Outcome |
|----|--------|-------|----------|---------|
| Q4-01 | Deliver Q4 value report | Jane (CSM) | 2026-01-15 | Delivered. Customer confirmed ROI data was useful for budget planning |
| Q4-02 | Enable SSO integration | Tom (Customer) | 2026-02-01 | Live. All 47 users now authenticated via SSO |

### Overdue
| ID | Action | Owner | Original Deadline | Days Overdue | Blocker |
|----|--------|-------|------------------|-------------|---------|
| Q4-03 | Resolve API latency issue | Engineering | 2026-02-28 | 10 | Engineering fix deployed but monitoring period extended |

### Summary
Open: 3 | Completed this period: 2 | Overdue: 1 | Cancelled: 0
Carry-forward rate: 1 item from prior QBR still open
```

## The Carry-Forward Problem

Items carried forward from QBR to QBR are the most corrosive pattern in the action tracker. Each carry-forward signals that either:
- The commitment was not realistic (it should not have been agreed)
- The owner is not prioritising it (accountability is failing)
- The context changed and the item should be cancelled (but nobody said so)

**Rules for carry-forward items:**
- Carried forward once: acceptable. Update the deadline with a revised, realistic date
- Carried forward twice: escalate. Discuss with the owner directly. Is this still relevant? Is there a blocker?
- Carried forward three times: remove or escalate to leadership. An item that has survived three QBRs without completion is either not important enough to do (cancel it) or too hard for the current owner (escalate it)

## Quality Gates

- Does every action have a named owner and a specific deadline? "We will look into it" is not an action item. "[Name] will deliver [specific thing] by [date]" is
- Are customer-side items tracked with the same rigour as your-side items? The tracker is bilateral. Customer commitments deserve the same follow-up as yours
- Is the carry-forward count accurate? Items that have been open for multiple QBRs should be visible and flagged, not quietly re-dated to look new
- Would the customer feel the QBR follow-through is strong if they reviewed this tracker? That is the bar. The tracker is a trust-building tool, not just an internal checklist

## Principles

- The QBR is only as valuable as the follow-through. A brilliant QBR with no action follow-up builds resentment, not trust. A mediocre QBR with perfect follow-up builds credibility
- Track their items as seriously as yours. When you follow up on a customer's commitment, it signals that you take the partnership seriously enough to hold them accountable too. Most customers respect this
- Overdue items are not failures to hide. They are items to address. An overdue item that is acknowledged, explained, and re-dated maintains trust. An overdue item that is quietly ignored erodes it
- The first QBR with a formal action tracker feels different. Customers notice when you show up with a structured register of everything that was committed and everything that was delivered. It changes the dynamic from "vendor presentations" to "partnership accountability"
