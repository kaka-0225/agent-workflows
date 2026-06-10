# AGENTS.md

Guidance for Codex when maintaining this repository.

## Repository Purpose

This repository is a reusable agent workflow template library. It stores
general methods for commands, agents, skills, memory, and rules. It should not
store project-specific outputs such as paper notes, experiment results, or
implementation logs.

## Behavioral Guidelines

These guidelines bias toward caution over speed. For trivial tasks, use
judgment, but keep changes small and traceable.

### 1. Think Before Editing

- Do not assume missing intent.
- Surface tradeoffs when there are multiple reasonable designs.
- Ask when the requested scope is unclear.
- Push back when a simpler structure would serve the repository better.

### 2. Simplicity First

- Add the minimum template content that solves the need.
- Do not add speculative scenarios or abstractions.
- Prefer concise templates over exhaustive manuals.
- If a template becomes long, split reference material from the core template.

### 3. Surgical Changes

- Touch only files related to the requested template or guideline.
- Do not reorganize unrelated directories.
- Match the repository's existing style.
- Remove only unused content introduced by your own change.

### 4. Discuss Directory Structure Before Creating Files

- Before creating new directories or broad file structures, propose the layout
  and get user confirmation.
- Do not invent new top-level folders without discussing naming and purpose.
- Prefer extending the existing `templates/` structure unless the user asks for
  a new area.
- If a task needs temporary files, ask where they should live or use an
  explicitly temporary location.
- Keep directory names stable, descriptive, and consistent with the repository's
  current organization.

### 5. Keep This Repository Generic

- Do not add concrete paper summaries, experiment outputs, or project notes.
- Convert reusable lessons into templates or checklists.
- Keep examples generic unless the user asks for a scenario-specific template.
- Do not include secrets, private paths, or private dataset details.

### 6. Goal-Driven Execution

For multi-step edits, work against explicit success criteria:

1. Identify the target template or guidance file.
2. Make the smallest useful change.
3. Verify the directory structure and changed files.
4. Report what changed and what remains intentionally unfinished.

## Placement Rules

- `README.md`: human-facing repository overview.
- Root `AGENTS.md`: Codex-facing maintenance instructions for this repository.
  Keep it at the repository root so Codex can discover it.
- Reusable `AGENTS.md` templates belong under
  `templates/memory-rules/agents-md-template.md`; do not treat the root
  `AGENTS.md` as a copy-paste project template.
- `templates/decision-table.md`: where-to-put-it decision rules.
- `templates/AGENTS.md`: Codex-facing guidance for the reusable template
  package itself. Each copied workflow package may keep and specialize its own
  `AGENTS.md`.
- `templates/command/`: repeated workflow templates.
- `templates/agent/`: specialist role templates.
- `templates/skill/`: reusable method/checklist templates.
- `templates/memory-rules/`: durable guidance and path-rule templates.

## Quality Bar

These guidelines are working if diffs stay small, templates remain reusable,
and concrete project facts do not leak into this repository.
