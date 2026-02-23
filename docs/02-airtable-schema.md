# Airtable Schema

This schema defines the structure of the “ChatGPT Wins” Airtable base used by the Wins Tracker.  Each field name, type, and list of options is reproduced here so you can recreate the table without exposing any IDs or sensitive data.  A formula field is included to convert a dollar string into a numeric value.

## Table: Imported table

| # | Field Name | Field Type | Options/Notes |
|---|------------|------------|---------------|
| 1 | **Title** | Long text (multiline) | A descriptive title of the win or task. |
| 2 | **Status** | Single select | Choose one of: **Complete**, **In progress**, **Not‑Started**, **Hold**, **Built and Testing**. |
| 3 | **Date** | Date/time | When the win occurred.  Use date with time if helpful. |
| 4 | **What I did** | Long text (multiline) | Describe the actions you took. |
| 5 | **Impact** | Long text (multiline) | Explain the impact or benefit. |
| 6 | **Links** | Long text (multiline) | Paste any relevant links (e.g., docs, tickets). |
| 7 | **URL** | Long text (multiline) | Historically used to store a *dollar value string* such as `$150`.  See notes below. |
| 8 | **Multiple Select** | Multiple select | Options: **automation**, **home‑ops**, **printing**, **productivity**, **tracking**.  Use this to tag the type of win. |
| 9 | **Notes** | Long text (multiline) | Additional notes or context. |
| 10 | **Priority** | Single select | Rank the importance: **P1** through **P10** (P1 is highest priority). |
| 11 | **Value (Number)** | Formula | Converts the dollar string in **URL** to a numeric value.  Formula concept: `VALUE(SUBSTITUTE({URL}, "$", ""))`. |
| 12 | **Cost Value Justification** | Long text (multiline) | A short rationale explaining how you arrived at the value estimate. |
| 13 | **Next Steps** | Long text (multiline) | Describe what should happen next. |

### Notes on the “URL” Field

This template originally used a field named **URL** to store the dollar value as text (for example, `$150`).  The formula field **Value (Number)** then strips the dollar sign and converts it to a number.  Although this works, it can be confusing because the name suggests a web link rather than a value.

**Optional improvement:** Rename the field to **Value (USD text)** and add a new field called **Related URL** (single line text) to store any actual links associated with the win.  The formula can then reference `Value (USD text)` instead of `URL`.  However, to remain consistent with the existing setup, this documentation retains the original field name.
