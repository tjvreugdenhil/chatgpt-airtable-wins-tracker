# Overview: Wins Tracker Framework

This document explains the purpose of the **ChatGPT + Airtable Wins Tracker** and outlines a typical weekly workflow for using it.  The framework is designed to help you capture and reflect on your accomplishments—both personal and professional—while making it easy to compute approximate monetary value and track next steps.  It leverages a structured Airtable schema and ChatGPT prompts to streamline data entry and analysis.

## Purpose

The Wins Tracker addresses two common challenges:

1. **Remembering successes** – Accomplishments are easy to forget in the day‑to‑day rush.  Recording them helps with performance reviews, resume updates, and self‑reflection.
2. **Quantifying impact** – By approximating the time saved or value generated, you can prioritize future efforts and communicate impact more clearly.

## Weekly Workflow

1. **Collect wins**: Throughout the week, whenever you complete a task or solve a problem that feels meaningful, open ChatGPT and run the **“Create Win Record”** prompt (see [`docs/03-chatgpt-prompts.md`](03-chatgpt-prompts.md)).  Provide details such as what you did, the impact, any links or supporting notes, and a rough monetary value estimate.
2. **Review and categorize**: At the end of the week, review your new entries in Airtable.  Update the **Status** field (e.g., “In progress,” “Complete”) and refine the **Priority** if needed.
3. **Recalculate value**: Use the **“Recalculate Value”** prompt to compute a more conservative expected value and write a concise justification.  This helps reduce optimism bias and ensures consistency across records.
4. **Plan next steps**: For incomplete tasks, fill in the **Next Steps** field with specific actions or follow‑ups.  For completed wins, summarize what you learned or would do differently next time.
5. **Reflect**: Periodically, browse your Airtable table to remind yourself of your accomplishments.  Seeing your progress can be motivating and can inform future goals.

This workflow is flexible—you can adapt it to daily check‑ins or monthly retrospectives.  The key is to maintain a rhythm of capture, categorize, evaluate, and reflect.
