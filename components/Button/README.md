# Button

Buttons start an action on the current page. Primary is graphite, never copper.

- **primary**: `inverse` fill, `on-inverse` label. One per view ("Request quote", "Contact sales").
- **secondary**: `canvas` fill with a 1px `border-strong` edge, `text` label. Parallel actions ("Datasheet"). An icon may sit before the label.
- **tertiary**: text only, `muted` on hover. Low-priority actions in dense areas ("Compare").
- **danger**: `danger` fill. Only for destructive actions in account areas.

Sizes: small 32px (`control-s`, pointer-only areas such as table toolbars), medium 40px (`control-m`, default), large 48px (`control-l`, hero and product header). Radius `r-2`. Label 15px, weight 560, sentence case, verb first.

States: hover and pressed change the fill in `t-fast`; focus is a 2px `accent` ring with 2px offset; disabled is `muted` with `text-3`; loading keeps the width and shows a spinner and a present-tense label ("Sending").

The consumer gives the label, the variant, the size and an optional Lucide icon. A button that goes to another page is an `<a>` with the same classes.
