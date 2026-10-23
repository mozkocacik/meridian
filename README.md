# Meridian

Meridian is the design language for the public site of an electronics company: product catalog, product pages, documentation, support and company pages. It treats specifications as the main content. It has a light and a dark theme, one accent color that each company sets, Instrument Sans and JetBrains Mono, and Lucide icons.

| System | For |
| --- | --- |
| Solaris | Dense management and collaboration apps |
| **Meridian** | Company sites for growing electronics companies |
| Azimuth | Corporate sites for established electronics manufacturers |
| Vesper | Developer and infrastructure tools |

Meridian is a reference, not a component library. Each component is a definition (`README.md`) and a static HTML picture (`preview.html`). There is no JavaScript. Build the components in your own stack.

## Files

| Path | Content |
| --- | --- |
| `README.md` | This page. |
| `GUIDELINES.md` | Rules for principles, color, type, layout, content and accessibility. Read it before you build a page. |
| `tokens.json` | All tokens with a usage note for each token. |
| `tokens.css` | The same tokens as CSS custom properties and type classes. When you change a token, change both files. |
| `components/bundle.css` | Styles for the previews. It uses only the custom properties from `tokens.css`. |
| `components/<Name>/README.md` | The definition of one component: parts, states, content and when to use it. |
| `components/<Name>/preview.html` | A static HTML picture of one component. |

## Fonts and icons

The repository does not contain font or icon files. Get them from their own sources:

- **Fonts:** Instrument Sans and JetBrains Mono (Google Fonts). `components/bundle.css` loads them.
- **Icons:** Lucide (lucide.dev). Use the Lucide icon names.

## Theme

```html
<html data-theme="light" data-accent="copper"> <!-- accent: copper, cobalt, teal or graphite -->
```

With no `data-theme`, Meridian follows the system setting. The accent sets `--accent`, `--accent-hover`, `--accent-subtle` and `--on-accent` together. Do not set `--accent` alone. Component classes use the prefix `md-`.

## Components

AccentOptions, Accessory, Annotation, Badge, Breadcrumb, Button, Checkbox, Cover, DataTable, DocumentList, FeatureList, Footer, Icon, KeyFigures, KeyValueGrid, Logo, MegaMenu, NavBar, Notice, PartNumber, ProductFinder, ProductHeader, ProductPage, SectionBar, SectionHeader, SegmentedControl, SpecTable, Tabs, Tag, TextField, TextLink, ThemeToggle
