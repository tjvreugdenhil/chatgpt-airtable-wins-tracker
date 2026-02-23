# Valuation Model

This document outlines a **conservative expected value model** for estimating the monetary benefit of your wins.  The goal is to produce realistic, comparable numbers while accounting for uncertainty and optimism bias.

## Formula

The estimated value of a win can be approximated as:

```
Value ≈ (Time Saved × Frequency × Hourly Rate) × Confidence Factor + (Risk Avoided × Probability)
```

Where:

- **Time Saved** is the amount of time saved per occurrence (in hours).
- **Frequency** describes how often the benefit occurs (for example: one‑time, weekly, monthly, quarterly, annually).  Convert this to an annualized multiplier (e.g. weekly → ~52 times per year).
- **Hourly Rate** is a rough estimate of the value of your time.  See default rates below.
- **Confidence Factor** ranges from 0.5 to 1.0.  Lower values reflect uncertainty (e.g. a process still in testing); higher values reflect confirmed savings.
- **Risk Avoided** represents the cost of preventing a negative outcome (e.g. avoiding a $1,000 penalty).  Multiply by its **Probability** of occurring.

After computing the value, round to the nearest dollar and record it as a string (e.g. `$120`) in the **URL** field.  Document your assumptions in **Cost Value Justification**.

## Default Hourly Rates

Use these suggested hourly rates when estimating value, unless you have more specific numbers:

| Context | Hourly Rate (USD) | Example |
|--------|------------------|---------|
| **Work deliverables** | $150/hr | Client work, billable projects, internal tools that save teammates’ time |
| **Personal/Home** | $60/hr | Household tasks, family errands |
| **Learning/Study** | $100/hr | Certifications, tutorials, professional development |

If your organization uses different internal bill rates or salary numbers, feel free to adjust these values accordingly.

## Confidence and Discounting

To avoid overestimating value, apply a confidence factor.  Examples:

- **0.9** – High confidence: The win has been implemented and proven to save time repeatedly.
- **0.7** – Moderate confidence: The win is partially tested or depends on user adoption.
- **0.5** – Low confidence: The win is still in design/testing and may not deliver full benefits.

You can also apply a discount if the outcome is not confirmed or the estimation relies on optimistic assumptions.  For example, multiply the result by 0.8 or 0.6 to reduce the value.

## Justification Template

When filling in the **Cost Value Justification** field, aim for a concise explanation (2–4 sentences).  Address these elements:

1. **Inputs**: Time saved, frequency, chosen hourly rate, any risk avoidance.  Mention if these are estimates or based on hard data.
2. **Confidence**: Explain whether the process is confirmed or in testing, and any discount applied.
3. **Outcome**: Conclude with a rounded dollar value and why it’s reasonable given the inputs.

Example:

> We save ~2 hours per week by automating this report.  At $150/hr and 52 occurrences per year, that’s $15,600 annually.  Given this is a new process with moderate adoption, I applied a 0.7 confidence factor and a 10% discount, resulting in a conservative estimate of **$9,800**.

Remember: The aim is to produce realistic numbers, not to inflate the impact.  Being conservative helps maintain credibility and allows fair comparisons between different wins.
