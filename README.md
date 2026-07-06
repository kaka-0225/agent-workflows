# agent-workflows

Reusable agent workflow templates for Codex and Claude Code.

This repository stores general-purpose templates for turning repeated AI work
into reusable, reviewable workflows. It is a method library, not a project
workspace: keep concrete paper notes, experiment results, and project-specific
implementation logs in their own repositories or work directories.

## What Belongs Here

- Durable guidance templates
- Command templates
- Agent templates
- Skill templates
- Memory and rules placement guidance
- Checklists that improve repeatability and reviewability

## What Does Not Belong Here

- Notes for a specific paper
- Details of a specific code implementation
- Results from a specific experiment
- Temporary task logs
- Project-specific credentials, paths, or private data

## Structure

```text
agent-workflows/
  README.md
  AGENTS.md
  templates/
    AGENTS.md
    README.md
    decision-table.md
    command/
    agent/
    skill/
    memory-rules/
  paper-read-single/
  ai-infra-code-read/
  book-read/
```

## Workflow Packages

- `templates/`: generic reusable workflow package.
- `paper-read-single/`: single-paper deep reading workflow. It supports paper
  mapping, section reading, method analysis, experiment extraction, claim
  auditing, and final structured notes for one paper at a time.
- `ai-infra-code-read/`: AI infrastructure source-reading workflow. It supports
  repository mapping, execution tracing, module reading, config tracing, tensor
  flow, KV cache analysis, performance path analysis, kernel/backend mapping,
  and final structured source notes.
- `book-read/`: reflective book-reading workflow for literature, psychology,
  relationships, philosophy, and personal-growth books. It separates literal
  reading/translation from chapter understanding, theme analysis, quote
  reflection, personal reflection, and reading summaries.

## Core Principle

Use the smallest durable surface that matches the need:

- One-off request -> prompt
- Long-term general rule -> `AGENTS.md` / `CLAUDE.md`
- Path-specific rule -> rules
- Repeated workflow -> command
- Specialist role -> agent
- Reusable method/template/checklist -> skill
- External tool/data -> MCP
- Runtime boundary -> settings
- Event-triggered automation -> hooks
