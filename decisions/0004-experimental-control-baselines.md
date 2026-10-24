# 0004 — Experimental control baselines

Status: accepted

## Decision

When Babel Lab is used to explore the visual/interaction shell of an existing product, establish a faithful observable control baseline before deliberate divergence whenever a simplified harness would contaminate the design judgment.

The baseline may reproduce the relevant product shell comprehensively with isolated fake/local state and functional visible interactions. Lab-only developer/navigation/explanation chrome stays outside the product canvas or behind an explicit Lab boundary.

## Boundary

Fidelity does not make Lab authoritative. The owning product retains doctrine, runtime, data, specs, tests, and canonical implementation. Approved Lab decisions are deliberately reimplemented and validated in the owning product.

## Why

A simplified mini-app can introduce its own navigation, geometry, missing interactions, and dead affordances. Review then measures harness artifacts rather than the candidate visual system. A faithful control condition makes experimental differences attributable.
