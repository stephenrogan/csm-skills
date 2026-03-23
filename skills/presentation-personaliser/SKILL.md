---
name: presentation-personaliser
description: Adapts a generic presentation deck or template to a specific customer account by inserting relevant data, adjusting framing for the audience, and ensuring all references are account-specific. Use when asked to personalise a deck, customise a presentation for a specific customer, adapt a template for a meeting, tailor slides with account data, or when any generic presentation needs to be made specific before a customer interaction. Also triggers for questions about deck customisation, presentation personalisation, template adaptation, or making a generic deck feel account-specific.
license: MIT
metadata:
  version: "1.0.0"
  standalone: true
---

# Presentation Personaliser

Takes a generic deck or template and transforms it into an account-specific presentation. Every slide should feel like it was built for this customer, not adapted from a template -- even though it was.

The difference between a personalised deck and a generic one is 15 minutes of preparation that saves 45 minutes of the customer's goodwill. Customers can always tell when a deck is a template. They cannot always tell when a template has been genuinely adapted.

## How to Use

Provide:
- The template content or structure (slide titles, generic content, standard sections)
- The account context (name, ARR, segment, product tier, key contacts, goals)
- Data to insert (usage metrics, value evidence, milestones, support summary)
- The audience (who will see this, what they care about, their communication preferences)
- The meeting purpose (QBR, renewal, onboarding review, executive presentation, expansion pitch)

## Personalisation Layers

### Layer 1: Data Insertion (Minimum -- Do This Always)

Replace every placeholder and generic reference:

| Generic | Personalised |
|---------|-------------|
| "Your company" | "[Account name]" |
| "Your team" | "[Specific team name -- e.g., 'the analytics team']" |
| "Key metrics" | "[Actual metrics with numbers]" |
| "Recent achievements" | "[Specific milestone with date]" |
| "Our product" | "[Product name as the customer knows it]" |

If a slide references data you do not have, note it ("Data not available -- recommend removing this slide or replacing with qualitative observation").

### Layer 2: Framing Adjustment (Standard -- Do This for Important Meetings)

Adjust the narrative to match the audience and their priorities:

| Audience | Framing Shift |
|----------|--------------|
| Technical team | Lead with product capabilities and usage depth. Less business case, more technical evidence |
| Finance / CFO | Lead with ROI and cost efficiency. Frame every metric in terms of return on investment |
| Operations | Lead with process improvement and time savings. Frame in terms of workflow efficiency |
| Executive | Lead with strategic alignment and business impact. Frame in terms of competitive advantage and growth |
| Mixed audience | Lead with the highest-seniority person's priorities. Address other perspectives in supporting slides |

### Layer 3: Narrative Customisation (Premium -- Do This for Strategic Accounts)

Rewrite the slide narrative to tell this customer's specific story:

- Replace generic success language with their specific achievements
- Reference conversations you have had ("As we discussed in our January review...")
- Connect product usage to their stated business goals, not to generic value propositions
- Include forward-looking content specific to their plans ("As you prepare for the Q3 expansion into the EMEA region...")

## Slide-by-Slide Personalisation

For each slide in the template, the skill produces:

```
## Slide [N]: [Title]

### Template Content
[What the generic slide says]

### Personalised Content
[What this slide should say for this account]

### Data Needed
[Specific data points to insert]

### Personalisation Notes
[Framing adjustments, audience considerations, things to add or remove]

### Confidence
[High: data is available and accurate / Medium: data is estimated or partial / Low: slide should be removed or replaced]
```

## Output Format

The complete personalised deck content, slide by slide, ready to be transferred into the actual presentation tool. Each slide includes the personalised content, any data points with their sources, and notes for the CSM on how to present the slide.

## Quality Gates

- Is every instance of "your company" replaced with the actual account name? A single "your company" in a sea of "[Account Name]" references screams template
- Is every data point current? Presenting last quarter's data as if it is current undermines credibility. Check freshness of every number
- Does the deck tell a story specific to this customer? If you could present this deck to any other customer with minimal changes, it is not personalised enough
- Is the level of detail appropriate for the audience? An executive does not need 15 data slides. A technical team does not need 3 slides of business case
- Has anything been included that the customer should not see? Internal risk scores, competitor analysis, CSM assessments, or notes from internal discussions must be stripped

## Principles

- Personalisation is not just find-and-replace. Swapping "[Company]" for "Acme Corp" is the minimum. True personalisation means the customer recognises their own story in every slide
- Less is more. A 10-slide personalised deck with strong data on every slide is better than a 20-slide template where half the slides have generic content
- The slide you remove matters as much as the slide you personalise. If a template slide is not relevant to this customer, cut it. Do not present irrelevant content just because the template includes it
- The customer will remember one number and one insight. Make sure the deck is structured so that one number and one insight are unmissable. Everything else supports those two things
