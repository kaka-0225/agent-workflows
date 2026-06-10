# Decision Table

Use this table to decide where a piece of guidance belongs.

| Need | Use | Why |
|---|---|---|
| One-off instruction | Prompt | It does not need to persist. |
| Long-term general rule | `AGENTS.md` / `CLAUDE.md` | It should apply across most tasks. |
| Path-specific rule | Rules | It should load only for matching files or directories. |
| Repeated workflow | Command | It has a stable entry point and ordered steps. |
| Specialist role | Agent | It needs a dedicated persona, scope, tools, and output contract. |
| Reusable method/template/checklist | Skill | It is a task-specific method that can be reused. |
| External tool or data source | MCP | The agent needs live tools, APIs, databases, or private context. |
| Runtime boundary | Settings | It controls tools, permissions, model, environment, or defaults. |
| Event-triggered automation | Hooks | It should run automatically at lifecycle events. |

## Quick Heuristics

- If it is always true, put it in durable guidance.
- If it is only true in one path, put it in rules.
- If it is a sequence of steps, make a command.
- If it is a job description, make an agent.
- If it is a method or checklist, make a skill.
- If it must be enforced mechanically, consider settings or hooks.
