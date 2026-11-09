# Annotation

The signature of Meridian. A copper leader connects a part of the drawing or photo to a reference designator. The legend repeats each designator with name and value, so the image can stay small on phones.

| part | specification |
|---|---|
| Ground | `subtle` with a 16px grid in `grid-line`, radius `r-4` |
| Drawing | outlines 1.5px `draw-stroke`, fills `draw-fill`, dimension lines 1px `draw-line`, dimension values mono 11px `draw-dim` |
| Leader | 1.2px `accent`, vertical or horizontal only, ends on the part edge |
| Marker | JetBrains Mono 600, 11px, `r-1`, `accent` fill, `on-accent` text |
| Designator | J = connector, D = indicator, S = switch, U = module, F = fuse. Same as the schematic |
| Legend | marker, name in 15px 560, value in mono 12px `text-2`. Order follows the leaders from left to right |
| Caption | mono 11px `text-3` under the drawing: view name left, unit right |

The consumer gives the drawing (SVG with `currentColor`-free strokes bound to the draw tokens) and the legend rows.
