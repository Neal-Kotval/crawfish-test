# IDE / LSP support + type stubs for typed IO

> Auto-drafted by crawfish for Linear issue **CRA-147**.

**Goal:** authors get editor autocomplete + type errors on a Definition's typed inputs/outputs (leans on the Type model, [CRA-132](https://linear.app/crawfish/issue/CRA-132/27-type-model-and-registry-structural-typed-io)).

- [ ] Generate type stubs from registered types so IDEs autocomplete `inputs`/`outputs`
- [ ] Surface wiring/type errors in-editor (LSP or generated `.pyi`)

**Acceptance:** editing a Definition, the author gets autocomplete on declared inputs and a red squiggle on a mistyped wire.

**Relates:** [CRA-132](https://linear.app/crawfish/issue/CRA-132/27-type-model-and-registry-structural-typed-io) (type model), [CRA-113](https://linear.app/crawfish/issue/CRA-113/15-craw-cli-init-install-and-module-discovery) (CLI).
