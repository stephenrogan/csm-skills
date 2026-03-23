---
name: cs-metrics-explainer
description: Takes a CS metric and produces a comprehensive explanation including definition, calculation method, industry benchmarks, what drives it, how to influence it, and common misinterpretations. Use when asked to explain a CS metric, understand NRR or GRR, learn about health scoring, define a retention metric, understand what a metric means and how to move it, or when a CSM needs to build commercial and analytical fluency on CS metrics. Also triggers for questions about CS KPIs, metric definitions, benchmark ranges, how metrics are calculated, what good looks like for a specific metric, or how to explain a CS metric to leadership.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# CS Metrics Explainer

Takes any CS metric and produces a complete breakdown: what it measures, how to calculate it, what good looks like, what drives it, how to influence it, and how to present it to different audiences. The analytical fluency tool for CSMs levelling up their commercial and data skills.

## How to Use

Provide:
- The metric you want to understand (NRR, GRR, logo churn, health score, time-to-value, expansion rate, etc.)
- Your context (why you need to understand it -- presenting to leadership, building your knowledge, preparing for an interview, setting team targets)
- Your current level of familiarity (new to this metric, understand the basics but want depth, need to explain it to others)

## Metric Breakdown Framework

For each metric, the skill produces:

### 1. Definition
What it measures in one sentence, with no jargon.

### 2. Calculation
The exact formula with an example using realistic numbers.

### 3. Benchmarks
What "good" looks like by company stage, segment, and motion:

| Context | Good | Median | Concerning |
|---------|------|--------|-----------|
| [Company stage / segment / motion] | [range] | [range] | [range] |

### 4. What Drives It
The 3-5 factors that most influence this metric, ranked by impact.

### 5. How to Influence It
Specific actions a CSM or CS leader can take to move the metric.

### 6. Common Misinterpretations
How the metric is frequently misunderstood or misused.

### 7. How to Present It
How to explain this metric to different audiences (CFO, CRO, board, team).

## Core CS Metrics Library

### Net Revenue Retention (NRR)

**Definition:** The percentage of revenue retained from existing customers over a period, including expansion and contraction. Measures whether you are growing or shrinking from your existing base.

**Calculation:**
NRR = (Starting ARR - Churn - Contraction + Expansion) / Starting ARR * 100

**Example:** Starting ARR EUR 10M, Churn EUR 500k, Contraction EUR 200k, Expansion EUR 1.2M
NRR = (10M - 500k - 200k + 1.2M) / 10M = 115%

**Benchmarks:**

| Context | Good | Median | Concerning |
|---------|------|--------|-----------|
| Enterprise SaaS | >120% | 110-120% | <105% |
| Mid-Market SaaS | >110% | 100-110% | <95% |
| SMB SaaS | >100% | 90-100% | <85% |

**What drives it:** Churn rate (negative impact), expansion rate (positive impact), contraction rate (negative), pricing power, product-market fit.

**How to influence it:** Reduce churn through proactive risk management. Drive expansion through adoption depth and value evidence. Reduce contraction by maintaining product relevance and stakeholder coverage.

**Misinterpretation:** NRR >100% does not mean you are not losing customers. It means expansion from remaining customers exceeds the revenue lost. You can have 15% logo churn and still show 110% NRR if your expanding accounts grow enough. Track logo churn separately.

**Present to CFO as:** "For every EUR 1 of revenue we started the year with from existing customers, we ended the year with EUR 1.15. Our existing customer base is a growing asset, not a depreciating one."

### Gross Revenue Retention (GRR)

**Definition:** The percentage of revenue retained from existing customers, excluding expansion. Measures the health of your base without the offset of growth.

**Calculation:**
GRR = (Starting ARR - Churn - Contraction) / Starting ARR * 100. Maximum is 100% (expansion is excluded).

**Benchmarks:**

| Context | Good | Median | Concerning |
|---------|------|--------|-----------|
| Enterprise SaaS | >95% | 90-95% | <88% |
| Mid-Market SaaS | >90% | 85-90% | <80% |
| SMB SaaS | >85% | 75-85% | <70% |

**What drives it:** Product-market fit, customer health, service quality, competitive positioning, pricing appropriateness.

**Misinterpretation:** GRR is harder to hide behind than NRR. A company with 85% GRR and 115% NRR is losing a lot of customers but making up for it with aggressive expansion. That works until expansion slows -- then GRR becomes the real retention story.

**Present to board as:** "We retained [X]% of our existing revenue base. This is our loyalty metric -- it tells us whether customers are staying and at what level, independent of growth."

### Additional metrics the skill covers:

- **Logo churn rate** -- percentage of customers lost
- **Time-to-value** -- days from contract to first measurable outcome
- **Health score** -- composite assessment of account health
- **Expansion rate** -- revenue growth from existing customers
- **CSM-to-account ratio** -- capacity metric
- **Touchpoint cadence compliance** -- process metric
- **First call resolution** -- support quality proxy
- **Product adoption breadth** -- feature utilisation metric
- **Customer lifetime value (CLV)** -- long-term revenue projection per customer

For each, the skill produces the same 7-element breakdown.

## Output Format

```
## Metric Explainer: [Metric Name]

### Definition
[One sentence]

### Calculation
[Formula + worked example]

### Benchmarks
[Table by context]

### What Drives It
1. [Factor 1 -- highest impact]
2. [Factor 2]
3. [Factor 3]

### How to Influence It
- [Action 1]
- [Action 2]

### Common Misinterpretations
- [Misinterpretation 1 with correction]

### How to Present It
- To CFO: [framing]
- To CRO: [framing]
- To board: [framing]
- To your team: [framing]
```

## Quality Gates

- Is the calculation correct with a worked example? A formula without an example is theoretical. A worked example with realistic numbers makes it concrete
- Are the benchmarks sourced or qualified? Present ranges, not precise numbers. Benchmarks vary by source, industry, and methodology. Ranges are honest; precise numbers imply false precision
- Is the "how to influence it" actionable by a CSM? "Improve product-market fit" is not CSM-actionable. "Drive adoption depth in the top 20 accounts to reduce churn probability" is

## Principles

- Metrics are a language, not a science. Understanding CS metrics is how you participate in commercial conversations with leadership. You do not need to be a data analyst -- you need to speak the language and know what the numbers mean for your work
- Every metric tells a story and hides a story. NRR of 115% tells the growth story. It hides the churn story. Know what each metric reveals and what it conceals
- Metrics without context are just numbers. "GRR is 88%" means nothing without knowing whether that is good (for SMB SaaS, it is above median) or bad (for enterprise SaaS, it is concerning). Always present metrics with context
