# VazmonSkill

A learning-first tech lead for AI-assisted software projects: understand the idea, agree the plan, then build and verify in small steps.

**Status:** draft 0.1.0. Documentation-based compatibility, not cross-agent runtime certification.
Public repository: [eeelian8/SkillVazmon](https://github.com/eeelian8/SkillVazmon). No release archive or custom installer is published.

## Quick start

With a compatible Node.js installation, run the third-party Skills CLI:

```bash
npx skills add eeelian8/SkillVazmon --skill vazmonskill -g
```

Review the package execution prompt and choose the target agents interactively. This downloads and runs third-party CLI code; it is not required by the skill itself.
For manual installation, copy the entire [vazmonskill directory](skills/vazmonskill/SKILL.md), including references/.
See [Installation](docs/installation.md) for prerequisites, locations and caveats.

1. Start a new agent session and invoke the installed skill.
2. Describe your idea. Choose tutor mode or guided implementation.
3. Expect questions and stage approvals before application code.

Example request: "Use VazmonSkill to help me learn while building my first project."

## What it does

| Capability | Behavior |
|---|---|
| Learning mode | Ask once per new project; preserve it when resuming; change only explicitly. |
| Tutor | Hints, pseudocode and feedback; the learner writes the code. |
| Guided implementation | Agree the next small unit before the agent implements it. |
| Lifecycle | Discovery, SRS, architecture/DFD, UI/UX, planning, build/tests, deployment and handover. |
| Help | Brief explanations, meaningful choices and optional deep-dive chat handoffs. |
| Context | File-based progress; optional verified memory integrations. |

The skill recommends appropriate DFD depth but does not silently discard requested levels.
No-UI projects can skip UI/UX only after discussing applicability.
It suggests model selection from actual available models, not a hardcoded price list.

## Boundaries

A skill guides an LLM; it cannot enforce permissions or guarantee understanding.
It does not install Graphify/Engram, change models, buy hosting or deploy by itself.
Repository, publishing and destructive operations need scoped approval.
No open-source license has been selected; UNLICENSED is a placeholder, not a license grant.
Public visibility does not grant an open-source license; redistribution/modification terms still need to be selected by the owner.

## Review and verification

- Read [the skill](skills/vazmonskill/SKILL.md), then its linked references.
- Follow [evaluation scenarios](docs/evaluation.md) in each target agent.
- Read [project context](PROJECT_CONTEXT.md) for architecture and roadmap.
- Follow [source notes](docs/installation.md#sources) for verified installation conventions.

One inline-instruction kickoff smoke passed in Codex. Claude was blocked by session quota, and Kimi was unavailable. Native loading and the full behavioral matrix remain unverified.
