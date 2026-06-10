# Command Checklist

Before creating or updating a command, check:

- [ ] The workflow is repeated often enough to justify a command.
- [ ] The command has a clear input contract.
- [ ] The command does not try to be a universal entry point.
- [ ] Specialist reasoning is delegated to an agent.
- [ ] Fixed methods or checks are delegated to skills.
- [ ] Tool permissions are minimal.
- [ ] Execution contract says what must happen.
- [ ] Forbidden behaviors are explicit.
- [ ] Failure conditions distinguish stop vs uncertain.
- [ ] Output summary reports work done, artifacts, and uncertainty.

Avoid:

- Combining unrelated workflows into one command too early.
- Letting the command do specialist work directly.
- Allowing broad tools without a reason.
- Continuing silently after missing or unreadable input.
