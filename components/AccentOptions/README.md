# AccentOptions

The four accent options. A company picks one and sets it on the page root with the `data-accent` attribute: `<html data-theme="light" data-accent="cobalt">`.

Each option sets `--accent`, `--accent-hover`, `--accent-subtle` and `--on-accent` together, for each theme (rules at the end of `components/bundle.css`). Do not set `--accent` alone.

| option | light fill | label on fill | dark fill | label on fill |
|---|---|---|---|---|
| copper (default) | #a8501c | white, 5.5:1 | #e58a55 | #0e1116, 7.3:1 |
| cobalt | #1f5fbf | white, 6.1:1 | #6fa0f0 | #0e1116, 7.2:1 |
| teal | #0f766e | white, 5.5:1 | #4fc3b5 | #0e1116, 8.8:1 |
| graphite | #16191f | white, 17.6:1 | #e8ecf1 | #0e1116, 15.9:1 |

Every accent value is 4.5:1 or more as text on canvas, subtle and its own accent-subtle, in both themes. The accent is a signal color, not the brand fill: buttons stay graphite (`inverse`). Use graphite when the company color is red or green, so the accent does not look like a status.
