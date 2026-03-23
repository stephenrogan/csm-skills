---
name: value-narrative-builder
description: Constructs a compelling value narrative for a customer account by connecting product usage to business outcomes in the customer's language. Produces different versions for different audiences -- the champion, the CFO, the board. Use when asked to build a value story, articulate ROI, create a business case for the customer, prepare value evidence for a renewal or QBR, or when a CSM needs to translate usage metrics into business impact the customer will recognise. Also triggers for questions about value articulation, ROI storytelling, customer business case, value evidence, or how to prove the product is worth the investment.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Value Narrative Builder

Translates product usage into business outcomes in the customer's own language. The gap between "your team made 2,847 API calls this month" (product metric) and "your team eliminated 340 hours of manual work this quarter" (business outcome) is the value narrative. Most CSMs report metrics. The best CSMs tell value stories.

## How to Use

Provide:
- What the customer uses (features, workflows, frequency)
- What outcomes they have experienced or you can estimate (time saved, revenue impact, cost reduction, error reduction, speed improvement)
- Their original goals (why they bought -- from the sales process or onboarding)
- The audience for this narrative (champion, CFO, CEO, board, procurement)
- Any customer-confirmed value ("they told us X" vs. "we estimate X")

## The Value Hierarchy

Value narratives work on three levels. Higher levels resonate with more senior audiences:

| Level | Frame | Example | Best Audience |
|-------|-------|---------|-------------|
| Activity | What the product does | "Your team automated 2,847 workflows this quarter" | End users, technical leads |
| Outcome | What the activity produces | "That automation eliminated 340 hours of manual work this quarter" | Champions, managers, directors |
| Impact | What the outcome means for the business | "At your team's loaded cost, that is EUR 51,000 in recovered productivity -- a 3.4x return on the annual investment" | CFOs, CROs, executives, board |

**Rule:** Always present at least one level above what the audience already knows. Your champion knows the activity. Give them the outcome. Your CFO does not care about the outcome. Give them the impact.

## Building the Narrative

### Step 1: Connect Usage to Outcomes

For each major feature or workflow the customer uses:

| Usage Metric | Outcome Translation | Calculation |
|-------------|-------------------|------------|
| [Metric] | [What it means in business terms] | [How you calculated it] |

**Example:**
| Usage | Outcome | Calculation |
|-------|---------|------------|
| 2,847 automated workflows | 340 hours of manual work eliminated | Average 7 minutes saved per workflow * 2,847 = 19,929 minutes = 332 hours (rounded to 340) |
| 47 active users (of 60 seats) | 78% adoption -- above the 65% segment median | Active users / licensed seats |
| 12 custom reports running automatically | Replaced a manual weekly process | Customer confirmed: "We used to spend 4 hours every Monday compiling this" |

### Step 2: Translate Outcomes to Impact

| Outcome | Impact Translation | Method |
|---------|-------------------|--------|
| 340 hours saved | EUR 51,000 in recovered productivity | 340 hours * EUR 150 loaded cost/hour (mid-market SaaS team average) |
| Weekly manual process eliminated | 208 hours/year freed for strategic work | 4 hours/week * 52 weeks |
| 78% adoption (vs. 65% median) | Team is extracting above-average value from the investment | Benchmark comparison |

### Step 3: Frame by Audience

**For the Champion:**
"Your team automated 2,847 workflows this quarter -- up 22% from last quarter. That is roughly 340 hours your team did not spend on manual work. The adoption rate of 78% puts you in the top quartile for companies your size."

**For the CFO:**
"The annual investment in [product] is EUR [X]. This quarter alone, the platform eliminated an estimated 340 hours of manual work across the team -- approximately EUR 51,000 in recovered productivity at your team's loaded cost. That is a 3.4x annualised return. The adoption rate continues to grow, which means this return is increasing, not plateauing."

**For the Board:**
"[Customer] achieved a 3.4x return on their [product] investment this quarter through workflow automation and process efficiency. Adoption is in the top quartile for their segment. Expansion discussion is underway."

### Step 4: Address the Gaps Honestly

If value evidence is weak in some areas, acknowledge it:
- "We estimate 340 hours saved based on workflow completion data. This has not yet been validated by the customer -- I recommend confirming in our next QBR"
- "Adoption is at 78% but the analytics team (12 users) has not engaged. The value narrative is strong for the engineering team but untested for analytics"

## Value Evidence Types (Ranked by Credibility)

| Type | Credibility | Example |
|------|-----------|---------|
| Customer-confirmed | Highest | "The customer said: 'This tool saved us 10 hours a week'" |
| Customer-validated | High | "We presented the estimate and the customer agreed it was accurate" |
| Data-derived | Medium | "Based on workflow volume and estimated time savings per workflow" |
| Estimated | Low-Medium | "Based on industry benchmarks for similar companies" |
| Assumed | Low | "We believe the product is delivering value" (do not use this) |

**Rule:** Always label your evidence type. "340 hours saved (data-derived, not yet customer-confirmed)" is honest and credible. "340 hours saved" without qualification will be challenged.

## Output Format

```
## Value Narrative: [Account Name]
**Audience:** [who this is for]
**Period:** [timeframe]

### Headline Metric
[The single number that best captures the value: "3.4x ROI" or "340 hours saved" or "67% reduction in manual reporting"]

### The Story
[3-5 sentences: what they use, what it produces, what it means for their business]

### Supporting Evidence
| Metric | Value | Type | Confidence |
|--------|-------|------|-----------|
| [metric] | [value] | [customer-confirmed / data-derived / estimated] | [H/M/L] |

### Gaps and Caveats
[What is not yet proven, what needs customer validation, what is estimated vs. confirmed]
```

## Quality Gates

- Does the narrative contain at least one number? A value story without quantification is an opinion, not evidence
- Is the evidence type labelled? Presenting an estimate as a confirmed metric will backfire when challenged
- Is the framing calibrated to the audience? Activity metrics for a CFO waste their time. Impact metrics for an end user feel disconnected from their daily experience
- Does the narrative connect to the customer's original goals? If they bought to "reduce manual reporting time" and your narrative is about "API call volume," you have missed the connection
- Would the customer agree with this narrative if they read it? That is the ultimate test. If they would push back on the numbers or the framing, revise before presenting

## Principles

- Value is not what the product does. Value is what the customer achieves because of what the product does. The product automates workflows. The value is the 340 hours the team spends on strategic work instead of manual tasks. Always articulate value in the customer's terms, not yours
- Customer-confirmed value is 10x more credible than your estimate. One sentence from the customer -- "this tool saved us 10 hours a week" -- is more powerful in a renewal conversation than a 5-page ROI analysis you built yourself. Capture customer language whenever they express value
- The value narrative should get stronger over time. If you cannot articulate more value at renewal than at the 90-day mark, something is wrong -- either value is not growing or you are not measuring it
- An honest value narrative with gaps acknowledged is more credible than an inflated one. CFOs and procurement teams are trained to challenge vendor claims. Presenting conservative, well-sourced evidence builds trust. Presenting aggressive, unvalidated claims invites scrutiny
