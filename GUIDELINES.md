# Meridian brand book

Meridian is the marketing system: product landing pages and the public site. It is calm and light, with lots of white space, one accent color and plain copy. It follows the style of Untitled UI and Geist. It is not for app screens; management apps use Solaris and developer tools use Vesper.

## Content fundamentals

- Write short, plain and calm. One idea per sentence. No exclamation marks, no hype words ("revolutionary", "supercharge").
- Speak to the reader as "you" and "your team". The product speaks as itself ("Lumen follows up for you"), never "we".
- Sentence case everywhere: headings, buttons, nav, badges.
- Buttons start with a verb: "Start for free", "Watch demo", "Talk to sales", "Get started".
- Headlines state the benefit in plain words: "The calm way to run your team's internal work". Leads explain it in one sentence: "Docs, requests and approvals in one place."
- Feature copy is one or two sentences under 90 characters: "Set who signs off and in what order. Lumen follows up for you."
- Marketing pages can explain. Unlike app UI, helper copy is fine here when it answers a real question.
- No emoji. No stock photos of people; show the product.
- Placeholders still open: `[N]` (trial days) and `[Integration list]`. "Lumen", "Elif" and the request rows are sample content.

## Visual foundations

**Color.** The page is `surface` (white). Soft bands (`surface-soft`) with `line` borders top and bottom separate big sections. Text is `ink` for headings, `ink-secondary` for nav and control labels, `ink-muted` for body copy and hints, `ink-placeholder` for placeholders only. There is one accent, set per product (see Accent). Use it for the primary button, the logo mark, eyebrows, text links, the featured pricing card, check marks in plan lists and accent badges, and nowhere else. Status color appears in badges (`success`, `warning`, `danger`, neutral: a pale `-soft` fill with a darker label) and in form messages (`danger` for errors, `success` for the done line), always with words. The closing call to action is the only dark block (`inverse-surface`).

**Accent.** The accent is set per product. Pick one of `accent-option-violet` (default), `accent-option-teal`, `accent-option-orange`, `accent-option-ink`, and apply it with `data-accent="<option>"` on the page root. That sets `--accent`, `--accent-text`, `--accent-soft` and `--on-accent` together. Never set `--accent` alone. Every option gives 4.5:1 or more for the label on the fill and for `accent-text` on `surface`, `surface-soft` and `accent-soft`, in both themes, so no option needs a size rule. Ink flips to a near-white fill with a dark label in the dark theme.

**Themes.** Light is the reference. Dark is derived: `surface` #0c111d, raised panels #161b26, lines #1f242f, with lighter accent and status tints so text stays at 4.5:1 or more. In dark, the call-to-action block becomes a raised panel with a line edge so it does not disappear into the page.

**Contrast.** Every text token passes 4.5:1 on the surfaces its usage note names, in both themes; check the dark values too when you add a color. Borders that show where a control is (`line-input`, `line-control` in dark, the focus ring) pass 3:1. Two borders stay below 3:1 on purpose because a text label already marks the control: `line-control` in light (secondary buttons) and `inverse-line` in light (the outlined button in the CTA block). Never use those two for an input.

**Type.** Geist only (400, 500, 600, 700), Geist Mono for versions and code. Use the styles, not raw sizes:
- `display` (60px, 600, -0.03em, 1.1) for the hero H1, once per page.
- `heading-1` (40px, -0.02em) for section H2, `heading-2` (36px) in the call-to-action block, `heading-3` (20px) for feature titles.
- `lead` (20px, 1.55) under the H1; `body-lg` (18px, 1.6) under an H2; `body` (16px, 1.6) for everything else.
- `eyebrow` (16px, 600) in `accent-text` above section headings.
- `quote` (24px, 500) for testimonials, `price` (48px, 600, tabular) for plan prices, `faq-question` (18px, 600) for FAQ questions and plan names, `body-sm` (14px) for hints, errors, fine print and plan descriptions.
- Weight 700 is for the rare emphasis in long docs pages; headings stay 600.

**Layout.** Content is max `container` (1216px) with `space-8` side gutters. The NavBar folds into a menu button below 768px of width. Sections have `space-24` (96px) vertical padding. The hero is centered; all other sections are left aligned. Grids use `auto-fit` with a 300px minimum, so they fall to one column on phones.

**Shape.** Buttons and inputs `radius-md` (8px). Icon tiles `radius-lg` (10px). Cards and tables `radius-xl` (12px). Pricing cards, the product frame and the call-to-action block `radius-2xl` (16px). Badges, avatars and the announcement pill `radius-full`.

**Borders and shadows.** Every card and tile has a 1px `line` border. Buttons, inputs, tiles, stat cards and pricing cards get `shadow-xs` only. The product frame is the one element that floats (`shadow-frame`). No other shadows, no gradients.

**States.** Primary hover darkens the fill a little. Secondary hover fills `surface-soft`. Nav and footer links go from `ink-secondary` to `ink`; text links in copy (`TextLink`) are `accent-text` and underlined, and the underline gets thicker on hover. Keyboard focus is a 2px `surface` gap then a 2px `accent-text` ring (on the dark block: `inverse-ink`), on every control including inputs and FAQ rows.

**Forms.** Marketing forms are short: one email field (EmailCapture) or a few TextFields. Inputs are `field-h` (44px), radius-md, `line-input` border, label above in 14px 500. Show a hint only when it answers a real question. An error replaces the hint, turns the border `danger` and says what to do. Never use a placeholder as a label.

**Motion.** Color transitions of 120ms on buttons, inputs and segments only. Nothing moves on scroll. Respect reduced motion.

## Iconography

Line icons on a 24px grid, round caps and joins, drawn with `currentColor` (see the Icon component). Stroke 2 at 16 to 20px in buttons, pills and fields; stroke 1.8 at 22px in icon tiles. The source page draws these paths inline; there is no icon font. Add new icons in the same style (Lucide-like) and keep them decorative: the text next to an icon carries the meaning.

## Page structure

A landing page uses these sections in this order: NavBar, Hero, ProductFrame (product preview), a soft band with SectionHeader and FeatureGrid, a Testimonial, CtaBlock, Footer. The LandingPage card shows the full page.

A pricing page: NavBar, a centered SectionHeader (level 1) with PricingTable, a soft band with an FaqList, CtaBlock, Footer. The PricingPage card shows it.

A changelog page: NavBar, a SectionHeader (level 1) with an EmailCapture for release mail, then ChangelogEntries newest first, Footer.

Use the Footer with columns on any site with more than one page.
