# PricingTable

Two to four PricingCards in a grid (min column 300px), with an optional billing switch (SegmentedControl) centered above them.

A plan's `price` and `period` can be one string or an object with one value per billing option (`{monthly: '$12', yearly: '$10'}`); the switch picks which one shows. Plans with one string stay the same in both.

Put it under a centered SectionHeader on a plain surface section. Follow it with an FaqList about billing. The PricingPage card shows the full page.

**Content:** the plans (each one a PricingCard), and optional billing options with the default option and a label.
