---
name: action-item-extractor
description: Extracts commitments, action items, and follow-ups from any unstructured text including call notes, email threads, meeting transcripts, Slack conversations, or internal discussions. Outputs a structured list with owners, deadlines, and priority. Use when asked to pull action items from notes, find commitments in a conversation, extract follow-ups from an email chain, or when a CSM says "what did I commit to in that call?" Also triggers when someone says "what did we agree to," "pull out the next steps," or needs to find buried commitments in a long conversation thread.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Action Item Extractor

Finds every commitment buried in unstructured text. Paste an email thread, call notes, Slack conversation, or meeting transcript -- the skill pulls out every action item with owner, deadline, and priority.

The problem this solves: commitments made in conversations disappear within 48 hours unless they are captured in a structured format. The average customer call generates 3-7 commitments. Most CSMs capture 1-2 of them. The rest evaporate.

## How to Use

Paste any text that contains commitments. The skill scans for explicit and implicit commitments, classifies them, and produces a structured register.

## What It Scans For

### Explicit Commitments (High Confidence)

| Pattern | Example | Classification |
|---------|---------|---------------|
| "I will [action]" | "I will send the documentation by Friday" | Action item. Owner: speaker. Deadline: Friday |
| "We will [action]" | "We will deploy the fix this week" | Action item. Owner: the team. Need to confirm the specific person |
| "You will receive [thing] by [date]" | "You will receive the proposal by March 20" | Action item. Owner: speaker. Deadline: March 20 |
| "Can you [action]?" (followed by agreement) | "Can you send the user list?" "Yes, I will get that to you" | Action item. Owner: the person who agreed |
| "Action item:" or "TODO:" | "Action item: update the CRM with the new contact" | Action item. Owner: needs assignment |

### Implied Commitments (Medium Confidence)

| Pattern | Example | Risk | Handling |
|---------|---------|------|---------|
| "Let's [action]" | "Let's schedule a follow-up for next week" | Who is "let's"? No named owner | Flag as "Owner TBD -- confirm who is scheduling" |
| "I can look into that" | "I can look into the API performance issue" | Offer without commitment. No deadline | Flag as "Possible commitment -- confirm intent and timeline" |
| "We should [action]" | "We should include the product team next time" | Intent without commitment | Flag as "Discussed, not committed -- confirm if this is an action" |
| "Good idea, let's do that" | "Good idea, let's add that metric to the dashboard" | Agreement without assignment | Flag as "Agreed in principle -- who will do this and by when?" |

### Customer Commitments (Track These Too)

Commitments from the customer are action items the CSM should track and follow up on:

| Pattern | Example | CSM Action |
|---------|---------|-----------|
| Customer promises data | "I will get you the headcount plan by next week" | Track with deadline. Follow up if not received |
| Customer commits to internal action | "I will talk to our CFO about the budget" | Track. This is a dependency for your commercial conversation |
| Customer agrees to schedule | "Yes, let's do a follow-up in two weeks" | Track. Confirm the specific date. Do not let it drift |

## Output Format

```
## Action Items Extracted
**Source:** [description of the source material]
**Extracted:** [date]

### Confirmed Action Items
| # | Action | Owner | Deadline | Priority | Source Quote | Confidence |
|---|--------|-------|----------|----------|-------------|-----------|
| 1 | Send API documentation to Lisa Park | Jane (CSM) | March 14 | High | "I will get that documentation over to you by Friday" | High |
| 2 | Provide headcount plan for April onboarding | Tom (Customer) | March 21 | Medium | "I will get you the details of who is starting and when" | High |
| 3 | Confirm API fix is stable after monitoring period | Jane (CSM) | March 17 | Medium | "We will confirm resolution after the monitoring period" | High |

### Items Needing Clarification
| # | Item | Issue | Suggested Resolution |
|---|------|-------|---------------------|
| 4 | Build training plan for new engineers | Owner unclear -- "let's put together a plan" | Confirm: is this Jane's responsibility or Tom's? |
| 5 | Include product team in next QBR | Discussed but not committed | Confirm: is this an action or a consideration? |

### Possible Commitments (Low Confidence)
| # | Quote | Why It Might Be a Commitment | Why It Might Not |
|---|-------|----------------------------|-----------------|
| 6 | "I can look into the reporting module" | Offered to investigate | Could be polite acknowledgement without intent to act |
```

## Deduplication

When the same commitment appears multiple times (discussed, then confirmed, then repeated in the meeting close), the skill:
- Lists it once with the most specific version
- Notes the repetition: "Mentioned 3 times -- confirmed in meeting close" (repetition signals importance)
- Uses the version with the clearest owner and deadline

## Priority Assignment

| Priority | Criteria |
|----------|----------|
| High | Customer-facing deadline, affects customer's business, time-sensitive, or blocking other work |
| Medium | Important but flexible. Internal commitment, no hard deadline, or customer can wait |
| Low | Nice-to-have, internal housekeeping, or long-term consideration |

## Quality Gates

- Does every action item have a named owner? "The team" is not an owner. If the owner is unclear, flag it for clarification rather than assigning it to "us"
- Are deadlines specific dates? Convert "next week" to a date. Convert "soon" to "no deadline stated -- confirm." Convert "by the end of the month" to the specific date. Vague deadlines produce vague accountability
- Are customer commitments tracked with the same rigour as your own? Following up on customer commitments is a CSM responsibility. If they promised to send data by Friday and did not, that is an item you need to action
- Is the "Possible Commitments" section populated? Ambiguous language is the most common source of lost commitments. Surfacing them for confirmation is more valuable than ignoring them
- Would someone who was not in the conversation understand each action item? "Follow up on the thing we discussed" is meaningless to anyone else. "Send the Q1 value report to Tom Chen by March 14" is clear to anyone

## Principles

- When in doubt, capture it. A false positive (flagging something that is not actually a commitment) is easily dismissed. A false negative (missing a real commitment) can cost you a customer's trust
- Commitments from the customer are as important as your own. If Tom said he would get you the headcount plan by next week and he does not, that is not his failure -- it is your failure to follow up. Track their items and hold them accountable
- "Let's" is the most dangerous word in CS. It sounds like a commitment but it assigns no owner. Every "let's" in your notes should trigger a follow-up question: "Just to confirm -- who is taking the lead on this?"
- The action register is a trust-building tool. When you email the customer after a call with a clear list of commitments from both sides, you signal professionalism and accountability. Customers respect CSMs who track what was promised
