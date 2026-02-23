# Redaction and Security Guidelines

Keeping your data secure and private is critical.  This project is designed to be used without revealing any sensitive information.  Follow these guidelines whenever you share, publish or contribute to the Wins Tracker:

## Remove Sensitive Data

Never include or commit the following:

- **Airtable identifiers**: Base IDs (`app...`), table IDs (`tbl...`), field IDs (`fld...`), record IDs (`rec...`).
- **API tokens or keys**: Personal Access Tokens, API keys, session tokens or secrets.  These should never be stored in code or docs.
- **Personal or partner information**: Real names, emails, phone numbers, addresses, proprietary URLs or internal references.
- **Attachments or external file links**: Unless intentionally shared, avoid including files that contain private data.

If you find any of the above in your content, replace them with placeholders like `<REDACTED>` or omit them entirely.

## Placeholder Patterns

Use these conventions when describing sensitive fields or values:

- Use `<VALUE>` for confidential numbers or strings (e.g. `<VALUE>` instead of a real record ID).
- Use `<URL>` for private links.
- Use `<NAME>` for real names when anonymity is required.
- Use `<EMAIL>` for emails.

These placeholders indicate that a value exists but has been intentionally removed.

## Connector Benefits

This framework leverages the **ChatGPT Airtable connector**, which handles authentication via ChatGPT’s secure interface.  By using the connector, you avoid exposing API tokens or base IDs.  Always prefer the connector over manual API calls unless you have a specific reason to write code—and even then, store secrets in environment variables and never commit `.env` files to version control.

If you decide to include optional scripts for advanced workflows (e.g. Python scripts for batch updates), place them in a clearly marked **optional** folder and ensure that any secret configuration stays in `.env` files.  Provide an example `.env.example` with placeholder values and add `.env` to `.gitignore`.

## Publishing a Repository

Before making your repository public:

1. Search your codebase for patterns like `pat_`, `app`, `tbl`, `fld`, `rec`, `token`, `api key` and any full URLs.  Ensure none appear, except in this guidance or as placeholder patterns.
2. Confirm that no real record titles, descriptions or notes from your Airtable base have been accidentally copied into docs or code.
3. Double‑check that `.env` files and other secret‑containing files are listed in `.gitignore` and not committed.

Adhering to these guidelines will protect both your data and the privacy of anyone who interacts with your tracker.
