# AGENTS.md

Guidance for Codex when working with the `paper-read-single` workflow.

## Purpose

This workflow supports deep reading of one research paper at a time. It helps
map the paper, read specific sections, analyze methods, extract experiments,
audit claims, and produce a final structured summary.

## Scope

This workflow supports:

- One paper file at a time
- Section-by-section reading
- Method/design analysis
- Experiment analysis
- Claim and evidence checking
- Final structured notes

This workflow does not support:

- Multi-paper comparison
- Batch folder processing
- Literature review over many papers
- Automatic replacement of missing paper files
- Editing, moving, or deleting original paper files

## Language

- Default user-facing responses should be in Chinese.
- Keep paper titles, technical terms, file paths, command names, frontmatter
  fields, and API names in their original language.
- Follow explicit user requests for another output language.

## Working Rules

- Do not invent paper content.
- Do not summarize from filename, title, abstract, or prior knowledge only.
- Separate evidence-backed claims from interpretation.
- Mark uncertainty when tables, figures, formulas, or sections cannot be read.
- Before creating new directories or output files, propose the layout and get
  user confirmation.
- Keep generated notes outside raw paper locations unless the user explicitly
  confirms otherwise.

## Workflow Boundaries

- Commands coordinate workflow steps.
- Agents perform specialist reading and analysis.
- Skills provide reusable templates and checklists.
- Rules protect files and define workflow scope.

## Directory Rules

- `command/`: workflow entry points.
- `agent/`: specialist paper-reading roles.
- `skill/`: reusable paper-reading methods and output templates.
- `memory-rules/`: durable rules for this workflow.

## Verification

Before reporting completion, state:

- What paper or section was read
- What evidence was found
- What could not be verified
- What remains uncertain
