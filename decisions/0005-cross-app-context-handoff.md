# ADR 0005 — Cross-app context and handoff contract

**Status:** Accepted

## Context

Babel products are intended to remain independently useful while becoming more capable together. FIRE is the first real specialist product; World remains a concept/experiment. As product shaping moved beyond shell design, a recurring requirement became clear: a decision made in one Babel product should be able to inform another product without forcing the user to repeat the same context or allowing the destination product to absorb the source product's entire internal model.

This is especially important for future flows such as a FIRE song becoming part of a larger body of work, World directing production work back into FIRE, or a future specialist product contributing visual, learning, live, or other domain state.

The design also needs to preserve a low-friction front door. A person must be able to open a specialist product such as FIRE, do that product's job, and leave satisfied without first creating a World profile, completing an ecosystem questionnaire, or adopting a professional-artist workflow.

## Decision

### Specialist products stand alone

A Babel specialist product must fulfill its own primary job independently. World or another ecosystem surface may add context and coordination, but must not be required merely to use the specialist.

A specialist should provide value before inviting broader ecosystem use. Optional expansion is revealed only when the user's work creates a genuinely relevant possibility.

### Context follows the work

Babel should understand the user progressively through explicit work, choices, relationships, and occasional timely clarification rather than demanding a large profile or personality investigation before helping.

When a product already has a relevant answer, a destination product should not ask the same question again unless the prior answer is stale, ambiguous, or intentionally being reconsidered.

### Handoffs carry meaning, not whole product internals

A cross-app handoff may carry the smallest meaningful shared context needed by the destination, such as:

- stable object identity and type
- owning/source product
- relevant relationships to other objects
- explicit user intent or goal
- meaningful state that genuinely transfers across products
- provenance for that state or decision
- prior decisions that should not be re-asked
- handoff purpose / requested destination capability
- a return or continuation target when useful

The exact schema is not frozen by this ADR. Prove fields through real cross-app flows before standardizing them.

Specialist internals remain local. For example, FIRE may retain detailed production observations, diagnoses, experiments, skill evidence, and technical decisions while exposing only the subset that another product genuinely needs to understand the song/project at a higher level.

### Share semantics before infrastructure

Do not build a speculative universal Babel object schema, shared component runtime, or backend merely because future integration is expected. First prove the semantic contract with real product flows. Shared storage, accounts, APIs, sync, and packaging may be introduced later around validated needs.

### Artist remains the author

Babel should increase the user's judgment rather than replace it. The system may teach principles, recommend a strongest next move, explain why, provide alternatives, remember explicit preferences, and adapt as evidence accumulates. It should not require opaque personality profiling or generated creative identity as the basis for guidance.

Recommendations may be opinionated when evidence supports a best current move, while preserving user agency to reject, defer, or choose an alternative. Preferences should be learned progressively from actual decisions and timely questions.

## Consequences

- FIRE Core breadboarding should identify what FIRE must know to make good production decisions and which resulting facts, if any, are meaningful outside FIRE.
- World shaping should focus on artist/project context, development guidance, relationships, re-entry, and orchestration rather than duplicating specialist workflows.
- Future specialist products must earn their own product job and remain useful without World.
- A future World/FIRE experiment should test one real context loop before any universal data model is designed.
- Product packaging remains open: Babel may later ship separate apps, one container app, or both. Product boundaries are semantic and do not require separate installation boundaries.
