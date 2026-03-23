---
name: call-summary-generator
description: Generates a structured post-call summary from raw notes, key observations, or a brain dump of what happened. Organises the chaos into discussion points, decisions, action items, sentiment, and flags. Use when asked to summarise a call, structure meeting notes, organise what happened in a conversation, create a call summary from notes, or when a CSM has raw thoughts from a customer call and needs them structured. Also triggers for questions about call documentation, meeting summarisation, note organisation, or turning a call brain dump into a usable record.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Call Summary Generator

Takes your raw, unstructured post-call notes and turns them into a structured summary. The input can be messy -- bullet points, fragments, stream-of-consciousness. The output is clean and actionable.

Different from the follow-up email (customer-facing) and the meeting outcome log (CRM-facing) -- this is the comprehensive record for your own reference and your team's context.

## How to Use

After a call, provide:
- Your raw notes (however messy -- the skill structures them)
- Who was on the call (customer and internal)
- Call duration and type
- Anything you want to highlight or flag

## What It Produces

### Discussion Points (What Was Covered)

Organises the conversation into distinct topics, each with:
- Topic name
- What was discussed (2-3 sentences)
- Conclusion or outcome (if any)
- Open questions (if the topic was not resolved)

### Decisions (What Was Agreed)

Explicit agreements from the call:
- What was decided
- Who decided (consensus, or one person's call)
- Any conditions or caveats

### Action Items (Who Committed to What)

Extracted from the notes using the same patterns as the action-item-extractor:

| Action | Owner | Deadline | Confidence |
|--------|-------|----------|-----------|
| [action] | [name] | [date] | [High: explicit commitment / Medium: implied / Low: vague offer] |

### Sentiment Assessment

Based on your notes and observations:
- Overall: positive / neutral / negative / mixed
- Specific signals: what you noticed about the customer's energy, engagement, specific statements
- Shift: did the sentiment change during the call? (Started positive, turned negative during the pricing discussion)

### Flags

Signals that should trigger downstream attention:
- **Risk flags:** Frustration expressed, competitive mention, budget concern, disengagement signals
- **Expansion flags:** Growth interest, new team mentions, feature requests indicating deeper adoption
- **Product flags:** Feature requests, bug reports, integration needs
- **Relationship flags:** Champion sentiment change, new stakeholder identified, political observation

## Output Format

```
## Call Summary: [Account Name]
**Date:** [date] | **Type:** [type] | **Duration:** [minutes]
**Attendees:** [customer contacts] | [internal team]

### Discussion Points
1. **[Topic]**: [2-3 sentence summary]. Conclusion: [outcome or "open"]
2. **[Topic]**: [2-3 sentence summary]. Conclusion: [outcome or "open"]

### Decisions
- [Decision 1]
- [Decision 2]

### Action Items
| Action | Owner | Deadline | Confidence |
|--------|-------|----------|-----------|
| [action] | [name] | [date] | [H/M/L] |

### Sentiment
Overall: [assessment]
Signals: [specific observations]

### Flags
- [Risk/Expansion/Product/Relationship]: [detail]

### Next Touchpoint
[When and what]
```

## Handling Messy Input

The skill works with various input quality levels:

| Input Quality | What You Provide | What the Skill Does |
|-------------|-----------------|-------------------|
| Detailed notes | Structured bullet points with quotes and observations | Organises into the template with minimal inference |
| Rough notes | Fragments, shorthand, incomplete sentences | Interprets and structures. Flags anything unclear for your review |
| Brain dump | Stream-of-consciousness paragraph about what happened | Extracts topics, actions, and sentiment. Asks for clarification on ambiguities |
| Minimal notes | "Discussed renewal, they are happy, Tom will send the data" | Produces a minimal summary. Flags: "Notes are sparse -- review for completeness before finalising" |

## Quality Gates

- Are all action items extracted? Scan the raw notes for commitment language ("I will," "we will," "let's") and confirm each one appears in the action item table
- Is the sentiment assessment honest? "Positive" because no one complained is not the same as "positive" because the customer expressed enthusiasm. Label the evidence
- Are flags captured? A competitive mention buried in paragraph 3 of your notes should appear as a flag in the summary, not disappear into the narrative
- Could someone who was not on the call understand the summary? That is the bar. Your manager, your successor, your colleague covering your accounts while you are on leave -- they should be able to read this and know what happened

## Principles

- Write the summary within 1 hour. The quality of your recall degrades exponentially. Notes written the same day are 3x more accurate than notes written the next day
- The summary is a thinking tool, not just a documentation tool. The act of structuring your notes forces you to process what happened: what was the most important topic? What did the customer really mean? What did I commit to? The structure creates clarity that raw notes do not
- Err on the side of capturing too much. You can always trim a comprehensive summary. You cannot reconstruct a missing observation 2 weeks later. When in doubt, include it
- The flags section is the highest-value part for downstream use. The discussion points are for you. The flags are for the system -- they trigger risk reviews, expansion conversations, and product feedback loops
