# book-read

Reflective book-reading workflow for Codex and Claude Code.

This workflow is designed for literature, psychology, relationships,
philosophy, and personal-growth books. It supports careful passage reading,
translation, chapter understanding, theme analysis, quote reflection, personal
reflection, and staged reading summaries.

It separates pure reading from interpretation: `passage-read` preserves the
provided text and translates it when needed, while analysis and reflection are
handled by separate commands.

## Recommended Reading Flow

1. `book-map`: build a map of the book, chapters, themes, and reading path.
2. `passage-read`: read a provided passage literally and translate if needed.
3. `chapter-understand`: understand one chapter or section after reading.
4. `theme-analysis`: analyze a recurring theme across provided passages or
   chapters.
5. `quote-reflection`: reflect on one quote or short passage.
6. `personal-reflection`: connect a book idea to the reader's own experience in
   a respectful, non-diagnostic way.
7. `reading-summary`: produce staged or final reading notes.

## Commands

| Command | Purpose |
|---|---|
| `book-map` | Build book structure, themes, and reading route. |
| `passage-read` | Preserve provided text and translate it without summary or analysis. |
| `chapter-understand` | Explain one chapter or section after reading. |
| `theme-analysis` | Analyze a theme across provided book material. |
| `quote-reflection` | Carefully reflect on one quote or short passage. |
| `personal-reflection` | Guide personal reflection without diagnosis or judgment. |
| `reading-summary` | Produce staged or final structured reading notes. |

## Agents

| Agent | Purpose |
|---|---|
| `book-structure-agent` | Identifies book structure, chapters, themes, and reading route. |
| `literal-reading-agent` | Performs faithful passage reading and translation only. |
| `chapter-understanding-agent` | Explains chapter-level meaning and structure. |
| `theme-analysis-agent` | Analyzes a theme using provided book evidence. |
| `quote-reflection-agent` | Performs close reading and reflection on a quote or passage. |
| `reflection-guide-agent` | Guides personal reflection respectfully and safely. |
| `reading-summary-agent` | Synthesizes staged or final reading notes. |

## Skills

| Skill | Purpose |
|---|---|
| `book-map-template` | Standard book map output. |
| `passage-reading-template` | Standard literal reading and translation output. |
| `chapter-understanding-template` | Standard chapter understanding output. |
| `theme-analysis-template` | Standard theme analysis output. |
| `quote-reflection-template` | Standard quote reflection output. |
| `personal-reflection-template` | Standard personal reflection output. |
| `reading-summary-template` | Standard staged or final reading summary. |
| `evidence-checklist` | Evidence, translation, and interpretation boundary check. |

## Non-Goals

- Do not summarize or analyze during `passage-read`.
- Do not invent content that was not provided or read.
- Do not reproduce full copyrighted books from memory.
- Do not diagnose the reader or other people.
- Do not treat any book's viewpoint as absolute truth.
- Do not create reading notes or output files before confirming placement.
