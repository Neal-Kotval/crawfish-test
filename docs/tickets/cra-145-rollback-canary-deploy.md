# Rollback / canary deploy

> Auto-drafted by crawfish for Linear issue **CRA-145**.

**Goal:** safe operational deploys for pipelines — versioning supports freeze, but not the rollback *operation* or gradual rollout.

- [ ] `craw rollback` a pipeline to a prior frozen version
- [ ] Canary / gradual rollout: route a % of runs to a new version, watch eval/cost, promote or revert
- [ ] In-flight runs stay on their pinned version ([CRA-134](https://linear.app/crawfish/issue/CRA-134/29-execution-state-ledger-durability-reconciliation))

**Acceptance:** a bad version is rolled back in one command; a canary routes a fraction and auto-reverts on regression.

**Relates:** [CRA-115](https://linear.app/crawfish/issue/CRA-115/17-container-builddeploy-triggers-craw-build-webhooks) (deploy), [CRA-134](https://linear.app/crawfish/issue/CRA-134/29-execution-state-ledger-durability-reconciliation) (version pinning), [CRA-139](https://linear.app/crawfish/issue/CRA-139/34-eval-data-lifecycle-cases-labeling-golden-sets-llm-judge) (regression baseline).
