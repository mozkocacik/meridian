# Button

Buttons start an action or go to a page.

- **primary:** graphite fill (`inverse`), `on-inverse` label. One per view: "Request quote".
- **secondary:** `canvas` fill, 1px `border-strong` ring. Parallel actions: "Datasheet".
- **tertiary:** text only, `muted` on hover. Low-priority actions in dense areas: "Compare".
- **danger:** `danger` fill. Destructive actions in account areas only.

The accent is never a button fill. Sizes: `s` 32px (toolbars, tables), `m` 40px (default), `l` 48px (product header). Radius `r-2`. Weight 560.

States: hover, pressed, focus (2px `accent` ring, 2px offset), disabled (`muted` fill, `text-3` label), loading (spinner and a present-tense label: "Sending").

**Content:** a verb that names the result, sentence case. A button that goes to another page is a link (`<a>`).
