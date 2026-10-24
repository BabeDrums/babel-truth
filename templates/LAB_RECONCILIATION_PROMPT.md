# Babel Lab — Truth Reconciliation Prompt

Use this prompt when an existing Babel Lab chat needs to reconcile its current prototype with the latest approved Babel Truth state **without blindly overwriting discoveries made in Lab**.

---

Continue the existing Babel Lab project from `BabeDrums/babel-lab`. Treat the repository and this chat's existing prototype decisions as evidence; do not ask me to reconstruct them.

Before changing any prototype code:

1. Read `BABEL_TRUTH.md` in `babel-lab` and follow its pinned Truth commit.
2. Read the pinned `BabeDrums/babel-truth` files in this order: `START_HERE.md`, `AGENTS.md`, `PRODUCT_PRINCIPLES.md`, `DESIGN.md`, `PROCESS.md`, then relevant accepted decision records.
3. Read `babel-lab/START_HERE.md`, `README.md`, and inspect the full current Prototype 02 implementation, including `app-core.js`, `app.css`, `fire.js`, `index.html`, and relevant deployment/workflow state.
4. Incorporate durable decisions already made in this existing Lab conversation. Do not treat the new Truth system as proof that older Lab work is automatically wrong.
5. Check the Babel Truth Continuity Buffer (Issue #1) for relevant unresolved Lab/ecosystem items.

Then perform a **reconciliation audit before implementation**.

For every meaningful difference between current Lab behavior/design/process and Babel Truth, classify it as exactly one of:

- **Stale divergence** — Lab simply predates an accepted shared rule and should adopt Truth.
- **Intentional experiment** — Lab is deliberately testing an alternative; preserve the difference and state the hypothesis being tested.
- **Potential upstream improvement** — the Lab approach may be better than the current Truth rule. Do **not** silently overwrite Lab or Truth. Surface the conflict, explain the evidence/tradeoff, and tell me whether you recommend changing Babel Truth first.
- **Product/local exception** — the difference belongs specifically to this prototype/future product job and should not become a Babel-wide rule.

Do not begin a broad restyle until that audit is complete.

When the audit reveals a potential upstream improvement or genuine product decision, stop that specific change and surface it to me for discussion. You may continue unrelated safe reconciliation work if it does not depend on that decision.

When implementing approved/stale-divergence updates:

- follow Babel Truth by default
- preserve explicit experiments
- keep Babel Lab isolated from FIRE production runtime/data/storage
- do not turn Babel Lab itself into Babel World; a World prototype may live inside Lab, while a real World product earns its own repo later
- do not promote fake prototype controls (including simulation/dev controls) into final mechanics merely because they exist
- do not invent global Babel XP/levels or collapse source marks, achievements, and skill evidence into one meaning
- clean up replaced CSS/code/docs instead of layering contradictory systems
- use the shared Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate process
- use the central Babel Truth Continuity Buffer under the persist-before-reply rule for new durable unresolved findings

At the end, give me a concise reconciliation report with four sections:

1. **Adopted from Truth** — stale divergences you updated.
2. **Intentional Lab experiments kept** — what still differs and what each experiment is testing.
3. **Potential Truth improvements** — anything Lab appears to do better that we should consider promoting upstream before standardizing it elsewhere.
4. **Still unresolved** — decisions/questions that need me before further convergence.

Also state whether the current Prototype 02 is now safe to continue iterating under Babel Truth, or whether a Truth-level decision should happen first.

Do not touch `BabeDrums/babel-fire` runtime or make FIRE product changes as part of this task.
