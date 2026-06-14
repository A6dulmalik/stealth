# Stealth UI system

The design system is the shared visual and interaction layer for feature-owned UI.

## Modules

- `styles/fonts.css` loads and assigns interface, preview, and long-form reader typography.
- `styles/tokens.css` defines color, radius, density, gradient, glass, and shadow values.
- `styles/surfaces.css` owns reusable glass, tile, modal, mail-list, and reader treatments.
- `styles/interactions.css` owns focus, scrolling, motion, selection, and reduced-motion behavior.
- `components/` contains typed action, surface, and empty-state primitives.
- `feedback/` contains queued application notifications and their accessible viewport.

Import React primitives from `@/features/design-system`. Global CSS modules are composed once by
`src/styles.css`; feature code should consume the resulting tokens and utility classes rather than
redeclaring their values.

Feature-specific layouts stay in their feature folders. A primitive belongs here only when it has a
stable API and is useful in more than one workflow.
