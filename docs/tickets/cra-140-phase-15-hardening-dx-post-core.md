# Phase 1.5 — Hardening & DX (post-core)

> Auto-drafted by crawfish for Linear issue **CRA-140**.

# Phase 1.5 — Hardening & DX

Production-hardening and developer-experience polish surfaced by the gap reviews. **Not model-level and not blocking the Phase 1 core** ([CRA-98](https://linear.app/crawfish/issue/CRA-98/crawfish-framework-foundation-primitives-craw-cli-and-runtimes)) — sequence after the framework + docs are solid. Captured here so nothing is lost.

## Sub-issues

* Trigger robustness (webhook signature verify, dedup/debounce, single-flight, backfill/manual run)
* Provider rate-limit resilience (429-aware backoff in Source/Sink)
* Structured error model / typed failure taxonomy
* Output schema migration across Definition versions
* Rollback / canary deploy
* Failure alerting / notifications
* IDE / LSP support + type stubs for typed IO
* `craw new source|sink|definition` generators
* Hot-reload in `craw dev`

## Why separate

These make the framework *robust and pleasant* but aren't part of the *model*. Keeping them out of [CRA-98](https://linear.app/crawfish/issue/CRA-98/crawfish-framework-foundation-primitives-craw-cli-and-runtimes) keeps the core build focused; they slot in opportunistically once the trust loop runs.
