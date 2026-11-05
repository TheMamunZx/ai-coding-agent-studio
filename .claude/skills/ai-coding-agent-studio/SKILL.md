---
name: ai-coding-agent-studio
description: "Coordinate end-to-end ai coding agent studio workflows from one master skill, loading specialist playbooks as needed."
---

# AI Coding Agent Studio

## Mission
Build capable coding agents with explicit tool contracts, least-privilege access, bounded autonomy, durable context, observable actions, and reliable recovery.

## Use this skill when
The user asks to create, extend, analyze, or deliver a ai coding agent studio project and expects one coordinated workflow rather than manually selecting individual specialist skills.

## Invocation contract
This is the only selectable skill in this repository. The specialist modules below are internal reference playbooks, not separate skills to invoke. Start from the user's brief, load only relevant references, and coordinate the complete workflow.

## Required inputs
Infer what is clear from the user's brief and repository. Identify only essential missing information. Typical inputs include goal, target users/platform, scope, references, constraints, existing stack, output format, budget, deadline, and acceptance criteria. Ask one concise clarification only when a missing fact blocks safe or correct execution; otherwise state reasonable assumptions and proceed.

## Operating protocol
1. Inspect the current repository, project instructions, files, configuration, and existing conventions before editing.
2. Translate the request into deliverables, explicit assumptions, non-goals, acceptance criteria, and risks.
3. Build a short phased plan. Prefer a working vertical slice over broad scaffolding that does not run.
4. Read the relevant internal references from the map below. Do not load unrelated modules or duplicate work.
5. Discover the actual tools, dependencies, APIs, providers, and runtime capabilities available in the current environment. Never invent tool names, provider availability, model IDs, endpoints, test results, or completed outputs.
6. Implement the requested outcome in the existing project. Preserve working behavior and avoid unnecessary rewrites.
7. Validate with the strongest available automated and manual checks. Fix issues found, then re-run the relevant checks.
8. Report exact files changed, commands/tests executed and results, deliverables created, unresolved issues, and what remains unverified.

## Internal specialist reference map
- `ai-agent-architect` — read `references/ai-agent-architect.md` when this capability is needed.
- `coding-agent-engineer` — read `references/coding-agent-engineer.md` when this capability is needed.
- `mcp-server-engineer` — read `references/mcp-server-engineer.md` when this capability is needed.
- `function-calling-engineer` — read `references/function-calling-engineer.md` when this capability is needed.
- `multi-agent-engineer` — read `references/multi-agent-engineer.md` when this capability is needed.
- `agent-memory-engineer` — read `references/agent-memory-engineer.md` when this capability is needed.
- `codebase-intelligence` — read `references/codebase-intelligence.md` when this capability is needed.
- `human-centered-product-design` — read `references/human-centered-product-design.md` when this capability is needed.
- `design-quality-critic` — read `references/design-quality-critic.md` when this capability is needed.
- `product-experience-engineer` — read `references/product-experience-engineer.md` when this capability is needed.

## Coordinated workflow
1. Define agent tasks, allowed repositories, tools, success conditions, and prohibited actions.
2. Inspect the target runtime, model/provider, tool protocol, and execution environment.
3. Design planner/executor loops, state machine, context retrieval, and checkpoints.
4. Implement tool schemas, validation, permissions, sandboxing, and audit logs.
5. Build codebase indexing and context selection with freshness and token budgets.
6. Add memory only for necessary, user-approved durable facts and project state.
7. Test prompt injection, unsafe commands, tool failures, loops, partial completion, and cancellation.
8. Measure task success, edit quality, latency, token cost, and recovery behavior.

## Expected deliverables
- agent architecture and state model
- tool/MCP contracts and permission matrix
- codebase context and memory design
- sandboxed execution workflow
- evaluation scenarios and failure analysis

## Quality gates
- Requirements map to implemented behavior or clearly documented non-goals.
- The project builds/runs with available dependencies, or blockers are stated with evidence.
- Tests cover critical user flows or critical subsystem invariants.
- Security, privacy, accessibility, performance, and failure states are considered where relevant.
- Documentation matches the delivered implementation.
- No capability is described as complete unless the corresponding artifact exists and has been checked.

## Human-centered quality requirement
For any user-facing interface, load the human-centered design, design critique, and product-experience references. Apply them as quality gates throughout the work, not as a last-minute decoration pass. The result should be distinctive and fit the product domain, not a generic AI template.


## Security, privacy, and rights
- Protect secrets and personal data. Never place API keys, access tokens, passwords, signing keys, or private credentials in source files, prompts, examples, or logs.
- Use only dependencies, media, datasets, and assets with verified rights and compatible licenses.
- Do not claim external APIs, models, services, or tools are configured unless verified in the current environment.

## Approval gates
Ask before paid API/service usage, production deployment, public publication, destructive changes, external account actions, large cloud jobs, or changes that can incur charges. Do not ask for approval for ordinary reversible local edits within the user's requested scope.

## Stop conditions
Stop and explain the blocker when required permissions, credentials, source material, tools, dependencies, or target hardware are unavailable. Continue with independent work where possible, but do not simulate unavailable external generation or claim a final build succeeded.

## Final response format
Summarize: outcome; key implementation; files/artifacts; validation results; required user actions; known limitations. Be explicit about partial completion.
