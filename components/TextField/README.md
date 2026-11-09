# TextField

A single-line input with its label above it.

- Height 40px (`control-m`), radius `r-2`, 1px `border-strong` edge on `canvas`. Value 15px in `text`; placeholder `text-3`.
- Label 14px, weight 560, always above the field. Never use a placeholder as the label.
- A hint (`md-help`, 13px `text-3`) only when it answers a real question.
- Units sit inside the field on the right in mono `text-3` (`md-unit`). Numbers use tabular figures.
- Focus: 2px `accent` outline on the field edge. Error: `danger` edge, and a message under the field that says what is wrong and how to correct it ("Use digits only in the part number. Example: GW-410-4C-LTE-E."). The message replaces the hint and is linked with `aria-describedby`; the field gets `aria-invalid`.
- Disabled: `muted` fill, `text-3`.

The consumer gives the label, the value or placeholder, an optional unit, hint and error text.
