# Structured error model / typed failure taxonomy

> Auto-drafted by crawfish for Linear issue **CRA-143**.

**Goal:** coherent failure handling — define how errors propagate and surface, instead of raw exceptions.

- [ ] Typed failure taxonomy: `config` / `transient` / `permanent` / `policy-blocked` / `cost-halted`
- [ ] Each node maps its failures into the taxonomy; the executor routes by class (retry transient, dead-letter permanent)
- [ ] Errors surface in run results + inspector with class + cause

**Acceptance:** a transient error retries, a permanent one dead-letters, a policy-blocked one halts with a clear reason — all from one taxonomy.

**Relates:** [CRA-122](https://linear.app/crawfish/issue/CRA-122/24-retries-backoff-dead-letter-and-replay) (retries), [CRA-120](https://linear.app/crawfish/issue/CRA-120/22-run-inspector-devtools-streaming-craw-logs-inspect) (inspector).
