# Frozen Babel Shell — Handoff Checklist

Use this only when a product has already completed its owning-product shell freeze and is handing work into product-core development or another adopter.

- Name the exact approved runtime commit.
- State which product remains production and whether promotion is separate.
- State that the shell is frozen, not immutable: new product requirements may extend the smallest necessary primitive without casually reopening unrelated locked foundations.
- Point to the owning product's current doctrine/spec/handoff rather than copying workflow details into Truth.
- Identify which shell principles were promoted to `FOUNDATIONS.md` and which product-specific details deliberately stayed local.
- Identify downstream adopters that still require explicit reconciliation.
- Keep unresolved durable questions in Continuity Buffer Issue #1; remove stale blocker language from active authority.
