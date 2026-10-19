# Meridian

Meridian is a calm, light design system for marketing sites and product landing pages. It has a light and a dark theme, one accent color that each product sets, Geist and Geist Mono, and Lucide icons.

| System | For |
| --- | --- |
| Solaris | Dense management and collaboration apps |
| **Meridian** | Marketing and landing pages |
| Vesper | Developer and infrastructure tools |

Meridian is a reference, not a component library. Each component is a definition (`README.md`) and a static HTML picture (`preview.html`). There is no JavaScript. Build the components in your own stack.

## Files

| Path | Content |
| --- | --- |
| `README.md` | This page. |
| `GUIDELINES.md` | Rules for color, type, layout, content and accessibility. Read it before you build a screen. |
| `tokens.json` | All tokens with a usage note for each token. |
| `tokens.css` | The same tokens as CSS custom properties and type classes. When you change a token, change both files. |
| `components/bundle.css` | Styles for the previews. It uses only the custom properties from `tokens.css`. |
| `components/<Name>/README.md` | The definition of one component: parts, states, content and when to use it. |
| `components/<Name>/preview.html` | A static HTML picture of one component. |

## Fonts and icons

The repository does not contain font or icon files. Get them from their own sources:

- **Fonts:** Geist and Geist Mono (Google Fonts). `components/bundle.css` loads them.
- **Icons:** Lucide (lucide.dev). Use the Lucide icon names.

## Theme

```html
<html data-theme="light" data-accent="teal"> <!-- accent: violet, teal, orange or ink -->
```

The accent sets `--accent`, `--accent-text`, `--accent-soft` and `--on-accent` together. Do not set `--accent` alone. Component classes use the prefix `md-`.

## Components

AccentOptions, AnnouncementPill, Badge, Button, ChangelogEntry, Cover, CtaBlock, DataTable, EmailCapture, FaqList, FeatureGrid, FeatureItem, Footer, Hero, Icon, LandingPage, Logo, NavBar, PricingCard, PricingPage, PricingTable, ProductFrame, SectionHeader, SegmentedControl, StatCard, Testimonial, TextField, TextLink
