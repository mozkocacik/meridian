# AccentOptions

The four accent options. A product picks one and sets it on the page root with the `data-accent` attribute: `<html data-theme="light" data-accent="teal">`.

Each option sets `--accent`, `--accent-text`, `--accent-soft` and `--on-accent` together, for each theme (rules at the end of `components/bundle.css`). Do not set `--accent` alone: the text tint and the label color must change with it.

| option | fill | label on fill | accent-text light | accent-text dark |
|---|---|---|---|---|
| violet (default) | #5b4ee8 | white, 5.7:1 | #5b4ee8 | #a49cf5 |
| teal | #0e7c66 | white, 5.1:1 | #0b6e5a | #5cc9ac |
| orange | #b9470f | white, 5.3:1 | #b9470f | #f08a5d |
| ink | #101828, #f5f5f6 in dark | white; #101828 in dark | #101828 | #f5f5f6 |

Every accent-text value is 4.5:1 or more on surface, surface-soft and accent-soft in its theme, so eyebrows, badges and links pass at any size. Orange was darkened from #d4561c, which gave only 4.1:1 with white and 3.7:1 on its tint.
