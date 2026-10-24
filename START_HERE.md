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
8. GitHub Issue #1 (`Babel Continuity Buffer`) only for unresolved durable deltas
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

## Contradiction rule

> **Active authority should contain one current truth.**

When a current rule is replaced, rewrite/remove the superseded active wording instead of leaving two competing instructions. Preserve implementation history in Git. Preserve major architectural reasoning in a decision record when future maintainers genuinely need to know why a prior approach was superseded.

Historical truth is not active truth.

## Continuity rule

GitHub Issue #1 is the lightweight unresolved continuity buffer.

For Babel work, use **persist-before-reply** when a conversation produces a new durable decision, constraint, real-device finding, cross-app rule, or important unresolved question that is not already safely represented in authority.

This does **not** mean storing every message. Persist only information whose loss at a chat boundary would cost real work or change the next decision.

At consolidation, every active buffer item becomes one of:

- promoted to Babel Truth
- promoted to an app-local authority
- retained as an intentional Lab experiment
- intentionally deferred and left in the buffer
- rejected/superseded and removed from the active buffer

## Repo roles

Current intended model:

- `BabeDrums/babel-truth` — cross-app truth/control plane; no product runtime
- `BabeDrums/babel-fire` — FIRE product; production + successor work remain here
- `BabeDrums/babel-lab` — experimental sandbox/incubator using fake/prototype state by default
- future real products such as Babel World earn their own repos when they become real products

A Babel World **prototype** may live in Lab. Babel Lab itself must not be renamed into World or treated as the World product.

## Shared-system boundary

Do not build a giant speculative universal component library.

Centralize proven cross-app principles, semantic patterns, small foundation tokens, process, and contracts first. Extract shared implementation only after multiple real products prove that the same component semantics and code genuinely need reuse.

Apps should feel related without becoming skins of one template.

## Adoption model

Truth changes do **not** silently mutate product repos.

Each app adopts Truth changes through an explicit reviewed update. This prevents an experimental/global change from breaking production merely because `main` changed elsewhere.

Until automated version tooling is justified, apps should record the Truth commit/version they last reconciled against in a small local pointer file.

## Current next step

Finish the initial Babel Truth bootstrap, wire FIRE and Lab to this authority model, reconcile the latest unresolved FIRE physical review into the new continuity flow, then resume FIRE shell work under this process.
