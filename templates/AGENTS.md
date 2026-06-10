# AGENTS.md

Guidance for Codex when working with this workflow template package.

## Purpose

This `templates/` directory is a reusable agent workflow package. It contains
generic templates for commands, agents, skills, memory, and rules.

When copied into another workflow or project, adapt this file to describe that
specific workflow's purpose, structure, and constraints.

## Working Rules

- Keep templates generic unless the workflow explicitly specializes them.
- Do not add project-specific facts, paper notes, experiment results, or private
  paths to generic templates.
- Before creating new directories or broad file structures, propose the layout
  and get confirmation.
- Prefer extending existing folders (`command/`, `agent/`, `skill/`,
  `memory-rules/`) before inventing new ones.
- Keep examples short and reusable.

## Language

- Default user-facing responses should be in Chinese.
- Keep code identifiers, file paths, command names, frontmatter fields, and API
  names in English.
- Follow explicit user requests for another output language.

## Placement Guide

- `decision-table.md`: decide where each kind of guidance belongs.
- `command/`: repeated workflow entry points.
- `agent/`: specialist roles.
- `skill/`: reusable methods, templates, and checklists.
- `memory-rules/`: durable guidance and path-scoped rules.

## Copying Into A Workflow

When this directory is copied into a concrete workflow:

1. Update this `AGENTS.md` with the workflow's purpose.
2. Remove template files that are not needed.
3. Rename or specialize templates only after the workflow boundaries are clear.
4. Keep workflow outputs outside this template package unless they are reusable
   examples.

## Do Not

- Do not treat this package as a place for task logs.
- Do not store concrete project implementation notes here.
- Do not mix unrelated workflows in one copied template package.
