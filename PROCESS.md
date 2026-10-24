# Babel Process

This is the shared operating model for nontrivial Babel product/design work.

## Core loop

> **Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate**

### 1. Observe
Collect current reality: user/device feedback, current product behavior, repo state, relevant open work, and relevant research/reference guidance. Do not begin by assuming the proposed fix is the actual problem.

### 2. Diagnose
Classify findings before changing code: system/foundation, component/pattern, screen/local composition, behavior/navigation, copy/naming, or data/safety. Repeated defects are system/component problems rather than endless local patches.

### 3. Shape
Explore the smallest coherent solution. Identify root cause, affected surfaces, intended invariant, risks, and what deliberately remains unchanged. Prefer removing complexity over compensating UI.

### 4. Contract
Before implementation, record the problem, success conditions, explicit non-goals, ownership (global/app-local/experimental), and validation needed. Do not create a permanent spec for every pass.

### 5. Build
Implement coherent integrated slices rather than scattered cosmetic patches. When relevant: primitive/token/rule → component family → affected screens → behavior/tests → docs/authority reconciliation.

### 6. Verify
Use layered verification: syntax/static checks, behavior regressions, geometry/style assertions when useful, compact/wide responsive checks, physical-device review, and real-project validation when product logic is being tested. Automated browser tests do not equal physical-device verification.

### 7. Consolidate
Every material finding becomes resolved/promoted, intentionally deferred, rejected/superseded, or explicitly experimental. Remove dead/replaced implementation and stale active wording, update owning authority, reconcile Truth only for genuinely global lessons, and update adopter pointers only through explicit adoption.

## Experimental control-baseline rule

When Lab explores the visual/interaction shell of an **existing product**, do not begin from a knowingly simplified mini-app if missing behavior or invented harness chrome would affect the design judgment.

Instead:

1. establish a faithful observable control baseline for the relevant product surfaces using isolated fake/local Lab state
2. make the visible interactions required for the experiment functional
3. keep Lab-only navigation, explanation, state jumping, and developer controls outside the product canvas or behind an explicit Lab-only boundary
4. verify parity on representative physical devices
5. only then introduce deliberate experimental divergence
6. compare the candidate against the control baseline
7. if approved, implement the decision deliberately in the owning product and validate it there

A faithful Lab replica is still **evidence, never authority**. Fidelity is for experimental validity; it does not transfer product ownership to Lab and must not create a runtime/data dependency on the production app.

This rule does not require every unrelated Lab concept to reproduce a full product. Fidelity should cover the observable surfaces and behavior whose absence would contaminate the experiment.

## Persist-before-reply

When a new durable unresolved fact emerges and its loss would materially change future work, persist it to Babel Truth Issue #1 before relying on another chat turn. Comments are the append-only intake log; the issue body is the consolidated snapshot and is rewritten only during an explicit consolidation pass. Buffer evidence is low authority until classified.

Persist immediately when Babel explicitly says not to lose a durable item, a real-device review changes the next contract, a new architecture/process/product boundary is reached, a Lab discovery conflicts with accepted Truth, or a chat boundary risks losing unresolved work. Do not persist transient chatter, already-canonical facts, immediately rejected ideas, or every brainstorm option.

## Parallel work and write ownership

Before durable writes, re-read current target state and relevant open PRs. If another lane owns the same branch/file/PR, reconcile rather than writing from stale state. Truth adoption remains pinned and explicit.

## Contradiction handling

When rule B replaces A: update current authority to B, remove/rewrite A where it still presents as current, update guards/tests protecting A, leave historical commits alone, and preserve architectural reasoning only when worth a decision record.

## Lab / Truth / App flow

Babel Lab is an experiment chamber. Lab may contain stale divergence, intentional experiments, potential upstream improvements, and app-local differences; classify them rather than silently normalizing everything.

When promoting a Lab concept into a real app, transfer validated semantics/decisions deliberately. Prototype code does not become canonical merely because it worked in Lab.

## Truth adoption by apps

Truth should not live-couple production repos. Adoption is explicit: inspect changes since the app's recorded reconciliation ref, classify relevant changes, surface conflicts, update app docs/code/tests as appropriate, and record the new Truth ref.

## Review efficiency

For physical/product review, review changed system surfaces first, sanity-check unchanged surfaces second, separate system feedback from detail feedback, and avoid re-litigating settled rules without new evidence. The goal is for each pass to eliminate a class of inconsistency.
