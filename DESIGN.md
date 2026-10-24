# Babel Design Foundations

These are transferable defaults for Babel products. They are intentionally smaller than a universal component library.

Exact feature layouts and app-specific visual identity remain local.

## Design goal

A Babel product should feel calm, deliberate, learnable, and human. Repeated interactions should become predictable without forcing every app into the same visual skin.

> **Same meaning = same visual grammar. Different meaning may use different presentation.**

## Hierarchy

- one clear primary task per focused screen
- minimum required context
- obvious continuation/exit where appropriate
- helper/subtitle text is optional, not default
- remove duplicated explanation before compressing or decorating it

## Geometry and rhythm

- repeated component roles should not change size/position arbitrarily from screen to screen
- state changes should not cause geometry to jump
- use a small spacing vocabulary rather than one-off values for structural layout
- current default spacing vocabulary: **4 / 8 / 12 / 16 / 20 / 24**
- optical exceptions are allowed when deliberate; arbitrary page-specific drift is not
- interactive targets should generally remain about **44px or larger** where touch is expected

Exact row heights, card dimensions, and app-specific density are not global until reuse across real products proves they should be.

## Typography

Typography communicates role and hierarchy; state should generally use color, fill, or accessories rather than changing label geometry.

Within a component family:
- keep the same label role at the same size/weight/alignment
- do not make text shift horizontally because a different state/accessory appears
- reserve stronger hierarchy changes for genuinely different semantic roles

## Shared interaction-state grammar

Every interactive family should define the states it actually needs:
- normal
- pressed
- focus-visible
- selected
- disabled
- destructive where relevant
- completed where relevant

Do not add a state merely to make two components look more alike.

Selection and completion are different semantics.

## Selection surfaces

For connected/grouped selection controls:
- the parent surface owns the outer border and corner radius
- child choices should not draw competing nested outlines/radii
- selection should usually be legible through fill/contrast/state, with checks/icons only when they add meaning rather than duplicate it
- single-select and multi-select may share a family while preserving different semantics

## Rows and lists

Repeated rows should share a stable content grammar:
- consistent leading text anchor
- stable vertical alignment
- stable text role
- predictable trailing metadata area
- accessories occupy semantic slots without pushing the primary label around

Accessories must mean something:
- chevron = navigate deeper
- drag handle = reorder
- ellipsis = management/actions
- plus = add/create the primary discrete object for the current view
- completion mark = actual completion, not decoration

Apps may define additional accessories, but should not reuse a familiar symbol with a contradictory meaning.

## Buttons and actions

Use clear role hierarchy:
- primary action
- secondary/cancel action
- destructive action
- toolbar utility/action

Related actions should have intentional alignment and sizing. Do not let flex wrapping or content count accidentally choose the composition.

A standalone Cancel may use a different composition from paired Cancel + Save/Create only when the modal type makes that distinction intentional.

## Sheets and dialogs

Sheets/dialogs create or manage discrete objects while preserving context.

- group related choices tightly
- separate distinct conceptual groups with stronger spacing
- avoid redundant headings when the source action already makes purpose obvious
- keep consequence-bearing confirmation headings when they clarify risk
- modal presentation may adapt by environment (for example phone bottom sheet vs centered regular-width dialog) while keeping the same semantics and action hierarchy
- do not show fake drag handles/grabbers on non-resizable sheets

## Navigation

A visible Back affordance should retrace the path the user actually took when a meaningful history exists. Deep/direct entry may use a safe product-defined fallback.

Visible Back and platform/browser history should not tell contradictory stories.

## Responsive/adaptive behavior

One product logic across device sizes.

Adapt:
- width
- density
- column count
- modal presentation
- optional secondary detail

Do not fork core semantics simply because the device changed.

## Metaphor and personality

Personality should sit on top of clear product meaning.

Pixel language, Fire, glow, lore, animation, haptics, and other expressive systems may become shared or app-local when proven. They must not compensate for unclear hierarchy or make functional terminology harder to understand.

## Extracting shared components later

Do not create a universal Babel UI package yet.

When at least two real products independently prove the same semantic component and behavior, consider extracting shared implementation. Until then, share the rule/pattern, not speculative code.
