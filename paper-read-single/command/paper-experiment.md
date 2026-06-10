---
description: Extract and analyze experimental setup, results, and evidence from one paper.
argument-hint: [paper-file]
arguments: paper_file
allowed-tools:
  - Read
  - Agent
  - Skill
model: haiku
---

# paper-experiment

Analyze experiments from one paper.

## Execution Contract

You MUST distinguish reported evidence from interpretation.

You are forbidden from:

- Inventing datasets, metrics, baselines, or results.
- Treating unreadable tables as reliable evidence.
- Claiming a result supports a paper claim without explaining why.
- Performing multi-paper comparison.

## Workflow

1. Validate `$paper_file`.
2. Invoke `experiment-analysis-agent`.
3. Apply `experiment-extraction-template`.
4. Run `claim-evidence-checklist` on result-related claims.

## Failure Conditions

Stop if the file cannot be read.

Mark uncertainty if tables, figures, metric definitions, or baseline descriptions
cannot be parsed reliably.

## Output Summary

Return:

- Datasets
- Metrics
- Baselines
- Main results
- Ablations
- Implementation details
- Claims supported or not supported by experiments
- Uncertain evidence
