# EJ2 Icon Theme Specification: Fluent2

## Theme Identity

- Product: EJ2
- Theme: Fluent2
- Theme ID: `ej2-fluent2`

## Icon Specification

- Base Size: 16 × 16 px
- ViewBox: `0 0 16 16`
- Safe Area: 14 × 14 px
- Padding: 1 px
- Stroke Width: 1 px
- Stroke Alignment: Center
- Stroke Cap: Round
- Stroke Join: Round
- Corner Radius: 1.5 px
- Cut Style: Sharp
- Cut Angle: 45°
- Terminal Style: Rounded
- Pixel-Perfect Rendering: Required

## Pixel-Perfect Alignment

Icons must be optimized for crisp rendering at the 16 × 16 px base size.

- Align geometry according to the complete visible bounds of fills and centered strokes.
- Position 1 px strokes on integer or half-pixel coordinates based on the geometry, symmetry, and intended visible stroke bounds.
- Use half-pixel coordinates when they produce crisp horizontal or vertical edges.
- Use integer coordinates when required to maintain optical or mathematical symmetry.
- Align filled shapes to integer coordinates where practical.
- Allow fractional coordinates for curves, diagonals, proportional geometry, and optical corrections.
- Include stroke caps and joins when checking visible bounds.
- Keep repeated and mirrored elements consistently aligned.
- Avoid unintended fractional coordinates that produce blurred or uneven rendering.
- Validate the final icon at the actual 16 × 16 px target size.

## Corner-Radius Behavior

The 1.5 px corner radius is the default radius for standard-sized elements.

For smaller elements:

1. Calculate a proportional starting radius based on the element size.
2. Compare the result with visually relevant EJ2 Fluent2 production SVG references.
3. Adjust the radius visually when the element appears too circular or too sharp.
4. Preserve the Fluent2 visual character.
5. Keep the corner radius editable in Figma wherever practical.

The proportional calculation provides a starting value only. Visual quality determines the final radius.

Complex silhouettes may use path-based curves when editable primitives cannot preserve the required shape, overlap, or negative space.

## Construction Style

Determine the construction style from visually relevant EJ2 Fluent2 production SVG references.

Supported construction styles:

- Outlined
- Filled
- Mixed

### Outlined Construction

For outlined elements:

- Use live 1 px center-aligned strokes.
- Preserve the stroke as an editable stroke.
- Use rounded caps and joins by default.
- Apply a different terminal treatment only when visually required and supported by relevant production references.

### Filled Construction

For filled elements:

- Preserve meaningful elements as separate editable objects where practical.
- Maintain clear negative space.
- Use filled path construction when required for complex silhouettes, overlaps, or cutout areas.

### Mixed Construction

For mixed icons:

- Keep outlined and filled elements as separate editable objects.
- Preserve live strokes for outlined elements.
- Maintain consistent visual weight between outlined and filled elements.
- Use mixed construction only when it is supported by visually relevant production references.

## Safe-Area Behavior

The 14 × 14 px safe area is the default construction area.

Artwork may cross the safe area when visually necessary for:

- Optical balance
- Recognizability
- Negative-space preservation
- Small-size readability
- Circular geometry
- Curved geometry
- Diagonal geometry
- Pointed geometry
- Elongated 
