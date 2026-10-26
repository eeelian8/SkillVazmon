# VazmonSkill

VazmonSkill helps beginners develop software with AI without outsourcing their understanding.
The owner initially requested a private repository named SkillVazmon, then explicitly authorized making it public and committing/pushing to main. The skill targets Claude Code, Kimi, Codex and other compatible agents.

## Product boundaries

- Ask at each new project: tutor mode or guided implementation.
- Explore the idea and agree requirements before application code.
- Guide discovery, SRS, technical design, UI/UX, DFD, planning, implementation, testing, deployment and final documentation.
- Ask meaningful multiple-choice questions and offer brief explanations at every stage.
- Recommend models and optional memory tools based on verified capabilities.
- Keep learning progress resumable without requiring a memory service.

## Architecture

An instruction-only Agent Skills package lives in skills/vazmonskill/.
SKILL.md routes to local references; no executable installer, service, dependency or agent-specific tool API is required.
Display name: VazmonSkill. Technical identifier: vazmonskill.
Installation compatibility is documented, not certified by cross-agent execution.
The skill cannot enforce permissions or guarantee that an LLM obeys instructions.

## Initial roadmap

1. Foundation: portable instructions, lifecycle, installation and evaluation scenarios.
2. Publish the owner-approved draft on main; continue target-agent trials only as agreed.
3. Refine only from observed trial feedback; add integrations only with approval.

## Git and delivery

Remote: https://github.com/eeelian8/SkillVazmon (public publication authorized).
Publication branch: main, explicitly requested by the owner for this initial commit.
Keep future development on feature branches. No unrelated publishing, release or merge is authorized.
Local planning (odd/) and trial logs (.atl/) are ignored and excluded from publication.
License/distribution terms remain an owner decision; no open-source license is granted by this draft.
