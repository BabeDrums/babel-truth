# ADR 0006 — Bounded Lab incubation for owning-product experiments

**Status:** Accepted

## Context

Babel now has one real specialist product (`babel-fire`) with a frozen, physically validated shell and a separate experimental repository (`babel-lab`). After the FIRE G7 shell was frozen, early FIRE Core work exposed a workflow problem: putting an unproven interaction directly into the owning product repo can make disposable product-shaping work feel prematurely canonical, while rebuilding the complete owning product inside Lab would blur ownership and create competing runtimes.

At the same time, Babel Lab now consumes the frozen Babel shell for generic UI roles and has a living Shell Gallery for shared-UI candidates. That makes Lab a useful low-cost environment for some bounded product auditions without changing which repository owns the product.

## Decision

### Real product ownership does not move to Lab

A real product repository remains the sole owner of that product's:
- doctrine and canonical product behavior
- production/runtime data and schemas
- promoted implementation
- product-specific specs, tests, migrations, and release state

Lab evidence never becomes product authority merely because it is runnable or visually convincing.

### Unproven interaction behavior may incubate in Lab

A real product may deliberately place a **bounded, unproven interaction or product-behavior slice** in Babel Lab when:
- the uncertainty is genuinely product-shaping rather than ordinary implementation work;
- fake/local state can answer the question honestly;
- cheap disposability and rapid physical use are materially valuable; and
- the specimen can remain isolated from real product data/runtime.

The default path is:

**owning-product doctrine/question → bounded Lab specimen inside proven shell → physical/real-use validation → deliberate owning-product implementation/promotion**

Lab is optional. Once behavior is proven, or when the question requires real product navigation, state relationships, migrations, or production data, work returns to the owning product.

Prototype code is not automatically promoted code. Surviving behavior should be reimplemented/reconciled against the owning product's real runtime and authority rather than copied blindly.

### FIRE-specific application

`babel-fire` remains the owner of FIRE doctrine, canonical behavior, runtime/data, and promoted implementation.

Unproven FIRE Core interaction slices may incubate under a clearly labeled Lab lane such as `babel-lab/fire/core/**` with fake/local state. FIRE's historical G7 Shell Test remains in `babel-fire` as certification evidence for the approved FIRE runtime; it is not moved into Lab and is not a product-prototyping destination.

The existing Fire visualization/progression experiment is a different hypothesis and must not be silently redefined as FIRE Core.

### Shell Gallery has a different job

The Babel Shell Gallery in Lab is the living visual/device-testable proving environment for **generic shared UI roles and semantic variants**. It may contain explicit statuses such as Proven, Candidate, and Experimental.

The Gallery is not FIRE's Shell Test, not a product runtime, and not Babel Truth. Babel Truth owns the transferable shell contract and promotion decision. A universal shared component package remains unearned until multiple real products prove the same implementation genuinely needs reuse.

### Parallel-lane concurrency

FIRE, WORLD, and other Lab experiments may proceed in parallel when they own disjoint product-specific paths. Shared Lab surfaces require explicit reconciliation before writes.

Examples of shared surfaces include:
- `shared/**`
- `shell/**`
- the Lab root launcher/navigation
- the Lab Truth-adoption pointer
- cross-cutting CI/tests that span multiple experiments

Before changing a shared surface, re-read current `main` and relevant open PRs. If another lane already owns the same branch/file/surface, reconcile rather than overwrite or independently reinterpret it. Product-specific findings should be classified back to the owning product; genuinely cross-app findings go to Truth; unresolved durable conflicts go to the Continuity Buffer.

## Consequences

- Product experimentation can stay cheap after the generic shell is solved without creating a second canonical product runtime.
- FIRE Core may use Lab as an audition floor while FIRE remains the sole product owner.
- WORLD can continue its separate Lab audition without giving the FIRE lane permission to edit WORLD product logic, and vice versa.
- Shared UI candidates can evolve in Shell Gallery while proven shell behavior remains regression-protected and Truth remains authoritative.
- The owning-product preview remains the required proving environment once real runtime/data/navigation relationships are necessary.
- Lab must keep experiment boundaries explicit and must never read/write FIRE production storage merely to make a prototype feel more realistic.
