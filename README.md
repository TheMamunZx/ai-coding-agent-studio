<div align="center">

# AI Coding Agent Studio

**Design and build bounded, tool-using coding agents with repository understanding, memory, and safe execution.**

`1 Master Skill` · `10 Internal Modules` · `Claude Code` · `OpenCode`

</div>

---

## About

Build capable coding agents with explicit tool contracts, least-privilege access, bounded autonomy, durable context, observable actions, and reliable recovery.

This repository exposes one discoverable skill: `ai-coding-agent-studio`. Specialist playbooks live inside that skill's `references/` directory and are loaded by the master workflow as needed. You do not select each module separately.

## Quick start

### Project-local use

Copy this repository's `.claude/skills/ai-coding-agent-studio/` folder into the target project's `.claude/skills/` directory. Then invoke the master skill from your compatible coding agent.

### Claude Code

```text
/ai-coding-agent-studio
```

### OpenCode

```text
@ai-coding-agent-studio
```

Agent discovery behavior can vary by installed version and configuration. Confirm the skill appears in the agent's available skill list before relying on it.

## Internal specialist modules

| Module | Role |
|---|---|
| `ai-agent-architect` | Internal specialist reference |
| `coding-agent-engineer` | Internal specialist reference |
| `mcp-server-engineer` | Internal specialist reference |
| `function-calling-engineer` | Internal specialist reference |
| `multi-agent-engineer` | Internal specialist reference |
| `agent-memory-engineer` | Internal specialist reference |
| `codebase-intelligence` | Internal specialist reference |
| `human-centered-product-design` | Shared human-centered quality reference |
| `design-quality-critic` | Shared human-centered quality reference |
| `product-experience-engineer` | Shared human-centered quality reference |

## Repository layout

```text
ai-coding-agent-studio/
├── .claude/skills/ai-coding-agent-studio/
│   ├── SKILL.md
│   ├── references/
│   ├── scripts/
│   ├── templates/
│   └── assets/
├── scripts/
├── README.md
├── README_BN.md
└── AGENTS.md
```

## Validation

Run: `python scripts/validate_pack.py`

The validator checks the master skill, expected reference files, frontmatter, basic link integrity, and accidental secrets. It does not prove provider/API availability or guarantee production behavior.

## Safety and service requirements

This repository contains agent instructions, reference playbooks, templates, and helper scripts. It is not itself a model, API subscription, cloud runtime, media-generation engine, or deployment service. Actual capabilities depend on tools, credentials, permissions, provider terms, quotas, dependencies, and hardware configured in your environment. Never commit secrets.

## Contribution and updates

Keep the master skill as the sole discoverable entry point. Add new specialist knowledge as internal references unless there is a deliberate decision to expose a new independent skill. Update the manifest and validation checks whenever modules change.
