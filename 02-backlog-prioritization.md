# Backlog prioritization
Rank reflects today's FDE execution, not absolute business importance.

| Rank | Original task | Business impact / feasibility | Decision | Autonomy |
|---|---|---|---|---|
| 1 | #1 Daily policy dashboard | High; recurring one-hour manual effort; three available sources | Select one-day prototype | Agent-led within approved scope; human privacy/release decisions |
| 2 | #2 Expiry email reminder | Potential renewal value; rules and recipient mapping not established | Defer; background job feasible with synthetic data | Human-in-loop for timing, recipients, consent and content |
| 3 | #5 Spreadsheet to PostgreSQL | Strategic; non-urgent, unassigned; may unblock search | Defer; distinguish one-time import from full transformation | Human decision on schema, cutover and reconciliation; agent implements approved script |
| 4 | #4 Slow policy search | Highest business impact; already assigned | Do not duplicate ownership | Agent-led technical investigation/fix after ownership and query semantics confirmed |
| 5 | #3 AI customer chatbot | Undefined scope; wrong answers directly affect customers | Defer | Human decision on permitted answers, identity, privacy and escalation |

Earlier brief suggested missing index; interview suggested spreadsheet full-load and migration dependency. Neither root cause is independently verified here. No work on search or migration is claimed. Earlier discussion specified reminders to agents rather than customers and LINE chatbot channel with OA/group undecided. These are deferred, not implemented. Relative ranks 2–5 are proposed execution decisions, not a client-confirmed full ranking.
