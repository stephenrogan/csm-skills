---
name: account-swot-analyser
description: Produces a structured SWOT analysis for a customer account, identifying strengths to leverage, weaknesses to address, opportunities to pursue, and threats to mitigate. Connects each element to specific actions. Use when asked to analyse an account strategically, build a SWOT for a customer, assess an account's position, prepare for a strategic planning session, or when a CSM needs to move beyond operational management to strategic thinking about a key account. Also triggers for questions about strategic account analysis, account positioning, opportunity and risk mapping, or comprehensive account assessment.
license: MIT
metadata:
  author: Stephen Rogan
  version: "1.0.0"
  standalone: true
---

# Account SWOT Analyser

Produces a structured SWOT analysis for a specific account. Not the generic "Strengths: good product, Weaknesses: competitive market" variety -- a specific, evidence-based analysis that connects each element to an action the CSM should take.

The SWOT framework is simple. The value is in the discipline of honest assessment across all four quadrants, not in the framework itself.

## How to Use

Provide:
- Account name, ARR, tenure, segment, product tier
- Usage and adoption data (what they are using, what they are not)
- Relationship landscape (who you know, relationship strength, coverage gaps)
- Customer goals and how the product serves them
- Any known risks (competitive, commercial, product, relationship)
- Any known opportunities (expansion, new teams, new use cases)
- Recent events (positive or negative)

## SWOT Framework

### Strengths (Internal Positive -- What is working in your favour)

These are factors within the account relationship that support retention and growth:

| Strength Category | What to Assess | Example |
|------------------|---------------|---------|
| Product adoption | Deep usage, high feature breadth, strong workflows | "Team has automated 2,847 workflows. Feature adoption at 75% breadth -- above segment median" |
| Value delivery | Quantified ROI, customer-confirmed outcomes | "Customer confirmed 67% reduction in manual reporting time in last QBR" |
| Relationship | Multi-threaded, champion engaged, executive sponsor exists | "3 active contacts including VP Engineering sponsor. Champion engagement is strong" |
| Strategic alignment | Product roadmap matches customer direction | "Our Q3 reporting features directly address their biggest gap" |
| Switching cost | Deep integrations, trained team, embedded workflows | "3 API integrations, 47 trained users, 23 configured workflows. Migration cost is significant" |
| Advocacy | Customer is a promoter, has done references or case studies | "NPS 9, completed a case study last quarter, spoke at user conference" |

**For each strength, ask:** How are we leveraging this? A strength that is not leveraged is a wasted asset.

### Weaknesses (Internal Negative -- What is working against you)

These are factors within the relationship that create vulnerability:

| Weakness Category | What to Assess | Example |
|------------------|---------------|---------|
| Adoption gaps | Underutilised features, shallow usage, declining engagement | "Advanced Reporting untouched despite being relevant to their goals. 3 features abandoned in Q4" |
| Value gap | ROI unproven, value not articulated, customer questioning the investment | "No quantified ROI. Customer has not confirmed value in 6 months" |
| Relationship | Single-threaded, champion cooling, no executive, detractor present | "Single-threaded to Tom. No economic buyer relationship. Tom's engagement is declining" |
| Product fit | Feature gaps, workarounds, performance issues, integration limitations | "Custom reporting gap is the #1 feature request. Customer is building manual workarounds" |
| Service | Support history, unresolved issues, CSAT decline | "3 P2 tickets in 60 days. Average resolution time above SLA" |
| Commercial | Pricing concerns, contract friction, competitor pricing pressure | "Customer mentioned pricing in last QBR. Competitor is 20% cheaper for comparable features" |

**For each weakness, ask:** What is the plan to address this? A documented weakness without a mitigation plan is just a risk you are choosing to accept.

### Opportunities (External Positive -- What could go right)

These are factors in the customer's environment that could benefit the relationship:

| Opportunity Category | What to Assess | Example |
|---------------------|---------------|---------|
| Growth | Customer is expanding (new teams, new geographies, new use cases) | "Marketing team expressed interest in the product. 15 new engineers starting in April" |
| Strategic alignment | Customer's priorities shifting toward capabilities you offer | "New CEO focused on operational efficiency -- directly aligned with our value proposition" |
| Competitive | Competitor weakness, failed competitor implementation at another company, market consolidation | "Customer's peer had a public failure with Competitor X. Reinforces our stability narrative" |
| Product | Upcoming features that address their gaps, roadmap alignment | "Custom reporting shipping in Q3 -- addresses their #1 request" |
| Relationship | New hire in a relevant role, stakeholder willing to advocate, executive open to engagement | "New VP of Operations starts next month -- opportunity to build executive relationship" |
| Industry | Market trends favouring your product category, regulatory changes creating demand | "New data compliance requirements will drive demand for our audit capabilities" |

**For each opportunity, ask:** What is the trigger to pursue this, and what is the first action?

### Threats (External Negative -- What could go wrong)

These are factors in the customer's environment that could damage the relationship:

| Threat Category | What to Assess | Example |
|----------------|---------------|---------|
| Competitive | Active evaluation, competitor outreach, competitive feature advantage | "Customer mentioned 'exploring options' in last check-in. Competitor has stronger reporting" |
| Economic | Budget cuts, headcount freeze, strategic pivot away from your category | "Customer announced 15% cost reduction across all departments" |
| Stakeholder | Champion departure risk, executive change, reorg | "Champion has been at the company 5 years -- typical tenure for their role. Departure risk is real" |
| Product | Feature sunset that affects them, breaking change, performance degradation | "API v2 deprecation will require migration effort from their team" |
| Market | Industry downturn, customer's business model under pressure | "Customer's core market is contracting. Revenue pressure may lead to vendor consolidation" |

**For each threat, ask:** What is the early warning signal, and what is the response plan if it materialises?

## Connecting SWOT to Action

The analysis is only useful if it drives action. For each quadrant:

| Quadrant | Action Type | Example |
|----------|------------|---------|
| Strength | Leverage it | "Use the strong champion relationship to introduce an executive sponsor" |
| Weakness | Mitigate it | "Build value evidence before the renewal conversation. Cannot enter the renewal without ROI data" |
| Opportunity | Pursue it | "Propose a demo for the Marketing team next month. Champion can facilitate the introduction" |
| Threat | Prepare for it | "Begin multi-threading now so champion departure does not strand the relationship" |

## Output Format

```
## SWOT Analysis: [Account Name]
**Date:** [date] | **Analyst:** [CSM name]
**ARR:** [amount] | **Health:** [band] | **Renewal:** [date]

### Strengths
| Strength | Evidence | Action to Leverage |
|----------|---------|-------------------|
| [strength] | [specific evidence] | [how to use this] |

### Weaknesses
| Weakness | Evidence | Action to Mitigate |
|----------|---------|-------------------|
| [weakness] | [specific evidence] | [plan to address] |

### Opportunities
| Opportunity | Evidence | Action to Pursue |
|------------|---------|-----------------|
| [opportunity] | [specific evidence] | [first action + trigger] |

### Threats
| Threat | Probability | Impact | Early Warning | Response Plan |
|--------|-----------|--------|--------------|--------------|
| [threat] | [H/M/L] | [H/M/L] | [signal] | [what to do] |

### Strategic Priority
[One sentence: given this analysis, what is the single most important thing to focus on for this account in the next 90 days?]
```

## Quality Gates

- Is every cell in the table filled with specific evidence, not generic observations? "Good relationship" is not evidence. "3 active contacts, champion engagement weekly, NPS 9" is evidence
- Are there items in every quadrant? An account with no weaknesses or no threats has been assessed optimistically, not honestly. Every account has vulnerabilities
- Does every item connect to an action? The SWOT without actions is an observation exercise. The SWOT with actions is a strategic plan
- Is the strategic priority clear? If you cannot distil the entire analysis into one priority, the analysis is unfocused
- Would your manager agree with this assessment? If they would push back on a strength you listed or a threat you omitted, the analysis needs revision

## Principles

- Honesty is the prerequisite for usefulness. An optimistic SWOT that underplays weaknesses and overplays strengths produces a strategy built on false assumptions. When the assumptions break, so does the strategy
- Threats and weaknesses are not the same thing. Weaknesses are within your control to address (relationship gaps, adoption issues, value evidence). Threats are external (competitor moves, budget cuts, champion departure). The distinction matters because the responses are different
- The SWOT should be reviewed quarterly. Account dynamics change. A strength 6 months ago (strong champion) may be a weakness now (champion disengaging). The analysis is a snapshot, not a permanent classification
- One strong strategic priority is more valuable than a comprehensive list of actions. A CSM who knows "the most important thing for this account is securing executive sponsorship before the renewal" has a clear focus. A CSM with 12 action items across all quadrants has a to-do list, not a strategy
