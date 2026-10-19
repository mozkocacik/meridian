# TextField

A labelled text input: label above, the field, then a hint or an error.

- Field: `field-h` (44px), radius-md, `line-input` border (3:1 or more), surface fill, shadow-xs, 16px ink text. Placeholder is `ink-placeholder`.
- Label: 14px 500 in ink-secondary. Mark optional fields with "(optional)", not required ones with a star.
- Hint: `body-sm` in ink-muted. Show it only when it answers a real question ("We send the receipt here").
- Error: replaces the hint, `danger` text with the alert icon, and the border turns `danger`. Say what to do: "Enter an email address like name@company.com."
- Focus: the border turns accent-text and the standard focus ring shows.

**Content:** a label (always, also when it is visually hidden), the type, a placeholder, a hint and an error. Never use the placeholder as the label.
