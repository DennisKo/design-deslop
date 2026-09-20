# Decoration and affordances

Improve the visual treatment of the elements that remain after earlier passes. Preserve the Layout pass’s container decisions. Implement and verify changes within the manager’s assignment unless the user requested review only.

## Look for

- Oversized icons parked in rounded, tinted tiles above every heading. Lucide is not itself a defect: the repeated decorative composition is.
- Text blocks with a colored left border used indiscriminately to make ordinary prose look important.
- Large corner radii on every panel, image, input, menu, and button, regardless of scale or function.
- Wide, blurred drop shadows repeated across flat content, creating fuzzy halos or implying elevation without an interaction reason.

## Improve

1. Remove decorative icon backplates and oversized heading icons when they communicate nothing beyond the heading. Keep informative icons, and size and align them with the text they support. Preserve accessible names for icon-only controls.
2. Present ordinary prose without an accent border. Use spacing, a useful heading, or existing text hierarchy. Retain a callout treatment for genuine alerts, quotations, or distinct states where the pattern helps recognition; color must not be the only signal.
3. Establish a small, consistent radius scale matched to component size and the product's visual character. Reserve pill shapes for components that benefit from them, such as chips or segmented controls. Do not flatten every component mechanically.
4. Remove ambient shadows from static sections. Use restrained elevation for overlays, floating controls, and draggable items when it clarifies stacking or interaction. A separator, surface contrast, or whitespace may provide sufficient distinction.

## Verify and report

Inspect desktop and narrow layouts, plus available hover, focus, disabled, and open states. Check that controls remain recognizable, focus rings remain visible, overlays separate from underlying content, and shadows do not create clipping or scroll overflow. Confirm icon removal leaves no empty wrappers or awkward gaps.

Report decorative changes and affected shared styles. Keep changes scoped so unrelated components are preserved. Report inspected states and unavailable preview evidence honestly.

Return the short specialist handoff defined in SKILL.md: completed changes, files, checks, and any limits or dependencies. In review-only mode, report recommendations instead. Do not create report files or start another round of subagents.
