# Intent — Daily Insurance Operations Dashboard
## Why
Remove repetitive manual report preparation and provide central visibility into sales, renewal and inquiry activity.
## Do
Use only Daily New Policies, Policies Near Expiry and Customer Questions Week. Show daily new policy count, active upcoming expiry count, question count and recent inquiries with actual handling type. Label source periods. Provide reusable CSV replacement, validation, filters, aggregate charts and masked optional holder details. Preserve policy numbers and permitted agent codes; mask names and email local parts. Withhold unrecognized free text. Use synthetic data only.
## Do not
Do not access real systems, files 4–5, automate responses/escalations, send reminders, migrate databases, implement chatbot, infer resolution status, or deploy to production. No individual agent dashboards or RBAC in prototype. No external runtime AI or unapproved services. Premium is optional recorded value, not revenue.
## Engineering contract for formal F2
Use approved Claude Code and TypeScript/React/Prisma/PostgreSQL per written brief; BullMQ only if justified. Follow Team Handbook, test-first red/green evidence, naming conventions, hooks, PR, build/lint/test CI, tagged Alpha, handover and simulated production decision. The existing HTML is a preliminary implementation, not evidence of these requirements.
## Agent boundary
Agent may implement bounded parsing, validation, aggregation, presentation and tests. Humans approve privacy policy, scope changes, external services, access rules and release. See acceptance criteria and Go/No-Go.
