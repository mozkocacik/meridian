# OrderingTable

The ordering table lists each orderable variant. It starts with the part number format, where each variable segment is in `accent`, then one row per variant.

- Table in a 1px `border` frame, radius `r-3`. Header row `subtle`, 12px weight 600 `text-2`. Cells 14px, 10px by 14px padding, rules in `border`.
- Part numbers in mono. Number columns right aligned with tabular figures.
- Lifecycle in a LifecycleBadge. Discontinued rows are dimmed to `text-3` and link to the replacement.
- The last column is an arrow link ("Quote", "Replacement").
