# Placement Guide

Use this guide to decide where guidance belongs.

## Durable Guidance

Put in `AGENTS.md` or `CLAUDE.md` when it should apply across most tasks:

- General safety rules
- Repository purpose
- Verification expectations
- Output style
- Broad maintenance principles
- Directory creation rules, such as requiring the agent to discuss new folder
  layouts before creating files

## Path Rules

Put in rules when it applies only to matching files or directories:

- Raw files that must not be edited
- Notes directories with naming conventions
- Code areas with special testing expectations
- Documentation formatting conventions

## Skills

Use skills for reusable methods:

- Summary templates
- Evidence checklists
- Diff review checklists
- Experiment plan formats

## Commands

Use commands for repeated workflows:

- Review a paper
- Plan an experiment
- Map a module

## Agents

Use agents for specialist roles:

- Literature reviewer
- Code reader
- Experiment planner
- Diff reviewer

## Anti-Patterns

- Do not put full task workflows in durable guidance.
- Do not put long templates in global memory.
- Do not put project-specific facts in generic templates.
- Do not put specialist role definitions in skills.
