---
description: Analyze the method, design, model, algorithm, or system details of one paper.
argument-hint: [paper-file]
arguments: paper_file
allowed-tools:
  - Read
  - Agent
  - Skill
model: haiku
---

# paper-method

Analyze the method or design section of one paper.

## Execution Contract

You MUST base method analysis on the provided paper file.

You are forbidden from:

- Reconstructing missing method details from prior knowledge.
- Treating ambiguous diagrams or formulas as certain.
- Skipping design rationale when it is stated in the paper.
- Modifying the paper file.

## Workflow

1. Validate `$paper_file`.
2. Invoke `method-analysis-agent`.
3. Apply `method-analysis-template`.
4. Run `claim-evidence-checklist` for important method claims.

## Failure Conditions

Stop if the file cannot be read.

Mark uncertainty if formulas, diagrams, model components, or algorithm steps are
not reliably extracted.

## Output Summary

Return:

- Method goal
- Core components
- Input/output flow
- Training or inference process
- Design rationale
- Reproducibility notes
- Uncertain method details
