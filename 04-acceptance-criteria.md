# Acceptance criteria
Status: implemented in prototype source unless marked gap; not equivalent to executed acceptance tests. Browser checks remain pending.

| ID | Observable acceptance criterion | Expected / status |
|---|---|---|
| AC01 | Only three approved schemas accepted | Implemented; reject other schemas |
| AC02 | 26 Nov new policy count | 40 unique policies; 31 active, 9 pending |
| AC03 | Active expiry within inclusive 0–30 days from 26 Nov | 17; exclude expired/cancelled |
| AC04 | Switch 7/15/60/90-day windows | 2/9/28/28 |
| AC05 | Count all valid inquiries | 60; 34 staff, 26 escalated |
| AC06 | Recent questions sorted descending; filters work | Implemented; browser check pending |
| AC07 | Show actual unresolved questions | Gap: no resolution field; do not infer |
| AC08 | Label reporting periods | Daily date, expiry reference/window, inquiry date range |
| AC09 | Mask names and emails | First character per name component; first/last local-part characters, domain retained; short local part hidden |
| AC10 | Keep permitted policy number visible | Expiry table; agent code accepted but not shown in overview |
| AC11 | Withhold unknown free text | Exact allowlist after pattern replacement; no general PII detection claim |
| AC12 | Reject invalid headers, duplicate policy IDs, invalid dates/enums | Implemented in source |
| AC13 | Empty valid header-only CSV | Zero counts / empty tables; browser check pending |
| AC14 | Replace file rather than append; failed upload retains old snapshot | Implemented in source |
| AC15 | No files 4–5 or external calls | Excluded from package and prototype inputs |
| AC16 | Raw PII absent from frontend responses/logs | Not applicable as API test; browser reads raw uploaded mock CSV transiently; production backend required |
| AC17 | Formal TDD/PR/CI/Alpha | Outstanding |

Proposed manual cases: upload original three files; compare counts; switch filters; toggle masked details; upload wrong schema and duplicate ID; upload header-only CSV; replace with same file; inject fictional email/phone/name in a question and expect withholding; reset. Record actual outcomes, not assumed passes.
