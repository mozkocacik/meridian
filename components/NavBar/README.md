# NavBar

The top bar of every marketing page: logo, five links, "Log in" (tertiary) and "Get started" (primary). A 1px line border closes it.

The content is inside `container` (1216px) with space-8 side gutters. Links are nav style (15px, 500) in ink-secondary.

**Narrow screens.** The bar is a size container. Below 768px of its own width, the links and buttons go into a menu panel behind a 40px menu button (line-control border, radius-md). The panel lists the links at 16px with line separators, then "Log in" (secondary) and "Get started" (primary) at full width. The button has `aria-expanded` and `aria-controls`; Escape closes the panel and returns focus to the button; a link click closes it.

**Content:** the brand, the links (label and link), and optional call-to-action and log-in links. Keep to five links or less. Below 768px the links move into a menu; the preview shows the menu open.
