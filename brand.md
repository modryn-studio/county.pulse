# Brand

---

## Voice

How the product sounds in UI copy, headings, CTAs, and error messages.

- Clear and factual. The data does the talking — the UI just makes it readable.
- Confident without being technical. A county board member and a site selector should both understand every word.
- Honest about coverage. If data is stale or unavailable, say so plainly — never fake completeness.
- Never use: "AI-powered", "cutting-edge", "revolutionary", "unlock insights", "leverage", "synergy", "data-driven decision-making" (ironic — but the phrase is meaningless now)

---

## The User

A county economic development director with no data team, who pulls stale spreadsheets from five government websites and presents to the county board with year-old slide decks. They don't need a data scientist. They need someone who already did the data science and put it where they can use it.

---

## Visual Rules

- Color mode: Light mode base. Data dashboards need readability — dark mode is optional, not default. Government/civic audiences expect light backgrounds.
- Fonts: Inter (body — clean, neutral, reads well in data-dense layouts) + Space Grotesk (headlines — modern, confident, stands apart from gov-default Arial/Calibri)
- Motion: Minimal. Subtle number animations on load (counters ticking up). No scroll-triggered animations. Data should feel like it's already there waiting, not performing for you.
- Avoid: No stock photos. No fake testimonials. No generic "city skyline" imagery. No government-blue clichés. No gradients. No popups. No cookie banners unless legally required.

---

## Color System

Five named slots — these become the `@theme` tokens in `globals.css`.

| Name | Hex | Role |
|---|---|---|
| Accent | #10B981 | Primary — growth, economic health, key interactive moments. Emerald green. |
| Secondary | #F59E0B | Supporting accent — highlights, alerts, positive change indicators. Amber. |
| Background | #FAFAFA | Page background — light, clean, maximizes data readability |
| Text | #1A1A2E | Body text — near-black with warmth, not cold gray |
| Muted | #6B7280 | Secondary text, axis labels, borders, metadata |

Color rules:
- Catalis/GovBrands and most government tech own navy blue. Avoid blue entirely as a primary color. Green signals growth, economy, health — and differentiates immediately from every competitor in this space.
- No gradients. No neon. No pure black. The palette should feel trustworthy and calm — like a financial report that's actually pleasant to read.

---

## Logomark

Discovery questions — answer all before attempting to design the mark.

**Direction:**
Abstract shape — a pulse/heartbeat line that resolves into an upward trend. Not a literal heartbeat monitor — more like a single clean line that suggests both a pulse and economic growth.

**Primary color:**
Accent #10B981 (emerald green)

**Background:**
Transparent — no container. Must work on both light and dark backgrounds.

**Future-proofing:**
Mark must not reference Columbia County, Wisconsin, or any specific geography. It must work when the product covers 50 states and 3,000 counties.

**Competitor exclusions:**
Catalis/GovBrands owns blue corporate rounded-rectangle badges. ProximityOne has no real brand identity to avoid. Datawheel uses a stylized "D" in teal. Avoid: blue badges, teal letterforms, generic globe/map imagery.

**Anti-patterns:**
No map pins. No pie charts in the logo. No bar graphs. No generic "data visualization" imagery. No government seal aesthetics. No eagles or shields.

---

## Emotional Core

The product exists because of one sentence. Everything — the copy, the UI density, the data labels, the hero — should trace back to it:

> **"Nobody showed us."**

Every CCEDC director in America has been making economic development decisions without a real-time picture of their own community. Not because the data doesn't exist — it does, and it's free and public. But no one built the thing that makes it visible. That's the product. That's the brand.

## Emotional Arc

What a visitor feels at each stage — land, read, scroll, convert.

- Land: "This looks nothing like a government website."
- Read: "Wait — this is my county's actual data, and I can understand it instantly."
- Scroll: "I've been looking for something like this for years."
- Convert: "What would this look like for my county?"

---

## Copy Examples

Real copy to use as reference when writing UI text.

- Hero: "Your county, clearly."
- CTA: "See your county's data."
- Footer: "Built by Modryn Studio. Data from Census Bureau, BLS, USDA, and Wisconsin DWD. countypulse.dev"
- Error: "Data temporarily unavailable. Source may be updating."
