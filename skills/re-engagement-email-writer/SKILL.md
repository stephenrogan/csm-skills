---
name: re-engagement-email-writer
description: Writes outreach to customers who have gone dark -- not responded to recent communications, missed meetings, or disengaged from the product. Differs from a check-in email by acknowledging the silence and offering a specific reason to re-engage rather than asking if everything is fine. Use when asked to write a re-engagement email, reach out to a silent customer, draft an outreach to a customer who has gone dark, break through to an unresponsive contact, or when a no-reply streak indicates the customer has disengaged. Also triggers for questions about customer silence, unresponsive accounts, re-engagement strategy, or breaking through communication barriers.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Re-Engagement Email Writer

Writes outreach to customers who have stopped responding. Different from a check-in email -- this acknowledges the silence (without making it awkward) and offers a specific reason to re-engage.

The fundamental question: why should this customer respond to you today when they did not respond to you last week? If you do not have an answer, the email will not work regardless of how well it is written. This skill helps you find and frame that answer.

## How to Use

Provide:
- Account name and contact name
- How long since the last response (days/weeks)
- How many outreach attempts have been made without a response
- The last meaningful interaction (what was discussed, any open items)
- Account health (is the product being used even though the person is not responding?)
- Any known context (are they busy? Did something change? Is there a new contact?)
- What you want from them (a call, a reply, a decision, awareness of something new)

## Why Customers Go Dark

Before writing the email, diagnose the likely cause. The approach changes based on the root cause:

| Likely Cause | Signals | Email Approach |
|-------------|---------|---------------|
| Busy / deprioritised | Product usage is stable but contact is not responding to emails. No negative signals | Low-pressure, offer value, make it easy to respond with minimal effort |
| Frustrated / dissatisfied | Usage declining, open support tickets, prior negative interactions | Acknowledge the possibility. Do not pretend everything is fine. Offer to address concerns |
| Champion departure | Contact may have left. Email bounces, LinkedIn update, sudden silence after regular engagement | Investigate whether they have left. If confirmed, pivot to finding the replacement |
| Decision avoidance | Approaching renewal with silence, prior conversation about concerns or alternatives | Direct but empathetic. Name the elephant: "I suspect the renewal is on your mind. I would rather have the conversation than wonder" |
| Wrong contact | The person you are emailing is not the right person for this conversation (delegated, moved roles) | Ask: "Are you still the right person for this? If not, could you point me to the right contact?" |
| You are not providing value | Your emails are generic check-ins with no specific reason to respond | Bring something genuinely useful. A benchmark, a new feature, a specific observation about their usage |

## Email Patterns

### Pattern 1: The Value-First Re-Engagement

**Best for:** Busy/deprioritised contacts. Product usage is healthy.

**Structure:**
Lead with something useful -- a metric, an insight, a new feature, a benchmark -- not a request for time.

**Example:**
"Hi [name], I pulled some numbers on your team's usage and noticed your workflow automation count has grown 30% since last quarter. That puts you in the top quartile for companies your size. I have a few recommendations for features that could accelerate that trend further -- happy to share in a quick call or just send them over by email. Whatever works best for your schedule."

**Why it works:** You are offering something, not asking for something. The customer's response requires minimal effort (reply "send by email" and they are re-engaged).

### Pattern 2: The Direct Acknowledgement

**Best for:** When the silence is conspicuous and pretending it is not happening would be dishonest.

**Structure:**
Acknowledge the silence without making it about you. Express genuine curiosity about what is driving it. Offer to adjust the engagement model.

**Example:**
"Hi [name], I have reached out a few times without hearing back. I want to respect your time and not add to the noise. A couple of possibilities: (a) things are going well and you do not need anything from me right now, (b) something has changed and it would be helpful to talk, or (c) I am not reaching you at the right time or with the right topics. Any of those would be useful to know. A one-line reply is plenty."

**Why it works:** It is honest without being passive-aggressive. It gives the customer three easy options and asks for minimal effort. Most importantly, it names the silence without blaming them for it.

### Pattern 3: The New Angle

**Best for:** When your previous outreach was generic and did not give them a reason to respond.

**Structure:**
Drop the thread entirely. Come in with something completely new -- a different topic, a different value proposition, or a different ask.

**Example:**
"Hi [name], different topic from my recent notes -- I wanted to flag that we just released [specific feature] that directly addresses the [specific use case] your team was exploring last quarter. It is live on your account now. Would a 15-minute walkthrough be useful, or would you prefer I send a quick video?"

**Why it works:** If your previous emails were "just checking in" and they did not respond, more of the same will not break through. A new topic resets the conversation.

### Pattern 4: The Honest Last Attempt

**Best for:** After 3+ unanswered outreach attempts. This is the closing email in the sequence.

**Structure:**
Be direct that this is your last attempt on this thread. No guilt trip, no corporate language. Just honesty and an open door.

**Example:**
"Hi [name], I know you are busy and I do not want to keep filling your inbox if this is not a priority. I will hold off on further outreach for now. When you are ready to reconnect -- whether that is about [specific topic], something else, or just a catch-up -- I am here. My door is always open."

**Why it works:** It releases the pressure. Some customers respond to the "last chance" framing because removing the obligation paradoxically creates permission to engage. Others genuinely need the space, and sending this email protects the relationship for the future.

## Sequence Logic

If you are planning a re-engagement sequence (not just a single email):

| Attempt | Timing | Pattern | Escalation |
|---------|--------|---------|-----------|
| 1 | Day 0 (first re-engagement attempt after silence is identified) | Value-First or New Angle | None -- standard outreach |
| 2 | Day 7 | Direct Acknowledgement | Consider changing channel (call instead of email) |
| 3 | Day 14 | Honest Last Attempt | Consider reaching out through a different contact at the account |
| Post-sequence | Day 30+ | No outreach. Monitor usage and engagement signals. If product usage drops, escalate as a risk signal | CSM manager awareness |

**Critical rule:** After the Honest Last Attempt, stop emailing this contact. Continued outreach after a clear sign-off degrades the relationship. If you need to re-engage later, wait for a genuine trigger (new feature, renewal approaching, usage change) and come in fresh.

## Output Format

For each email, the skill produces:
- Subject line (specific, not "Following up" or "Checking in")
- Body text (under 100 words for re-engagement emails -- shorter than standard check-ins)
- Pattern used and rationale
- Suggested timing
- Alternative channel recommendation (if email has not worked, maybe a call or Slack message would)
- Next step if they do not respond (escalation path)

## Quality Gates

- Is the subject line specific enough to earn an open? "Quick question about your Q2 reporting workflow" works. "Following up" does not
- Is the email under 100 words? Re-engagement emails must be shorter than normal emails. The customer has already demonstrated they do not have time for (or interest in) your outreach
- Does the email give them a reason to respond that serves their interest, not just yours? "Can we schedule a QBR?" serves you. "Your automation metrics are impressive -- I have 3 recommendations to push them further" serves them
- Does the email make it easy to respond? The ideal response is one sentence or a single click. "Reply 'yes' and I will send them over" is lower friction than "let me know if you would like to discuss"
- Have you acknowledged the silence without blaming them for it? "I have not heard from you" is neutral. "You have not responded" is accusatory. "I know you are busy" is presumptuous but forgivable. "I want to make sure I am adding value, not noise" is honest

## Principles

- Silence is feedback. If a customer stops responding, something has changed. Your job is to figure out what changed, not to email louder
- Volume is not the answer. Sending 5 emails in 2 weeks to someone who did not respond to the first one does not show persistence. It shows poor judgment. Space the sequence, vary the approach, and know when to stop
- The best re-engagement emails do not ask for time. They offer value. "Here is something useful" beats "Can we talk?" every time
- Sometimes the right answer is to stop emailing and pick up the phone. Email is easy to ignore. A direct call is harder to avoid and often more respectful of the seriousness of the silence
