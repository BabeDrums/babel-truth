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
3. an intentional Lab experiment may diverge from Truth while explicitly testing an alternative
4. the Continuity Buffer is low-authority and never silently overrides accepted Truth or app authority
5. old prototypes, old summaries, and Git history are evidence/history, not current authority

### Four homes for information

- **Global** → Babel Truth
- **App-local** → owning app repository
- **Experimental** → Babel Lab / experiment authority
- **Unresolved** → Babel Continuity Buffer until resolved

Do not copy app-local runtime state into Babel Truth merely so another chat can find it.

## Lab evidence boundary

> **Lab is evidence, never authority.**

Babel Lab may contain mutually contradictory styles, controls, layouts, interactions, prototypes, and product hypotheses. There is no single Lab style that downstream work should inherit.

Lab is best used for **bounded experiments** that can be judged honestly without reconstructing an owning product. If the complete product shell, navigation, state relationships, or behavior are necessary to judge a change, work in the owning product's isolated preview/successor instead.

The attempted full FIRE shell replica in Lab is rejected evidence. It created duplicate implementation work and reconstruction drift that obscured the design question. Git history preserves that experiment; it is not an active surface or workflow.

For FIRE shell work, the current evidence path is:

**observe G7 on physical device → diagnose systemic defects → optionally test a bounded idea in Lab → implement the promising decision in G7 → physical G7 validation → explicit shell approval/freeze → promote genuinely transferable rules to Babel Truth.**

Promote validated decisions/semantics, not prototype code by default.

## Contradiction rule

> **Active authority should contain one current truth.**

When a current rule is replaced, rewrite/remove the superseded active wording instead of leaving two competing instructions. Preserve implementation history in Git. Preserve major architectural reasoning in a decision record only when future maintainers genuinely need it.

Historical truth is not active truth.

## Continuity rule

GitHub Issue #1 is the lightweight unresolved continuity buffer. Use **persist-before-reply** when a conversation produces a durable decision, constraint, real-device finding, cross-app rule, or important unresolved question that is not already safely represented in authority.

For routine capture, append a **new comment** to Issue #1. Do not replace the issue body. The body is the consolidated current snapshot and is refreshed only during explicit consolidation after reading newer comments.

At consolidation, each active item becomes one of: promoted to Truth; promoted to app-local authority; retained as an intentional Lab experiment; intentionally deferred; or rejected/superseded.

## Repo roles

- `BabeDrums/babel-truth` — cross-app truth/control plane; no product runtime
- `BabeDrums/babel-fire` — FIRE product; production + successor work remain here
- `BabeDrums/babel-lab` — experimental sandbox/incubator using fake/prototype state by default
- future real products such as Babel World earn their own repos when they become real products

A Babel World prototype may live in Lab. Babel Lab itself must not be renamed into World or treated as the World product.

Exact current adoption commits/status live in `registry/apps.json`.

## Shared-system boundary

Do not build a giant speculative universal component library. Centralize proven cross-app principles, semantic patterns, small foundation tokens, process, and contracts first. Extract shared implementation only after multiple real products prove genuine reuse.

Apps should feel related without becoming skins of one template.

## Adoption model

Truth changes do **not** silently mutate product repos. Each app adopts Truth changes through an explicit reviewed update. Apps record the immutable Truth commit they last reconciled against.

Parallel chats may work safely in different repos/surfaces. If two chats might write the same durable file/branch/PR, the later writer must re-read current state and reconcile.

## Current next steps

1. **Babel FIRE:** keep V6 production untouched and G7 unfrozen. Continue coordinated shell refinement directly in G7 from the last real physical review. FIRE Core remains blocked until the generic shell fundamentals are explicitly approved after real-product validation.
2. **Babel Lab:** keep the current Lab workspace styling plus active Fire Lab and World Lab experiments. The retired full FIRE shell replica is removed from the active tree. Create bounded visual/interaction specimens only when useful; a Lab step is optional.
3. **Promotion:** validate shell decisions in real FIRE/G7 first; only then promote genuinely transferable rules into Babel Truth.

New unresolved durable findings use append-only Issue #1 comments; consolidation periodically refreshes the body.
