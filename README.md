# F2 · InsurTech | Submission package
**27 November 2026 · Synthetic-data demonstration · Prototype only**

## Run the demo
Extract this ZIP and open `insurance_operations_dashboard.html` in a modern Chrome or Edge browser. No installation, network, server, API key or environment variable is required. The three approved mock datasets are embedded in sanitized form. Use the three upload slots to replace snapshots with authorized synthetic CSVs. Invalid uploads retain previous data. Reset restores the bundled snapshot. Raw CSVs are intentionally not redistributed; use the evaluator's originals for upload testing.

## Deliverable index
| File | Purpose |
|---|---|
| 01-discovery.md | Confirmed discovery and proposed success measures |
| 02-backlog-prioritization.md | All five requests and autonomy |
| intent.md | Implementation contract |
| 04-acceptance-criteria.md | Testable criteria and status |
| 05-decisions-and-assumptions.md | Decisions, gaps and constraints |
| 06-data-analysis.md | Recomputed source metrics |
| 07-pii-strategy.md | Privacy controls and limitations |
| 08-go-no-go.md | Release gates, rollback and approval |
| 09-code-walkthrough.md | Narrative handover and quiz |
| 10-verification.md | Actual checks and missing evidence |

## Demo sequence
Show the four KPIs; change expiry window; toggle masked holder details; filter inquiries by handling/category/channel; upload a replacement synthetic file; reset. Explain that handling is not resolution status.

## Maintenance
The client IT team owns future updates. Keep a known-good copy of the HTML; use the approved schemas in the data analysis document. Changes to the question allowlist require privacy review. For production, move parsing and redaction to a trusted backend, implement authorization and automated ingestion, and validate against the Team Handbook. The browser prototype is not a production security boundary.

## Submission status
Discovery, prioritization, intent, acceptance criteria, data analysis and handover are consolidated. Standalone HTML prototype exists. Formal TypeScript/React/Prisma/PostgreSQL implementation, TDD history, PR, CI, hooks, Alpha deployment/tag and IT Head approval are not evidenced. Claude Code was specified; this prototype was created with ChatGPT and requires evaluator authorization for official use. Verbal briefing reportedly differed from written F2; no waiver is assumed.
