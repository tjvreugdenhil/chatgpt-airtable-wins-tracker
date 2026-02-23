# ChatGPT + Airtable Wins Tracker

This repository provides a framework for tracking personal and work wins using a combination of **Airtable** and **ChatGPT**.  It is written for people who want to replicate the workflow described in our internal documentation but without exposing any secrets or proprietary data.  By default it uses the built‑in Airtable connector available in ChatGPT (Settings → Apps → Airtable → Connect) so there are no API tokens to manage.

## Quick Start (Connector‑First)

1. **Create a new Airtable base and table** using the schema documented in [`docs/02-airtable-schema.md`](docs/02-airtable-schema.md).  The schema defines the fields, select options and formula you need.
2. **Connect Airtable to ChatGPT**.  In ChatGPT, open **Settings → Apps/Connectors → Airtable** and click **Connect** to grant read/write access to your base.  When prompted, choose the base you created in the previous step.  No API keys or tokens are required.
3. **Create and update win records** using the prompts in [`docs/03-chatgpt-prompts.md`](docs/03-chatgpt-prompts.md).  These prompts are designed for the ChatGPT Airtable connector and include guardrails to avoid making up data or exposing IDs.

You can run these prompts either in normal ChatGPT conversations or by using ChatGPT’s Agent mode.  Agent mode isn’t required for most tasks, but it can be helpful if you want ChatGPT to perform multi‑step tasks in the UI (for example, creating this repository on GitHub) but it’s optional.

## Do I Need Agent Mode?

You do **not** need Agent mode to use this framework.  Everything described here can be done in a normal ChatGPT chat by copying and pasting prompts and reviewing the results yourself.  Agent mode is useful if you want ChatGPT to perform multi‑step tasks in the UI (for example, creating a GitHub repository) but it’s optional.

## Repository Contents

This repo is intentionally minimal and sanitized.  It contains only the schema, prompts, valuation model and redaction guidelines.  No sensitive information—such as Airtable API tokens, base IDs, table IDs, field IDs, record IDs, personal URLs or emails—is included.

```
.
├── README.md                # This overview and quick‑start guide
├── LICENSE                  # MIT license text
├── .gitignore               # Ignore patterns for local development
└── docs/
    ├── 01-overview.md       # Purpose and weekly workflow
    ├── 02-airtable-schema.md# Airtable schema (fields, types, select options)
    ├── 03-chatgpt-prompts.md# Prompts for creating and updating records via the connector
    ├── 04-valuation-model.md# Conservative valuation rubric and formula
    └── 05-redaction-and-security.md# Guidance on redacting sensitive data
```

## Contributing

Feel free to fork or clone this repository and adapt it for your own use.  If you find an issue or want to add improvements, please open a pull request.  Always ensure that no secrets or personal data are included in your contributions.

## License

This project is released under the MIT License.  See [`LICENSE`](LICENSE) for details.
