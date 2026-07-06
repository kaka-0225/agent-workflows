---
description: Analyze a recurring theme across provided book material.
argument-hint: [theme] [provided-material]
arguments: theme provided_material
allowed-tools:
  - Read
  - Grep
  - Agent
  - Skill
model: sonnet
---

# theme-analysis

Analyze one theme using provided book material.

## Execution Contract

You MUST analyze only `$theme` using `$provided_material`.

You are forbidden from:

- Inventing supporting passages.
- Claiming the theme appears across the book without evidence.
- Turning the analysis into personal diagnosis.
- Replacing the author's view with generic self-help advice.

## Workflow

1. Validate `$theme` and `$provided_material`.
2. Invoke `theme-analysis-agent`.
3. Apply `theme-analysis-template`.
4. Apply `evidence-checklist`.

## Failure Conditions

Stop if the theme or material is missing.

Mark uncertainty if only partial book material is available.

## Output Summary

Return:

- Theme
- Relevant passages or sections
- Author viewpoint
- Pattern across material
- Tension or nuance
- Reader-facing reflection prompts
- Uncertain points
