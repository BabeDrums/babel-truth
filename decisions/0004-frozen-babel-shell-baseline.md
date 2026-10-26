# ADR 0004 — Promote the frozen FIRE G7 shell into the Babel foundation

**Status:** Accepted

## Context

Babel FIRE spent the G7 certification cycle separating generic shell fundamentals from disposable product fixtures. The shell was exercised through the shared primitive layers, the developer Shell Test, real G7 screens, automated compact/regular-width regressions, repeated physical iPhone/iPad review, and final explicit Babel approval.

The runtime that received final approval is FIRE commit `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489` (PR #96 merged and deployed). FIRE's Setup → Structure → Tracks fixtures remain disposable and are not part of this cross-app promotion.

Before this decision, Babel Truth already contained many semantic foundations, but it intentionally stopped short of defining a recognizable shared shell baseline. That made it possible for another Babel surface to satisfy the abstract rules while still feeling visually unrelated.

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

The promotion explicitly does **not** include FIRE workflow, FIRE fixture labels, music-specific progression, FIRE Core product architecture, exact future data models, or shared runtime components.

Do not extract a universal Babel component library from this single-product implementation. Shared code remains unearned until at least two real products prove the same semantics and implementation genuinely need reuse.

## Consequences

- FIRE may proceed to FIRE Core breadboarding without waiting for Lab.
- Lab should explicitly reconcile its provisional generic chrome against the promoted shell baseline in a separate bounded pass; Lab remains evidence, never authority.
- A future product starts from the Babel shell defaults but may introduce a deliberate local exception when its job requires one.
- Locked FIRE shell categories are not casually reopened by later product work. A genuinely new FIRE Core requirement should extend the smallest necessary primitive and only reopen a locked category when evidence shows the foundation itself is wrong.
- The approved FIRE runtime commit remains historical implementation evidence; Babel Truth owns the transferable rule, not FIRE's exact CSS/JS.
