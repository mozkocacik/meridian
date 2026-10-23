# Meridian brand book

Meridian is the company system for electronics makers: the product catalog, product pages, documentation, support and company pages. Engineers and buyers come to find one part and compare it. So specifications are the main content, and they get the clearest type, the best position and the most space. For established groups with long lifecycles and regulated customers, use Azimuth. App screens use Solaris; developer tools use Vesper.

## Principles

1. **Specification first.** Every claim has a value and a unit. Numbers get tabular figures and the best position.
2. **Drawn, not decorated.** Layouts align to a 4px grid. Lines are 1px. Radii are small. Visual interest comes from product drawings, photos and data, never from ornaments.
3. **The accent marks the signal.** It shows the selected item, the annotated part and the key data series. It covers less than 5% of a screen. Actions use graphite.

## Content fundamentals

- Write like a datasheet: short sentences, active voice, measured values. Sentence case everywhere.
- Every feature claim names a value or a concrete use. "Four isolated CAN FD channels", not "Seamless, powerful connectivity".
- Units follow SI: a space before the unit (`12 V`, `8 Mbit/s`), the minus sign and "to" in written ranges (`−40 to +85 °C`), an en dash in compact ranges (`9–36 V DC`).
- Dates are ISO 8601 (`2026-09-02`). Part numbers, versions and register values use JetBrains Mono.
- Buttons name the result: "Request quote", "Datasheet", "Compare", "Talk to an engineer".
- Use the terms of the trade: protocols, standards, designators. Explain a term once, in the glossary, not in every paragraph.
- No emoji, no stock photos, no "10x" claims, no three-column icon grids with one-word features.
- Acme and its products are sample content.

## Visual foundations

**Color.** Two layers. Primitive values (slate neutrals, the accent ramp) feed semantic tokens; components use semantic tokens only. The page is `canvas`. `subtle` is for table headers, filter panels and the drawing ground. Text is `text`, `text-2` for descriptions and labels, `text-3` for metadata and placeholders on canvas or subtle only. Actions use `inverse` (graphite). The accent (copper by default) is the signal color; see AccentOptions. Status color (`info`, `success`, `warning`, `danger`, each with a `-subtle` fill) is for lifecycle and notices, always with words. The `band` (cover and footer) is dark in both themes.

**Themes.** Light is the reference. Dark uses `canvas` #0e1116 with lighter text, accent and status values so all text stays at 4.5:1 or more. The accent label flips to dark (`on-accent` #0e1116) in the dark theme. With no `data-theme`, follow the system setting; a ThemeToggle keeps the visitor's pick.

**Type.** Instrument Sans for all text, JetBrains Mono for data. Display sizes use weight 560 and tight tracking; they are never uppercase. Use the styles in `tokens.css`: `display-xl` once per page, `display-l` for section titles, `h1` to `h4`, `body-l` for leads, `body`, `body-s`, `caption`, `overline` (uppercase, group labels only), `data` and `marker`.

**Layout.** Content is at most 1280px wide. Grid: 4 columns below 600px (16px gutter and margin), 8 columns to 1023px (24px gutter, 32px margin), 12 columns above (24px gutter, 40px margin). Sections have 96px vertical padding on wide screens and a hairline between them. Most blocks use 4 + 8 columns (heading left, content right) or full width.

**Shape.** `r-1` (2px) for badges, tags and markers, `r-2` (4px) for buttons and inputs, `r-3` (6px) for cards, tables and notices, `r-4` (8px) for drawings and frames.

**Borders and shadows.** Flat surfaces use a 1px `border`. Only layers that float over content get a shadow: `shadow-2` for menus, `shadow-3` for dialogs. No gradients.

**Imagery.** Every image shows a real device or a real interface. Use line drawings in datasheet style (see Annotation) or studio photos on a cool grey ground. Show connectors, labels and part numbers sharp.

**States.** Hover darkens a fill or adds `subtle`. Focus is a 2px `accent` ring with a 2px offset on every control. Disabled uses `muted` and `text-3`. Loading shows a spinner and a present-tense label.

**Motion.** `t-fast` (120ms) for hover and press, `t-base` (200ms) for expand and highlight, `t-slow` (320ms) for the mega menu. Nothing moves on scroll. Respect reduced motion.

## Iconography

Lucide, stroke 1.5, round caps and joins, `currentColor`. 20px in content, 16px in buttons and links, 24px in navigation. Icons are decorative; the text next to them carries the meaning.

## Page structure

A product page: NavBar, ProductHeader, SectionBar, then sections in this order: Overview (SectionHeader, KeyFigures, FeatureList), an application example, Specifications (SpecTable), Ordering (PartNumber, DataTable), Documents (DocumentList, software table, Notice), Accessories, a contact block, Footer. The ProductPage card shows it.

A category page: NavBar with MegaMenu, SectionHeader, ProductFinder, Footer.

## Accessibility

WCAG 2.2 AA is the minimum. Every text token passes 4.5:1 on the surfaces its usage note names, in both themes. Borders that alone show a control (`border-strong`, the focus ring) pass 3:1. Touch targets are 40px or more; 32px buttons are for pointer areas such as table toolbars. Status is never shown by color alone. Tables have header cells and a caption.
