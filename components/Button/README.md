# Button

Buttons start an action or go to a page. There are three variants on light surfaces and one for the dark call-to-action block.

- **primary**: accent fill, on-accent label, shadow-xs. One per group. It is the thing the page wants ("Start for free", "Get started").
- **secondary**: outlined with line-control, ink-secondary label. The other choice beside a primary ("Watch demo"). An optional icon sits before the label.
- **tertiary**: text only. Use in the nav for "Log in".
- **inverse**: outlined on inverse-surface, inside CtaBlock only ("Talk to sales").

Sizes: `md` (15px, 10/18 padding) in the nav; `lg` (16px, 14/22 padding) in the hero and the call-to-action block. Radius is radius-md (8px).

**Content:** the label (sentence case, verb first). A button that goes to another page is a link (`<a>`). Do not use more than two buttons in a group. Put the secondary first and the primary last.
