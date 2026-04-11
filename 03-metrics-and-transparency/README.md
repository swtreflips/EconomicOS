# Phase 3: Ecosystem-Built Metrics, Frameworks, and Applications

> **Status: Future** -- Built by the ecosystem on top of Phase 1 (data pipes) and Phase 2 (analytical infrastructure).

## Purpose

This is the layer where econOS data becomes tools that regular people use. But critically: **econOS doesn't build this layer. The ecosystem does.**

econOS is GPS -- open data pipes broadcasting standardized economic signals. This phase is the Google Maps, the Waze, the Uber -- applications that independent actors build on top of those signals, using their own methodologies, serving their own users, making their own editorial decisions about what to show and how to present it.

econOS's role is to make this layer possible by providing reliable, granular, standardized data. The power and the interpretation belong to the ecosystem.

## What the Ecosystem Builds

### Derived Metrics (Layer 1)

Multiple independent analysts and organizations build competing metrics from econOS raw data:

- An economist publishes a weekly CPI estimate for a capital city, using their own basket and weights
- A university research group publishes a "Regional Activity Index" for each state or province
- A think tank publishes a "Recovery Tracker" using satellite + jobs + price stability
- Another economist publishes a different CPI with different methodology -- and publicly argues why theirs is better

**Multiple competing interpretations of the same raw data is a feature, not a bug.** It produces better understanding than any single authoritative number.

### Applications (Layer 2)

Purpose-built tools for the decisions people actually face:

**For the worker/migrant**
"I'm a nurse. Should I stay in my city, move to the capital, or go abroad?"
- Labor demand for nurses by city
- Wage levels (adjusted for cost of living)
- Cost of living comparison (rent, food, transport)
- Community size at each destination (diaspora network)
- Legal status pathway

**For the student**
"I'm about to choose a university program. What's actually in demand?"
- Field-level job demand across the country and region
- Wage trends by field
- Remote work opportunities
- Saturation risk

**For the small business owner**
"I want to open a bakery in this neighborhood. Is there demand?"
- Local spending patterns
- Competition density
- Foot traffic and population trends
- Rent trajectory

**For the investor / diaspora**
"Is the recovery real? Where should I put money?"
- Regional activity indexes (which regions are growing?)
- Sector growth rates
- Price stability trends
- Formal employment signals

These applications are built by startups, NGOs, universities, diaspora organizations, government agencies -- anyone who sees a need and has the skills to serve it.

## Why econOS Doesn't Build This Layer

- Every application involves editorial decisions about what to show, what to emphasize, what to recommend. These decisions shape user behavior. If econOS makes these decisions, it becomes a gatekeeper of interpretation.
- Multiple competing applications serving different users with different priorities is healthier than a single "official" dashboard.
- This keeps econOS focused on what it does best: collecting and standardizing data.
- It prevents power concentration: no single entity controls both the data AND the interpretation.

## What econOS Does Provide

- A simple **reference dashboard** -- a basic data browser for exploring raw econOS data (like the built-in map on a GPS device)
- **Reference implementations** -- example code for building common metrics (basic price index, job posting aggregator) from econOS data
- **Documentation and guides** -- how to build on econOS data, API reference, schema documentation
- **Validation tools** -- compare your derived metric against established statistical agency benchmarks to check methodology

## Design Principles for Ecosystem Builders

- **Mobile first.** Most users access via phone.
- **Local language first.** Primary users are in the implementation country, not international audiences.
- **Translate, don't prescribe.** Show data, don't tell people what to decide.
- **Show your work.** Link to methodology, sources, freshness.
- **Avoid false precision.** Honest uncertainty bands beat fake confidence.
- **Partial is better than nothing.** A rough real-time view is infinitely better than the void that exists today.

## Depends On

- [01-data-infrastructure/](../01-data-infrastructure/) -- the raw data pipes
- [02-algorithmic-coordination/](../02-algorithmic-coordination/) -- the analytical/validation layer
- [00-foundations/architecture/data-pipes-architecture.md](../00-foundations/architecture/data-pipes-architecture.md) -- the GPS architecture document
