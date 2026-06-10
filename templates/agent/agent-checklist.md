# Agent Checklist

Before creating or updating an agent, check:

- [ ] The role is narrow and named clearly.
- [ ] The agent has explicit scope and non-scope.
- [ ] Tool permissions are minimal.
- [ ] The model choice matches task complexity.
- [ ] `maxTurns` prevents runaway exploration.
- [ ] Required skills are preloaded, not copied inline.
- [ ] Forbidden behaviors are explicit.
- [ ] Failure conditions are defined.
- [ ] Output is structured for downstream use.

Avoid:

- Creating a broad "do everything" agent.
- Giving write or shell tools to read-only roles.
- Hiding full workflow orchestration inside an agent.
- Mixing specialist reasoning with reusable method templates.
