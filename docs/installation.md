# Install the instruction-only skill

Copy skills/vazmonskill/ as a complete directory. Do not copy only SKILL.md.
These are documented discovery locations, not an automatically tested installer.
Before copying, check that the destination does not already contain a skill with this name; do not overwrite it blindly.
The source is published at https://github.com/eeelian8/SkillVazmon on main; GitHub access does not require a collaborator invitation.

## Simplest route: Skills CLI

The third-party [Skills CLI](https://github.com/vercel-labs/skills) can discover the package under skills/vazmonskill/:

```bash
npx skills add eeelian8/SkillVazmon --skill vazmonskill -g
```

Use a Node.js version supported by the current CLI (its documentation currently requires 22.20 or later), with npm/npx available.
Review npm's package execution prompt and the CLI's installation summary. Select the intended agents interactively; do not blindly overwrite an existing installation.
-g installs at user scope across projects; omit -g to install in the current project.
The command downloads and executes third-party software; it is optional, not an in-repository installer or a dependency of the skill.
This command is documented upstream, but has not been executed against this repository during publication. Agent discovery and destination conventions may differ by CLI version; inspect the chosen target and use manual installation if needed.

## Manual route

Download the repository from GitHub using Code → Download ZIP, or clone it:

```bash
git clone https://github.com/eeelian8/SkillVazmon.git
```

Copy SkillVazmon/skills/vazmonskill/ to one of the destinations below, preserving all four reference files.
Manual copying does not require Node.js. Native loading still needs verification in the target agent.

## Agent-specific locations

| Agent | User-level destination | Explicit invocation |
|---|---|---|
| Claude Code | ~/.claude/skills/vazmonskill/ | /vazmonskill |
| Codex | ~/.agents/skills/vazmonskill/ | $vazmonskill |
| Kimi Code CLI | ~/.kimi/skills/vazmonskill/ | /skill:vazmonskill |

Here ~ means your user home, including on Windows; use your file manager or shell's home-directory syntax.
Copy the directory manually to avoid shell-specific installation assumptions.
For project-only installation, use .claude/skills/vazmonskill/ for Claude Code, .agents/skills/vazmonskill/ for Codex, or .kimi/skills/vazmonskill/ for Kimi.
Kimi discovery behavior can depend on version/configuration; use its own namespace to reduce ambiguity.
Restart the agent if the skill does not appear; check the installed version's official docs if discovery differs.

## Verify loading

1. Confirm the destination contains SKILL.md and all four reference files.
2. Start a session and explicitly invoke the skill.
3. Ask for a beginner project; verify that it asks for learning mode rather than writing code.
4. Run the behavioral matrix before calling that agent supported in practice.
If the skill is not visible, inspect discovery/settings; do not claim installation succeeded just because copying worked.

## Other agents and plain chats

For an Agent Skills-compatible host, consult its own supported discovery directory and invocation syntax.
For a host without native skills, provide SKILL.md and its references as instructions/attachments.
This is a manual fallback, not native installation or equivalent tool support.
A chat that cannot read local files needs the actual reference content; paths alone are insufficient.
Higher-priority host instructions and permissions always apply.

## Sources

Consulted during this implementation; host behavior may change:
- [Skills CLI](https://github.com/vercel-labs/skills): GitHub source, --skill filter, -g user scope and interactive agent selection.
- [Agent Skills specification](https://agentskills.io/specification): lowercase identifier matching directory, YAML metadata and local references.
- [Claude Code skills](https://code.claude.com/docs/en/skills): personal/project locations and slash invocation.
- [Codex skills](https://developers.openai.com/codex/skills): .agents/skills locations and explicit skill selection; cross-checked against Context7 /openai/codex.
- [Kimi Code CLI skills](https://moonshotai.github.io/kimi-cli/en/customization/skills.html): .kimi/skills and /skill:name invocation.
- [Engram](https://github.com/Gentleman-Programming/engram): candidate persistent memory; integration/setup is separate from this skill.
No particular Graphify implementation was established from the user's name alone; obtain its intended URL before recommending installation.
