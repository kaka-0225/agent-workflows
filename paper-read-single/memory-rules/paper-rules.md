# Paper Rules

Durable rules for the `paper-read-single` workflow.

## Scope

- This workflow handles one paper at a time.
- If the user provides multiple papers or a folder, stop and explain that this
  workflow is single-paper only.

## File Safety

- Do not modify, delete, move, or rename original paper files.
- Do not create output directories or files without confirming the intended
  layout.
- Keep generated notes separate from raw paper files unless the user confirms
  otherwise.

## Evidence Rules

- Do not invent paper content.
- Do not summarize from filename, title, abstract, or prior knowledge only.
- Mark unreadable figures, tables, formulas, or sections.
- Separate author claims, experimental evidence, and your interpretation.

## Failure Rules

Stop if:

- The paper file is missing.
- The paper file cannot be read.
- Extracted text is empty or clearly incomplete.
- The user asks for multi-paper comparison or batch processing.

Continue but mark uncertainty if:

- Specific tables, figures, formulas, or appendices cannot be parsed.
- Dataset, metric, result, or method details are ambiguous.
