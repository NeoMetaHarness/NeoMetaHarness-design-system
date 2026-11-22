# NeoMetaHarness-design-system

The Neo theme and experience rules built on Astryx. Product consumers use @neometaharness/ui. Keep shared design decisions here and implementation wiring in the product repo.

## Component process
1. Search Astryx exports before proposing a custom Neo component.
2. Describe user task, semantic states, keyboard interaction and error behavior.
3. Review semantic theme tokens in both light and dark.
4. Test accessible contrast, focus, responsive behavior and reduced motion.
5. Document the adoption path through @neometaharness/ui and record any upstream gap.

Use templates/component-spec.md and templates/theme-review.md as review records. No unrelated UI libraries or per-component hardcoded token forks.

## Source boundaries
The design-system owns patterns and theme decisions. Product package sources and actual exports determine what ships. Progress-Memory ROUTER.md resolves work ownership.
