# Handover — the journey of a daily report
A sales manager opens the HTML. The embedded JSON seed is copied into working memory, so the first view does not need an external service. The source is a single HTML file containing CSS, markup and JavaScript.

When IT selects a replacement CSV, `parseCSV` handles BOM, quoted fields and line endings. `validate` checks exact schema membership, row width, dates, enumerated values and unique policy identifiers. It normalizes dates through `dateVal` and `timestamp`. Only after validation succeeds does the upload handler replace the relevant snapshot; errors preserve previous data. Uploads are limited to 10 MB.

Before expiry records enter working state, `maskName` and `maskEmail` transform holder fields. `redact` applies pattern replacements and an exact approved-text allowlist to inquiries. Unrecognized content is withheld. This avoids claiming a regex can identify every name or address. Raw uploaded data still exists transiently in browser memory, so this is not a production trust boundary.

`render` selects daily sales by issue date, calculates inclusive expiry days for active policies, and counts all inquiries in the loaded snapshot. `group` and `bars` build breakdowns; `table` renders escaped cells. Filters select inquiry category/channel/handling and newest records. The reset handler restores seed data and default controls. No runtime AI or database is involved.

## Maintenance and future design
Keep parsing, aggregation and privacy logic separate when porting to TypeScript. Introduce a repository interface with spreadsheet and later Prisma implementations. React should receive only sanitized DTOs from a backend. Add authentication, scheduled ingestion if needed, and tests before production. IT owns changes; privacy owner approves allowlist updates. For problems, check schema, date selection and snapshot period; reset or restore known-good file. Do not bypass validation to load legacy/search data.

## Quiz
1. Why does `handled_by = escalated` not mean an inquiry is unresolved?
2. What happens when a replacement CSV contains a duplicate policy number, and why?
3. Why does the prototype withhold unknown questions, and what must change before real customer data can be used?

### Answer key
1. Handling type is not resolution status; no resolution field exists.
2. Validation rejects the replacement; previous snapshot remains to avoid corrupt or double-counted metrics.
3. Pattern detection cannot guarantee all PII is found; use approved backend privacy controls, authorization, contextual evaluation and human review before production.
