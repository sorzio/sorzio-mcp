# Sorzio for Google Antigravity

Bulk B2B lead enrichment, email verification, multi-page website scraping, AI cell enrichment, and multi-step Flows across Sorzio Lists and connected Google Sheets.

## Setup & Authentication

Sorzio connects over Streamable HTTP MCP (`https://www.sorzio.com/api/mcp`) with OAuth 2.1 + PKCE Dynamic Client Registration (`https://antigravity.google/oauth-callback`).

1. Install the plugin from the Antigravity Marketplace (or run `agy plugin install https://github.com/sorzio/sorzio-mcp`).
2. Open **Customizations > Installed**, find **Sorzio**, and click **Authenticate** next to the `sorzio` MCP server.
3. Sign in to your Sorzio account and approve access, then complete authorization if prompted.

Prerequisites: a Sorzio account (`https://www.sorzio.com`). Read-only discovery tools (`list_models`, `estimate_cost`) work right away; workspace runs require an authenticated account with credits or BYOK keys on Pro.

## Included Skills

- `/sorzio-quickstart`: End-to-end bulk workflow loop (list lookup, estimate, run, check results, export)
- `/sorzio-icp-qualification`: Match and score companies (`GO`, `AMBER`, `NO_GO`) against your ICP
- `/sorzio-lead-research`: Pull structured firmographics and buyer positioning from websites and LinkedIn
- `/sorzio-email-verification`: Bulk mailbox verification (`deliverable`, `undeliverable`, `catch_all`, `risky`, `unknown`)
- `/sorzio-flow-builder`: Build, test on 3, 10, or 50 rows, and execute multi-step Flows on lists or Google Sheets
- `/sorzio-check-results`: Read run quality summaries and sample rows cleanly

## Key MCP Tools

- **Discovery & Cost:** `get_started`, `get_account`, `list_models`, `estimate_cost`
- **Lists & Sheets:** `list_lists`, `create_list`, `add_rows`, `get_rows`, `export_list`, `list_sheets`, `read_sheet`
- **Execution:** `run_ai`, `run_verify`, `run_scrape`, `get_run`, `retry_failed`
- **Flows & Decisions:** `list_flows`, `get_flow`, `save_flow`, `run_flow`, `get_flow_run`, `compile_decision_profile`, `run_decide`

## Example Prompts

- `List my Sorzio lists and available AI models`
- `Estimate verifying 500 emails on my Sorzio list before running`
- `Run a 3-row test of a verify plus AI enrichment Flow on a Sorzio list`
