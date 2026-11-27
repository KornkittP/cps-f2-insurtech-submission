# Privacy strategy
## Confirmed rules
Policy number and agent code permitted for intended view. Names reveal first character of each component; email reveals first and last local-part characters and domain. Customer questions can contain unexpected personal details. Exclude search logs and legacy policy data.
## Actual prototype
Bundled holder fields are masked. Uploaded names are masked per whitespace-separated component (minimum three asterisks); short email local parts fully hidden, invalid/missing email shown unavailable. `redact` replaces common email/phone/13-digit patterns, then allows only exact matches to bundled generic question texts; all other text is withheld. This is an allowlist, not NER or general PII detection. Table values are HTML-escaped. No external API calls. Raw replacement CSVs are read locally in browser memory; no server-side access control or secure deletion guarantee. Policy IDs may still be personal data in context.
## Proposed synthetic tests (not executed)
- John Smith → J*** S****; Thai names reveal first character per component.
- somchai@example.com → s*****i@example.com; short local part fully masked.
- Question containing a fictional phone, email, name or address → withheld unless exact approved safe text after replacement.
- Generic approved question → visible; unknown generic question → withheld too (false positives accepted for prototype).
## Production gates
Backend sanitization, authorization, minimal data projection, secure logging/retention, Thai/English contextual evaluation, human review of uncertain text and approved runtime processors. No real data in this demo. Do not claim anonymization or complete PII detection. Review allowlist changes with privacy owner.
