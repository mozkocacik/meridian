# Annotation

The signature of Meridian. A technical drawing or product photo with leaders that connect parts to reference designators, and a legend that repeats each designator with its name and value. Because the legend carries the text, the image can stay small on phones.

Parts:
- **Drawing:** line drawing in `draw-stroke`, fills in `draw-fill`, dimension lines in `draw-line`, dimension text in `draw-dim` (JetBrains Mono 11px). Ground is `subtle` with the 16px grid (`grid-line`). Radius `r-4`.
- **Leader:** 1.2px in `accent`, vertical or horizontal only. It ends on the edge of the part.
- **Marker:** `marker` type (mono 11px, 600), fill `accent`, label `on-accent`, radius `r-1`.
- **Legend:** marker, name (15px, 560), value (`data`, 12px, `text-2`). Order follows the leaders from left to right.
- **Caption:** below the drawing: view name left, units and tolerance right.

Designators follow the schematic: J connector, D indicator, S switch, U module, F fuse.

**Content:** the drawing, a list of designator, name and value, and the view name.
