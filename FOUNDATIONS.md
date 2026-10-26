# Babel Foundations

These are the shared product, design, and interaction defaults for Babel products. App-specific jobs, workflows, layouts, and expressive identity remain local.

Core rule:

> **Same meaning = same grammar. Different meaning may use different presentation.**

## Product boundaries

### Product need earns the product
Do not invent apps to complete an elemental set, fill Babel World, create visual symmetry, or justify an ecosystem diagram. A focused product with a real job is better than a complete-looking family of unnecessary apps.

### Shared ecosystem, distinct products
Babel products may share identity, semantics, standards, and infrastructure where useful, but each product must remain understandable and useful on its own. Do not make every app a skin of FIRE or World.

### Share meaning only when meaning transfers
Preserve compatibility when two products genuinely mean the same thing. Do not force a universal model when their jobs differ.

Examples:
- provenance is not achievement
- selection is not completion
- app usage is not proof of skill
- visual similarity is not semantic equivalence

### Evidence before interpretation
Preserve what happened, where, and with what context before reducing it to a conclusion. Interpretations may evolve; historical evidence should remain inspectable.

### Local identity, honest foundations
Shared foundations should reduce relearning and inconsistency without erasing the job or personality of each product.

## Product-shaping defaults

- **Delete before styling.** Remove labels, helpers, containers, pages, and features that do not make the task easier to understand or complete.
- **Fundamentals before signature polish.** Stabilize information architecture, navigation, task purpose, spacing, states, accessibility, and data safety before personality, lore, glow, pixels, animation, or metaphor.
- **Metaphor should clarify or delight, not translate the task.** Functional language stays immediately understandable.
- **One product logic across device sizes.** Presentation may adapt; the product job and semantics should not silently fork.
- **Build the smallest believable whole.** Prove a thin end-to-end path before deeply polishing isolated screens.
- **Real-world validation beats internal certainty.** Automated tests and browser simulation do not replace physical-device or real-project validation where those matter.

## Validated Babel shell baseline

FIRE G7 was the first owning product to physically validate a complete generic Babel shell and explicitly freeze it. The rules below are therefore shared defaults, not a mandate to copy FIRE screens or code.

- **Calm scaffold.** Navigation/actions occupy a stable toolbar row; page/project identity and quiet metadata compose below it rather than competing with the controls.
- **Content before chrome.** Generic chrome recedes until a real decision, state, risk, or primary action earns emphasis.
- **Quiet material, full interaction.** Touch targets should generally stay about 44px or larger even when the visible button material is smaller/quieter inside that target.
- **Parent owns the surface.** A grouped row, selection family, or split-action row owns its outer geometry and pressed/selected surface. Child targets keep distinct semantics without painting competing nested rectangles.
- **Symbol placement is systematic.** Start from shared geometry, allow a small intrinsic optical metric only when the glyph itself needs one, then let the host/container place it consistently. Do not repair shared symbols with page-specific nudges.
- **Related vs major rhythm is deliberate.** Use the shared spacing vocabulary. As a default shell rhythm, tightly related disclosure/control groups may use 12px separation while major conceptual groups and task-content-to-footer separation may use 24px; owning products may deliberately choose another value when evidence requires it.
- **Ordinary text fields behave like ordinary text fields.** Preserve normal platform correction/spelling/predictive assistance unless the value genuinely requires specialized input semantics. Numeric or otherwise specialized fields keep the appropriate input mode rather than inheriting generic text behavior.
- **Temporary UI may adapt form, not meaning.** Compact layouts may use a bottom sheet while regular width uses a centered dialog/card; the semantic content, action hierarchy, and task consequence remain the same.
- **Familiar first, signature second.** Commodity controls should be platform-legible and excellent. Distinctive Babel expression belongs where it improves the job rather than decorating routine UI.
- **Tactile, not decorative.** Character comes from hierarchy, rhythm, proportion, material, motion, and interaction—not gratuitous glow, gradients, borders, or metaphor.

This baseline is intentionally semantic and compositional. Do not extract a universal Babel component library from one product implementation; shared code remains unearned until multiple real products prove the same semantics and implementation genuinely need reuse.

## Hierarchy

A Babel product should feel calm, deliberate, learnable, and human.

- one clear primary task per focused screen
- minimum required context
- obvious continuation/exit where appropriate
- helper/subtitle text is optional, not default
- remove duplicated explanation before compressing or decorating it

## Geometry and rhythm

- repeated component roles should not change size or position arbitrarily
- state changes should not cause geometry to jump
- use a small structural spacing vocabulary rather than one-off values
- current default spacing vocabulary: **4 / 8 / 12 / 16 / 20 / 24**
- optical exceptions are allowed when deliberate; arbitrary page-specific drift is not
- touch targets should generally remain about **44px or larger** where touch is expected

Exact row heights, card dimensions, and app-specific density remain local until reuse across real products proves otherwise.

## Typography

Typography communicates role and hierarchy. State should usually use fill, contrast, or accessories rather than moving/changing label geometry.

Within a component family:
- keep the same label role at the same size/weight/alignment
- do not shift text because a different state/accessory appears
- reserve stronger hierarchy changes for genuinely different semantic roles

## Interaction states

Define only the states a family actually needs, commonly:
- normal
- pressed
- focus-visible
- selected
- disabled
- destructive where relevant
- completed where relevant

Selection and completion are different semantics. Do not add a state merely to make unrelated components look alike.

## Selection surfaces

For connected/grouped selection controls:
- the parent owns the outer border and corner radius
- child choices do not draw competing nested outlines/radii
- selection should usually be legible through fill/contrast/state
- checks/icons should add meaning, not duplicate it
- single-select and multi-select may share a family while preserving different semantics

## Rows, lists, and accessories

Repeated rows should share:
- a stable leading text anchor
- stable vertical alignment
- stable text roles
- a predictable trailing metadata/accessory area
- accessories that do not push the primary label around

Familiar accessories keep familiar meaning:
- chevron = navigate deeper
- drag handle = reorder
- ellipsis = management/actions
- plus = add/create the primary discrete object for the current view
- completion mark = actual completion

Apps may define additional accessories, but should not reuse a familiar symbol with contradictory meaning.

## Actions

Use clear role hierarchy:
- primary
- secondary/cancel
- destructive
- toolbar utility/action

Related actions should have intentional alignment and sizing. Do not let flex wrapping or content count accidentally choose the composition.

## Sheets and dialogs

Sheets/dialogs create or manage discrete objects while preserving context.

- group related choices tightly
- separate distinct conceptual groups with stronger spacing
- avoid redundant headings when the source action already makes purpose obvious
- keep consequence-bearing confirmation headings when they clarify risk
- presentation may adapt by environment while semantics/action hierarchy stay the same
- do not show fake drag handles on non-resizable surfaces

## Navigation

A visible Back affordance should retrace the path the user actually took when meaningful history exists. Deep/direct entry may use a safe product-defined fallback. Visible Back and platform/browser history should not tell contradictory stories.

## Adaptive behavior

Adapt presentation through width, density, column count, modal form, and optional secondary detail. Do not fork core semantics merely because the device changed.

## Shared implementation boundary

Do not build a speculative universal Babel component library.

Share principles, semantic patterns, small foundation tokens, process, and contracts first. Extract shared implementation only after at least two real products prove that the same component semantics and code genuinely need reuse.
