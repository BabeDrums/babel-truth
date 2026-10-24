# Decision 0001 — Babel Truth / App / Lab boundary

**Status:** Accepted

## Context

Babel needs shared continuity and standards across multiple repositories without turning experimental work into production authority or forcing every product into one repo/template.

## Decision

Use three distinct ownership layers:

- **Babel Truth** owns cross-app current truth: transferable product principles, design foundations, process, shared semantic contracts, repo roles, and major architecture decisions.
- **Real app repos** own app-specific product behavior, runtime, data, specs, tests, and local handoffs.
- **Babel Lab** owns experiments/prototypes. It may deliberately diverge from Truth when the divergence is the experiment.

A future Babel World prototype may live in Lab. A real Babel World product earns its own repo; Babel Lab itself does not become World.

## Consequences

- No single app repo needs to summarize the entire Babel ecosystem.
- Lab discoveries can challenge Truth without automatically overriding it.
- Real successor implementations such as FIRE G7 remain in the owning app repo because they have real product semantics/data/regression concerns.
- Cross-app reuse is deliberate and promoted, not inferred from proximity.

## Supersession

If a future monorepo or package architecture proves materially better, create a new decision record that supersedes this one rather than leaving both as active instructions.
