# book-read Decision Table

Use this table to decide which command, agent, or skill should be used.

| Need | Use |
|---|---|
| Understand the structure of a book | `book-map` |
| Read provided text without shortening or analysis | `passage-read` |
| Translate English text faithfully and naturally | `passage-read` |
| Understand one chapter or section | `chapter-understand` |
| Analyze a recurring theme | `theme-analysis` |
| Reflect on one quote or short passage | `quote-reflection` |
| Connect an idea to personal experience | `personal-reflection` |
| Produce staged or final reading notes | `reading-summary` |
| Check evidence and interpretation boundaries | `evidence-checklist` |

## Default Flow

```text
book-map
passage-read
chapter-understand
quote-reflection
theme-analysis
personal-reflection
reading-summary
```

Use `passage-read` whenever the user wants faithful reading or translation.
Use analysis commands only when the user asks for explanation, interpretation,
reflection, or summary.
