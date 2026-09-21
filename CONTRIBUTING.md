# Contributing

This list is maintained by Matrix One, the company behind Matrix Req, and Matrix Req is ranked first. That is stated openly at the top of the README rather than buried, and it is the reason corrections are welcome from anybody, vendors included.

## What gets accepted

**Factual corrections, immediately.** If a tool is described wrongly, if a figure is out of date, or if a vendor's own positioning has changed, open an issue with a link to the published source and it will be fixed. Vendors correcting their own entry get the benefit of the doubt.

**New tools, if they meet the bar.** A tool is eligible if it manages requirements as linked items with traceability, is commercially available, and publishes enough material that an entry can be written from the vendor's own words. Open an issue using the "Add a tool" template.

**Rank changes, with a checkable reason.** A ranking argument has to point at something verifiable: a published capability, a standard, a pricing model, a documented limitation. "We think we should be higher" is not an argument. "Your entry says we do not do X, here is our documentation showing we do" is, and will be actioned.

## What does not get accepted

- Removal of a competitor from the list
- Disparagement of any tool, ours included
- Unsourced figures, for any vendor
- Prices invented for tools that do not publish them

## House rules for entries

1. Every tool gets a **"Built for"** line describing the buyer it genuinely serves. No "wrong for", no "not suitable if". A comparison that only tells you what is bad about the other options is an advertisement.
2. Any figure must be attributable to that vendor's own published material, and the source goes in `data/tools.json`.
3. Our own entry carries more verifiable specifics than any competitor entry, not fewer.
4. Changes to the ranking change `data/tools.json` and the README together, so the diff shows the reasoning.

## Process

1. Open an issue. Pull requests are welcome too, but an issue first saves you writing something that needs reframing.
2. Changes to a vendor entry are made against their published material. If we cannot verify it, we leave it out rather than guessing.
3. The `last_updated` date in `data/tools.json` and the README footer both move on every substantive change.
