# Decision 0003 — Reviewed Truth adoption, not live coupling

**Status:** Accepted

## Context

Cross-app standards need to propagate without letting a change in Babel Truth silently alter production apps or overwrite intentional local decisions/experiments.

## Decision

Apps and Lab consume Babel Truth through **explicit reconciliation** rather than a live runtime dependency.

Each adopter records the Truth commit it last reconciled against. When adopting a newer Truth state:

1. inspect changes since the recorded ref
2. classify relevant conflicts as stale divergence, intentional experiment, potential upstream improvement, or app-local exception
3. surface potential upstream improvements instead of silently overwriting them
4. update local docs/code/tests as appropriate
5. record the new Truth ref after reconciliation

## Consequences

- Cross-app consistency can improve without silent production breakage.
- Lab remains allowed to challenge current defaults.
- A future automation may open adoption PRs, but automatic deployment/mutation remains out of scope.
- Shared implementation packages may be introduced later only after proven reuse warrants them.
