# Data analysis — verified mock snapshots
Recomputed from the three supplied CSVs on 27 November 2026. Files 4 and 5 were not read for this analysis.

| Source | Rows | Fields |
|---|---:|---|
| item1-daily-new-policies-2026-11-26.csv | 40 | issue_date, policy_number, product, premium, sales_channel, agent_code, status |
| item2-policies-near-expiry.csv | 40 | policy_number, holder_name, holder_email, product, start_date, end_date, status, email_consent |
| item3-customer-questions-week.csv | 60 | received_at, channel, question, category, handled_by |

## New policies — 26 November
40 distinct policy IDs; 31 active (77.5%), 9 pending payment. Recorded premium sum 1,069,251 (THB assumed by dashboard). Product: health 12, motor 8, travel 8, home 6, life 6. Channel: agent 17, online 9, call_center 8, partner 6. 23 missing agent codes; no other missing fields.

## Expiry snapshot
40 distinct policy IDs; 28 active, 7 expired, 5 cancelled. Three missing holder emails. Active expiry count with end_date between reference date and reference date + N days inclusive: 7 days = 2; 15 = 9; 30 = 17; 60 = 28; 90 = 28. Reference date 26 November 2026. Snapshot extraction timestamp not provided.

## Customer questions
60 records; 16 Nov 2026 08:03 through 23 Nov 2026 06:38. 34 staff and 26 escalated (43.3%). Categories: claim 13, coverage 11, renewal 10, policy_change 7, cancellation 5, document 5, complaint 4, pricing 4, payment 1. Channels: LINE 17, phone 16, email 14, web_chat 13. No missing fields; 11 distinct question texts. Claims/coverage/renewals account for 34/60 (56.7%). No resolution field or customer identifier. Mock findings are not evidence of real customer demand.

## Formula definitions
New count = validated unique policy rows for selected issue date. Expiry = active rows with inclusive date difference 0..N. Inquiry count = valid rows in entire loaded inquiry snapshot; escalation rate = escalated / all inquiries (undefined when empty). No cross-file joins. Replacing snapshots avoids accumulating duplicates.
