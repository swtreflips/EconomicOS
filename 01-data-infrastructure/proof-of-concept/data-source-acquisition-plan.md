# Data Source Acquisition Plan

## Organizing Principle

Data sources are categorized by accessibility, not by importance. The proof-of-concept starts with what's freely available, demonstrates value, then expands to sources that require partnerships or cost.

**The allocation lens**: Each data source is valued by how much it improves allocation decisions. A free, imperfect signal that's available today is worth more than a perfect signal that requires a 6-month partnership negotiation.

---

## Tier 1: Freely Available Today (Start Immediately)

These sources can be collected with engineering effort and no partnerships.

### Web-Scraped Prices

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Online marketplace (e.g., major e-commerce platform) | Prices for electronics, clothing, household goods, auto parts | Public listings, scrapeable | Largest platforms often list prices in both local currency and USD. |
| Pharmacy chains | Pharmacy and personal care prices | Website with product listings | Major chains with online presence |
| Supermarket chains | Supermarket prices (food staples) | Check for online ordering/catalogs | Coverage varies -- some chains have online catalogs |
| Instagram business accounts | Prices for food, clothing, services | Public posts, scrapeable with API | In many developing countries, businesses post prices on Instagram -- this is a real, widespread data source |
| Facebook Marketplace | Used goods, vehicles, real estate, services | Public listings | Rich pricing data for informal economy goods |

**Technical requirements**: Web scraping infrastructure (Python + Scrapy/Playwright), cloud hosting for automated daily collection, price normalization and categorization pipeline.

**Estimated timeline**: 2-4 weeks to build initial scrapers, ongoing maintenance for site changes.

### Exchange Rate Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| P2P exchange platform API | Real-time local currency/USDT exchange rate | Public API | The de facto market rate. Accessible, reliable, high-frequency. |
| Independent rate trackers | Parallel exchange rate tracking | Website, scrapeable | Long-running community-maintained rate trackers |
| Central bank official rate | Official exchange rate | Central bank website | Published but often diverges from market rate |

**Technical requirements**: API integration for P2P exchange platforms, scrapers for others. Simple, low-maintenance.

**Estimated timeline**: 1 week.

### Job Posting Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Regional job boards | Job postings with titles, locations, some salary data | Public listings | Dominant employment platforms in each target country |
| LinkedIn (public postings) | Professional job postings | Public search results | Skews toward formal/professional roles |
| Country-specific employment platforms | Job postings for validation markets | Public listings | Major local platforms in each country |
| Facebook Groups | Informal job postings | Public groups | Enormous volume of informal labor market activity in developing countries |

**Technical requirements**: Scraping + NLP for extracting structured data (job title, location, salary when listed, skills required) from unstructured postings.

**Estimated timeline**: 3-4 weeks for initial collection, ongoing classification refinement.

### Satellite Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| VIIRS Nighttime Lights (NASA/NOAA) | Nighttime light intensity by geography | Free, public | Monthly composites. Proven proxy for economic activity (Henderson et al., 2012). |
| Sentinel-2 (ESA) | Daytime satellite imagery | Free, public | 10m resolution, can detect construction, agriculture, commercial activity |
| Google Earth Engine | Processed satellite data | Free for research | Platform for analyzing satellite time series |

**Technical requirements**: Satellite data processing pipeline (Google Earth Engine or local processing), geographic mapping to target-country municipalities/states.

**Estimated timeline**: 2-3 weeks for initial pipeline, monthly updates automated.

### Rental / Real Estate Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Online marketplace (real estate section) | Rental and sale listings with prices | Public listings | Prices in USD common in dollarized economies |
| Country-specific real estate platforms | Local rental and sale listings | Public listings | Major platforms vary by country |
| Facebook Marketplace | Rental listings, especially informal | Public | Significant volume in developing countries |

**Technical requirements**: Same scraping infrastructure as price data, with real estate-specific fields (location, size, price, currency).

---

## Tier 2: Requires Light Partnership or Registration (Months 1-3)

### Delivery App Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Local delivery platforms | Restaurant and grocery prices, order volumes (if partnered) | Prices visible in app; volumes require partnership | Major delivery platforms in each target country |
| Regional delivery platforms | Restaurant prices across multiple countries | Prices visible in app | Multi-country delivery services |

**Approach**: Start by scraping visible menu prices (Tier 1 difficulty). Approach for volume data partnership if initial price data proves valuable.

### Central Bank Published Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Central bank statistical publications (crisis economy) | Monetary aggregates, banking system data, official exchange rates | Published on central bank website, sometimes irregularly | Quality and timeliness vary. Monetary aggregates (M2, reserves) are useful even if GDP/CPI are questioned. |
| Central bank (validation country) | Monetary data, financial statistics | Published, accessible, reliable | Strong central bank with good data culture |
| National statistical agency (validation country) | CPI, employment, retail sales, GDP | Published, accessible | The validation benchmark for econOS |
| Banking supervisor (crisis economy) | Banking sector data | Published | Banking system activity as economic signal |

**Approach**: Systematic monitoring and automated collection of whatever these institutions publish. Low effort, potentially high value for cross-validation.

---

## Tier 3: Requires Significant Partnership (Months 3-6)

### Transaction Volume Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Mobile payment system aggregate data (central bank) | Transaction volumes and values through the interbank mobile payment system | Unknown -- may require formal request or partnership with central bank or banks | This would be the single most valuable data source for economic activity measurement in a crisis economy |
| Digital payment platform aggregates | Mobile payment volumes | Likely requires partnership with platform operators or parent banks | Growing rapidly, could be transformative |
| Card network transaction volumes | Card network transaction volumes | Requires partnership | Local card networks |

**Approach**: The proof-of-concept should demonstrate value WITHOUT transaction data first. Once the system is credible, approach banks and payment networks with: "We've built this with public data. With your aggregate data (anonymized, no individual information), we could make it X times better. Here's how."

### Remittance Volume Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Formal remittance providers | Formal remittance volumes to target country | Likely requires partnership | Published aggregate data may be available through central bank or industry reports |
| World Bank remittance data | Country-level annual estimates | Published, free | Too infrequent for real-time tracking, but useful as benchmark |
| Central bank balance of payments data | Official remittance receipts | Published, irregular | May undercount informal channels significantly |

---

## Tier 4: Aspirational (6+ Months)

### Electricity Consumption

State electricity company data would be a powerful physical-world economic signal, but accessibility is unknown and the institution may be poorly managed. Satellite thermal data may be an alternative proxy.

### Tax Revenue Data

Tax authority collection data would be a direct economic activity signal. Likely requires government partnership or legislative access -- a long-term goal, not a Phase 1 item.

### Telecom / Mobile Data

Telecom regulator data -- mobile phone activity, data usage, geographic patterns -- would provide population and activity signals. Requires regulatory or operator partnership.

---

## The Acquisition Sequence

```
Week 1-2:    Exchange rates (P2P exchange platform API, independent rate trackers)
Week 2-4:    Web-scraped prices (online marketplace, pharmacies, supermarkets)
Week 3-5:    Job postings (regional job boards, LinkedIn, Facebook)
Week 4-6:    Satellite nighttime lights (VIIRS pipeline)
Week 5-8:    Rental/real estate listings
Week 6-10:   Delivery app prices (scraping visible menus)
Month 2-3:   Central bank / national statistical agency published data integration
Month 3-6:   Partnership approaches for transaction volumes
Month 6+:    Electricity, tax, telecom if partnerships develop
```

**The principle**: Start collecting data the day you start building. Don't wait for partnerships. Don't wait for the perfect source. Every week of data you have is a week of baseline you can compare against later. Start now, improve continuously.

---

## Cost Estimates

### Tier 1 (Freely available)

| Item | Monthly cost |
|------|-------------|
| Cloud compute for scraping + processing | $50-200 (small scale) |
| Satellite data processing | Free (Google Earth Engine) or $50-100 (cloud compute) |
| Data storage | $10-50 |
| Domain + hosting for public dashboard | $20-50 |
| **Total** | **$100-400/month** |

### Tier 2-3 (With partnerships)

Costs depend entirely on partnership terms. Academic/research framing may unlock free or reduced-cost access. NGO/development organization partnerships (e.g., through IDB, UNDP, CAF) could provide institutional support.

**The key point**: The proof-of-concept can be built for under $500/month in infrastructure costs using freely available data. This is not a capital-intensive project. It's an engineering and analytical project that happens to produce enormous value.
