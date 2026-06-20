# Governance: Open Standard, Community-Governed

> **Status: Active design** -- Standard governance is load-bearing architecture, not a future concern.

## Purpose

econOS is an **open standard for economic data publication**. Governance determines who controls the standard -- and the answer must be: the community, not any single government, institution, or interest group.

This is not abstract. In the GPS model, the US Air Force operates the satellites but doesn't control how anyone uses the signal. In the econOS model, governments operate data collection sensors (they already collect this data through regulatory authority), but the community governs the standard that defines how data is published, formatted, and validated.

## The Core Separation

| Role | Who | Examples |
|------|-----|----------|
| **Standard governance** | Community (multi-stakeholder) | Data schemas, methodology rules, quality requirements, publication protocols |
| **Tier 1 sensor operation** | Government agencies | Central bank publishes payment volumes under the standard; tax authority publishes revenue data |
| **Tier 2 sensor operation** | Regulated entities | Banks, mobile payment platforms publish aggregates under the standard |
| **Tier 3 sensor operation** | Community/private sector | Scraped prices, job postings, satellite data, exchange rates |
| **Interpretation/metrics** | Ecosystem (anyone) | CPI estimates, activity indexes, BI dashboards, applications |

The government is a **node operator**, not the **protocol designer**. It publishes data under the standard but doesn't control what the standard requires, how the data is interpreted, or who accesses it.

## Standard Governance Model

### Multi-Stakeholder Community

The standard is governed by a community that includes:
- **Academic economists** -- methodology rigor, validation
- **Civil society / NGOs** -- public interest representation
- **Technology contributors** -- engineering, data architecture
- **Diaspora representatives** -- ensuring the standard serves populations outside the country
- **Government representatives** -- as stakeholders, not authorities

No single category holds majority control. The government participates in standard development but cannot unilaterally change it.

### RFC Process

Standard changes follow an open process modeled on the IETF (Internet Engineering Task Force):

1. **Proposal**: Anyone submits a change proposal (new data schema, methodology update, quality requirement)
2. **Public review**: Community reviews, critiques, suggests modifications
3. **Consensus building**: Discussion until rough consensus emerges
4. **Implementation**: Standard updated, versioned, documented
5. **Validation**: Changes tested against established statistical agency benchmarks

This prevents both unilateral government changes and unilateral community changes. The process is transparent and documented.

### Conflict Resolution

When the government wants to change the standard in a way the community disagrees with:
- The government can publish data under its own modified standard (fork)
- The community retains the canonical standard
- The divergence is visible and documented
- Users choose which standard to trust

This is the open-source immune system: forkability constrains power.

## Anti-Weaponization Design

History has repeatedly demonstrated what happens when a single institution controls economic data with no oversight. econOS prevents this through five layers:

1. **Open standard** -- methodology is public, auditable, forkable
2. **Multi-source cross-validation** -- Tiers 1, 2, and 3 provide overlapping signals; if government data diverges from independent sensors, the divergence is detectable
3. **Published methodology as manipulation detector** -- consistency checks make data tampering mathematically visible
4. **Community governance** -- government participates but doesn't control
5. **Tier 3 permanent fallback** -- community sensors provide degraded but functional coverage if any tier goes dark

The lesson is NOT "never let government touch data." It's "never let government be the sole, unauditable, ungoverned source."

## The Governance Reality in Developing Countries

**In countries with functional institutions:** Where the national statistical agency is respected and institutional capacity exists, the standard can be adopted as an incremental step -- the agency already publishes open data, and adding an econOS-standard publication layer builds on existing infrastructure.

**In countries with collapsed or hostile institutions:** Where the government that suppressed data publication is being asked to adopt an open standard for economic transparency, this is the hardest sell. Pragmatic answer: design and validate the standard first where institutions are functional. Adoption in harder environments follows when institutional conditions permit. Meanwhile, Tier 3 community sensors provide coverage.

**What makes adoption attractive to governments:**
- International credibility (IDB, World Bank, IMF value transparent data)
- Investment attraction (investors need trustworthy economic data to deploy capital)
- Institutional modernization (open data standards are the global direction)
- Reduced burden (standardization makes existing reporting more efficient)

**The instrument is a publish-mandate.** Adoption takes concrete legal form as a transparency/disclosure law requiring institutions to publish data they already collect -- not a new data agency, not government control of the data. The most direct path to enacting it is a political champion who runs on data transparency as a platform commitment; the architecture keeps the system independent of that champion so it survives changes of government, and a pre-mandate Tier 3 proof-of-concept demonstrates the policy before it exists. See [open-standard-governance.md](../00-foundations/architecture/open-standard-governance.md) §7.

## International Precedents

- **Estonia X-Road**: Open-source (MIT license), government operates infrastructure, community governs the standard. Now adopted by multiple countries.
- **India UPI**: Government-backed open payment protocol. Standard body defines the interface, private banks and fintechs operate. Billions of monthly transactions.
- **IETF**: Governs internet protocols (HTTP, TCP/IP). Governments use the internet but don't control the specifications. Multi-stakeholder, consensus-based.
- **GPS**: US Air Force operates satellites. Signal specification is public. Alternative systems (GLONASS, Galileo, BeiDou) provide redundancy. Anyone builds receivers.

## What This Means for Contributors

- **Standard developers**: Contribute to schema design, methodology documentation, validation tools
- **Sensor operators**: Implement the standard for their data domain (government agencies, banks, community scrapers)
- **Ecosystem builders**: Use published data to build metrics, dashboards, and applications -- no permission needed
- **Auditors**: Verify compliance between published data and the standard's methodology requirements

## Depends On

- Operational experience from initial implementation (start where institutions are functional)
- A community of contributors (which grows from demonstrated value)
- [00-foundations/architecture/open-standard-governance.md](../00-foundations/architecture/open-standard-governance.md) -- detailed governance architecture
- [00-foundations/architecture/data-pipes-architecture.md](../00-foundations/architecture/data-pipes-architecture.md) -- the three-tier sensor model
