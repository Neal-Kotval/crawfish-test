# Provider rate-limit resilience (429-aware backoff)

> Auto-drafted by crawfish for Linear issue **CRA-142**.

**Goal:** Source/Sink calls to external APIs must survive provider rate limits, distinct from the generic per-item retry ([CRA-122](https://linear.app/crawfish/issue/CRA-122/24-retries-backoff-dead-letter-and-replay)).

- [ ] Detect provider 429s / `Retry-After` and back off accordingly
- [ ] Per-provider concurrency + rate caps (token-bucket)
- [ ] Surface throttling in telemetry; never silently drop items

**Acceptance:** a Source/Sink hitting 429s backs off and completes without losing items; rate caps are honored.

**Relates:** [CRA-103](https://linear.app/crawfish/issue/CRA-103/02-source-framework-single-and-multi-item-fan-out)/104 (Source/Sink), [CRA-108](https://linear.app/crawfish/issue/CRA-108/08-batch-executor-and-scheduling-rule-based) (executor backpressure).
