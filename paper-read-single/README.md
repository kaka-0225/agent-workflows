# paper-read-single

Single-paper deep reading workflow for Codex and Claude Code.

This workflow is designed for reading one research paper in a structured,
evidence-aware way. It avoids batch processing and multi-paper comparison so
that each reading session stays focused and verifiable.

## Recommended Reading Flow

1. `paper-map`: build a map of the paper.
2. `paper-read-section`: read a specific section such as introduction,
   motivation, related work, method, or discussion.
3. `paper-method`: analyze method, design, model, algorithm, or system details.
4. `paper-experiment`: extract datasets, metrics, baselines, results, and
   ablations.
5. `paper-summary`: produce the final structured reading note with claim
   evidence checks.

## Commands

| Command | Purpose |
|---|---|
| `paper-map` | Build a paper map and recommended reading path. |
| `paper-read-section` | Read and explain one named section or module. |
| `paper-method` | Analyze method/design details. |
| `paper-experiment` | Extract and evaluate experimental evidence. |
| `paper-summary` | Produce final structured notes and uncertainty report. |

## Agents

| Agent | Purpose |
|---|---|
| `paper-structure-agent` | Identifies paper structure and reading modules. |
| `literature-review-agent` | General deep-reading specialist for one paper. |
| `section-reader-agent` | Reads one section in depth. |
| `method-analysis-agent` | Analyzes method/design/algorithm details. |
| `experiment-analysis-agent` | Extracts experiment setup and evidence. |
| `claim-audit-agent` | Checks whether important claims are supported. |

## Skills

| Skill | Purpose |
|---|---|
| `paper-map-template` | Standard paper map output. |
| `section-reading-template` | Standard section reading output. |
| `method-analysis-template` | Standard method/design analysis output. |
| `experiment-extraction-template` | Standard experiment extraction output. |
| `claim-evidence-checklist` | Claim support and uncertainty check. |
| `paper-summary-template` | Final structured paper summary. |

## Non-Goals

- Do not compare multiple papers.
- Do not process folders of papers.
- Do not create literature review tables.
- Do not infer missing results from prior knowledge.
