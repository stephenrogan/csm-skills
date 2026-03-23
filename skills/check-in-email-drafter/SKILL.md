---
name: check-in-email-drafter
description: Writes personalised customer check-in emails that do not sound like templates. Calibrates tone by segment, incorporates account-specific context, and always includes a specific question or observation rather than generic outreach. Use when asked to write a check-in email, draft a touchpoint email, compose a proactive outreach, or when a CSM needs to reach out to a customer with something better than "just checking in." Also triggers when someone says "I need to email this customer" or "what should I say to them" or needs a personalised outreach for an account on their cadence.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Check-In Email Drafter

Writes check-in emails that customers actually want to read. The bar: would you respond to this email if you received it? If not, rewrite.

The "just checking in" email is the most common and most ignored communication in CS. This skill replaces it with emails that contain a specific observation, a relevant data point, or a genuine question -- something that shows you are paying attention to this account, not running a template across your book.

## How to Use

Provide:
- Account name and contact name
- What you know about the account right now (health, recent activity, usage, open items)
- How long since your last touchpoint
- Anything specific you want to raise or ask about
- Segment (enterprise, mid-market, SMB) for tone calibration
- The purpose: is this a scheduled cadence touchpoint, a re-engagement, or a specific reason?

## The Anti-Template Approach

Every email must pass three tests:
1. **Specificity test:** Does it contain at least one reference that could only apply to this account? If you could swap in another customer name and the email still works, it fails
2. **Response test:** Does it contain exactly one question or observation that invites a response? Zero questions means no reason to reply. Multiple questions means choice paralysis
3. **Value test:** Does the recipient gain something by reading this? Information, recognition, a useful offer, or a relevant question all qualify. "Just wanted to touch base" qualifies as none of these

## Email Patterns

### Pattern 1: The Data Observation

Lead with something you noticed in their usage or engagement. Shows you are watching, not just emailing.

"Hi [name], I noticed your team's workflow automation count grew 30% this quarter -- that puts you ahead of most companies your size on that metric. Are you seeing the time savings on the operations side, or is the volume growth driven by something else?"

**When to use:** When you have a specific data point worth sharing. Best for accounts with strong or growing usage.

### Pattern 2: The Relevant Trigger

Reference something that happened (product update, milestone, industry event) that is relevant to them.

"Hi [name], we released the custom dashboard builder last week -- given your team's investment in reporting, I think this could replace the manual process Lisa mentioned in our last call. Want me to set up a 15-minute demo, or would you prefer I send a walkthrough video?"

**When to use:** When something has changed (product release, industry news, their company news) that gives you a reason to reach out.

### Pattern 3: The Value Share

Offer something useful without asking for anything.

"Hi [name], I pulled a benchmark comparison for your account against similar mid-market SaaS companies. Your adoption depth is in the top quartile. I have a few suggestions for features that could push your efficiency even further -- happy to send them by email or cover in a quick call."

**When to use:** When you have something to offer. Best as an occasional touchpoint, not a pattern (offering something every email creates obligation fatigue).

### Pattern 4: The Genuine Question

Ask something you actually want to know the answer to. Not "how are things going?" but a question that would change how you manage the account based on the answer.

"Hi [name], as you head into Q2 planning, I wanted to ask -- are there any new initiatives on your team's roadmap where our product could play a role? I want to make sure we are supporting what matters most to you this quarter, not just what worked last quarter."

**When to use:** At transition points (quarter change, budget cycle, annual planning) or when you genuinely do not know what the customer's current priorities are.

### Pattern 5: The Scheduled Cadence (With Substance)

For routine check-ins that are cadence-driven, not event-driven. Still must contain substance.

"Hi [name], our regular check-in is coming up next week. Since we last spoke, I have noticed [specific observation] and wanted to make sure we cover [specific topic]. Anything on your side you want to add to the agenda?"

**When to use:** Before scheduled check-in calls. The email serves double duty: it prepares the customer for the call and gives them a chance to add their topics.

## Tone Calibration

| Segment | Register | Examples |
|---------|----------|---------|
| Enterprise | Professional, measured. Full sentences. Proper salutations | "Dear [name]" or "Hi [name]" depending on relationship depth. Structured paragraphs. Formal close |
| Mid-Market | Warm professional. First-name basis. Conversational but polished | "Hi [name]" always. Shorter paragraphs. Direct tone. Casual close |
| SMB | Casual, direct. Minimal formality | "Hey [name]" is acceptable if the relationship supports it. 2-3 sentences max. No formal structure |

**Overrides:** If the account is at risk, use empathetic and solution-oriented tone regardless of segment. If post-escalation, use accountable and specific tone. If new relationship, use professional regardless of segment until rapport is established.

## Output Format

For each email:
- Subject line (specific, under 50 characters, not "Checking in" or "Quick question")
- Body text (under 100 words for check-ins -- shorter is better)
- Pattern used (which of the 5 patterns above)
- Personalisation elements (what makes this specific to this account)
- One flag if any: "Note: account is at risk -- consider calling instead of emailing" or "Note: no specific data available -- Pattern 4 recommended"

## Quality Gates

- Does the email contain a specific reference that could only apply to this account? The universal test for personalisation
- Is it under 100 words? Check-in emails should be short. If you have a lot to say, that is a call, not an email
- Is there exactly one question or observation? One. Not zero (no reason to reply), not three (overwhelming)
- Does the subject line earn an open? "[Account] -- Q1 automation results" works. "Quick question" does not
- Does it sound like a human wrote it? Read it aloud. If it sounds like a CRM workflow, rewrite
- Is the timing right? Do not send a check-in within 3 days of the last touchpoint. Do not send a check-in to a customer mid-escalation

## Principles

- Every email you send either strengthens or weakens the relationship. There is no neutral. A generic check-in weakens it because it signals you are going through the motions. A specific, relevant email strengthens it because it signals you are paying attention
- If you have nothing specific to say, do not email. A skipped check-in is invisible. A bad check-in is remembered. Wait until you have something worth saying
- The best check-in emails do not feel like check-ins. They feel like a colleague sharing something useful. That is the register to aim for
- Response rate is the quality metric. If your check-in emails get <20% response rate, they are too generic. If they get >50%, you are doing it right. Track your own data
