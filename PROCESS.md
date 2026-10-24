# Babel Process

This is the shared operating model for nontrivial Babel product/design work.

## Core loop

> **Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate**

### 1. Observe

Collect current reality:
- user/device feedback
- current product behavior
- repo state
- open PRs/branches that matter
- relevant research/reference guidance

Do not begin by assuming the proposed fix is the actual problem.

### 2. Diagnose

Classify findings before changing code:
- system/foundation
- component/pattern
- screen/local composition
- behavior/navigation
- copy/naming
- data/safety

If the same class of defect appears on multiple screens or survives multiple passes, treat it as a system/component defect rather than another local patch.

### 3. Shape

Explore the smallest coherent solution. Prefer removing complexity over compensating UI.

Identify:
- root cause
- affected surfaces
- intended invariant
- risks
- what should deliberately remain unchanged

### 4. Contract

Before implementation, write a short iteration contract in the working issue/PR/plan:
- problem being solved
- success conditions
- explicit non-goals
- ownership: global vs app-local vs experimental
- validation needed

Do not create a permanent spec for every pass.

### 5. Build

Implement in coherent integrated slices rather than scattered cosmetic patches.

Good order when relevant:
- shared primitive/token/rule
- component family
- affected screens
- behavior/tests
- docs/authority reconciliation

### 6. Verify

Use layered verification:
- syntax/static checks
- behavior regressions
- geometry/computed-style assertions for design invariants when useful
- representative compact/wide responsive checks
- real-device review for visual/mobile behavior
- real-project/use-case validation when the product logic itself is being tested

Automated browser tests do not equal physical-device verification.

### 7. Consolidate

Every material finding ends as one of:
- resolved and promoted into authority
- intentionally deferred and captured in the Continuity Buffer
- rejected/superseded and removed from active guidance
- intentional experiment kept explicitly experimental

Then:
- remove dead/replaced implementation
- remove or scope superseded active wording
- update the owning handoff/spec
- reconcile Babel Truth if the lesson is genuinely global
- update adopter pointers when they intentionally adopt the new Truth state

## Persist-before-reply

When a new durable unresolved fact emerges in conversation and its loss would materially change future work, write it to the Babel Continuity Buffer before relying on another chat turn.

This is a safety net, not a transcript mirror.

### Persist immediately when

- Babel explicitly says not to lose/remember a durable item
- a real-device review changes the next implementation contract
- a new architecture/process/product boundary is reached
- a Lab discovery conflicts with an accepted Truth rule and needs adjudication
- a conversation is at a plausible boundary and the unresolved item is not yet in authority

### Do not persist when

- the information is already canonical
- it is transient implementation chatter
- it is one of many speculative brainstorm options with no durable consequence yet
- it was immediately rejected

## Contradiction handling

Do not solve contradiction by accumulating qualifiers forever.

When rule B replaces rule A:
1. update the current authority to B
2. remove/rewrite A anywhere it still presents as current
3. update tests/guards that protect A
4. leave historical commits alone
5. create/supersede a decision record only if the architectural reasoning is important enough to preserve explicitly

## Lab → Truth → App flow

Babel Lab is an experiment chamber, not downstream implementation by default.

When reconciling Lab with Truth:

- **stale divergence** → Lab adopts Truth
- **intentional experiment** → Lab keeps the deviation and labels the hypothesis
- **potential upstream improvement** → stop and compare evidence; Truth may change first
- **app-local difference** → keep it local; do not universalize it

When promoting a Lab concept into a real app, transfer the validated semantics and decisions, not every line of prototype code.

## Truth adoption by apps

Truth should not live-couple production repos.

Adoption is explicit:
1. inspect Truth changes since the app's recorded reconciliation ref
2. classify each relevant change
3. surface conflicts instead of silently overwriting intentional local decisions
4. update app docs/code/tests as appropriate
5. record the new Truth ref in the app pointer

A future automated updater may open adoption PRs, but it must not silently deploy cross-app changes.

## Review efficiency

For physical/product review:
- review changed system surfaces first
- sanity-check unchanged surfaces second
- separate overall-system feedback from detail feedback
- avoid re-litigating settled rules unless new evidence actually challenges them

The goal is not more passes. The goal is for each pass to eliminate a whole class of inconsistency.
