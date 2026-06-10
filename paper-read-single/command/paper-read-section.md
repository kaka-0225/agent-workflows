---
description: Read and explain one named section or module of a single paper.
argument-hint: [paper-file] [section-name]
arguments:
  - paper_file
  - section_name
allowed-tools:
  - Read
  - Agent
  - Skill
model: haiku
---

# paper-read-section

Read one section or conceptual module of a paper in depth.

## Execution Contract

You MUST focus on `$section_name` in `$paper_file`.

You are forbidden from:

- Summarizing the whole paper unless needed for local context.
- Treating missing section text as if it were read.
- Inventing motivation, design, or results not present in the paper.
- Comparing with other papers.

## Workflow

1. Validate paper file and requested section.
2. Invoke `section-reader-agent`.
3. Apply `section-reading-template`.
4. Return section-level notes and follow-up questions.

## Failure Conditions

Stop if the file cannot be read.

Mark uncertainty if the requested section cannot be found exactly; use the
closest matching section only if you clearly state the mapping.

## Output Summary

Return:

- Section read
- Section purpose
- Key points
- Evidence-backed claims
- Uncertain or unreadable parts
- Suggested next section
