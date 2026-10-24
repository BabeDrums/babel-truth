# Babel Process

This is the shared operating model for nontrivial Babel product/design work.

## Core loop

> **Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate**

### 1. Observe
Collect current reality: user/device feedback, current product behavior, repo state, relevant open work, and useful reference guidance. Do not begin by assuming the proposed fix is the actual problem.

### 2. Diagnose
Classify findings before changing code: system/foundation, component/pattern, screen/local composition, behavior/navigation, copy/naming, or data/safety. Repeated defects should be treated as system/component defects rather than local patches.

### 3. Shape
Explore the smallest coherent solution. Prefer removing complexity over compensating UI. Identify root cause, affected surfaces, intended invariant, risks, and what should remain unchanged.

### 4. Contract
Before implementation, write a short iteration contract: problem, success conditions, non-goals, ownership, and validation needed. Do not create a permanent spec for every pass.

### 5. Build
Implement coherent integrated slices rather than scattered cosmetic patches. When relevant: shared rule/primitive → component family → affected screens → behavior/tests → docs/authority reconciliation.

### 6. Verify
Use layered verification: syntax/static checks, behavior regressions, geometry assertions when useful, compact/wide responsive checks, real-device review, and real-project validation when product logic is being tested. Automated browser tests do not equal physical-device verification.

### 7. Consolidate
Every material finding ends as resolved/promoted, intentionally deferred, rejected/superseded, or explicitly experimental. Remove dead implementation and superseded active wording; update the owning handoff/spec; reconcile Truth only for genuinely global lessons; update adopter pointers when they intentionally adopt new Truth.

## Persist-before-reply

When a durable unresolved fact emerges and losing it would materially change future work, persist it to the Babel Continuity Buffer before relying on another chat turn. Routine capture is append-only through Issue #1 comments; the issue body is rewritten only during explicit consolidation after reading newer comments.

Persist immediately for durable user requests, real-device findings that change the next contract, architecture/process/product boundaries, unresolved conflicts with Truth, or important chat-boundary state. Do not persist transient chatter, already-canonical facts, speculative options, or immediately rejected ideas.

## Parallel work and write ownership

Parallel chats are encouraged when they own different repositories or independent surfaces. Before durable writes, re-read current target state and relevant open work. Do not write from stale state into another lane's branch/file/PR.

Truth adoption remains pinned and explicit.

## Contradiction handling

Do not solve contradiction by accumulating qualifiers forever. When rule B replaces rule A: update current authority to B; remove/rewrite A anywhere it still presents as current; update guards protecting A; leave historical commits alone; preserve a decision record only when the reasoning is important enough.

## Lab, owning-product, and Truth flow

Babel Lab is an experiment chamber, not a required stage and not downstream implementation by default.

Use Lab when a question is bounded enough to test without reconstructing the owning product. If complete product context is required, work in the owning product's isolated preview/successor instead.

When reconciling Lab with Truth:
- **stale divergence** → Lab may adopt Truth
- **intentional experiment** → Lab keeps and labels the deviation
- **potential upstream improvement** → gather evidence; do not silently change Truth
- **app-local difference** → keep it local

When a Lab concept is promising, transfer the validated decision/semantics into the owning product rather than treating prototype code as authority. Validate it in the owning product. Only after that validation should genuinely transferable principles move into Truth.

For FIRE shell work specifically, G7 owns coordinated in-context shell iteration. Lab may host bounded specimens, but it must not become a duplicate FIRE shell implementation.

## Truth adoption by apps

Truth should not live-couple production repos. Adoption is explicit: inspect Truth changes since the recorded ref; classify relevant changes; surface conflicts; update app docs/code/tests; record the new Truth ref. Automation may open adoption PRs but must not silently deploy cross-app changes.

## Review efficiency

For physical/product review: review changed system surfaces first, sanity-check unchanged surfaces second, separate system feedback from detail feedback, and avoid re-litigating settled rules without new evidence.

The goal is not more passes. The goal is for each pass to eliminate a whole class of inconsistency.
