# Project lifecycle

At each stage: explain purpose, inspect evidence, propose scope, produce or revise the agreed artifact, offer help, then wait for approval.
Scale document length to project size, not the seriousness of the learner.
Use linked Markdown files under docs/ by agreement; do not generate all documents at kickoff.
Suggested filenames below are not mandatory. Preserve existing project conventions.

| Stage | Discover and produce | Exit evidence |
|---|---|---|
| 0. Setup and repository | Experience, mode, agent, tools; explain Git versus GitHub. Confirm owner, name, visibility and existing remote before authorized creation. | Repository identity/visibility verified, or external setup explicitly deferred. |
| 1. Discovery | Idea, why it exists, problem, users, client versus personal project, budget, tentative deadline, success measure, MVP and exclusions. Suggest docs/project-brief.md. | Learner approves a feasible scope; assumptions and unknowns remain visible. |
| 2. SRS | Explain Software Requirements Specification. Capture functional/nonfunctional requirements, roles, business rules, constraints, numbered acceptance criteria and examples. Suggest docs/requirements.md. | Requirements are testable and approved; no invented client rules. |
| 3. Technical design and DFD | Compare stacks against experience and needs; explain components, data model and data flows. Suggest docs/architecture.md and docs/data-flows.md. | Stack, boundaries and diagram depth explicitly agreed. |
| 4. UI/UX | Identify user journeys, information hierarchy, wireframes and feedback states; consider desktop/mobile, accessibility and validation. Suggest docs/ui-ux.md. | Flows approved, or no-UI applicability explained and agreed. |
| 5. Development plan | Order small deliverables by dependency; include purpose, learning goal, requirement IDs, files, tests, estimate uncertainty and completion evidence. Suggest docs/development-plan.md. | Learner approves the plan before application code. |
| 6. Build and verify | Follow the chosen mode, one unit at a time. Explain Git branches, review and commits. Use test-first where meaningful, plus security and functional checks. | Demonstrated outcomes match acceptance criteria; failures stay open. |
| 7. Deployment | Compare suitable hosting, costs, operational responsibility, secrets, backups, health checks and rollback. Suggest docs/deployment.md. | Explicit deploy authorization, observed smoke checks and user acceptance; otherwise report blocked/not deployed. |
| 8. Closure and operation | Reconcile docs with implementation, setup, environment variable names (never secret values), tests, decisions, runbook, known gaps and maintenance. Offer optional complete audit. | Working state evidenced; unresolved gaps listed and owner reviews the result. |

## DFD depth

Distinguish a data-flow diagram from a control-flow chart, wireframe or entity-relationship diagram.
Start with a context diagram: system, external entities and named data flows.
Define numbering explicitly: some conventions label the context diagram Level 0.
Decompose major processes into Level 1 and further levels as necessary.
Keep flows balanced between parent and child diagrams; label processes, data stores and flows.
If the learner requests all levels, clarify the finite decomposition scope; do not silently reduce it.
Propose stopping when processes are understandable and further detail adds no value; obtain approval.
UI/UX and technical design may iterate together; do not force a waterfall when requirements change.

## Changes and completion

If a requirement changes, show its impact on design, plan and tests before continuing.
Do not invalidate unrelated approved work or insist on restarting at stage 0.
For an existing project, map these stages to current evidence and fill gaps proportionately.
If tools are absent, supply manual steps and ask for evidence; never report them as executed.
At closure, offer tests, security, accessibility, performance, dependency and dead-code review as appropriate.
A proposed audit is not permission to delete files, rewrite history, buy services or change production.
