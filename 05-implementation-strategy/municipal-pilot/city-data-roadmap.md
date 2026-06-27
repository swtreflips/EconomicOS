# City Economic Data Roadmap: Capture → Structure → Publish

*How to take a data-rich city's scattered records and turn them into a legible, real-time picture of the local economy — useful to every agent who makes decisions in it. This is the data substance beneath the [champion pitch](champion-pitch.md); the [micro-standard](micro-standard.md) is the schema it produces.*

---

## Why a city is not a small country

The national econOS vision is built around **currency, prices, and inflation in a data *void*** — the economy is invisible because the central bank stopped publishing. None of that transfers cleanly to a city:

- A city has **no currency, no central bank, no inflation crisis** of its own. The price/exchange-rate spine of the national PoC mostly doesn't apply.
- A **functional, data-rich city is not a void — it's a silo.** It already collects business licenses, building permits, inspections, 311 calls, and property records. The data exists. It's just trapped in separate departments, in incompatible formats, never joined, and never made legible to the people making decisions.

So the city economy is fundamentally **spatial**: a map of *who is doing what, where*. The framework holds — capture → structure → publish, three tiers, open standard, allocation-first — but the **spine changes**. Place-based commercial activity replaces currency and inflation as the core signal. The work shifts from *collecting data that doesn't exist* to **integrating and making legible data that already does.**

---

## The conceptual spine: the city economy as a spatial panel

Every dataset, whatever department it comes from, becomes rows keyed on three things:

> **geography × time × category**

All of the "structuring" work is getting each siloed source onto **one** canonical geography, **one** time bucket, and **one** category taxonomy — then aggregating with privacy and attaching methodology. That shared key is the entire trick: it's what turns a pile of department CSV exports into a single readable map where a business-formation layer, a permit layer, and a rent layer line up over the same neighborhoods.

This is the open standard ([micro-standard.md](micro-standard.md)), generalized from one dataset to many.

---

## Allocation anchor: capture only what answers a decision

The roadmap is organized around **agents and the decisions they face**, never around "datasets we happen to have." If a dataset doesn't help someone allocate their resources better, it's not in scope yet.

| Agent | The decision they're making | Indicators that serve it |
|---|---|---|
| Business owner (existing or aspiring) | Where do I open or relocate? | Business formation & churn, storefront vacancy, foot traffic, sector mix |
| Investor / developer | Where is investment flowing? | Building permits, property sales, rents, formation trend |
| Worker / job-seeker | Where are the jobs? | Local postings, hiring by sector and area |
| Resident / mover | Where can I afford to live? Is my area improving? | Rents, permits, vitality trend, 311 conditions |
| City government | Where do I target support? Where is decline starting? | All of the above, read as an early-warning map |

The **lead slice** answers one question — *"Where is the local economy alive?"* — and serves business owners, investors, and the city itself at once. That is where the roadmap starts.

---

## CAPTURE — the city three-tier model

Your three tiers carry over directly; only the *content* changes from currency/inflation to place-based commerce.

### Tier 1 — City-held administrative data (the open-data portal)
The city already publishes most of this. No permission, no scraping — just an API pull or download.
- **Business licenses / registrations** (issued, renewed, closed) → formation & churn
- **Building permits** → construction and investment pipeline
- **Code enforcement / vacancy registrations** → blight, empty storefronts
- **311 service requests** → neighborhood conditions and demand signals
- **Property assessments / parcels** → land use and value
- **Procurement / contracts** → where public money flows
- **Transit ridership, parking/meter data** → activity and footfall proxies

### Tier 2 — Other institutional data (semi-public, light partnership)
- **County recorder:** property sales & deeds → the real-estate market
- **State business registry:** entity formations → a cross-check on city licenses
- **Utility connections** (if a separate authority) → real-growth ground truth
- **Public-school enrollment** → household movement
- **BID / chamber of commerce** → curated local-business data

### Tier 3 — Open / community / scraped (no permission needed)
This is the independent cross-check and the freshness layer — and the part that works even if the city never lifts a finger.
- **Commercial-vacancy & rental listings** → vacancy and rent in near-real-time
- **Job postings** (local boards, LinkedIn, Indeed) → labor demand by area
- **Yelp / Google business status + Popular Times** → closures and foot-traffic proxies
- **Satellite / aerial imagery** → parking-lot fullness, construction, as ground truth

**The lead slice uses:** Tier 1 business licenses + building permits, cross-validated by a Tier 3 foot-traffic / vacancy signal. Tier 1 tells you what the records say; Tier 3 tells you whether reality agrees.

---

## STRUCTURE — the make-it-legible layer (the heart of the work)

This is where the value is created. Five normalization steps, applied to every source:

1. **Canonical geography.** Pick ONE official spatial layer — neighborhoods, council districts, or census tracts — and geocode every record to it. This is the join key; everything snaps to it. Choose the finest layer at which most cells still clear the privacy threshold (step 4).
2. **Canonical time bucket.** Month to start (weekly where the source supports it). Consistent buckets make every indicator comparable over time.
3. **Canonical taxonomy.** NAICS sector codes for businesses; a property/use taxonomy for buildings. Map every source's local categories onto the shared scheme, and record the mapping.
4. **Aggregate + protect privacy.** Produce counts per (geography × time × category). Suppress any cell below **N = 5** — never publish a number that could identify an individual business or person. (Reuse the rule in [micro-standard.md §4](micro-standard.md).)
5. **Attach methodology metadata.** Every indicator carries: source, cadence, lag, operational definitions, known limitations, and a confidence level.

**Output:** a tidy **indicator panel** (rows of geo × time × category with counts) plus a **metadata registry**. Built once, this pipeline is reusable for every indicator that follows — the second dataset is far cheaper than the first.

---

## PUBLISH — two layers (the GPS model)

econOS broadcasts signals; others build the maps. Two outputs, in order:

1. **The open data layer.** Each indicator as **CSV *and* JSON** on a public, forkable location (the city portal or a public repo), plus a simple read API. No login, no paywall. This is the raw signal anyone — startups, journalists, the city, a student — can build on ([data-pipes-architecture.md](../../00-foundations/architecture/data-pipes-architecture.md)).
2. **A reference dashboard, organized by agent decision — not by dataset.** Following the [minimum-viable-dashboard](../../01-data-infrastructure/proof-of-concept/minimum-viable-dashboard.md) pattern, but spatial:
   - **"Where is the economy alive?"** — a neighborhood map of formation, vacancy, and foot traffic *(ship first)*
   - **"My neighborhood"** — one area's vitality, permits, rents, conditions
   - **"Where are the jobs?"** and **"The construction pipeline"** *(later)*
   - Mobile-first, no login, and **every tile shows its methodology, freshness, and confidence.**

---

## THE STAGED ROADMAP — one vertical slice at a time

Resist building all of it at once. Each stage ships something real and reuses the last stage's pipeline.

**Stage 0 — Lay the backbone (~2 weeks).**
Choose the canonical geography, write the agent/decision map, fix the taxonomy, and name the lead indicator. No data is processed yet — you're defining the keys everything will snap to. Cheap, and it prevents every downstream re-keying headache.

**Stage 1 — One vertical slice, end to end.**
"Commercial vitality" from **business licenses alone**: pull from the portal → geocode, bucket by month, classify by NAICS, aggregate, suppress → publish CSV/JSON + ONE neighborhood map + a methodology page. This is the thinnest thing that proves the *entire* capture→structure→publish pipeline works. Ship it before adding anything.

**Stage 2 — Add the spatial join.**
Add **building permits** and a real-estate indicator on the *same* geo/time keys. Now the join pays off: you can overlay formation vs. permits vs. rents on one map and *see* a neighborhood's story. This is the moment the silo-breaking becomes visible.

**Stage 3 — Add an independent cross-check.**
Bring in a **Tier 3** scraped signal (vacancy or foot traffic) to validate the Tier 1 picture and add freshness between monthly admin releases. Ship the "My neighborhood" view. Where Tier 1 and Tier 3 disagree, that divergence is itself information.

**Stage 4 — Make it legible.**
Build a reference **"commercial vitality index"** per neighborhood — clearly labeled as *one interpretation*, with published weights, forkable so anyone can build their own. Assemble the agent-organized dashboard.

**Stage 5 — Extract the value.**
Get a real agent to use it: a business owner siting a shop, a journalist citing the map, the economic-development office targeting support. That usage is the proof — and it feeds the political stepping-stone in the [champion pitch](champion-pitch.md).

---

## Honesty about the limits (state these prominently, never bury them)

- **Administrative data records legal events, not real activity.** A license's official close date is not the day the shop actually shuttered. Permits are filed before — sometimes long before — anything is built.
- **The informal / cash economy stays largely invisible.** Street vendors, informal labor, and cash-only businesses don't appear in licenses or listings. The blind spot is the same one the national vision has — smaller, but real.
- **"Monthly admin data" is not truly real-time.** Tier 3 scraping is what buys you freshness between releases; say so.
- **Privacy suppression caps your resolution.** Below N = 5, cells disappear — which limits how fine the neighborhood or sector granularity can go. Coarsen the geography rather than publish identifiable data.

---

## The one-paragraph version

A data-rich city isn't missing economic data — it's drowning in siloed records nobody can read. The city PoC doesn't collect new data; it puts what already exists onto one spatial backbone (geography × time × category), aggregates it safely, and publishes it both as open signal and as a map organized around the decisions real people face — *where should I open, where can I afford to live, where are the jobs, is my area improving?* Start with a single end-to-end slice (business formation by neighborhood), prove the whole pipeline, then add indicators on the same keys until the local economy is legible to everyone who participates in it. That legibility — cheap, reproducible, and impossible to honestly oppose — is the proof that the publish-mandate works.
