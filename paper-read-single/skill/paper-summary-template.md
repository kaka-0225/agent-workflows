---
name: paper-summary-template
description: Produce final structured notes for one paper with evidence and uncertainty sections.
user-invocable: true
allowed-tools:
  - "Read"
---

# Paper Summary Template

## Task

Produce final structured reading notes for one paper.

## Expected Output

```md
# Paper Summary

## Paper Identity

- Title:
- Authors:
- Venue/Year:

## Research Question

## Motivation

## Core Method

## Design Details

## Experiments

## Main Contributions

## Limitations

## Useful Ideas

## Evidence-Backed Claims

| Claim | Evidence | Confidence |
|---|---|---|

## Uncertain Points

## Suggested Next Reading Action
```

## Rules

- If a field is not found, write "not found in the provided paper".
- Do not invent missing details.
- Separate evidence-backed claims from interpretation.
