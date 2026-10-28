# Babel Truth — Start Here

Use **Babel** as the project-facing name.

Babel Truth is the cross-app control plane. It owns only rules that genuinely need to transfer between products; product behavior stays with the owning repo and experiments stay in Lab.

## Read order

1. `START_HERE.md` — routing and current cross-app state
2. `AGENTS.md` — shared operating rules
3. `FOUNDATIONS.md` — shared product/design/interaction defaults when relevant
4. `registry/apps.json` and relevant accepted `decisions/` only when the task needs them
5. Babel Continuity Buffer Issue #1 for current unresolved durable state
6. then the owning app/Lab handoff and code

Read `CHAT_CLOSEOUT.md` only when closing/migrating a conversation.

## Authority

When sources conflict:
1. settled Babel Truth wins for cross-app semantics/process/foundations
2. the owning product wins for product-local doctrine/behavior/runtime/data
3. a labeled Lab experiment may intentionally diverge while testing an alternative
4. Issue #1 is unresolved evidence, not authority
5. PRs, old prototypes, and Git history are evidence/history, not current authority

> **One current truth. Clear ownership. History stays in Git.**

Durable information has one primary owner:
- **Global** → Babel Truth
- **Product-local** → owning product repo
- **Experimental** → Babel Lab
- **Unresolved** → Continuity Buffer Issue #1

## Repository roles

- `BabeDrums/babel-truth` — cross-app authority/control plane; no product runtime
- `BabeDrums/babel-fire` — FIRE product and production owner
- `BabeDrums/babel-lab` — disposable/prototype sandbox and incubator
- **WORLD** — concept/product audition inside Lab; no standalone repo yet
- **ARC** — distinct time/capacity-coordination product candidate; no standalone repo, runtime, or required UI yet

Lab is evidence, never authority. ADR 0006 allows an existing product to audition bounded unproven interaction behavior in Lab without moving ownership. The owning product keeps doctrine, canonical behavior, runtime/data, and promoted implementation.

## Shared architecture boundaries

- **ADR 0004 — Babel shell:** the frozen FIRE G7 shell is the current canonical implementation reference for proven generic shell behavior. Truth owns the transferable contract; Lab Shell Gallery is the living proving/showroom environment for new generic candidates. Presence in the Gallery does not make a pattern canonical.
- **ADR 0005 — cross-app context:** specialist products remain independently useful; context may follow the work without copying specialist internals or re-asking settled decisions. Shared schema/backend infrastructure must be earned by real flows.
- **ADR 0006 — bounded Lab incubation:** use Lab when product behavior is still genuinely uncertain and cheap disposability is useful; return surviving behavior deliberately to the owning product.

Do not build a universal component package, Babel-wide data model, backend, account system, or product merely to complete an architecture. Earn shared implementation through repeated real-product need.

## Current ecosystem state

- FIRE **V6 remains production**.
- FIRE **G7 shell is 10/10 Locked and Frozen**. Approved shell runtime anchor: `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489`.
- FIRE Core doctrine is owned by `babel-fire`. The current Lab specimen is the merged/deployed **top-of-product heartbeat** under `babel-lab/fire/core/**`; it supersedes the earlier V1/V2 interaction auditions and remains gated on physical iPhone review before any promotion into FIRE production.
- Lab currently contains **Shell Gallery**, **Fire Lab**, and **World Lab**. Shared Lab surfaces are integration surfaces; product-local experiment paths may advance independently when disjoint.
- WORLD remains an experiment/concept until physical use proves an independent product job strong enough to earn a repo.
- ARC has earned a distinct candidate job — **Adapt → Reconcile → Coordinate** a person's commitments, responsibilities, capacity, and changing reality into an executable schedule — but has not earned a standalone repo, runtime, backend, or visual app. Its next proof is the smallest real-life conversation → reconcile → calendar loop. Future Babel products may hand ARC only the smallest useful scheduling intent under ADR 0005; ARC does not absorb WORLD or other specialist internals.

The owning repo's `START_HERE.md` controls its exact current gate.

## Adoption, continuity, and parallel work

Truth changes do **not** silently mutate adopters. Apps/Lab explicitly reconcile to an immutable Truth commit and `registry/apps.json` records that adoption.

Issue #1 is the unresolved durable buffer:
- routine capture = new append-only comments
- body = consolidated current unresolved snapshot
- body rewrite = explicit consolidation only, after reading the body and all newer comments

Parallel product lanes are allowed when write scopes are disjoint. Before any shared-surface write or merge, refresh current `main`, inspect relevant open PRs/changed files, and serialize overlap rather than racing it.

For fresh-chat migration, follow `CHAT_CLOSEOUT.md`: persist durable state first; keep the handoff prompt small and routing-focused.
