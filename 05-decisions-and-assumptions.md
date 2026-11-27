# Decisions and assumptions
| Topic | Decision / evidence |
|---|---|
| Reference date | 2026-11-26 from daily file; selectable |
| Expiry | Inclusive today through N days; active only; default 30 days proposed |
| Date format | ISO or US month/day/year; no timezone conversion in prototype; Asia/Bangkok business timezone proposed for future backend |
| Questions | Entire supplied snapshot, not daily count; latest 10 default; filter by category/channel/handling |
| Resolution | Unknown; staff/escalated is handling type only |
| Joining | No customer/policy key in inquiry file; no inferred joins |
| Premium | File 1 has premium despite earlier interview recollection; optional sum, not cash revenue |
| Refresh | Manual CSV replacement, not automated scheduled export or Drive integration |
| Privacy | Optional masked holder details; unknown question text withheld; no raw mock CSV redistributed |
| Data validation | Strict headers, enums, dates, unique policy IDs; nullable agent/email accepted; malformed email shown unavailable |
| Architecture | Standalone browser prototype; future adapter/backend and Prisma/PostgreSQL; no BullMQ now |
| Access | Central view intended; no enforced login/RBAC; synthetic data only |
| AI tooling | ChatGPT used for prototype; Claude Code specified; authorization unresolved |
| Delivery | Written F2 requires repo and Alpha; reported verbal variation not treated as waiver |

Team Handbook, official repository and Alpha deployment access/instructions were not supplied. No production readiness or actual time savings claimed.
