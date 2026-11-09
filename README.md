# Meridian

Meridian is the company design language for electronics manufacturers: the public site of a company that designs, builds and certifies hardware. It covers the product catalog, product pages, documentation, support and company pages, and it treats specifications as the main content. It has a light and a dark theme, one accent color that each company sets (copper by default), Instrument Sans and JetBrains Mono, and Lucide icons.

| System | For |
| --- | --- |
| Solaris | Dense management and collaboration apps |
| **Meridian** | Company sites for growing electronics companies |
| Azimuth | Corporate sites for established electronics manufacturers |
| Vesper | Developer and infrastructure tools |

Meridian is a reference, not a component library. Each component is a definition (`README.md`) and a static HTML picture (`preview.html`). Build the components in your own stack.

## Files

| Path | Content |
| --- | --- |
| `README.md` | This page. |
| `GUIDELINES.md` | Rules for principles, color, type, layout, content and accessibility. Read it before you build a page. |
| `tokens.json` | All tokens with a usage note for each token. |
| `tokens.css` | The same tokens as CSS custom properties and type classes. When you change a token, change both files. |
| `components/bundle.css` | Styles for the previews. It uses only the custom properties from `tokens.css`. |
| `components/bundle.js` | Preview helper only. It adds the drawing and icon sprite and connects the tabs and segmented controls. Do not use it in a product. |
| `components/<Name>/README.md` | The definition of one component: parts, states, content and when to use it. |
| `components/<Name>/preview.html` | A static HTML picture of one component. |

## Fonts and icons

The repository does not contain font or icon files. Get them from their own sources:

- **Fonts:** Instrument Sans and JetBrains Mono (Google Fonts). `components/bundle.css` loads them.
- **Icons:** Lucide (lucide.dev). Use the Lucide icon names.

## Theme

```html
<html data-theme="light"> <!-- light or dark -->
```

Light is the default theme. With no `data-theme`, the page is light. Meridian does not follow the system setting. Use `data-theme="dark"` for the dark theme.

Replace the copper ramp (`copper-*`) with the company color and keep its lightness steps. The semantic tokens (`accent`, `accent-hover`, `accent-subtle`, `on-accent`) then follow. Component classes use the prefix `md-`.

## Components

Annotation, Breadcrumb, Button, Checkbox, Cover, DocumentList, Footer, LifecycleBadge, Link, Notice, OrderingTable, ProductFinder, ProductHeader, SegmentedControl, Select, SiteHeader, SpecList, Tabs, TextField
