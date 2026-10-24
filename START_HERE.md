# Babel Truth — Start Here

Use **Babel** as the project-facing name.

This repository is the first read for **cross-app Babel rules**. It does not replace app-local authority.

## Read order

1. `START_HERE.md` — this routing/authority summary
2. `AGENTS.md` — repository/process rules
3. `PRODUCT_PRINCIPLES.md` — Babel-wide product principles
4. `DESIGN.md` — Babel-wide design and interaction foundations
5. `PROCESS.md` — iteration, continuity, contradiction, and promotion workflow
6. `registry/apps.json` — current repo/app roles and Truth adoption state
7. relevant accepted decision records in `decisions/`
8. GitHub Issue #1 (`Babel Continuity Buffer`) body + newer comments for unresolved durable deltas
9. then the owning app's local handoff/spec/code

## Authority model

Babel Truth owns only what must genuinely transfer across products.

When sources conflict:

1. a settled Babel Truth rule wins for cross-app semantics/process/design foundations
2. the owning app's canonical product spec wins for app-local behavior
3. an intentional Lab experiment may diverge from Truth while the experiment is explicitly testing an alternative
4. the Continuity Buffer is low-authority and never silently overrides accepted Truth or app authority
5. old prototypes, old summaries, and Git history are evidence/history, not current authority

### Four homes for information

Classify durable information before storing it:

- **Global** → Babel Truth
- **App-local** → owning app repository
- **Experimental** → Babel Lab / experiment authority
- **Unresolved** → Babel Continuity Buffer until resolved

Do not copy app-local runtime state into Babel Truth merely so another chat can find it.

## Lab evidence boundary

> **Lab is evidence, never authority.**

Babel Lab is allowed to contain mutually contradictory styles, controls, layouts, interactions, prototypes, and product hypotheses at the same time. No product or Truth rule should derive a design merely because that design exists in Lab, and there is no single "Lab style" that downstream work should inherit.

Lab experiments may use current Babel foundations as a convenient starting point, but that does not make those foundations mandatory inside an experiment. When an experiment intentionally tests an alternative, preserve and label the divergence rather than forcing convergence.

Promotion is deliberate. For shell/visual work the default evidence path is:

**Lab experiment → physical-device testing → candidate → owning product implementation → owning product physical validation → transferable rules promoted to Babel Truth.**

Promote validated decisions/semantics, not prototype code by default. A Lab result does not become Babel-wide merely because it is polished or approved inside the Lab.

## Contradiction rule

> **Active authority should contain one current truth.**

When a current rule is replaced, rewrite/remove the superseded active wording instead of leaving two competing instructions. Preserve implementation history in Git. Preserve major architectural reasoning in a decision record when future maintainers genuinely need to know why a prior approach was superseded.

Historical truth is not active truth.

## Continuity rule

GitHub Issue #1 is the lightweight unresolved continuity buffer.

For Babel work, use **persist-before-reply** when a conversation produces a new durable decision, constraint, real-device finding, cross-app rule, or important unresolved question that is not already safely represented in authority.

For routine capture, append a **new comment** to Issue #1. Do not replace the issue body. The body is only the consolidated current snapshot and is refreshed during explicit consolidation after reading all newer comments. This lets multiple Babel chats persist findings concurrently without overwriting each other.

This does **not** mean storing every message. Persist only information whose loss at a chat boundary would cost real work or change the next decision.

At consolidation, every active buffer item/comment becomes one of:

- promoted to Babel Truth
- promoted to an app-local authority
- retained as an intentional Lab experiment
- intentionally deferred and kept in the unresolved snapshot
- rejected/superseded and removed from the active snapshot

## Repo roles

Current model:

- `BabeDrums/babel-truth` — cross-app truth/control plane; no product runtime
- `BabeDrums/babel-fire` — FIRE product; production + successor work remain here
- `BabeDrums/babel-lab` — experimental sandbox/incubator using fake/prototype state by default
- future real products such as Babel World earn their own repos when they become real products

A Babel World **prototype** may live in Lab. Babel Lab itself must not be renamed into World or treated as the World product.

Exact current adoption commits/status live in `registry/apps.json`; do not duplicate them here.

## Shared-system boundary

Do not build a giant speculative universal component library.

Centralize proven cross-app principles, semantic patterns, small foundation tokens, process, and contracts first. Extract shared implementation only after multiple real products prove that the same component semantics and code genuinely need reuse.

Apps should feel related without becoming skins of one template.

## Adoption model

Truth changes do **not** silently mutate product repos.

Each app adopts Truth changes through an explicit reviewed update. This prevents an experimental/global change from breaking production merely because `main` changed elsewhere.

Until automated version tooling is justified, apps record the immutable Truth commit they last reconciled against in a small local pointer file.

Parallel chats may work safely in different repos/surfaces. If two chats might write the same durable file/branch/PR, the later writer must re-read current state and reconcile rather than assuming its earlier snapshot still owns the surface.

## Current next steps

1. **Babel Lab:** use a dedicated FIRE Shell / Visual Lab harness to explore the unresolved visual-interaction shell across representative surfaces, states, and iPhone/iPad adaptation. It is an experiment harness, not a FIRE fork and not a design-system authority.
2. **Babel FIRE:** keep V6 production untouched and G7 unfrozen. Pause further exploratory shell styling in the product while Lab develops a candidate. FIRE Core remains blocked until the generic shell fundamentals are explicitly approved after real-product validation.
3. **Promotion:** physically test Lab candidates; implement the chosen candidate deliberately in FIRE; validate it again in real FIRE; only then promote genuinely transferable rules into Babel Truth.

New unresolved durable findings use append-only Issue #1 comments; consolidation periodically refreshes the body.
