# Hot-reload in craw dev

> Auto-drafted by crawfish for Linear issue **CRA-149**.

**Goal:** the React-style instant feedback loop — edit an `instructions.md`/tool and `craw dev` re-runs without a manual restart.

- [ ] File-watch the project; recompile changed units
- [ ] Re-run the current fixture on change (with replay/cheap model so it's instant + free)

**Acceptance:** saving `instructions.md` re-runs the dev fixture automatically in seconds.

**Relates:** [CRA-112](https://linear.app/crawfish/issue/CRA-112/14-agentruntime-backends-craw-dev-claude-p-api-cma) (craw dev), [CRA-119](https://linear.app/crawfish/issue/CRA-119/21-craw-test-testing-harness-fixtures-snapshots-replay-eval-as-test) (fixtures/replay).
