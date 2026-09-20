# Typography and hierarchy

Inspect and improve typography in the current layout. Implement and verify changes within the manager’s assignment unless the user requested review only. Preserve earlier content and structural decisions.

## Detect

- Identify font families in use, including inherited stacks and display/body pairings. Flag Geist, Inter, Manrope, DM Sans, Satoshi, and Instrument Serif for replacement by default. These are the user's unwanted defaults; their presence is evidence of a preference mismatch, not proof that a font is inherently bad.
- Find large all-uppercase words or eyebrow labels placed above headlines. Look for oversized tracking, excessive weight, or a second headline competing with the actual headline.
- Check whether display styling overwhelms navigation, controls, data, and body text, or whether too many sizes and weights obscure hierarchy.

## Improve

1. Establish the product's audience, reading needs, character, and existing brand requirements before recommending a type direction. Preserve explicitly mandated brand fonts and report that constraint.
2. Choose a suitable alternative from available, supported, appropriately licensed fonts or a well-chosen system stack. Avoid replacing every rejected family with another habitual favorite. Account for required languages, weights, numeric forms, loading cost, and fallback metrics. Do not introduce a paid dependency or unsupported font asset merely to appear distinctive.
3. Use a restrained, coherent scale and pair families only when the pairing serves a clear purpose. Adjust size, weight, line height, measure, and spacing together; a font swap alone is insufficient.
4. Replace oversized uppercase pre-headlines with quiet sentence-case labels when the label provides useful orientation. Let the actual headline lead. Send redundant-label removal to the copy module; do not invent replacement text to occupy the same space.

## Verify and report

Check the result against small screens, long headings, readable body text, visible control labels, and fallback wrapping. Report changes and remaining dependencies. Preserve meaningful casing such as acronyms. Flag missing font assets or unverified language coverage instead of claiming readiness. Verify actual font loading and rendered hierarchy where preview access permits; otherwise request evidence from the manager.

Return the short specialist handoff defined in SKILL.md: completed changes, files, checks, and any limits or dependencies. In review-only mode, report recommendations instead. Do not create report files or start another round of subagents.
