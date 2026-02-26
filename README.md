# claude-code-best-practice

A practical, beginner-friendly intro to this repository for people who already code but are new to Claude Code workflow and project structure.

## What this repo is for
This repo is a collection of hard-earned notes and defaults for using Claude Code better:

- reusable workflows (`.claude/commands`, `.claude/skills`)
- agent and subagent patterns
- memory/rules/hooks
- MCP and plugins
- practical reports on features, flags, and setup

If you only remember one thing: **use this as a starter pack, not a finished product**.

## Start here (first 15 minutes)

1. Read the core docs in order
   - `AGENTS.md` (repo-specific constraints)
   - `README.md` (you are here)
   - `CLAUDE.md` (if present)
2. Open these sections in this repo when you need details:
   - [Extend Claude Code](https://code.claude.com/docs/en/features-overview)
   - [Skills](https://code.claude.com/docs/en/skills)
   - [Subagents](https://code.claude.com/docs/en/sub-agents)
3. Decide your first path:
   - Start with **Commands + Skills** for repeatable workflows
   - Add **Agents** only when a task needs role-specific context
   - Use **MCP** when you need external tools

## Core ideas (quick version)

- **Slash command**: quick entry point (`/plan`, `/compact`, `/memory`, etc.)
- **Skill**: reusable instruction packs; easiest way to scale context without bloat
- **Agent**: structured helper that can own a narrow set of tools/responsibility
- **Memory (`CLAUDE.md`)**: persistent context for behavior and preferences
- **Rules**: scoped behavioral constraints in `.claude/rules/*.md`
- **Hooks**: deterministic scripts that run on events
- **MCP**: external connectors (docs, browser, local apps, APIs)
- **Sandbox**: safer defaults for file/network isolation while running commands

## Recommended workflow for beginners

1. Keep task scope tiny
   - Break work into small, independent chunks.
2. Start with a command
   - Define objective + expected output explicitly.
3. Prefer `plan`-like thinking before large edits
   - especially for refactors.
4. Make one small commit per completed slice.
5. Re-check and iterate
   - If something fails, reduce scope and fix one failure at a time.

## Fast reference (most-used)

- Commands: `/compact`, `/context`, `/model`, `/plan`, `/doctor`, `/config`
- Features to read next:
  - [Claude CLI startup flags](reports/claude-cli-startup-flags.md)
  - [Claude commands reference](reports/live/agent-command-skills/claude-commands.md)
  - [Settings reference](reports/live/claude-settings.md)
- MCPs used daily in this repo:
  - [Context7](https://github.com/upstash/context7)
  - [Playwright](https://github.com/microsoft/playwright-mcp)
  - [Excalidraw](https://github.com/antonpk1/excalidraw-mcp-app)

## Practical onboarding path (minimum viable)

1. Run through a simple workflow (e.g., `workflow/rpi/rpi-workflow.md`).
2. Create one tiny local command under `.claude/commands/` for a repetitive task.
3. Move that workflow into a skill.
4. Optionally add one agent for repeatable role-specific work.

## Beginner-friendly tips from experience

- Use terminal-first workflows; keep IDE usage optional.
- Prefer commands and skills over many generic agents.
- Keep `CLAUDE.md` compact and focused.
- Ask for background logs/screenshots when debugging.
- Configure permissions with narrow wildcards (`Bash(npm run *)`) instead of broad skips.

This README is intentionally simplified. Use the linked reports for the full reference catalog when you need deeper details.
