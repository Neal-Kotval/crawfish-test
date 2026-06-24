# Trigger robustness (webhook auth, dedup, single-flight, backfill)

> Auto-drafted by crawfish for Linear issue **CRA-141**.

**Goal:** make triggers production-safe (the [CRA-115](https://linear.app/crawfish/issue/CRA-115/17-container-builddeploy-triggers-craw-build-webhooks) webhook trigger is currently naive).

- [ ] **Webhook signature verification** (reject unsigned/forged calls)
- [ ] Dedup / debounce of duplicate trigger events
- [ ] **Single-flight**: don't start a new run if the prior one for the same pipeline is still running (configurable)
- [ ] **Backfill / manual run** over a historical window or an ad-hoc input

**Acceptance:** a forged webhook is rejected; duplicate events fire once; overlapping triggers respect single-flight; a backfill replays a date range.

**Relates:** [CRA-115](https://linear.app/crawfish/issue/CRA-115/17-container-builddeploy-triggers-craw-build-webhooks) (triggers), [CRA-134](https://linear.app/crawfish/issue/CRA-134/29-execution-state-ledger-durability-reconciliation) (execution ledger).
