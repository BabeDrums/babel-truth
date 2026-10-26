# ADR 0004 — Promote the frozen FIRE G7 shell into the Babel foundation

**Status:** Accepted

## Context

Babel FIRE spent the G7 certification cycle separating generic shell fundamentals from disposable product fixtures. The shell was exercised through the shared primitive layers, the developer Shell Test, real G7 screens, automated compact/regular-width regressions, repeated physical iPhone/iPad review, and final explicit Babel approval.

The runtime that received final approval is FIRE commit `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489` (PR #96 merged and deployed). FIRE's Setup → Structure → Tracks fixtures remain disposable and are not part of this cross-app promotion.

Before this decision, Babel Truth already contained many semantic foundations, but it intentionally stopped short of defining a recognizable shared shell baseline. That made it possible for another Babel surface to satisfy the abstract rules while still feeling visually unrelated.

A later Lab reconciliation exposed a second failure mode: a consumer can technically satisfy the semantic rules while still re-solving already-validated shell fundamentals with different canvas geometry, materials, action hierarchy, spacing, and temporary-UI composition. That produces unnecessary physical-review work and weakens the meaning of a shared Babel shell.

## Decision

Promote only the generic, validated shell principles from the frozen FIRE G7 shell into `FOUNDATIONS.md` as the default Babel shell baseline.

The promoted layer covers:

- calm page/header/title composition and stable anchors
- small shared spacing vocabulary and deliberate related-vs-major grouping
- parent-owned surfaces and pressed/selection geometry
- familiar action/accessory meanings and canonical symbol placement rules
- ordinary text-entry assistance plus value-appropriate specialized input semantics
- adaptive temporary UI that may change presentation without changing hierarchy/meaning
- approximately 44px+ touch targets with quieter visible material allowed inside them
- content-first, quiet-until-important, tactile-not-decorative composition
- one product logic across compact and regular widths

The approved FIRE runtime at `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489` is the **canonical reference implementation** for those generic shell roles. A new Babel surface should begin by matching that reference where the semantic role is the same—page frame, toolbar geometry, typography roles, common action hierarchy, grouped rows, generic surfaces, field/control treatment, temporary-UI behavior, responsive adaptation, focus/accessibility, and motion defaults—rather than loosely reinterpreting the prose from scratch.

A consuming surface may diverge when its product job genuinely requires a different presentation or when the divergence is the explicit experiment. Such divergence should be deliberate and local, not accidental shell drift.

The promotion explicitly does **not** include FIRE workflow, FIRE fixture labels, music-specific progression, FIRE Core product architecture, exact future data models, or a mandatory cross-repository runtime dependency.

Do not extract a universal Babel component library from this single-product implementation. Shared code remains unearned until at least two real products prove the same semantics and implementation genuinely need reuse. Until then, the frozen FIRE implementation is a reference source that consumers may port/reconcile against, not a package they must import.

## Consequences

- FIRE may proceed to FIRE Core breadboarding without waiting for Lab.
- Lab should act as a **reference consumer** of the promoted shell: its generic chrome should closely reconcile to the frozen FIRE implementation, while experiment-specific content and expression remain local.
- Future Babel products start from the Truth shell contract plus the frozen FIRE reference implementation, then introduce product-specific exceptions only when their job earns them.
- Lab or another consumer should not create a visibly separate generic design system merely because Truth is semantic; matching shared semantics includes matching the already-proven generic visual/interaction grammar unless a local exception is intentional.
- Locked FIRE shell categories are not casually reopened by later product work. A genuinely new FIRE Core requirement should extend the smallest necessary primitive and only reopen a locked category when evidence shows the foundation itself is wrong.
- The approved FIRE runtime commit remains historical implementation evidence; Babel Truth owns the transferable contract and reference relationship, not FIRE's product-specific workflow.
