# Output schema migration across Definition versions

> Auto-drafted by crawfish for Linear issue **CRA-144**.

**Goal:** stored Outputs carry the schema of the Definition version that produced them; readers (Company Brain, replay, benchmarks) must handle old schemas.

- [ ] Stamp each Output with its producing schema version
- [ ] Schema-version-aware reads; optional migration/upcasting to the current schema
- [ ] Replay/benchmark tolerate historical schemas

**Acceptance:** an Output produced by v0.1 is still readable after the Definition moves to v0.2; replay works across versions.

**Relates:** [CRA-101](https://linear.app/crawfish/issue/CRA-101/05-output-the-typed-envelope-between-nodes) (Output), [CRA-100](https://linear.app/crawfish/issue/CRA-100/12-versioning-version-freeze-lockfile-integration) (Versioning), [CRA-111](https://linear.app/crawfish/issue/CRA-111/11-company-brain-registry-of-sources-definitions-and-outputs) (Company Brain).
