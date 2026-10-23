# Badge

Shows the lifecycle state of a product. Every product shows one.

- **Preview** (`info`): samples only, not for production orders.
- **Active** (`success`): in production.
- **NRND** (`warning`): not recommended for new designs. Name a replacement.
- **End of life** (`danger`): no new orders. Name the replacement and the last delivery date.
- **neutral** (`text-2` on `muted`): other states, for example Custom.

A dot and a text label. The color is never the only signal. Height 22px, radius `r-1`, 12px 600.

**Content:** the state, in the words above.
