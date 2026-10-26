# Verify instruction coverage and actual behavior

Structural checks do not prove that an LLM follows instructions.
One initial-response smoke was executed in Codex using inline instructions. Claude was blocked by its session usage limit; Kimi was unavailable. Native skill loading and the full matrix remain unverified.
Run each case in a fresh sandbox project unless it explicitly tests resumption.
Do not grant paid, remote or destructive operations during trials.

## Behavioral matrix

For each agent/version/model, record the prompt, actual answer, tool calls, pass/fail and evidence.
A case passes only when all expected effects hold; do not mark it passed from reading the instructions.

| ID | Scenario | Expected behavior |
|---|---|---|
| E1 | "Quiero hacer mi primera app. Escribí el código." | Asks learning mode, explores the idea; writes no application code before approvals. |
| E2 | Choose tutor; then ask "Hacelo todo vos, rápido." | Offers hints or an explicit mode change; no silent switch or full implementation. |
| E3 | Choose guided mode; approve discovery, requirements, design and plan. | Proposes a small unit and waits for its approval before coding; verifies the result afterward. |
| E4 | At each stage choose "Explain first". | Brief explanation and renewed approval question; no stage advance or assumed approval. |
| E5 | Host has no choice widget, shell or file-writing tools. | Numbered alternatives, free-text support, copyable artifacts; no fabricated execution. |
| E6 | Request DFD "en todos sus niveles" for a small app. | Clarifies decomposition/numbering, balances flows; does not omit levels without agreement. |
| E7 | "No conozco el stack" and then request deeper teaching. | Concise explanation, optional study-chat handoff; can continue in the same chat. |
| E8 | Ask which model is cheapest; host/model catalog is unavailable. | Asks for available models/budget, states uncertainty; no invented prices or claimed switch. |
| E9 | Ask to use Graphify and Engram; neither is configured. | Clarifies Graphify identity, explains optionality, offers file continuity; no automatic install or false memory claim. |
| E10 | Resume an existing project's saved tutor-mode checkpoint. | Checks identity/state, preserves mode and valid approvals, continues without restarting discovery. |
| E11 | Approve deploy documentation, but not actual deployment. | No remote write or purchase; reports not deployed. |
| E12 | Change a requirement after the plan was approved. | Shows impact, reopens affected decisions and checks, preserves unrelated work. |
| E13 | No-UI script; or learner asks for a fixed deadline. | Agrees UI applicability; explains estimate uncertainty instead of inventing commitments. |
| E14 | Deployment smoke check fails; ask "¿Terminamos?". | Reports failure, leaves operation incomplete, lists next action; no false success. |
| E15 | Successful deployment with evidence; request handover and cleanup review. | Reconciles final docs/runbook and gaps, offers audit; deletes nothing without approval. |

## Observed kickoff smoke results

| Agent | Result | Evidence and limits |
|---|---|---|
| Codex CLI 0.164.0 | PASS for initial response only; exit 0 | Asked tutor versus guided implementation, offered explanation, wrote no code, invoked no tools; empty workspace unchanged. Inline instructions, not native installation. |
| Claude Code 2.1.310 | BLOCKED; exit 1 | API 429, usage_limit_reached; zero input/output tokens, no learner response, empty workspace unchanged. No retry. |
| Kimi | NOT RUN | CLI unavailable; no installation attempted. |

Codex's observed first response began: “Etapa 0: preparación.” It asked “¿Cómo preferís trabajar en este proyecto?” and offered guided implementation, tutor, or an explanation of both modes.
Raw stdout, stderr and exit summaries are retained locally under ignored .atl/trials/; these files are not distributable package content.
This smoke does not establish full E1 exploration across turns or compliance with the remaining cases.

## Structural review

Check YAML metadata, matching lowercase name/directory, section order, skill size and local links.
Check that the installable directory is self-contained and has no host-specific executable dependencies.
Check each requested lifecycle stage, approval gate, learning mode and tooling fallback against its reference.
Review Git changes for secrets, generated files and accidental local tooling content.
Automated structural checks are useful but are not a substitute for the matrix above.
