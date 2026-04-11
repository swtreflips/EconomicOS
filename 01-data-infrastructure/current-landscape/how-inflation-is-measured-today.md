# How Inflation Is Measured Today

## Introduction

Inflation measurement in developed economies is a slow, resource-intensive process with structural lags that frustrate policymakers and market participants. In developing and crisis-hit economies, the problem is not merely lag -- it is total collapse. The most extreme modern cases involve central banks that stopped publishing inflation data entirely during hyperinflationary spirals that destroyed currencies and the savings of millions of people. For years, citizens of these crisis economies had no official measure of how fast their money was losing value, even as prices doubled every few weeks.

This document examines inflation measurement through the lens of the economies where econOS is designed to deploy: crisis economies with collapsed statistical infrastructure and middle-income developing countries with functional but imperfect systems. It then provides a condensed reference on the US system (BLS CPI, PCE), surveys the directly relevant prior art of the Billion Prices Project in developing economies, and maps the modern data sources available for real-time price tracking. The argument is simple: if there is any place on earth where real-time, independent, transparent price measurement is not merely an improvement but essential infrastructure, it is a country that went years without official price data while experiencing extreme hyperinflation.

---

## 1. Why Inflation Measurement Matters Even More in Unstable Economies

In the United States, a CPI release that comes in 0.1 percentage points above expectations moves bond markets, generates headlines, and influences Federal Reserve policy. But for most American consumers, the difference between 3.2% and 3.3% annual inflation is imperceptible in daily life. The stakes of inflation measurement are real but largely institutional.

In crisis economies and, to a lesser extent, middle-income developing countries with elevated inflation, the stakes are immediate, personal, and existential.

### 1.1 Purchasing Power Erosion

When inflation runs at 50% per month -- let alone 100% or 200% per month, as has occurred in crisis economies -- wages denominated in the local currency lose half their value before the next paycheck arrives. Workers who are paid biweekly lose a quarter of their purchasing power between payments. Workers paid monthly lose half. The ability to measure this in real time is not an academic exercise; it determines whether a family can plan grocery purchases, whether a business can set prices for the week, whether a worker knows what their labor is actually worth.

### 1.2 Wage Negotiation

In stable economies, wage negotiations reference annual CPI. In hyperinflationary environments, annual figures are meaningless. Workers in a crisis economy need to know whether to demand a 20% raise this week or a 50% raise, because prices are moving that fast. Without reliable, current inflation data, wage negotiations become blind guessing, systematically favoring employers who have more market information than individual workers.

### 1.3 Remittance Value

Crisis economies are often among the largest remittance-receiving countries in their region. When millions of people emigrate during an economic collapse, the diaspora sends money home to family members. The value of those remittances in local purchasing power depends on both the exchange rate and the local inflation rate. A family receiving $100 per month from a relative abroad needs to know what that $100 will buy this week in the capital city or other major cities. When the central bank is not publishing data and the exchange rate is split between an official fiction and a black market reality, the information gap is not an inconvenience -- it determines whether the remittance covers rent and food or falls short.

### 1.4 Business Planning

Businesses in crisis economies that survive hyperinflation do so largely by pricing in US dollars, adjusting prices daily or multiple times per day, and tracking competitor prices obsessively. Small merchants in capital cities develop informal price-tracking networks via WhatsApp groups long before anyone calls it "real-time price infrastructure." They do this because they have to: setting a price based on yesterday's costs could mean selling below replacement cost by the afternoon. The informal systems that emerge are, in essence, primitive versions of what econOS aims to build.

### 1.5 Government Accountability

When a government controls the statistical agency, the absence of inflation data is not a technical failure -- it is a political choice. Central banks in crisis economies have stopped publishing CPI data just as inflation accelerated past triple digits. The data blackout makes it harder for citizens, journalists, and international observers to quantify the scale of the economic catastrophe. Independent inflation measurement in this context is not merely better data; it is a check on power.

---

## 2. Hyperinflation and Measurement Collapse in Crisis Economies

The hyperinflation episodes in developing countries represent some of the most extreme economic crises in modern history, comparable to the Southern Cone crises of the 1980s and early 1990s, and Zimbabwe's 2007-2008 collapse. Understanding how they unfold -- and how measurement fails at every stage -- is the foundation of the case for econOS.

### 2.1 The Trajectory

A typical crisis economy's inflation is already elevated before the collapse begins. Dependence on commodity revenues, combined with massive fiscal spending, price controls, and currency controls, creates persistent inflationary pressure. But the collapse accelerates when commodity prices crash and political instability deepens:

- **Year 0**: Annual inflation ~20% (elevated but manageable by regional standards)
- **Year 1**: ~56% (beginning of acceleration amid political crisis)
- **Year 2**: ~69% (commodity prices collapse)
- **Year 3**: ~181% (central bank stops publishing CPI data)
- **Year 4**: ~274% (estimate, based on legislative and independent sources; no official central bank data)
- **Year 5**: ~862% (estimates vary widely; the IMF may project over 1,000%)
- **Year 6**: This is where estimates diverge dramatically. Legislative estimates may exceed 1,000,000%. Independent economists using PPP-based methods may estimate peak monthly inflation above 200%. The IMF may project hundreds of thousands of percent. Informal single-item price indexes -- tracking the cost of a cup of coffee in the capital city -- show prices doubling roughly every 18-19 days at the worst point.
- **Year 7**: Inflation begins to decelerate from hyperinflationary levels but remains extremely high, in the thousands of percent per year.
- **Years 8-9**: Continued high inflation in the triple to quadruple digits, but the economy increasingly dollarizes, providing a de facto stabilization mechanism.
- **Years 10-12**: Inflation moderates significantly in dollar terms as dollarization becomes entrenched, though local-currency-denominated inflation remains elevated. The central bank may resume publishing data, reporting single-digit monthly rates, though the credibility of these figures remains contested.

### 2.2 The Central Bank Blackout

A central bank's decision to stop publishing CPI data is typically not a sudden event but a gradual withdrawal. Publications become increasingly irregular before ceasing entirely. For approximately three years, citizens may have no official, regularly published consumer price index.

This is not a technical failure. The central bank has the institutional capacity to collect and publish price data. The blackout is a political decision, widely understood as an attempt to obscure the severity of the economic crisis from both domestic and international audiences. The government simultaneously maintains that economic conditions are manageable and blames hardship on external enemies or political opponents.

The consequences of the blackout are profound:

- **No official benchmark for wage adjustment**: The government sets minimum wage increases by decree, without reference to published inflation data. These increases consistently lag actual inflation, eroding real wages.
- **No basis for contract escalation**: Commercial contracts, lease agreements, and supplier terms that reference official CPI have no index to reference.
- **No international comparability**: The IMF, World Bank, and other international institutions are forced to produce their own estimates, which vary widely and carry explicit uncertainty caveats.
- **No accountability metric**: The government cannot be held to a specific inflation number because it is not publishing one.

### 2.3 Legislative Inflation Estimates

When opposition legislators gain power, one of their first economic initiatives is often to produce independent inflation estimates. A legislative finance commission may begin publishing monthly inflation data using its own price collection methodology.

The methodology typically involves collecting prices from a basket of goods and services across several cities. The estimates are produced by economists affiliated with the opposition and published regularly, providing the only domestically produced inflation series during the blackout period.

Limitations of legislative estimates:

- **Perceived political bias**: Because the legislature is controlled by the opposition, the government and its supporters dismiss the estimates as politically motivated. Whether or not the numbers are accurate, their provenance means they cannot serve as a neutral benchmark.
- **Methodological transparency**: The legislature publishes headline numbers but not detailed methodology. The basket composition, geographic coverage, price collection methods, and quality adjustment procedures are not documented to the standard expected of an official statistical agency.
- **Practical limitations**: Collecting prices in a hyperinflationary economy with severe shortages, where many goods are simply unavailable at any price, is extraordinarily difficult. Scarcity means that the "price" of a good that cannot be found on store shelves is effectively infinite, but no price index captures this. Legislative estimates, like any traditional CPI methodology, measure the prices of goods available for purchase, not the full cost of living in an economy with chronic shortages.

Despite these limitations, legislative estimates fill a critical vacuum and are widely cited by international media, the IMF, and academic researchers as the best available domestic source during a blackout.

### 2.4 Steve Hanke's Estimates

Steve Hanke, a professor of applied economics at Johns Hopkins University and a leading scholar of hyperinflation, has produced independent inflation estimates for crisis economies using purchasing power parity (PPP) methodology. His approach is elegant and, crucially, does not depend on any government data from the crisis country.

The method: Hanke uses the parallel (black market) exchange rate between the local currency and the US dollar, combined with the assumption of relative purchasing power parity, to infer the inflation rate. The logic is as follows: if the local currency depreciates by 50% against the dollar on the parallel market in a given month, and US inflation is approximately 0.2% per month, then domestic inflation is approximately 50.2% for that month. This works because, in a hyperinflationary environment, the exchange rate depreciation and the domestic price level move in close correlation -- the currency is collapsing because prices are rising, and prices are rising because the currency is collapsing, in a mutually reinforcing spiral.

Hanke's estimates have been published regularly through the Cato Institute's Troubled Currencies Project and his personal research channels. He has applied this methodology to multiple hyperinflationary episodes, identifying periods when monthly inflation exceeded 50% (the conventional Cagan threshold for hyperinflation).

Strengths of Hanke's approach:

- **Independence from crisis-country government data**: The only domestic input is the parallel exchange rate, which is determined by market forces, not government statistics.
- **High-frequency potential**: Exchange rates could be observed daily, enabling daily or weekly inflation estimates rather than monthly snapshots.
- **Consistent methodology**: The PPP approach had been validated against official statistics in numerous other hyperinflationary episodes (Zimbabwe, Yugoslavia, etc.).

Limitations:

- **PPP is an approximation**: Relative PPP holds well in the long run and during extreme inflation, but can diverge from actual price-level changes in the short run, especially when capital controls, import restrictions, and price controls distort the relationship between exchange rates and domestic prices.
- **Parallel exchange rate data quality**: The "parallel rate" is not a single, transparent market price. It is observed through informal broker networks, social media posts, rate-tracking websites, and anecdotal reports. The rate can vary by city, by transaction size, and by the relationship between buyer and seller. Independent rate trackers have been accused by governments of manipulating rates for political purposes. While such accusations are self-serving, the lack of a centralized, transparent parallel exchange market introduces genuine measurement uncertainty.
- **Does not capture relative price changes**: An exchange-rate-based approach measures the overall price level but cannot identify which goods or services are driving inflation. It tells you that prices, on average, doubled this month, but not whether food prices tripled while transportation costs merely rose 50%.

### 2.5 The Billion Prices Project in Crisis Economies

The Billion Prices Project (BPP), founded by Alberto Cavallo and Roberto Rigobon at MIT, collected daily online prices from retailers in over 60 countries, including crisis economies. This made the BPP one of the few sources of systematic, automated, goods-level price data during economic crises.

The BPP scraped prices from online retailers and e-commerce platforms in developing countries, producing daily price indexes for goods sold online. This data was incorporated into the PriceStats commercial product (later acquired by State Street Global Markets), which provided daily inflation indicators to institutional clients.

The BPP's crisis-economy data demonstrated several important points:

- **Automated collection was feasible even during crisis**: Despite economic turmoil, retailers in crisis economies maintained online presences, and prices were posted and scrapable.
- **Daily frequency captured the speed of price changes**: In a hyperinflationary environment where prices change daily or multiple times per day, monthly data is nearly useless. The BPP's daily scraping captured the dynamics that traditional CPI methods cannot.
- **Goods prices tracked exchange rate movements**: The BPP data showed strong correlation between the parallel exchange rate and online goods prices, validating the PPP-based approaches used by Hanke and others.

However, the BPP also faced challenges specific to crisis economies:

- **Severe goods scarcity**: Many products were simply unavailable, both in physical stores and online. Price controls and rationing meant that the "official" price of a good might exist on paper, but the good itself could not be purchased at that price. Online retailers that did have inventory often charged prices well above controlled levels.
- **Limited internet penetration**: During crises, internet connectivity deteriorates along with other infrastructure. The share of commerce conducted online in crisis economies is lower than in more stable economies, raising questions about how representative online prices are of the broader economy.
- **Website instability**: Frequent power outages, server issues, and the general deterioration of technical infrastructure mean that scraping websites in crisis economies is less reliable than scraping US or European retailers.

Despite these limitations, the BPP's work in crisis economies is the single most relevant piece of prior art for econOS. It proved that automated, daily price collection in a crisis economy is not only possible but urgently needed.

---

## 3. The Multi-Currency Problem

One of the most analytically challenging aspects of inflation measurement in crisis economies -- and a problem that econOS must solve -- is the coexistence of multiple currencies and multiple exchange rates.

### 3.1 Currency Collapse and Serial Redenomination

In the most severe hyperinflationary episodes, the local currency may be redenominated multiple times, each time removing several zeros from the denomination. Over the course of a decade, the total number of zeros removed can reach double digits, meaning one unit of the new currency is equivalent to trillions of the original. These redenominations are cosmetic -- they do not change the underlying value of the currency -- but they complicate any longitudinal analysis of local-currency-denominated prices.

### 3.2 Multiple Exchange Rates

During crisis periods, governments often operate systems of multiple official exchange rates alongside a much higher parallel (black market) rate:

- **Primary official rate**: Reserved for essential imports (food, medicine). Typically fixed at a rate that grossly overvalues the local currency. For example, the official rate may be set at a fraction of the parallel rate.
- **Secondary official rates**: Determined through periodic auctions, available for a broader range of imports. Higher than the primary rate but still well below the parallel rate. The names and structures of these mechanisms frequently change.
- **Parallel (black market) rate**: The rate at which local currency actually trades for dollars in informal markets. This is the rate that matters for most citizens and businesses. It is tracked by independent rate-tracking websites run by diaspora communities, social media accounts, and apps.

The spread between official and parallel rates can be enormous. At its peak, the official rate can overvalue the local currency by a factor of 100x or more relative to the parallel rate. This means that:

- A product imported at the official rate could be sold domestically at the parallel-rate-equivalent price, generating enormous rents for anyone with access to official-rate dollars (which were allocated by the government, creating a massive corruption vector).
- "Inflation" measured using official-rate-adjusted import prices was radically different from inflation measured using parallel-rate-adjusted prices.
- The "real" price of any imported good depended entirely on which exchange rate was used to acquire the dollars to pay for it.

### 3.3 De Facto Dollarization

In crisis economies, informal dollarization typically begins as a survival mechanism, not a policy decision -- governments resist acknowledging it for years. As the local currency becomes functionally worthless, businesses and individuals increasingly price, transact, and save in US dollars.

Once dollarization becomes pervasive:

- In major cities, an estimated 60-70% of transactions may be conducted in US dollars.
- Retail stores post prices in dollars (sometimes alongside local-currency prices at the day's exchange rate).
- Wages in the private sector were increasingly negotiated and paid in dollars or dollar-equivalent amounts.
- The government itself began allowing dollar-denominated transactions and eventually began accepting tax payments in dollars.

This creates a fundamental measurement question: what does "inflation" mean in a dollarizing economy?

- **Local-currency-denominated inflation**: Prices in local currency continue to rise rapidly, driven by ongoing monetary expansion by the central bank. But if a shrinking share of actual transactions occurs in local currency, this number becomes less meaningful for understanding lived economic experience.
- **Dollar-denominated inflation**: Prices quoted in dollars are far more stable, but they are not immune to change. Local dollar prices reflect both US inflation (transmitted through the global dollar-denominated goods market) and local supply-and-demand conditions. A can of imported tuna priced at $1.50 in a capital city in one year might cost $2.00 two years later -- partly because of US inflation, partly because of local cost structures (rent, labor, transportation), and partly because of changes in local purchasing power.
- **Effective inflation for bimonetary consumers**: Most people in dollarizing economies operate in both currencies simultaneously. They might receive a portion of their income in local currency (especially public-sector workers, whose salaries are set by the government in local currency) and a portion in dollars (through informal employment, remittances, or tips). Their "true" inflation rate depends on the share of spending in each currency and the inflation rate in each denomination.

For econOS, this means that a single inflation number is insufficient. The system must track prices in both currencies, record which currency each transaction or price quote is denominated in, and provide inflation estimates separately for local-currency-denominated and dollar-denominated spending, as well as a blended estimate based on the actual currency mix of transactions.

### 3.4 The Exchange Rate as a Price Signal

In the multi-currency environment, the exchange rate itself becomes one of the most important price signals in the economy. The daily parallel exchange rate effectively sets the local-currency price of all dollar-denominated goods. A merchant who sells a product for $5 and needs to restock will convert the dollar price to local currency using the current parallel rate. If the rate moves 10% in a week, all local-currency prices move with it, creating a direct transmission mechanism from the exchange rate to the consumer price level.

This means that exchange rate tracking is not separate from price tracking -- it is a core component. Independent rate-tracking services, which track the parallel rate in real time through informal market surveys, are performing a function that is directly equivalent to price measurement. For econOS, integrating exchange rate data with product price data is not optional; it is the only way to construct a meaningful price index in a dollarizing economy.

---

## 4. How Inflation Is Measured in Middle-Income Developing Countries

Middle-income developing countries represent a very different challenge from crisis economies. Their statistical infrastructure is functional, their central banks are independent and credible, and their inflation rates, while sometimes elevated, have remained within the range that conventional measurement methods can handle. But functional does not mean perfect, and the gaps in these systems are relevant for econOS.

### 4.1 The Standard National Statistical Agency CPI

**Produced by**: The national statistics office (e.g., DANE in Colombia, IBGE in Brazil, INEGI in Mexico, MOSPI in India).

**Methodology**: A typical middle-income country's statistical agency produces a monthly CPI based on price collection across dozens of cities and metropolitan areas, using a basket of several hundred items grouped into divisions following the international COICOP (Classification of Individual Consumption According to Purpose) classification.

**Expenditure weights** are derived from periodic national household budget surveys, typically conducted every 5-10 years with tens of thousands of households surveyed. The major categories and approximate weights follow a common pattern across developing countries:

1. Food and non-alcoholic beverages (~15-30%, higher in lower-income countries)
2. Housing, water, electricity, gas (~25-35% -- typically the largest component)
3. Clothing and footwear (~3-5%)
4. Transportation (~10-15%)
5. Restaurants and hotels (~5-10%)
6. Health (~2-5%)
7. Recreation and culture (~3-5%)
8. Education (~2-5%)
9. Furnishings and household maintenance (~3-5%)
10. Information and communication (~3-5%)
11. Alcoholic beverages and tobacco (~1-3%)
12. Personal care, insurance, and financial services (~5-10%)

**Price collection**: Statistical agencies collect hundreds of thousands to millions of price quotes per month from establishments across major cities. Data collection is performed by field staff who visit markets, supermarkets, stores, and service providers.

**Release schedule**: Better-performing agencies publish CPI within 5-10 business days of the reference month, making them among the faster-releasing statistical agencies in their regions.

### 4.2 Strengths of Functional Statistical Systems

- **Institutional credibility**: Well-functioning statistical agencies operate with reasonable independence and have track records of methodological transparency. Inflation targeting frameworks (managed by independent central banks) depend on credible CPI data, and institutional incentives generally support accuracy.
- **Geographic coverage**: Dozens of cities provides substantial coverage of urban areas. Many agencies publish city-level CPI data, allowing regional analysis.
- **COICOP alignment**: Using the international classification standard enables cross-country comparison.
- **Regular publication**: Monthly release on a predictable schedule with a short lag.

### 4.3 Gaps and Limitations

Despite their relative strength, CPI systems in middle-income developing countries have significant gaps that create an opportunity for supplementary real-time measurement:

**Informal commerce**: Many developing countries have large informal economies -- estimated at 40-60%+ of employment. Street vendors, neighborhood corner stores, and open-air markets are where many lower-income consumers do much of their shopping. These informal channels are underrepresented in CPI price collection, which tends to focus on formal retail establishments. Prices in informal markets may diverge from formal retail prices, especially for food and household goods.

**Rural coverage**: Urban-focused sampling covers major cities but not rural areas, where 20-40% of the population may live. Rural prices -- particularly for food, transportation, and energy -- can differ significantly from urban prices due to transportation costs, market access, and different consumption patterns.

**Regional price dispersion**: Many developing countries are geographically diverse, with distinct regions having different cost structures. A single national CPI, even with city-level breakdowns, may not capture the price experience of consumers in smaller towns or regions distant from major urban centers.

**Frequency**: Monthly data, with a 5-10 day lag, is good by international standards but still means that intra-month price dynamics are invisible. For food prices in particular, which can vary significantly within a month due to supply disruptions (strikes, transport blockades, weather events affecting agriculture), monthly averages smooth out volatility that affects household budgets in real time.

**Demographic shifts**: Large-scale migration flows -- whether internal rural-to-urban migration or cross-border refugee and economic migration -- affect local labor markets, housing markets, and consumer demand in destination cities. CPI baskets based on household surveys conducted years earlier do not fully reflect these demographic shifts.

### 4.4 Central Bank Supplementary Measures

Central banks in middle-income developing countries typically publish several supplementary inflation measures:

- **Core inflation**: Excludes food and regulated prices. Used by the central bank for policy analysis.
- **Food inflation**: Reported separately given its high weight and volatility.
- **Regulated prices inflation**: Covers utilities, fuel, and other price-controlled items.
- **Producer Price Index (PPI)**: Published monthly, covering prices at the producer level.

These provide useful analytical decomposition but do not address the fundamental frequency and coverage limitations.

---

## 5. Reference: How It Is Done in the United States

The US system is included here for reference, as it represents the gold standard of inflation measurement and the benchmark against which alternative approaches are evaluated. This section is condensed; the full US methodology is documented extensively elsewhere.

### 5.1 Consumer Price Index (CPI)

**Produced by**: Bureau of Labor Statistics (BLS), U.S. Department of Labor.

**Methodology**: The BLS collects approximately 80,000 price quotes per month from about 23,000 retail and service establishments in 75 urban areas. Prices are collected by trained field representatives who physically visit stores, call businesses, or collect prices online. The CPI basket contains approximately 211 item categories, weighted by the Consumer Expenditure Survey (CE), with weights updated every two years.

**Two versions**: CPI-U (all urban consumers, ~93% of population) and CPI-W (urban wage earners and clerical workers, ~29% of population, used for Social Security COLAs).

**Index type**: Modified Laspeyres (fixed-weight). Captures within-category substitution via geometric means but does not capture between-category substitution until weights are updated.

**Release**: 10-13 business days after the reference month. Not revised on a month-to-month basis, which is a significant advantage for real-time analysis.

### 5.2 Personal Consumption Expenditures Price Index (PCE)

**Produced by**: Bureau of Economic Analysis (BEA), U.S. Department of Commerce.

**Why it matters**: The Federal Reserve's preferred inflation measure, used to define the 2% inflation target.

**Key differences from CPI**: Chain-weighted (Fisher Ideal index), so it captures substitution effects continuously. Broader scope (includes third-party payments like employer health insurance and Medicare). Healthcare weight ~22% vs. CPI's ~8.5%. Shelter weight ~17% vs. CPI's ~36%.

**Release**: ~30 days after the reference month. Subject to revision.

**Empirical relationship**: PCE inflation typically runs ~0.3 percentage points below CPI inflation due to substitution effects and healthcare treatment differences.

### 5.3 The Shelter Lag Problem

The most consequential measurement issue in US CPI is the shelter component, which accounts for ~36% of the index. Because CPI measures rents on all outstanding leases (most of which are 12-month contracts), the shelter component is effectively a 12-month moving average of rent changes. This creates a 6-12 month lag between changes in market rents and their reflection in CPI.

This lag was dramatically demonstrated in 2022-2023: private rent indexes (Zillow, Apartment List) showed market rent growth decelerating sharply by late 2022 and going negative in some markets, but CPI shelter continued to accelerate, peaking above 8% year-over-year in March 2023. Because shelter is 36% of CPI, this single lag kept headline and core CPI elevated for over a year after market conditions had already changed, directly influencing Federal Reserve interest rate decisions.

The BLS is developing a New Tenant Rent Index (NTRI) to address this, but it remains experimental.

### 5.4 Summary Comparison

| Dimension | US (BLS CPI) | Middle-Income Developing Country | Crisis Economy |
|---|---|---|---|
| Institutional credibility | High | Moderate-high | Low (data blackouts common) |
| Frequency | Monthly | Monthly | Irregular / non-existent for years |
| Lag | ~13 days | ~5-10 business days | Months to years, when published at all |
| Geographic coverage | 75 urban areas | Dozens of cities | Limited (when operational) |
| Basket items | ~211 categories | ~200-500 items | Unknown during blackout |
| Weight update frequency | Every 2 years | ~Every 5-10 years | Unknown |
| Informal economy coverage | Minimal | Partial | Minimal |
| Crisis resilience | Not tested at crisis scale | Adequate for normal conditions | Total failure |

---

## 6. The Billion Prices Project in Developing Economies

The Billion Prices Project (BPP), launched in 2008 by MIT economists Alberto Cavallo and Roberto Rigobon, is the single most important piece of prior art for the econOS price measurement system. Its work in developing economies is directly relevant.

### 6.1 Methodology

The BPP used automated web scraping to collect prices from online retailers across more than 60 countries on a daily basis. For each retailer, the system recorded individual product prices daily, tracked changes over time, and aggregated the data into country-level price indexes. The approach was fully automated after initial setup: no field representatives, no phone calls, no physical visits.

The aggregation methodology used standard index number techniques, weighted by product category to approximate the composition of official CPI baskets. This allowed direct comparison with official statistics.

### 6.2 Coverage in Developing Economies

The BPP covered over 60 countries, with particular significance in cases where official statistics were compromised:

**Countries with manipulated statistics**: The BPP's data became internationally prominent in countries where national statistical agencies were accused of manipulating CPI data under political pressure. In Argentina (2007-2015), private estimates of inflation consistently ran 2-3x the official figures. The BPP's data showed inflation rates that aligned with private estimates and diverged sharply from official data, providing independent, methodology-transparent confirmation that the official statistics were unreliable.

This experience is a direct precedent for any crisis economy where a government compromises the credibility of its statistical agency: independent, automated price measurement fills the gap. The BPP demonstrated that web-scraped data could serve as a check on government statistics in exactly the political circumstances where such a check is most needed.

**Crisis economies**: The BPP collected prices from online retailers in countries experiencing hyperinflation and economic collapse. The data confirmed the general trajectory of extreme inflation and showed strong correlation with exchange-rate-based estimates. Coverage was limited by the challenges of crisis markets (scarcity, infrastructure degradation, limited e-commerce), but the data that was collected provided one of the few automated, granular price records during these episodes.

**Large developing economies**: The BPP's data from countries like Brazil covered large and relatively well-functioning e-commerce markets. These provided useful benchmarks for how well web-scraped indexes track official CPI in developing economies with moderate inflation. The correlation was high, similar to the US experience.

### 6.3 Key Findings Relevant to econOS

Cavallo and Rigobon's research, published in numerous academic papers, yielded several findings directly relevant to econOS:

1. **Web-scraped indexes track official CPI closely for goods categories**: In countries with credible statistical agencies, the BPP daily index tracked the goods component of official CPI with correlations above 0.9. This validates automated collection as a supplementary measurement tool.

2. **Divergence signals statistical manipulation**: When web-scraped indexes diverge from official statistics, it tends to indicate a problem with the official statistics, not the scraped data. The Argentine case is the clearest example.

3. **Price stickiness varies dramatically across countries**: In the United States, the median online price changes approximately every 3-4 months. In high-inflation Latin American economies, prices change much more frequently -- in some cases daily. This means that daily scraping frequency is not only feasible but necessary in high-inflation environments.

4. **Scraped data captures price dynamics invisible to monthly indexes**: The BPP documented phenomena like synchronized price changes (many firms adjusting prices on the same day, often following exchange rate movements), temporary price spikes during supply disruptions, and rapid pass-through of commodity price changes -- none of which are visible in monthly CPI data.

5. **The approach scales**: The BPP eventually covered over 60 countries with a relatively small team, demonstrating that the marginal cost of adding a new country or retailer is low once the infrastructure is built.

### 6.4 From BPP to PriceStats

The BPP methodology was commercialized through PriceStats, co-founded by Cavallo and Rigobon, which was later acquired by State Street Global Markets. PriceStats provides daily inflation indicators to institutional clients -- central banks, sovereign wealth funds, and investment firms. The commercial success of PriceStats demonstrates that there is institutional demand for higher-frequency inflation data and willingness to pay for it.

However, PriceStats is a proprietary, subscription-based service aimed at sophisticated institutional clients. Its data is not publicly available. This means that the populations who most need real-time inflation data -- families in crisis economies, small business owners in developing countries, NGOs, journalists -- cannot access it. The econOS opportunity is to build equivalent (or better) infrastructure as a public good.

---

## 7. Modern Data Sources for Real-Time Price Tracking in Developing Economies

The BPP proved the concept a decade ago. Since then, digital economies in developing countries have expanded significantly, creating new and richer data sources for real-time price measurement.

### 7.1 E-Commerce and Delivery Apps

**Regional e-commerce platforms**: Dominant e-commerce platforms in developing regions (e.g., MercadoLibre in Latin America, Jumia in Africa, Flipkart in India, Shopee in Southeast Asia) contain structured price data for millions of products. In dollarized or multi-currency economies, prices are often listed in both local currency and dollars. Scraping these platforms provides broad product coverage across categories.

**Delivery super-apps**: Delivery platforms covering groceries, restaurants, pharmacies, and general retail have proliferated across developing countries. Their structured product catalogs with prices updated in real time make them excellent sources for food, household goods, and restaurant prices.

**Country-specific delivery apps**: In many crisis economies, local delivery apps emerged during periods of disruption, providing restaurant and grocery delivery with real-time pricing -- often in dollars or other stable currencies.

**Pharmacy and retail chain websites**: Major pharmacy and retail chains with online platforms provide price data for health and personal care products.

**Supermarket chains with online platforms**: Major supermarket and retail chains increasingly offer online grocery platforms. Their websites and apps provide structured, scrapable price data for thousands of food and household products.

### 7.2 Messaging-Based Price Networks

One of the most distinctive and under-recognized data sources in crisis economies is the informal price-reporting network organized through WhatsApp, Telegram, and similar messaging platforms. During economic crises, citizens organize these groups spontaneously. They serve multiple functions:

- **Price sharing**: Members post photos of price tags, receipts, and product listings, sharing current prices in their city or neighborhood.
- **Exchange rate tracking**: Groups share the day's parallel exchange rate as it fluctuates.
- **Scarcity alerts**: Members report which stores have which products in stock -- critical during periods of severe shortages.
- **Price comparison**: The groups function as informal, crowd-sourced price comparison tools.

These groups typically operate at the city level and can have thousands of members. The data they contain is unstructured (photos, text messages, voice notes) but represents genuine, real-time price observations from actual consumers.

For econOS, these informal networks represent both a data source (with appropriate NLP and image processing to extract structured price data from unstructured messages) and a distribution channel (the user community already exists and is habituated to sharing and consuming price information through mobile messaging).

### 7.3 Social Media Price Reporting

Twitter (X), Instagram, and TikTok have become channels for price reporting in developing and crisis economies, particularly for high-visibility items:

- **Basic basket tracking**: Economists, journalists, and civil society organizations track and publish the cost of basic goods baskets (sufficient for a family) on social media. Independent labor or consumer organizations often publish monthly food basket cost figures that are widely cited when official data is absent or contested.
- **Single-item indexes**: Informal indexes tracking the cost of specific items (a cup of coffee, a lunch, a specific meal) as intuitive proxies for overall price changes. Media outlets have sometimes formalized these into named indexes (e.g., Bloomberg's "Cafe Con Leche Index").
- **Supermarket price reports**: Shoppers post photos of price tags from supermarkets, creating a crowdsourced record of price changes.

### 7.4 Currency Exchange Data

In economies with parallel exchange rates, several types of services track rates in real time or near-real time:

- **Independent rate aggregators**: Websites and apps that aggregate exchange rate data from multiple sources and publish daily updates, often multiple times per day.
- **Diaspora-operated rate trackers**: Services operated by expatriate communities that track parallel or informal market rates. These often become de facto reference rates, despite their methodologies sometimes being opaque.
- **P2P exchange platforms**: Peer-to-peer cryptocurrency exchanges provide another exchange rate signal. The USDT/local-currency rate on P2P platforms reflects real market conditions and is available in real time through platform APIs.
- **Border exchange operations**: In countries with porous borders, exchange operations in border cities provide real-time signals about the true market value of the local currency.

For inflation measurement purposes, the exchange rate data is critical because, as discussed in Section 3.4, the exchange rate is the primary transmission mechanism for price changes in dollarizing economies. A real-time exchange rate feed, combined with real-time product price data, enables the construction of both dollar-denominated and local-currency-denominated price indexes.

### 7.5 Government and Institutional Data (Where Available)

Despite the limitations discussed above, some official data does exist and should be incorporated:

- **Central bank data**: Even in crisis economies, central banks may resume publishing economic data intermittently. When published, official CPI data should be included as one input, even if its credibility is contested -- comparing it against independent measures is itself informative.
- **National statistical agency data**: In countries with functional statistical agencies (as discussed in Section 4), official CPI is a credible monthly benchmark. econOS should track it and report the differential between official monthly figures and econOS daily/weekly estimates.
- **IMF estimates**: The IMF produces annual inflation estimates for countries experiencing crises. These are based on the best available data and are useful as a cross-check, even though their annual frequency is too low for real-time use.
- **World Bank / regional development bank data**: Provide supplementary economic context (GDP estimates, poverty rates, remittance flows) that inform the interpretation of price data.

---

## 8. The econOS Opportunity

The experience of crisis economies -- where statistical agencies go dark during the worst inflation episodes in modern history -- is not merely an example of why real-time price measurement would be useful. It is the definitive case for why it is essential.

### 8.1 The Gap

In crisis economies, tens of millions of people have lived through extreme inflation without official price data. The information that did exist was fragmented across:

- Political opposition bodies producing estimates of contested credibility
- International academics inferring inflation from exchange rate data
- Academic research projects scraping online retailers
- Informal messaging groups where shoppers shared photos of price tags
- Websites run by expatriates tracking black market exchange rates

Each of these sources was partial, imperfect, and either inaccessible to ordinary citizens or lacking the structure and credibility to serve as a reliable economic benchmark. Meanwhile, the actual price data -- the prices displayed in every supermarket, pharmacy, and corner store, the exchange rates negotiated in every informal exchange and P2P platform transaction -- existed in real time, observed by millions of people, but never systematically collected, aggregated, or published.

This is the gap. Not a marginal improvement in data quality. Not a faster release schedule for an existing index. A total absence of one of the most fundamental pieces of economic information in countries experiencing extreme macroeconomic events.

### 8.2 What econOS Would Provide

In any developing or crisis economy, econOS would build the following:

**A multi-currency price index**: Daily (or higher-frequency) tracking of prices in both local currency and US dollars, with transparent methodology, covering:
- Food and household goods (sourced from online retailers, delivery apps, crowdsourced reports)
- Medicines and personal care (sourced from pharmacy chains with online platforms and health-focused apps)
- Transportation (fuel prices, informal taxi and bus fares tracked through surveys and app data)
- Housing (rental listings tracked from real estate platforms, classified sites, and social media postings)
- Services (sourced from service marketplace platforms and delivery apps)

**A real-time exchange rate feed**: Aggregated from multiple sources (independent rate trackers, P2P exchange platforms, bank rates, border exchange operations) with transparent weighting methodology. Published with sufficient frequency to serve as a pricing reference for merchants and consumers.

**A basic-basket cost tracker**: The cost of a basic food and goods basket, updated daily rather than monthly, broken down by city and region. This is the most immediately impactful metric for ordinary citizens -- not an abstract price index, but a concrete answer to the question: "How much does it cost to feed a family this week?"

**Historical archive**: A systematic, machine-readable archive of price data that does not exist anywhere today. When central banks stop publishing, that data is lost. When political bodies publish estimates, they are released as press statements, not structured datasets. When academics publish estimates, they are in spreadsheets and op-eds. econOS would maintain a structured, version-controlled, publicly accessible archive of price data that survives changes in government, institutional politics, and individual researchers' careers.

### 8.3 Where to Start: Structural Criteria

The argument for starting econOS in a specific country is not humanitarian (though the humanitarian dimension is real). It is structural. The ideal first implementation has these characteristics:

1. **Maximum information gap**: The wider the gap between the need for price data and the availability of official statistics, the lower the bar for adding value. econOS does not have to be better than the US BLS -- it just has to exist. The bar for adding value is as low as it can possibly be.

2. **Pre-existing demand**: In countries where citizens already seek out and share price information obsessively -- through messaging price groups, exchange rate checking habits, social media basket-cost posts -- there is unsatisfied demand for exactly the product econOS aims to build. The user base does not need to be created; it needs to be served.

3. **Dollarization simplifies comparison**: In economies where prices are quoted in US dollars (whether formally or informally), cross-country price comparison is straightforward. The relative price of goods is directly observable across borders.

4. **Adjacent validation market**: Starting in a crisis economy that borders a country with functional statistics provides a natural validation benchmark. Cross-border price differentials, remittance purchasing power, and migration-driven demand effects can all be tracked.

5. **Proof of concept for expansion**: If econOS can produce credible, real-time price data in the hardest possible case -- with the weakest infrastructure, the most volatile prices, and the least cooperative government -- then scaling to other developing economies becomes a straightforward matter of adding data sources and adjusting methodology.

### 8.4 Comparison: econOS vs. Current State

| Dimension | Current State (Crisis Economy) | Current State (Middle-Income Developing) | econOS Target |
|---|---|---|---|
| Frequency | Irregular central bank releases | Monthly (national statistics agency) | Daily or higher |
| Currency coverage | Local currency only (official) | Local currency only | Multi-currency (local + USD) |
| Lag | Months to years | ~5-10 business days | 1-3 days |
| Geographic coverage | Limited, when published | Dozens of cities | City and neighborhood level |
| Informal commerce | Not captured | Partially captured | Crowdsourced + delivery app data |
| Exchange rate integration | Not integrated with CPI | N/A (single exchange rate) | Integrated multi-source feed |
| Basic basket cost | Monthly (independent orgs) | Monthly (statistical agency) | Daily, by city |
| Public access | Limited to no access | Published but complex | Open, machine-readable, API-accessible |
| Crisis resilience | Total failure | Untested at crisis scale | Designed for instability |
| Historical archive | Destroyed/unavailable | Available but limited | Structured, version-controlled, permanent |

### 8.5 The Argument in One Paragraph

Crisis economies have gone years without official inflation data during the worst hyperinflation episodes in modern history. Millions of people made life-altering decisions -- whether to stay or emigrate, whether to save or spend immediately, how much to demand in wages, how to price their goods, how much to send home in remittances -- without access to the most basic economic information about the value of their currency. The data to measure prices existed in real time, scattered across millions of individual transactions, price tags, exchange rate quotes, and online listings. No system collected it, aggregated it, or made it available. econOS is that system. It is not a theoretical improvement to an adequate baseline. In crisis economies, it is the baseline itself -- the first layer of economic information infrastructure in countries where that infrastructure collapsed. If econOS cannot justify its existence in the hardest cases, it cannot justify its existence anywhere. And if it can work there -- in the most volatile, most data-starved environments imaginable -- it can work anywhere.

---

## 9. Summary

Inflation measurement is a solved problem in stable, well-governed economies -- imperfectly solved, with structural lags and methodological compromises, but solved in the sense that citizens, businesses, and policymakers have access to regular, reasonably credible price data. In crisis economies, it is an unsolved problem. The measurement infrastructure collapsed precisely when it was most needed, and the informal alternatives that emerged -- however resourceful -- are fragmented, unstructured, and inaccessible to most of the population.

Middle-income developing countries occupy a middle ground: their national CPI systems are functional and credible, but they miss the informal economy, lack real-time frequency, and were not designed for the cross-border, multi-currency complexity introduced by mass migration and dollarization.

The Billion Prices Project proved over a decade ago that automated, daily price collection can produce indexes that track official CPI closely in normal times and provide superior information in crisis times. The technology has only improved since then. Digital economies across the developing world -- delivery apps, e-commerce platforms, mobile payment systems, messaging-based price networks -- provide richer data than the BPP ever had access to.

What is missing is the infrastructure to collect this data systematically, aggregate it transparently, and publish it as a public good. That is what econOS builds. The place to start is the place where the need is greatest, the prior art is most relevant, and the argument is most compelling -- whichever developing or crisis economy meets those structural criteria.
