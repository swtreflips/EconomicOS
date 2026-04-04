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
| MercadoLibre Venezuela | Prices for electronics, clothing, household goods, auto parts | Public listings, scrapeable | Largest e-commerce platform in LatAm. Prices in both Bs and USD. |
| Farmatodo | Pharmacy and personal care prices | Website with product listings | Major chain with online presence |
| Central Madeirense / Excelsior Gama | Supermarket prices (food staples) | Check for online ordering/catalogs | Coverage varies -- some chains have online catalogs |
| Instagram business accounts | Prices for food, clothing, services | Public posts, scrapeable with API | Many Venezuelan businesses post prices on Instagram -- this is a real, widespread data source |
| Facebook Marketplace | Used goods, vehicles, real estate, services | Public listings | Rich pricing data for informal economy goods |

**Technical requirements**: Web scraping infrastructure (Python + Scrapy/Playwright), cloud hosting for automated daily collection, price normalization and categorization pipeline.

**Estimated timeline**: 2-4 weeks to build initial scrapers, ongoing maintenance for site changes.

### Exchange Rate Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Binance P2P API | Real-time bolivar/USDT exchange rate | Public API | The de facto market rate. Accessible, reliable, high-frequency. |
| Monitor Dolar / DolarToday | Parallel exchange rate tracking | Website, scrapeable | Long-running independent rate trackers |
| BCV official rate | Official exchange rate | BCV website | Published but often diverges from market rate |

**Technical requirements**: API integration for Binance, scrapers for others. Simple, low-maintenance.

**Estimated timeline**: 1 week.

### Job Posting Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Computrabajo Venezuela | Job postings with titles, locations, some salary data | Public listings | Dominant LatAm job board |
| Computrabajo Colombia | Same for Colombia | Public listings | Validation market |
| LinkedIn (public postings) | Professional job postings | Public search results | Skews toward formal/professional roles |
| elempleo.com | Colombian job postings | Public listings | Major Colombian platform |
| Facebook Groups | Informal job postings, especially for Venezuela | Public groups | Enormous volume of informal labor market activity |

**Technical requirements**: Scraping + NLP for extracting structured data (job title, location, salary when listed, skills required) from unstructured postings.

**Estimated timeline**: 3-4 weeks for initial collection, ongoing classification refinement.

### Satellite Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| VIIRS Nighttime Lights (NASA/NOAA) | Nighttime light intensity by geography | Free, public | Monthly composites. Proven proxy for economic activity (Henderson et al., 2012). |
| Sentinel-2 (ESA) | Daytime satellite imagery | Free, public | 10m resolution, can detect construction, agriculture, commercial activity |
| Google Earth Engine | Processed satellite data | Free for research | Platform for analyzing satellite time series |

**Technical requirements**: Satellite data processing pipeline (Google Earth Engine or local processing), geographic mapping to Venezuelan municipalities/states.

**Estimated timeline**: 2-3 weeks for initial pipeline, monthly updates automated.

### Rental / Real Estate Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| MercadoLibre Inmuebles Venezuela | Rental and sale listings with prices | Public listings | Prices in USD common |
| FincaRaiz (Colombia) | Colombian rental and sale listings | Public listings | Major Colombian real estate platform |
| Metrocuadrado (Colombia) | Colombian real estate | Public listings | Owned by El Tiempo media group |
| Facebook Marketplace | Rental listings, especially informal | Public | Significant volume in Venezuela |

**Technical requirements**: Same scraping infrastructure as price data, with real estate-specific fields (location, size, price, currency).

---

## Tier 2: Requires Light Partnership or Registration (Months 1-3)

### Delivery App Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Yummy (Venezuela) | Restaurant and grocery prices, order volumes (if partnered) | Prices visible in app; volumes require partnership | Major Venezuelan delivery platform |
| PedidosYa | Restaurant prices across LatAm | Prices visible in app | Owned by Delivery Hero |
| Rappi (Colombia) | Restaurant and grocery prices | Prices visible in app | Dominant Colombian delivery platform |

**Approach**: Start by scraping visible menu prices (Tier 1 difficulty). Approach for volume data partnership if initial price data proves valuable.

### Central Bank Published Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| BCV statistical publications | Monetary aggregates, banking system data, official exchange rates | Published on BCV website, sometimes irregularly | Quality and timeliness vary. Monetary aggregates (M2, reserves) are useful even if GDP/CPI are questioned. |
| Banco de la Republica (Colombia) | Monetary data, financial statistics | Published, accessible, reliable | Strong central bank with good data culture |
| DANE (Colombia) | CPI, employment, retail sales, GDP | Published, accessible | The validation benchmark for econOS Colombia |
| Superintendencia de Bancos (Venezuela) | Banking sector data | Published | Banking system activity as economic signal |

**Approach**: Systematic monitoring and automated collection of whatever these institutions publish. Low effort, potentially high value for cross-validation.

---

## Tier 3: Requires Significant Partnership (Months 3-6)

### Transaction Volume Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Pago Movil aggregate data (BCV) | Transaction volumes and values through the interbank mobile payment system | Unknown -- may require formal request or partnership with BCV or banks | This would be the single most valuable data source for Venezuelan economic activity measurement |
| Nequi / Daviplata aggregates | Colombian mobile payment volumes | Likely requires partnership with Bancolombia / Banco Davivienda | Growing rapidly, could be transformative |
| Redeban / Credibanco (Colombia) | Card network transaction volumes | Requires partnership | Colombian card networks |

**Approach**: The proof-of-concept should demonstrate value WITHOUT transaction data first. Once the system is credible, approach banks and payment networks with: "We've built this with public data. With your aggregate data (anonymized, no individual information), we could make it X times better. Here's how."

### Remittance Volume Data

| Source | What it provides | Accessibility | Notes |
|--------|-----------------|---------------|-------|
| Western Union / Remitly | Formal remittance volumes to Venezuela | Likely requires partnership | Published aggregate data may be available through central bank or industry reports |
| World Bank remittance data | Country-level annual estimates | Published, free | Too infrequent for real-time tracking, but useful as benchmark |
| BCV balance of payments data | Official remittance receipts | Published, irregular | May undercount informal channels significantly |

---

## Tier 4: Aspirational (6+ Months)

### Electricity Consumption

CORPOELEC (Venezuela's state electricity company) data would be a powerful physical-world economic signal, but accessibility is unknown and the institution is poorly managed. Satellite thermal data may be an alternative proxy.

### Tax Revenue Data

SENIAT (Venezuela) and DIAN (Colombia) tax collection data would be a direct economic activity signal. Likely requires government partnership or legislative access -- a long-term goal, not a Phase 1 item.

### Telecom / Mobile Data

CONATEL (Venezuela) and CRC (Colombia) telecom data -- mobile phone activity, data usage, geographic patterns -- would provide population and activity signals. Requires regulatory or operator partnership.

---

## The Acquisition Sequence

```
Week 1-2:    Exchange rates (Binance API, Monitor Dolar)
Week 2-4:    Web-scraped prices (MercadoLibre, pharmacies, supermarkets)
Week 3-5:    Job postings (Computrabajo, LinkedIn, Facebook)
Week 4-6:    Satellite nighttime lights (VIIRS pipeline)
Week 5-8:    Rental/real estate listings
Week 6-10:   Delivery app prices (scraping visible menus)
Month 2-3:   Central bank / DANE published data integration
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
