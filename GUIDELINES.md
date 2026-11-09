# Meridian brand book

Meridian is the company design language for electronics manufacturers: the public face of a company that designs, builds and certifies hardware. It covers the product catalog, product pages, documentation, support and company pages, and it treats specifications as the main content. Teltonika-level quality is the bar, not a look to copy. For established groups with long lifecycles and regulated customers, use Azimuth, the corporate form of Meridian. Management apps use Solaris; developer tools use Vesper.

## Principles

- **Specification first.** Every claim has a value and a unit. Engineers compare products by numbers, so numbers get the clearest type (`data`), the best position and the most space.
- **Drawn, not decorated.** Layouts align to a 4px grid. Lines are 1px. Radii are small (`r-1` to `r-4`). Visual interest comes from product drawings, photos and data, never from ornaments.
- **Copper marks the signal.** `accent` shows the selected item, the annotated part and the key data series. It covers less than 5% of a screen. Actions use graphite (`inverse`).

## Content fundamentals

Write like a datasheet: short sentences, active voice, measured values. Follow SI notation. Write part numbers, dates and units the same way everywhere.

| write | do not write |
|---|---|
| `12 V` (space before the unit) | `12V` |
| `−40 to +85 °C` (minus sign, written range) | `-40~85C` |
| `9–36 V DC` (en dash in compact ranges) | `9-36VDC` |
| `8 Mbit/s` (SI unit symbols) | `8Mbps` |
| `2026-09-02` (ISO 8601 dates) | `02/09/26` |
| Four isolated CAN FD channels | Seamless, powerful connectivity |

- Sentence case for headings, buttons, navigation and badges. Buttons start with a verb: "Request quote", "Contact sales".
- Speak to the reader as "you". The company speaks in the third person in legal text and as "we" nowhere else.
- No emoji, no exclamation marks, no hype words.
- Sample names (Kestrel, GW-410, LX-200) are placeholders until the real company data is known.

## Visual foundations

**Color.** Color has two layers. Primitive tokens (`slate-*`, `copper-*`) hold the raw values; semantic tokens give each value a job. Components use semantic tokens only, so the dark theme and a new accent need no component changes. Replace the copper ramp with the company color and keep its lightness steps.

- Surfaces: `canvas` page, `subtle` table headers, filter panels and drawing ground, `muted` disabled fields and chips, `sunken` pressed states.
- Text: `text` headings, body and values; `text-2` descriptions and spec labels; `text-3` captions, units, metadata and placeholders.
- Lines: `border` dividers, table rules and frames (decorative only); `border-strong` input, checkbox and secondary button edges.
- Action: `inverse` fill with `on-inverse` label for the primary button and selected segments.
- Signal: `accent` (copper) for selection, focus, annotation and the key chart series; `accent-subtle` for a highlighted cell.
- Status: `info` Preview, `success` Active, `warning` NRND and change notices, `danger` End of life, errors and security advisories. Each has a `-subtle` fill. A status is always a word as well as a color.
- Band: `band`, `band-2`, `band-line`, `band-text`, `band-text-2` are fixed and the same in both themes. Only the cover and the footer use them.

**Themes.** Light is the reference. Dark uses `slate-950` as `canvas`, lighter status colors and `copper-300` as `accent` so all text holds 4.5:1. Set the theme with `data-theme="light"` or `data-theme="dark"` on the root.

**Type.** Instrument Sans for all text and JetBrains Mono for part numbers, register values, versions and dimensions; load both from Google Fonts. Display sizes use tight tracking and weight 560; they are never all caps.

- `display-xl` (64/66, 560, −2.8%) page hero, once per page; `display-l` (48/52) section titles.
- `h1` (36/42, 580) product name; `h2` 28; `h3` 22; `h4` 18 for specification groups.
- `body-l` (18/28) lead text; `body` (16/24) default; `body-s` (14/20) table cells and notes; `caption` (12/16, 500).
- `overline` (12/16, 600, +8%, capitals) for group labels only.
- `data` (JetBrains Mono 13/20, 400 to 600) with tabular figures.

**Layout.** Content width 1280px (`page`). Grid: compact 0–599 has 4 columns, 16 gutter, 16 margin; medium 600–1023 has 8, 24, 32; wide 1024–1439 has 12, 24, 40; max ≥1440 has 12, 32, auto. Spacing base is 4px (`s-1` to `s-10`): 8–24 inside components, 32–64 between groups, 80–128 between page sections.

**Shape and elevation.** `r-1` (2) badges, tags and markers; `r-2` (4) buttons and inputs; `r-3` (6) cards, tables and notices; `r-4` (8) drawings and frames. Flat surfaces use a 1px `border`. Shadows only for layers that float: `shadow-2` menus and the mega menu, `shadow-3` dialogs.

**Drawings.** Product drawings sit on `subtle` with a 16px `grid-line` grid. Outlines 1.5px `draw-stroke`, fills `draw-fill`, dimension lines 1px `draw-line`, values mono 11px `draw-dim`. The Annotation component is the signature: copper leaders to reference markers, repeated in a legend.

**States.** Hover and press change fill in `t-fast` (120ms, ease 0.2, 0, 0, 1). Focus is a 2px `accent` ring with 2px offset on every control. Disabled is `muted` with `text-3`. Loading keeps the button width and shows a spinner.

**Motion.** `t-fast` 120ms hover, press and focus; `t-base` 200ms expand and tab change; `t-slow` 320ms mega menu and drawer; `t-exit` 160ms close (ease 0.4, 0, 1, 1). Motion confirms an action; it never decorates. Respect reduced motion.

## Iconography

Lucide icons (https://lucide.dev, ISC licence), stroke 1.5, round caps and joins, `currentColor`. 20px in content, 24px in navigation, 16px inside buttons and chips. Typical names: `cpu`, `plug`, `thermometer`, `download`, `git-compare-arrows`, `filter`, `globe`, `search`. No icon font is bundled; the previews draw the paths inline. An icon never carries meaning alone: the label or `aria-label` does.

## Page patterns

- **Global navigation**: SiteHeader with the mega menu (three product family columns and one featured product).
- **Product page**: ProductHeader (5 / 7 columns), then Tabs: Overview, Specifications, Ordering (OrderingTable), Documents (DocumentList), Software. Notices for change notices and advisories sit above the tabs.
- **Catalog**: ProductFinder with facets, chips, results table and compare.
- **Footer**: the fixed dark band.

Most visitors are engineers and buyers who search for one part. Put search, comparison and documents first.

## Accessibility

WCAG 2.2 AA is the minimum. Measured pairs:

| pair | light | dark |
|---|---|---|
| `text` on `canvas` | 17.6:1 | 15.9:1 |
| `text-2` on `canvas` | 6.8:1 | 7.6:1 |
| `text-3` on `canvas` | 4.6:1 | 5.2:1 |
| `accent` on `canvas` | 5.5:1 | 7.3:1 |
| `danger` on `canvas` | 5.5:1 | — |

Focus is a 2px `accent` ring with 2px offset. Touch targets are 40px or more; 32px buttons are for pointer-only areas such as table toolbars. Tabs use `tablist`, `tab` and `aria-selected`; segmented controls use `aria-pressed`; errors use `aria-invalid` and `aria-describedby`.

## Using Meridian

Meridian is a reference, not a component library. Take values from `tokens.json`, rules from this page, structure from each `components/<Name>/README.md`, and the look from each static preview. `components/bundle.css` shows how the tokens apply in CSS (classes prefixed `md-`). `components/bundle.js` is only a preview helper: it adds the drawing and icon sprite and connects tabs and segmented controls.
