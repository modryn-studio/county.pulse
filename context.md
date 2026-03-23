# Project Context

## Core Framework

Market: Small county economic development offices in the US (~3,000 counties). They make economic development decisions — site selection responses, county board budget justifications, grant applications, business retention — using stale PDFs, manually-pulled spreadsheets from 5+ government websites, and gut instinct. No affordable, modern data visualization layer exists for them.

Reference product (what people pay for): Catalis Economic Development Dashboard (now governmentbrands.com) — enterprise-priced ($10K+ contracts), PE-backed by TPG/PSG, 501–1,000 employees. Explicitly markets "community profiles powering your website at a price point your municipality can afford" — but the price point is still enterprise. ProximityOne — 1-2 person operation, 20+ years, ugly UI, charges for training/consulting/custom reports (~$200-500K/year estimated). Datawheel — ~20-25 people, Cambridge MA, national government clients, high-end custom. Top complaint across all: too expensive, too ugly, or not built for small counties.

Your angle: Affordable ($99-199/month white-label), genuinely beautiful (modern Next.js/Tailwind stack), and specifically built for small counties (under 60K population) that Catalis ignores because the contract size is too small for their sales team. Local go-to-market — walk into the CCEDC and demo a live dashboard of their own county. No enterprise sales rep will ever do that.

Contrarian truth: The data exists, is public, and is free. The CCEDC doesn't need a data scientist — they need someone who already did the data science and put it where they can use it. Every competitor assumes the buyer wants software. The real buyer wants to stop being the last to know.

## Customer Use Cases

These are the four concrete moments when Steve (and every county EDC director like him) actually needs this product. Every metric, label, and data view on the dashboard should serve at least one of these.

1. **Site selection response** — A company evaluating Portage for a new facility asks the CCEDC for current labor availability, wage rates, and industry composition data. Currently: stale PDFs assembled manually. With Pulse: open the dashboard, export the page, send it in 5 minutes. This is where the product earns its keep in a single conversation.

2. **County board budget justification** — CCEDC must justify its annual budget to the county board. Currently: slide decks assembled from 1-2 year old Census data. With Pulse: a live scoreboard of what the CCEDC's work is actually doing to the county's economic indicators. Dashboard becomes the annual report.

3. **Local business expansion decisions** — A restaurant owner wants to know if the market can support a second location. Currently: 8 clicks into Census.gov, requiring data literacy they don't have. With Pulse: accessible answer in plain English on a public-facing URL they can share with a banker or investor.

4. **Grant applications** — Federal EDC grants require data-backed documentation of economic conditions. Currently: small counties patch together stale sources or hire consultants. With Pulse: the data narrative is already assembled, citable, and current.

Common thread: the data is public and free — but inaccessible to anyone without hours of time and data skills the CCEDC staff doesn't have.

## Competitive Validation

What was learned from deep research on each competitor — and the product implications.

**Catalis / GovBrands** (enterprise, PE-backed: TPG + PSG, 501-1,000 employees)
- Explicitly markets affordable pricing, but contract sizes are still enterprise ($10K+)
- Sells to municipalities with IT departments and procurement processes
- Product implication: position as the version that requires no procurement, no IT dept, no contract — just a credit card and a 15-minute meeting

**ProximityOne** (1-2 person, 20+ years, single founder: wglimpse@proximityone.com)
- Actively updated weekly. Runs weekly training sessions. Quietly sustainable (~$200-500K/year estimated)
- 20-year-old UI. No modern stack. No API. No MCP
- Product implication: the market is survivable solo. The UI is the entire moat available to you — modern stack beats a maintenance-mode incumbent

**Datawheel** (~20-25 people, Cambridge MA, founded 2013)
- Started as the free OEC (Observatory of Economic Complexity) academic tool at MIT → grew to national government contracts through credibility earned from the free product
- This is the exact playbook: free first, institutional credibility second, paid product third
- Product implication: the free Columbia County dashboard isn't a loss leader — it's the Datawheel origin story. Build it like a flagship, not a demo

**Tyler Technologies** (7,000+ employees, serves large governments only)
- Not a threat at the small county level. Serves only the largest government contracts
- Product implication: confirms the market is real and large. If Tyler won't touch it, the small-county segment is yours by default

**21st.dev** (YC-backed, MCP monetization validated)
- Proved the model: free tier MCP server → paid limits at $20/month → sustainable recurring revenue from developer access
- 85% month-over-month growth in MCP protocol downloads. Less than 5% of 11,000+ MCP servers are monetized
- Product implication: the MCP layer (Layer 3) is early-mover territory. County economic data is exactly the type of structured, reliable, locally-specific data that AI agents cannot currently access

**Wisconsin Precedent**: UW-River Falls Center for Economic Research already built an economic dashboard for the St. Croix Valley EDC — meaning Wisconsin EDC directors already understand the product category. The ask is not foreign to them.

## Go-to-Market Sequence

The specific order that makes the launch work. Do not skip or reorder steps.

1. **Build quietly** — Complete the Columbia County dashboard with real public data. Do not announce. Do not share. Make it genuinely excellent first.
2. **Walk into the CCEDC** — Steve Sobiek, 1800 Kutzke Rd Suite 109, 608-617-7121. Open the laptop. Show him his own county's data visualized in a way he's never seen it. Don't pitch. Just show.
3. **Let the CCEDC share it** — If the demo lands, Steve will share it with the county board, other county contacts, and the Chamber. Word of mouth in a county of 60K moves fast.
4. **Write the log post** — Document the build on modrynstudio.com. This is the distribution for the developer/indie audience and the proof-of-work for future county clients.
5. **Expand to neighboring counties** — Baraboo, Wisconsin Dells, Beaver Dam — all within 30 minutes of Portage, all similarly underserved. Each new county is another white-label conversation.

## Product

A county-level economic data dashboard that pulls free public data (Census Bureau County Business Patterns, BLS, USDA ERS, Wisconsin DWD WisConomy) and visualizes it into a clean, real-time picture of a county's economic health. Columbia County, WI is the first build. The dashboard is layer 1. Layer 2 is a REST API exposing the same data. Layer 3 is an MCP server so AI agents can query county economic data directly. Layer 4 is scale — if the pipeline works for one county, it works for all 3,000+.

## Target User

Steve Sobiek, executive director of the Columbia County Economic Development Corp (CCEDC), 1800 Kutzke Rd Suite 109, Portage, WI. 608-617-7121. He makes economic development decisions for Columbia County — responding to site selectors, justifying the CCEDC's annual budget to the county board, supporting local business expansion, and writing grant applications. His current data sources are stale Census spreadsheets, Wisconsin DWD monthly snapshots, and word of mouth. He finds out about economic changes weeks or months after they happen. He doesn't need a data scientist — he needs someone who already did the data science and put it where he can use it.

## Deployment

mode: standalone-domain

This is a standalone product, not a modryn-studio tool. It gets its own domain and its own Vercel deployment. It links back to Modryn Studio as the builder, but it stands alone as a product and brand.

url: https://countypulse.dev
basePath: <!-- empty — standalone mode -->

## Minimum Money Loop

Free public dashboard (Columbia County) → CCEDC sees it / Luke demos in person → white-label offer meeting → Stripe subscription ($99-199/month) → white-labeled dashboard embedded on CCEDC site → CCEDC shares with county board as proof of value

Rule: the free Columbia County dashboard must be live and genuinely useful before any sales conversation happens. The product sells itself when Steve sees his own county's data visualized clearly for the first time.

## Stack Additions

- Census Bureau API (County Business Patterns — free, structured, annual)
- BLS API (employment, wages, unemployment — free)
- USDA ERS (poverty, population, education, median income — free downloadable county-level data)
- Wisconsin DWD WisConomy (monthly county snapshots)
- County assessor records (housing values, building permits)
- Resend for email capture / notifications
- Stripe for white-label subscriptions (Phase 2+)

## Project Structure Additions

- `/src/lib/data/` → Data fetching, transformation, and caching logic per data source
- `/src/lib/data/census.ts` → Census Bureau County Business Patterns API client
- `/src/lib/data/bls.ts` → BLS labor statistics API client
- `/src/lib/data/usda.ts` → USDA ERS data parser
- `/src/lib/data/wisconsin.ts` → Wisconsin DWD data client
- `/src/types/` → TypeScript types for economic data models
- `/public/data/` → Static/cached data snapshots (fallback if APIs are slow)

## Route Map

- `/` → Landing page + Columbia County overview (hero metrics, key indicators at a glance)
- `/employment` → Employment by industry, unemployment rate trends, wage data
- `/businesses` → Business counts by NAICS sector, openings/closings, establishment trends
- `/housing` → Housing values, building permits, vacancy rates
- `/population` → Population trends, demographics, age distribution, migration
- `/workforce` → Labor force participation, commuting patterns, education attainment
- `/income` → Median household income, poverty rate, income distribution
- `/about` → What this is, who built it, methodology, data sources with links

## Monetization

Phase 1: `none` — Free public dashboard for Columbia County. Pure credibility and demonstration play. Email capture for updates/notifications.

Phase 2: B2B SaaS — White-label dashboards for county EDCs at $99-199/month via Stripe subscription. The Columbia County dashboard is the demo instance.

Phase 3: Developer API — Tiered pricing for structured county economic data access. $29/month hobbyist, $99/month professional, $499/month commercial.

Phase 4: MCP server — Free tier with paid limits for AI agent access to county economic data. Modeled after 21st.dev's monetization pattern.

## Target Subreddits

- r/dataisbeautiful — county-level economic visualizations are exactly this audience's thing
- r/urbanplanning — economic development practitioners and planners
- r/wisconsin — local community interest, pSEO amplification
- r/econdev — economic development professionals (small but targeted)

## Social Profiles

- X/Twitter: https://x.com/lukehanner
- GitHub: https://github.com/modryn-studio/county.pulse
- Dev.to: https://dev.to/lukehanner
- Ship or Die: https://shipordie.club/lukehanner
