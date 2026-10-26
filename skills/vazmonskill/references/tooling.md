# Harness, models and optional memory

## Identify capabilities

Use host-reported identity and tool inventory first. A model name alone does not identify the harness.
If unknown, ask which application/CLI and version the learner uses.
Distinguish available from permitted: a discovered tool is not authorization to use it.
Do not assume interactive forms, shell access, browsing, subagents, model switching or persistent memory.
Use numbered text for questions and manual instructions when tools are absent.

## Recommend models without inventing a catalog

Ask about available models, subscription/API budget and privacy constraints.
If authorized tools expose a model list, use it; otherwise ask the learner to supply it.
Recommend a small/fast available model for summaries, routine explanations and bounded documentation.
Use a stronger reasoning model for unclear requirements, architecture, difficult bugs and security-sensitive analysis.
For each recommendation, state the task, actual available model (if known), tradeoff and how to verify the choice in this harness.
If names, prices or context limits are unknown, say so; consult current official docs when possible.
Never assert that a model is cheapest or supports a tool without evidence.
Suggest a switch; do not claim to have switched models or install a provider automatically.

## Memory and graph tools

Offer optional tools only after checking project size, recurring context loss, setup cost and privacy.
- Engram is a candidate for persistent project decisions and discoveries. Verify the exact implementation, host integration and available tools before recommending setup.
- Graphify is a named candidate to evaluate, not a verified universal integration. Ask for the intended project URL/version if ambiguous; inspect its documentation before describing its graph, indexing or memory capabilities.
- Explain that a code graph and persistent conversational memory solve different problems; neither substitutes for approved project docs.
- Offer plain Markdown continuity as the zero-dependency default.
- Ask before installing packages, configuring MCP, indexing code or sending project content externally.
- Never store credentials, customer personal data or private source content in external services without explicit authorization.
- Never guarantee token savings. Compare repeated context size and retrieval cost if measurement is available.
- When memory is callable, save approved decisions scoped to the project; retrieve narrowly and verify stale facts.
- If memory is absent or fails, report it and continue safely using project files or a copyable handoff.

## Context economy

Read the current stage reference and relevant artifacts, not the entire repository every turn.
Keep SKILL.md compact and load supporting material only when needed.
Summarize stable decisions; retain exact acceptance criteria, unresolved questions and evidence.
Do not shorten away a requirement, safety warning or learner explanation just to save tokens.
