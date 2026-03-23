---
name: customer-apology-crafter
description: Writes genuine, non-corporate apologies after service failures, outages, missed commitments, or other situations where the customer was let down. Provides multiple framing options calibrated to the severity of the failure and the state of the relationship. Use when asked to write an apology email, draft a service failure response, compose a mea culpa, acknowledge a mistake to a customer, or when any situation requires a formal acknowledgement that something went wrong. Also triggers for questions about customer apologies, service recovery communications, trust repair, or handling a situation where the company made a mistake.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Customer Apology Crafter

Writes apologies that are genuine, specific, and accountable. The bar: would you feel respected and heard if you received this? If not, rewrite.

Most corporate apologies fail because they apologise for the inconvenience instead of the failure, hedge accountability with passive voice, or rush to the solution before acknowledging the impact. This skill produces apologies that do none of those things.

## How to Use

Provide:
- What happened (the specific failure, not a euphemism)
- What the impact was on the customer (be honest -- if you do not know, say so)
- What caused it (root cause, if known)
- What has been done to fix it
- What is being done to prevent recurrence
- The relationship context (strong, neutral, strained, new)
- The severity (minor inconvenience, moderate disruption, major business impact)
- Your authority level (can you make commitments, or do you need to escalate?)

## Anatomy of a Good Apology

Every effective apology has five elements, in this order:

### 1. Acknowledge What Happened (Be Specific)

State the failure in plain language. Do not soften it, minimise it, or use passive voice.

| Bad | Good |
|-----|------|
| "We apologise for any inconvenience" | "We missed the deployment deadline by 8 days" |
| "There was an issue with the system" | "Our API was down for 4 hours during your peak usage period" |
| "The timeline was impacted" | "We committed to delivering the integration by March 1 and did not meet that commitment" |

### 2. Own the Impact (Not Your Feelings)

Describe the effect on the customer's business. Do not talk about how you feel -- the customer does not care that you are "deeply sorry." They care that you understand what this cost them.

| Bad | Good |
|-----|------|
| "We are deeply sorry for the disruption" | "Your analytics team could not run reports for 4 hours, which I understand delayed your board prep" |
| "We regret any negative experience" | "Your team had to build workarounds for the 8 days we missed the deadline" |

If you do not know the full impact, say so: "I want to understand the full impact on your team -- can you help me see what this cost you?"

### 3. Explain Without Excusing

Share the root cause if you know it. The customer deserves to understand why, but the explanation must not become a deflection.

| Bad | Good |
|-----|------|
| "Due to unforeseen circumstances..." | "We underestimated the complexity of the database migration" |
| "A third-party vendor caused the issue" | "The issue originated in our infrastructure provider, but it is our responsibility to have redundancy in place, and we did not" |

If you do not know the root cause yet: "We are still investigating the root cause and I will share what we find."

### 4. State What You Are Doing

Specific actions, not promises. The customer has already heard "we will do better."

| Bad | Good |
|-----|------|
| "We are taking steps to ensure this does not happen again" | "We are implementing automated failover for the API endpoint (live by March 20) and adding a monitoring alert that triggers at 99.5% uptime deviation" |
| "We will improve our processes" | "I am restructuring the deployment timeline to include a 3-day buffer for integration milestones" |

### 5. Offer to Discuss (Do Not Assume It Is Resolved)

The apology is the start of the recovery, not the end. Offer to talk, listen, and address further.

"I would like to discuss this with you directly. Are you available for a call this week? I want to make sure we have fully addressed the impact and that you are confident in our plan going forward."

## Severity Calibration

| Severity | Tone | Length | Channel | Who Sends |
|----------|------|--------|---------|----------|
| Minor (small delay, cosmetic issue) | Straightforward, brief | 3-5 sentences | Email | CSM |
| Moderate (missed commitment, noticeable disruption) | Serious, accountable | 5-8 sentences | Email, followed by call | CSM |
| Major (extended outage, significant business impact) | Grave, executive-level | Full structured apology, potentially from CSM + leadership | Call first, then written follow-up | CSM + CS leadership or executive |
| Critical (data loss, security incident, public-facing failure) | Formal incident response | Structured incident report with apology | Call from leadership, followed by formal written communication | Executive level |

## What Never to Say

| Phrase | Why It Fails |
|-------|-------------|
| "We apologise for any inconvenience" | "Any" suggests you are not sure there was one. "Inconvenience" minimises the impact. This is the most hollow phrase in corporate apologies |
| "Unfortunately..." | Signals that what follows is bad news you wish you did not have to deliver. Just deliver it |
| "The issue was caused by..." (passive) | Who caused it? Own it. "We caused the issue by..." |
| "We take this very seriously" | Proving you take it seriously through action is more credible than declaring it |
| "Please don't hesitate to reach out" | If you want them to call, say so directly: "Call me at [number] if you want to discuss" |
| "Going forward, we will..." (without specifics) | Promises without specifics are not commitments. They are hopes |

## Output

For each situation, the skill produces:
- The apology email or talking points (calibrated to severity and channel)
- A "what to expect" note on likely customer reactions and how to respond
- Suggested follow-up timeline (when to check back in to confirm resolution and rebuild trust)
- Escalation guidance (when the CSM should involve leadership)

## Quality Gates

- Does the apology name the specific failure? If you could swap in any other failure and the apology still works, it is too generic
- Does it own the impact in the customer's terms? The test: would the customer feel you understand what this cost them?
- Is every "we will" statement paired with a specific action and timeline? Vague commitments are worse than no commitments because they invite follow-up that you cannot deliver on
- Is the tone calibrated to the severity? An overly grave apology for a minor issue is patronising. An understated response to a major failure is dismissive. Match the weight of the words to the weight of the failure
- Would you accept this apology if you were the customer? Read it from their perspective. If it reads like corporate risk management instead of genuine accountability, rewrite

## Principles

- An apology is not a PR exercise. It is a trust repair conversation. The customer's trust was damaged by the failure. The apology begins rebuilding it by demonstrating that you understand, you care, and you are doing something about it
- Speed matters more than polish. A genuine, imperfect apology sent within hours beats a polished corporate statement sent in 3 days. The gap between the failure and the acknowledgement is where resentment builds
- The customer's emotional state is real and valid. Do not try to talk them out of their frustration. Acknowledge it, own what caused it, and focus on what comes next
- One genuine apology earns more trust than the failure destroyed -- if the follow-through matches the words. The apology sets a commitment. If you fail to deliver on the apology's promises, the trust damage compounds
