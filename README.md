# PrimAI for Gemini CLI

Swiss health insurance (Krankenkasse) in Gemini CLI: compare the 2027 basic-insurance premiums of all
insurers (premiums approved by the BAG, from its open data), check which deductible pays off, find
cancellation deadlines and addresses, premium subsidies per canton, help guides and who is behind
comparison portals and brokers. Every answer names its source and date and links the matching page on
primai.ch.

It is a remote MCP server: no key, no account and no personal data (only postcode, age or birth year,
deductible, model and accident cover). Nothing is booked, sent or bought from the chat.

## Install

```bash
gemini extensions install https://github.com/Benjaminamos11/primai-gemini-extension
```

Or without the extension:

```bash
gemini mcp add --transport http primai https://www.primai.ch/mcp
```

Then ask, for example: «Welche Krankenkasse ist 2027 in 8001 Zürich für Jahrgang 1990 mit Franchise
2500 am günstigsten?»

## Tools

compare_premiums, get_premium, compare_household, resolve_region, insurer_facts, cancellation_help,
franchise_check, subsidy_info, find_help, market_facts, consultation_options. Details:
https://www.primai.ch/ki/api

## Who runs it

PrimAI is a project of Vision Bohne (owner Nicole Bohne, Lyss), a non-tied insurance intermediary
registered with FINMA (Nicole Bohne F01536402, Vision Bohne F01536404). Loaded AG (Schlatt TG,
UID CHE-413.943.367) builds and runs the app, the website, the API and the MCP server.

- For AI and developers: https://www.primai.ch/ki
- Connect other assistants (ChatGPT, Claude, Cursor, VS Code): https://www.primai.ch/ki/verbinden
- Privacy (API and MCP server): https://www.primai.ch/ki/datenschutz
- Terms of use: https://www.primai.ch/ki/nutzungsbedingungen

Premiums are the BAG's approved list premiums, not an offer; the insurer's policy is binding.
