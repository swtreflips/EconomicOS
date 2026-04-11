# Minimum Viable Dashboard

## What Gets Shipped First

The MVP is not a full economic operating system. It's a single web page (mobile-first, local-language-first) that provides three things a person in a crisis economy can't reliably get anywhere else today:

1. **What do things cost right now?** (Real-time price tracker)
2. **What's the real exchange rate?** (Local currency/USD tracker)
3. **Where are the jobs?** (Labor market signal)

If these three signals are credible and updated daily, econOS has a product. Everything else builds from here.

---

## Dashboard Design

### Panel 1: Prices Today

**What it shows:**
- Daily price index for key categories: staple goods, personal care, household goods, electronics
- Price trend (last 7 days, 30 days, 90 days)
- Prices shown in BOTH local currency and USD (dual-currency reality)
- City-level breakdown where data permits (capital city, major cities)

**Data source:** Web-scraped prices from online marketplaces, supermarket sites, pharmacy chains, delivery apps.

**Update frequency:** Daily.

**Why this matters for allocation:** A worker negotiating wages needs to know what the cost of living is NOW. A business pricing products needs to see what competitors charge. A diaspora family needs to know what $200 buys this week vs. last month. This is the most fundamental allocation signal: what do things cost?

### Panel 2: Exchange Rate Today

**What it shows:**
- Current local currency/USD rate (P2P exchange platform midpoint)
- Central bank official rate for comparison
- Spread between market and official rate (a trust/policy signal)
- 7-day, 30-day, 90-day trend
- Rate of depreciation/appreciation

**Data source:** P2P exchange platform API (primary), independent rate trackers, central bank official rate.

**Update frequency:** Hourly during market hours.

**Why this matters for allocation:** In dollarized or multi-currency economies, every allocation decision runs through the exchange rate. Should I hold local currency or dollars? Should I price in dollars? Is my salary keeping up with the exchange rate? How much should I send home? The exchange rate is the conversion factor that makes every other number meaningful.

### Panel 3: Jobs Today

**What it shows:**
- Total job postings this week (trend vs. last week, last month)
- Top hiring sectors
- Top hiring cities (domestic + major diaspora destinations)
- Average posted salary ranges by occupation (where available)
- "Jobs for you" filter by occupation category

**Data source:** Local job platforms, LinkedIn, regional employment sites, Facebook Groups (scraped and classified).

**Update frequency:** Daily aggregates, weekly trend analysis.

**Why this matters for allocation:** This is the labor allocation tool. A person in a developing country deciding whether to stay, move to another city, or emigrate can see where demand exists for their skills. A student choosing a field can see what's actually hiring. A returning diaspora member can see what the job market looks like before committing to return.

---

## Additional Panels (Add After MVP)

### Panel 4: My City

Regional economic snapshot for a selected city:
- Price level relative to national average
- Job posting density
- Nighttime light trend (satellite-derived activity proxy)
- Rental prices

Enables: "Is my city recovering faster or slower than the rest of the country?"

### Panel 5: City Comparator

Side-by-side comparison of two cities (can be two domestic cities, or a domestic city vs. a diaspora destination):
- Cost of living comparison
- Job availability comparison
- Wage comparison (adjusted for cost of living)
- Real purchasing power comparison

Enables: "Am I better off in city A or city B, given my occupation?"

### Panel 6: Smart Remittance

For diaspora users sending money home:
- Current exchange rate (best available rate)
- What the remittance buys (purchasing power in local terms)
- Price trend for basic goods (is the money going further or shorter?)
- City-level breakdown (where does the remittance go furthest?)

Enables: Remittance allocation optimization -- the diaspora is often one of a developing country's largest economic actors, and they currently operate nearly blind.

---

## Technical Stack (Minimal)

| Component | Recommendation | Cost |
|-----------|---------------|------|
| Frontend | Static site (Next.js/Astro) or simple HTML/JS | Free (GitHub Pages / Vercel free tier) |
| Backend / data pipeline | Python scripts running on cron (scraping, processing, publishing) | $50-100/month (small VPS or cloud functions) |
| Database | SQLite or PostgreSQL (small dataset at this scale) | Included in VPS or free tier |
| API | Simple REST API serving JSON (FastAPI or Express) | Included in backend |
| Hosting | Vercel, Netlify, or Cloudflare Pages (free tiers) | Free |
| Domain | econos.org or similar | $12/year |

**Total infrastructure cost: ~$50-100/month.** This is not a capital-intensive project.

---

## Design Principles for the MVP

### Mobile First
Most users in developing countries access the internet through phones. The dashboard must work perfectly on a $100 Android phone over a mediocre mobile connection. This means:
- Light page weight (no heavy frameworks, no large images)
- Responsive design (works on small screens)
- Offline capability where possible (cache last-known data)
- Fast load times (< 3 seconds on 3G)

### Local Language First
Primary interface in the local language of the implementation country. English as secondary for diaspora and international audience.

### Show the Methodology
Every number links to a "How is this calculated?" page explaining:
- What data sources are used
- How they're combined
- What the known limitations are
- When the data was last updated

### Confidence Indicators
- Green: High confidence (multiple corroborating sources)
- Yellow: Moderate confidence (single source or partial data)
- Red: Low confidence (outdated data, single unreliable source)

Every panel shows its data freshness: "Last updated: 2 hours ago" or "Data from: March 25, 2026."

### No Account Required
The data is public. No login, no registration, no paywall. This is open-source infrastructure. You visit the page, you see the data. Period.

---

## Success Metrics for the MVP

### Month 1: Does it work?
- Data pipelines running reliably (>95% uptime)
- Prices updating daily
- Exchange rate updating hourly
- At least 3 data sources contributing to the price index

### Month 3: Do people use it?
- >1,000 unique visitors per month
- At least one media citation or social media share
- Feedback from users (what's useful, what's missing)

### Month 6: Do people trust it?
- >5,000 unique visitors per month
- Referenced by journalists, researchers, or NGOs
- Community contributions (people reporting data quality issues, suggesting sources)
- Methodology validated against established statistical agency benchmarks

### Month 12: Is it infrastructure?
- >20,000 unique visitors per month
- API used by other projects or organizations
- Methodology replicated or forked by others
- Recognized as a credible alternative data source for the implementation country

---

## What the MVP Proves

If the MVP succeeds, it demonstrates:

1. **The allocation thesis works**: People use the data to make better decisions (evidence: usage patterns, user feedback, behavioral changes)
2. **The methodology is credible**: Cross-validated, transparent, and trusted enough for real-world use
3. **The infrastructure is sustainable**: Low-cost, open-source, maintainable by a small team or community
4. **The leapfrog is real**: A developing country has real-time economic data that developed countries' statistical agencies don't provide in this format
5. **The platform extends**: The same infrastructure can add new indicators, new countries, and new BI views incrementally

From this MVP, everything else in the econOS vision becomes a matter of adding more data sources, more indicators, and more BI views on top of a proven foundation.
