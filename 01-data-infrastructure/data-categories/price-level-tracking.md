# Real-Time Price Level Tracking: Venezuela and Colombia

## Why Prices Are the Most Fundamental Economic Signal

Friedrich Hayek's 1945 essay "The Use of Knowledge in Society" made an argument that has never been improved upon: the central problem of economics is not optimization of a known production function but the utilization of knowledge dispersed across millions of individuals. No single agent -- no planner, no firm, no algorithm -- possesses even a fraction of the information needed to coordinate a complex economy. Markets solve this problem through the price system. Prices encode information about relative scarcity into a single number that anyone can observe and respond to, without needing to understand the underlying conditions that produced that number.

A tin miner in Bolivia does not need to know that a semiconductor fab in Taiwan increased its demand for tin. He only needs to see that the price of tin rose. That price signal tells him to increase production. Simultaneously, it tells manufacturers to economize on tin, tells recyclers to recover more, and tells prospectors to look for new deposits. The coordination happens without any coordinator. The information transmits without anyone sending a message. This is what Hayek meant by the price system as a "marvel" -- not hyperbole, but a precise description of a decentralized information processing system that outperforms any centralized alternative.

Every allocation decision in an economy depends on prices:

- **What to produce**: A farmer choosing between corn and beans looks at relative prices. A factory deciding whether to manufacture basic goods or luxury items looks at relative prices. Get this signal wrong and productive resources flow to goods nobody wants.
- **What to buy**: A household allocating its budget between food, transportation, and housing responds to relative prices. When food prices rise, consumption shifts. When housing costs fall in one city versus another, migration incentives change.
- **What wages to accept**: A worker deciding whether a job offer is adequate must compare the wage to the cost of living. Without current price information, the worker cannot evaluate the real value of the wage.
- **Whether to save or spend**: Inflation expectations -- which are fundamentally expectations about future prices -- drive the decision to consume now or defer. In a hyperinflationary environment, rational behavior is to spend immediately because prices will be higher tomorrow. This collective rationality produces collective destruction.
- **Whether to hold local currency or dollars**: In Venezuela, the daily decision of whether to keep earnings in bolivares or convert to dollars depends entirely on the expected trajectory of prices and the exchange rate. This is a price-dependent decision made by millions of people every day.
- **Whether to invest**: Capital allocation -- the engine of growth -- depends on expected returns, which depend on expected future prices of inputs and outputs. Opacity in the price system does not just slow investment; it stops it. Capital that cannot see does not move.

Price transparency is therefore the single highest-leverage information improvement that econOS can make. Not because prices are the only important signal, but because every other signal depends on prices. Labor market data is useful, but a wage number without a cost-of-living number is half an answer. Sectoral growth data is useful, but without knowing the price dynamics within the sector, you cannot distinguish real growth from nominal inflation. Remittance data is useful, but a remittance amount without knowing what it buys at the destination is just a number.

### Venezuela as the Definitive Case Study in Price Signal Destruction

Venezuela between 2013 and 2020 is the clearest modern demonstration of what happens when the price system is systematically destroyed. The destruction was not accidental. It was the cumulative result of policies that attacked prices at every level:

**Price controls eliminated the signaling function.** The government mandated maximum prices for hundreds of basic goods -- food, medicine, hygiene products, construction materials. When the controlled price was set below the cost of production, producers stopped producing. When it was set below the market-clearing price, demand exceeded supply and shortages emerged. The price could not rise to signal scarcity, so the scarcity expressed itself instead as empty shelves, multi-hour queues, and a black market where the same goods traded at multiples of the controlled price. The controlled price was a fiction. The black market price was the real price. But the black market price was opaque, variable, and punishable by law, so even the real price was degraded as an information signal.

**Currency controls destroyed the exchange rate signal.** The government maintained official exchange rates that overvalued the bolivar by orders of magnitude relative to the parallel market rate. An importer with access to official-rate dollars could buy goods abroad at one-hundredth of the parallel-market cost and sell them domestically at enormous profit. This created massive rents for the politically connected and massive distortion in every price that depended on imports -- which, in an economy that imported most of its food and consumer goods, meant virtually every price. The "price" of an imported good became a function not of global markets or domestic demand but of which exchange rate the importer had access to.

**The statistical blackout destroyed the ability to measure what was happening.** When the BCV stopped publishing CPI data in 2015, the government eliminated the benchmark that would have quantified the damage. Workers could not reference an inflation number in wage negotiations. Contracts could not adjust to a published index. International organizations could not calibrate their assistance. The information layer of the economy went dark.

The result was the most extreme misallocation in the modern Western Hemisphere. Food rotted at borders while people went hungry, because the price signals that would have directed distribution were broken. Factories sat idle while demand went unmet, because controlled prices made production unprofitable. Capital fled or froze, because no price signal was trustworthy. The economy contracted by approximately 75% -- a collapse worse than the Great Depression, driven not by a lack of resources but by a catastrophic failure of the information system that coordinates resources.

Rebuilding the price information layer is not a nice-to-have for Venezuela's recovery. It is rebuilding the market itself. A market without visible, current prices is not a market. It is a guessing game.

---

## What a Real-Time Price Index Needs to Capture in Venezuela

A price index for Venezuela must contend with conditions that no standard methodology was designed for: dual-currency pricing, recent hyperinflation history, deep informality, geographic fragmentation, and weak institutional data. The categories below reflect what actually matters for Venezuelan households and economic agents, not what a textbook index would measure.

### Food Prices: The Cesta Basica

Food dominates Venezuelan household budgets in a way that is difficult to appreciate from a developed-economy perspective. For lower-income families -- which, after the crisis, means the majority of the population -- food expenditure can consume 60-80% of income. The "cesta basica" (basic basket) and the "canasta alimentaria" (food basket) are the most politically visible and personally urgent price metrics in the country.

CENDA (Centro de Documentacion y Analisis de los Trabajadores) publishes a monthly canasta alimentaria figure that is widely cited in Venezuelan media and political debate. As of recent estimates, the cost of the food basket for a family of five has been multiples of the minimum wage, making the gap between the official minimum wage and the actual cost of survival one of the most politically charged statistics in the country.

The food categories that matter most, ranked by budget share and political sensitivity:

- **Proteins**: Chicken (the most consumed protein in Venezuela), eggs, beef, pork, cheese (queso blanco/llanero, a dietary staple). Prices vary significantly by cut, quality, and source (domestic vs. imported).
- **Grains and starches**: Rice, pasta, corn flour (harina de maiz -- the base for arepas, the most fundamental food item in Venezuelan cuisine), beans (caraotas negras), bread.
- **Cooking oils and fats**: Soybean oil, corn oil, margarine. These were among the most chronically scarce items during the crisis.
- **Dairy**: Milk (powdered milk is often more available than fresh), butter, yogurt.
- **Produce**: Tomatoes, onions, peppers, plantains, potatoes, yuca. Prices are highly seasonal and vary significantly by region.
- **Beverages**: Coffee (a daily necessity in Venezuelan culture), sugar.

The food basket must be tracked in both bolivares and dollars, because the price a consumer pays depends on which currency they use and where they shop. A kilo of chicken at a large supermarket chain priced in dollars may differ from the same item at a street vendor or an open-air market (mercado popular) priced in bolivares at the day's exchange rate.

### Currency Dynamics: The Bolivar/USD Exchange Rate

In a dollarized economy, "the price" of anything is a function of two variables: the nominal price in whatever currency it is quoted in, and the exchange rate between that currency and the other currency in which the consumer might hold their money. A bag of rice that costs 50 bolivares means something very different when the exchange rate is 35 Bs/USD versus when it is 45 Bs/USD.

The exchange rate is therefore not a separate data category from prices. It is a component of every price. For a Venezuelan worker paid in bolivares, the dollar price of food is the bolivar price divided by the exchange rate. For a Venezuelan receiving dollar remittances, the bolivar cost of rent is the dollar amount they need to convert. The exchange rate is the conversion factor that makes all other prices commensurable.

Currently, the de facto market exchange rate is set not by the BCV's official rate but by the rate on Binance P2P (the bolivar/USDT pair), supplemented by rates tracked by Monitor Dolar Venezuela, DolarToday, and informal broker networks. The BCV has narrowed the gap between its official rate and the parallel market rate significantly since the worst of the crisis, but discrepancies still arise, and the Binance P2P rate remains the reference that merchants and consumers actually use for pricing decisions.

Tracking the exchange rate at high frequency -- ideally hourly, at minimum daily -- is a prerequisite for any meaningful price index in Venezuela.

### Housing and Rent

Housing costs in Venezuela are among the most opaque price categories. The formal rental market was severely distorted by rent control laws that made eviction nearly impossible and froze rents at levels that became trivial during hyperinflation. This destroyed the formal rental market: landlords withdrew properties rather than rent them under controlled conditions, and new construction for rental purposes collapsed.

What emerged is a largely informal rental market where:

- Prices are negotiated privately, often in dollars
- Formal lease contracts may not reflect actual payment amounts
- Short-term and room rentals (including to Venezuelan returnees and internal migrants) operate entirely outside any data system
- In Caracas, rental prices vary enormously by neighborhood -- from Chacao and Las Mercedes (relatively expensive, heavily dollarized) to Petare and other popular sectors (cheaper, more bolivar-denominated)

Rental data is obtainable from online platforms (TuInmueble.com, MercadoLibre's real estate section, Corotos.com.ve), but these platforms skew toward the formal, higher-end market. Informal rentals -- the type most lower-income Venezuelans actually deal with -- are largely invisible.

This is a known limitation. The price index should include whatever rental data is scrapeable from platforms, clearly labeled as "formal market, online-listed" rather than presented as representative of all housing costs.

### Transportation

Transportation pricing in Venezuela has its own distinctive distortions:

- **Gasoline**: Venezuela historically had the cheapest gasoline in the world -- essentially free, as a political commitment by successive governments. The Maduro government partially reformed gasoline pricing in 2020, introducing a two-tier system: subsidized gasoline at near-zero prices (rationed, requiring a carnet de la patria government ID card) and international-priced gasoline available to anyone at approximately $0.50/liter. This two-tier system itself is a price signal worth tracking -- the gap between subsidized and unsubsidized prices, the availability of subsidized fuel, and the extent to which the black market fills the gap.
- **Public transportation**: Bus fares, metro fares (in Caracas), and informal transportation (por puestos, moto-taxis) are often regulated at artificially low levels, with actual costs supplemented by informal payments or simply by deteriorating service quality.
- **Private transportation / ride-hailing**: Apps like Yummy (which includes a ride-hailing function) provide market-rate pricing data for urban transportation.

### Services: Telecom, Utilities, Internet

- **Mobile phone service**: CANTV/Movilnet (state-owned, deeply subsidized, deteriorating) and Digitel/Movistar (private, market-priced). The gap between state and private telecom pricing reflects the broader dual-pricing reality.
- **Electricity**: Heavily subsidized, with price schedules that have not kept pace with costs. Blackouts and rationing are the "price" that consumers actually pay -- not in money but in deprivation.
- **Internet**: Service quality and pricing vary enormously. Satellite and private internet providers charge market rates in dollars; state telecom provides slow, unreliable service at subsidized bolivar rates.
- **Water**: Intermittent supply in many areas. The "price" of water includes not just the utility bill but the cost of storage tanks, delivery trucks, and bottled water.

### The Dual-Price Reality

This is the structural feature that makes Venezuelan price measurement fundamentally different from conventional CPI. Many goods and services have a bolivar price AND a dollar price, and they do not move in lockstep.

A restaurant in Caracas may post a menu with dollar prices. A customer paying in bolivares pays the dollar price converted at the day's exchange rate (sometimes at the restaurant's own rate, which may differ from the market rate). The dollar price may remain stable for weeks while the bolivar price fluctuates daily with the exchange rate. Or the dollar price may adjust independently -- rising due to input cost increases or falling due to competitive pressure -- while the exchange rate moves in the opposite direction.

This means the price index must track:

1. Dollar-denominated prices (for goods and services priced in USD)
2. Bolivar-denominated prices (for goods and services priced in VES)
3. The exchange rate (to convert between them)
4. The currency in which each price observation is denominated (metadata attached to every data point)

A single "inflation rate" for Venezuela is an oversimplification. The system should report: dollar-denominated price changes, bolivar-denominated price changes, and a blended rate weighted by the estimated currency composition of actual transactions. Econoanalitica has estimated that 60-70% of transactions in major cities are now dollar-denominated, but this share varies by city, by income level, and over time.

---

## Construction Methodology for Venezuela

### Layer 1: Web Scraping of Online Retail

Web scraping is the backbone of the Billion Prices Project methodology and remains the most scalable approach to systematic price collection. The key Venezuelan sources:

**MercadoLibre Venezuela (mercadolibre.com.ve)**

MercadoLibre is the dominant e-commerce platform in Latin America and has significant operations in Venezuela. It functions both as a marketplace (third-party sellers listing products) and as a retail platform. For price tracking purposes, MercadoLibre offers several advantages:

- Broad category coverage: electronics, household goods, food and beverages, personal care, automotive, clothing, and more
- Structured data: product names, prices, seller location, shipping information are presented in consistent formats amenable to scraping
- Dual-currency listings: many sellers list prices in both bolivares and dollars, or in dollars only, providing direct observations of dollar-denominated pricing
- Historical listings: products remain listed for extended periods, allowing tracking of price changes over time
- Seller geography: seller location provides a rough geographic dimension to the data

Limitations: MercadoLibre prices reflect formal e-commerce, which skews toward durable goods and electronics. Food and daily necessities are less well represented. Prices include platform fees and may not match in-store prices. During the worst of the crisis, MercadoLibre Venezuela had limited inventory in some categories due to supply disruptions.

Scraping approach: Daily collection of prices for a defined basket of products across key categories. Product matching by name, SKU, and description to track the same item over time. Flagging of new products, discontinued products, and significant price changes for quality review.

**Farmatodo (farmatodo.com.ve)**

Farmatodo is Venezuela's largest pharmacy chain and has maintained an online catalog throughout the crisis. It provides structured price data for:

- Medicines (over-the-counter and prescription)
- Personal care and hygiene products
- Baby products
- Some food and household items

Farmatodo's online prices are typically in bolivares, with conversion to dollar-equivalent possible via the exchange rate. The chain has locations across major Venezuelan cities, though its online catalog may not reflect all regional price variations.

**Supermarket chains with online presence**

Several Venezuelan supermarket chains maintain websites or apps with price listings:

- **Central Madeirense**: One of Venezuela's oldest supermarket chains, with an online catalog
- **Automercados Plaza's**: Chain with locations primarily in Caracas and surrounding areas
- **Excelsior Gama**: Operates in multiple Venezuelan cities

Coverage and reliability of these online presences varies. Some update prices regularly; others may display stale information. The scraping system must track price freshness (date of last change) and flag stale listings.

**Electronics and appliance retailers**

For the durable goods component:

- **Daka, Krash**: Electronics retailers with online presence
- Various MercadoLibre sellers specializing in electronics
- Instagram-based electronics sellers (a significant channel in Venezuela's informal digital commerce)

**Scraping frequency and infrastructure**

For Venezuela, daily scraping is the minimum useful frequency. In periods of exchange rate volatility, prices can change multiple times per day, but daily collection captures the trend. The BPP demonstrated that daily frequency was feasible and informative for Venezuela.

The scraping infrastructure should be:

- Cloud-hosted (not dependent on Venezuelan internet infrastructure, which remains unreliable)
- Resilient to website changes (sites in developing markets change layouts more frequently)
- Equipped with change detection to flag when a website's structure changes in ways that break the scraper
- Storing raw HTML alongside extracted data, to allow reprocessing if extraction logic is updated

### Layer 2: Binance P2P Exchange Rate

The bolivar/USDT rate on Binance P2P is the de facto market exchange rate for most Venezuelans. Tracking this rate is not optional -- it is a core component of the price index, because the bolivar price of any dollar-denominated good is a function of this rate.

**How Binance P2P works for bolivar/USDT:**

Binance P2P is a peer-to-peer trading platform where individuals post buy and sell orders for cryptocurrency (primarily USDT, the Tether stablecoin pegged to USD) in exchange for local currency. In Venezuela, the flow is:

1. A buyer wants USDT (to hold dollar-equivalent value or to send abroad)
2. A seller has USDT and wants bolivares
3. They agree on a rate (e.g., 36.5 VES per USDT)
4. The buyer transfers bolivares via Pago Movil to the seller
5. Binance releases the escrowed USDT to the buyer

The aggregate of these transactions produces a market-clearing exchange rate that reflects actual supply and demand for dollars among Venezuelans. Unlike the BCV's official rate, which is administratively set, the Binance P2P rate is a genuine market price.

**Data collection approach:**

- Binance provides a public API that includes P2P advertisement data (buy/sell offers with prices, quantities, and payment methods)
- Third-party aggregators (previously Useful Tulips for LocalBitcoins, now various crypto analytics platforms) compile P2P trading data by country
- The system should collect: the median and volume-weighted average buy and sell rates, the bid-ask spread (which reflects market liquidity and uncertainty), total daily volume (which reflects the intensity of currency exchange activity), and the time series of intraday rate movements

**The BCV rate as a secondary reference:**

The BCV publishes a daily exchange rate that has converged significantly toward the parallel market rate in recent years. The system should track both rates and report the spread between them. When the spread is narrow, the BCV rate is functionally market-determined. When it widens, it signals renewed divergence between official policy and market reality. The spread itself is an economic signal -- a measure of monetary policy credibility.

**Other exchange rate sources:**

- Monitor Dolar Venezuela: Aggregates rates from multiple informal sources, published several times daily
- DolarToday: Longest-running parallel rate tracker, though methodology is opaque
- Yadio: App aggregating multiple exchange rate sources

Cross-referencing these sources provides a robustness check. If Monitor Dolar, Binance P2P, and the BCV all report similar rates, there is a single effective exchange rate. If they diverge, the divergence itself must be analyzed and reported.

### Layer 3: Social Media and Informal Price Reporting

This layer is unique to contexts like Venezuela and is one of the most distinctive aspects of the econOS approach. Venezuelans have organically developed informal price-reporting networks that contain real-time, ground-level price observations that no formal data source captures.

**WhatsApp and Telegram price groups**

During the crisis, Venezuelans created city-level WhatsApp and Telegram groups dedicated to sharing prices. These groups -- with names like "Precios Caracas," "Mercados Maracaibo," "Cesta Basica Valencia" -- function as crowdsourced price databases. Members post:

- Photos of price tags in supermarkets and pharmacies
- Screenshots of delivery app prices
- Text messages reporting the cost of the day's grocery run
- Exchange rate observations from local casas de cambio
- Alerts about product availability and scarcity

These groups can have thousands of members and generate dozens to hundreds of price observations per day. The data is unstructured (photos, voice notes, text in informal Spanish, regional slang) but represents genuine, real-time price observations from actual consumers across geographic areas and income levels that formal e-commerce platforms do not reach.

Systematizing this data requires:

- **Image processing**: OCR (optical character recognition) applied to photos of price tags, receipts, and menus to extract product names and prices
- **Natural language processing**: Parsing text messages in informal Venezuelan Spanish to identify product names, quantities, prices, and currencies (people write "el pollo a 4.5" meaning chicken at $4.50, or "la harina en 3.20 Bs" meaning corn flour at 3.20 bolivares)
- **Geolocation inference**: Determining the city or neighborhood from group names, user profiles, or context clues in messages
- **Deduplication**: Multiple group members may report the same price from the same store; the system must identify and handle duplicates
- **Quality filtering**: Distinguishing genuine price observations from complaints, jokes, political commentary, and spam that inevitably appear in these groups

This is not a clean data source. It requires significant processing, and the resulting data will have higher noise and lower precision than web-scraped retail prices. But it captures a segment of the market -- informal vendors, neighborhood shops, open-air markets -- that no online platform reaches. For food prices specifically, where informal commerce is a major channel, this layer is essential.

**Instagram business accounts**

Many Venezuelan small businesses, particularly food vendors, restaurants, and service providers, use Instagram as their primary online presence (rather than a website). They post prices directly in their stories, posts, or bio links. Restaurants post daily menus with prices. Bakeries post daily price lists for bread and pastries. Home-based food businesses (a significant segment in Venezuela's economy) post prices for prepared meals, cakes, and snacks.

Instagram scraping is technically possible but subject to platform restrictions. An alternative is to build a voluntary reporting system where business owners opt in to share their prices through an econOS interface connected to their Instagram presence.

**Twitter/X price reporting accounts**

Several accounts and hashtags on Twitter/X track Venezuelan prices:

- Individual economists and journalists who post weekly or monthly cost updates
- The CENDA canasta alimentaria reports shared via social media
- Hashtags like #CestaBasica, #PreciosVenezuela used by consumers reporting prices
- Bot accounts that automatically post exchange rate updates

These are lower-volume than WhatsApp groups but have the advantage of being public and scrapeable via the Twitter/X API (subject to API access terms and costs).

### Layer 4: Delivery App Data

Delivery apps provide structured, real-time price data for food, groceries, and restaurant meals -- categories that are among the most important for the price index.

**Yummy**

Yummy is a Venezuelan delivery app operating in Caracas and other major cities. It covers:

- Restaurant delivery: menu prices for thousands of restaurants, updated by the restaurants themselves
- Grocery delivery: prices for supermarket and bodega products
- Pharmacy delivery: medicine and personal care prices

Yummy prices are typically in dollars, reflecting the dollarized economy. The structured nature of the data (product name, price, restaurant/store, category) makes it directly usable for price tracking.

**PedidosYa**

PedidosYa operates in Venezuela and Colombia, providing restaurant and grocery delivery. Its catalog structure is similar to Yummy's and provides complementary coverage.

**Rappi** (primarily Colombia, with limited Venezuelan presence)

Rappi is the dominant delivery super-app in Colombia and has been expanding. Its Colombian coverage is extensive and provides high-quality price data for food and groceries.

**Delivery app advantages:**

- Prices are structured and machine-readable
- Products are categorized consistently
- Prices update frequently (restaurants adjust prices in real time)
- Geographic coverage is tied to delivery zones, providing city-level data
- Both dollar and bolivar pricing is visible

**Delivery app limitations:**

- Coverage is primarily urban, concentrated in major cities
- Delivery app prices may include markups over in-store prices
- Restaurant prices on apps may differ from dine-in prices
- Product selection is curated by the app, not representative of all available goods

### Layer 5: Formal Retail and Institutional Reporting

**Consecomercio (Venezuelan federation of chambers of commerce)**

Consecomercio and its member chambers occasionally publish price surveys and economic reports. These are irregular but, when available, provide a business-community perspective on price trends.

**CENDA (Centro de Documentacion y Analisis de los Trabajadores)**

CENDA publishes the most widely cited monthly canasta alimentaria (food basket) cost. Its methodology involves direct price collection in Caracas markets. The monthly figure serves as a benchmark against which the higher-frequency econOS index can be validated.

**BCV published data**

When the BCV publishes CPI or inflation data, it should be incorporated into the system -- not as ground truth (given its credibility history) but as one data point to compare against independent measurements. Divergence between the BCV figure and the independently constructed index is itself informative.

### Layer 6: Cross-Validation

The multi-source approach is not just about coverage. It is about robustness. Each data layer has different biases:

- Web-scraped retail prices skew toward formal commerce and durable goods
- Binance P2P rates reflect the financial/exchange market, not necessarily small-transaction rates
- Social media prices skew toward food and daily necessities, with geographic and demographic biases depending on who participates in which groups
- Delivery app prices skew urban and include platform markups
- Formal reporting has institutional biases and lags

Where multiple sources agree, confidence is high. Where they diverge, the divergence itself is diagnostic:

- If online retail food prices rise but social media reports stable street prices, it may indicate a wedge between formal and informal channels
- If the Binance P2P rate moves sharply but delivery app dollar prices don't adjust, it suggests short-term exchange rate volatility that hasn't propagated to goods prices yet
- If formal institutional reports show low inflation but all independent sources show higher inflation, the institutional credibility problem has resurfaced

The cross-validation methodology should be systematic: for each product category, compare at least two independent sources where possible, report the mean and the range, and flag categories where only a single source is available.

---

## Construction Methodology for Colombia

Colombia presents a fundamentally different challenge. The statistical infrastructure works. DANE CPI is credible, comprehensive (38 cities, ~443 items, 1.5 million price quotes per month), and timely (released within 5 business days of the reference month). The question is not "can we build something where nothing exists?" but "can we add enough value to justify the effort?"

The answer is yes, for specific use cases:

### Higher Frequency

DANE CPI is monthly. For businesses adjusting prices weekly, for workers negotiating wages, for the central bank monitoring the impact of monetary policy decisions, and for border-region dynamics where Venezuelan migration and trade create rapid price changes, weekly or daily price signals add meaningful information.

Web scraping of Colombian online retail provides this higher frequency:

**MercadoLibre Colombia (mercadolibre.com.co)**: Dominant e-commerce platform with extensive product listings across all major categories.

**Exito (exito.com)**: Colombia's largest retail chain (owned by Grupo Exito, majority-owned by Casino Group). Exito has a mature e-commerce platform with comprehensive grocery, household, electronics, and general merchandise catalogs. Online prices generally match in-store prices, making this a high-quality source.

**Jumbo (tiendasjumbo.co)**: Major supermarket chain owned by Cencosud (Chilean retail conglomerate). Strong grocery and household goods coverage.

**Olimpica (olimpica.com)**: Colombian retail chain with supermarket and department store formats. Significant presence on the Caribbean coast.

**Rappi**: The dominant delivery super-app in Colombia, covering groceries, restaurants, pharmacies, and general retail in all major cities. Rappi's structured product catalogs with real-time pricing make it an excellent high-frequency data source, particularly for food prices.

**Merqueo**: Online grocery delivery service operating in Bogota and other major Colombian cities. Direct grocery price data.

### Informal Commerce Prices

DANE's price collection focuses on formal retail establishments. Colombia's tiendas de barrio (neighborhood corner stores, estimated at over 250,000 nationwide) and plazas de mercado (open-air markets) serve a large share of lower-income consumers, and their prices may diverge from formal retail. Capturing these prices through delivery apps that serve neighborhood stores (some Rappi orders come from tiendas) and through social media price reporting would supplement DANE's formal coverage.

### Rental Market Data

Colombia has relatively well-developed online real estate platforms:

**FincaRaiz (fincaraiz.com.co)**: The largest real estate listing platform in Colombia. Rental listings include price, location, property characteristics, and listing date. Scraping rental listings provides a real-time indicator of market rents, compared to DANE's CPI shelter component which captures existing lease rates with a lag similar to the US CPI shelter lag problem.

**Metrocuadrado (metrocuadrado.com)**: Major real estate platform owned by El Tiempo (Colombia's largest newspaper group). Similar coverage to FincaRaiz.

**Ciencuadras (ciencuadras.com)**: Newer platform with growing listings.

The rental data opportunity in Colombia mirrors the US shelter lag problem documented in the inflation measurement document: DANE CPI captures the rent on all existing leases, which is a lagging indicator of market conditions. A real-time index of new listing prices on FincaRaiz and Metrocuadrado would provide a leading indicator, particularly valuable in cities experiencing rapid change (Bogota neighborhoods gentrifying, Cucuta adjusting to Venezuelan migration, Medellin responding to digital nomad demand).

### DANE as Validation Benchmark

The most important structural advantage for Colombia is that DANE CPI exists and is credible. This allows rigorous validation:

- Build the web-scraped daily index for Colombia
- Compare it monthly against DANE CPI
- Where they track closely (which, based on BPP experience in countries with credible statistical agencies, should be most of the time), the daily index is validated
- Where they diverge, investigate whether the divergence reflects a genuine information gain (the daily index capturing an event before DANE's monthly average picks it up) or a data quality issue in the scraped data
- This validation builds the credibility needed to trust the Venezuelan index, which has no comparable benchmark

Colombia is the "easy case" -- methodologically, building and validating the daily price index in Colombia first, then applying the validated methodology to Venezuela's harder environment, is the right sequencing strategy.

### The Colombia-Venezuela Bridge

Colombia and Venezuela share a 2,219-kilometer border, a language, massive migration flows (2.8+ million Venezuelans in Colombia as of recent UNHCR figures), and increasingly integrated informal commerce. Border cities -- Cucuta (Colombia) and San Antonio/Urena (Venezuela) -- function as a single economic zone in practice.

A price index that covers both countries simultaneously enables:

- **Purchasing power parity comparison**: What does $100 buy in Caracas versus Bogota versus Cucuta? For the millions of Venezuelans deciding whether to migrate, return, or stay, this is decision-critical information.
- **Cross-border arbitrage detection**: When the price of a basic good is significantly cheaper on one side of the border, trade flows respond. Tracking the price differential identifies these arbitrage opportunities and, more importantly, measures the economic integration of the two markets.
- **Remittance purchasing power**: A Venezuelan in Bogota sending money home can see exactly what their dollars will buy in their family's city in Venezuela, compared to what those same dollars would buy in Bogota.

---

## The Billion Prices Project Model: What Worked, What Didn't, and How econOS Adapts

The Billion Prices Project, founded by Alberto Cavallo and Roberto Rigobon at MIT in 2008, is the most directly relevant prior art. Understanding what they did -- and where the approach's limits were -- is essential.

### What They Did

The BPP collected daily prices from online retailers in over 60 countries using automated web scrapers. For each country, they identified major retailers with online catalogs, built scrapers to extract individual product prices daily, and aggregated the resulting data into daily price indexes.

The aggregation used standard index number techniques: products were classified into categories approximating the composition of official CPI baskets, and category-level price changes were weighted to produce an overall index. This allowed direct comparison with official CPI.

The BPP was commercialized through PriceStats (later acquired by State Street Global Markets), which sold daily inflation indicators to institutional clients -- central banks, sovereign wealth funds, hedge funds.

### What Worked

1. **The basic methodology was validated globally.** In countries with credible statistical agencies (US, UK, Brazil, Germany), the BPP daily index tracked the goods component of official CPI with correlations above 0.9. This established that online prices are a reliable proxy for the broader goods price level.

2. **It detected statistical manipulation.** In Argentina, where the INDEC was widely accused of suppressing inflation numbers under the Kirchner governments, the BPP index showed inflation running 2-3x the official rate, consistent with private estimates. This demonstrated the methodology's value as an independent check on government statistics.

3. **It covered Venezuela during the crisis.** The BPP/PriceStats collected data from Venezuelan online retailers and produced daily indexes during the hyperinflationary period. Their Venezuela data showed:
   - Confirmation of hyperinflationary dynamics, with price changes accelerating in line with exchange rate depreciation
   - Strong correlation between online prices and the parallel exchange rate, validating the PPP-based approaches used by Hanke and others
   - Goods-level price dynamics invisible to monthly or quarterly reporting -- synchronized price jumps, rapid pass-through of exchange rate movements, intraday volatility

4. **It scaled.** The BPP eventually covered 60+ countries with a relatively small team, proving that the marginal cost of adding a new country is low once the infrastructure exists.

### What Didn't Work (or Worked Imperfectly)

1. **Services are invisible to web scraping.** The BPP methodology captures goods prices -- things you can buy online and have shipped. It does not capture services: haircuts, medical consultations, auto repair, legal services, domestic labor, tutoring. Services represent 60-70% of developed-economy spending (lower in Venezuela, but still significant). This means a web-scraped index is structurally a goods price index, not a full cost-of-living index.

2. **Online prices may not match offline prices.** The BPP's validation against official CPI was strong for goods, but the underlying assumption -- that online prices track offline prices -- holds best in markets with mature e-commerce where online and offline prices are arbitraged. In Venezuela, where online shopping was limited (particularly during the crisis), the representativeness of online prices for the broader market was lower.

3. **Scarcity is not captured by prices.** In Venezuela, the relevant economic signal was often not the price of a good but whether the good existed at all. Empty shelves, rationed products, and multi-hour queues impose real costs on consumers that no price index captures. A good listed at a "low" controlled price that cannot actually be purchased is a meaningless data point. The BPP, like any price index, measured the prices of goods that were available for purchase, not the full cost of living in an economy with chronic shortages.

4. **It was proprietary.** PriceStats served institutional clients at institutional prices. The populations who most needed the data -- Venezuelan families, small business owners, workers negotiating wages -- could not access it. The academic papers published aggregate findings, but the underlying daily data was not public.

5. **Limited geographic granularity.** The BPP produced country-level indexes but not city-level or regional indexes. For Venezuela, where Caracas prices differ significantly from Maracaibo, Barquisimeto, or border-town prices, national-level data is an incomplete picture.

### How econOS Adapts the BPP Approach

econOS takes the BPP's validated core methodology and extends it in four critical directions:

**More data sources.** The BPP relied almost exclusively on traditional e-commerce retailers. econOS adds delivery apps (Yummy, PedidosYa, Rappi), social media price observations (WhatsApp groups, Instagram, Twitter/X), exchange rate platforms (Binance P2P, Monitor Dolar), and formal institutional reporting. This dramatically broadens coverage, especially for food, services, and informal commerce.

**Dual-currency tracking.** The BPP tracked prices in local currency. econOS must track in both bolivares and dollars, record the denomination of each price observation, and maintain the exchange rate time series needed to express all prices in a common unit.

**Geographic granularity.** Instead of a single national index, econOS targets city-level indexes for major Venezuelan cities (Caracas, Maracaibo, Valencia, Barquisimeto, Merida, Ciudad Guayana, San Cristobal) and major Colombian cities (Bogota, Medellin, Cali, Barranquilla, Cucuta, Bucaramanga, Cartagena). Delivery app data and geotagged social media observations enable this disaggregation.

**Public access.** This is the fundamental difference. The BPP was commercialized as an institutional product. econOS publishes everything: the raw data, the methodology, the index values, and the API. The target users are not hedge funds but the Venezuelan nurse deciding whether to emigrate, the small business owner setting prices for the week, and the diaspora family evaluating what their remittance will buy.

---

## Handling the Hard Problems

### Quality Adjustment

When the price of a product changes, is it inflation or is it a different product? This is the classic quality adjustment problem in price measurement, and it is harder in developing markets.

Examples:

- A brand of rice that was sold in 1kg bags now comes in 900g bags at the same price. The "price per kg" has risen, but the sticker price hasn't changed. This is shrinkflation.
- A supermarket stops carrying a cheaper brand of cooking oil and replaces it with a more expensive brand. The "price of cooking oil" in the index rises, but it reflects a change in the available product, not a pure price increase.
- A smartphone listed at $200 this year has better specifications than the $200 smartphone listed last year. The sticker price is unchanged, but the quality-adjusted price has fallen.

The BLS handles these through "hedonic quality adjustment" -- statistical models that estimate the value of individual product characteristics. This is resource-intensive and not feasible for econOS at scale.

The pragmatic approach for econOS:

- **Match exact products where possible.** Track specific SKUs, not generic product categories. When the same 1kg bag of Harina P.A.N. (the dominant corn flour brand in Venezuela) changes price, that is a clean price observation.
- **Flag product changes.** When a tracked product disappears and is replaced by a similar product, flag the substitution. Report both the raw index (which includes the substitution effect) and a "matched-product" sub-index (which only includes price changes for products that remain identical).
- **Track unit prices.** Where quantity information is available (which it often is on e-commerce platforms), report price per kilogram, price per liter, etc. This automatically catches shrinkflation.
- **Accept imperfection.** Quality adjustment is an unsolved problem even in the BLS, with its $600 million annual budget. A transparent methodology that acknowledges its limitations is more valuable than a black-box adjustment that claims false precision.

### Representativeness

Online prices may not match street prices. Delivery app prices include markups. WhatsApp group prices are reported by a self-selected sample. No single source is representative of the full Venezuelan price experience.

The mitigation strategy is multi-source triangulation:

- If online retail, delivery app, and social media sources all show chicken at $4-5 per kilo, the price is likely in that range regardless of channel
- If online retail shows $5 but social media reports $3.50 at the mercado popular, the difference itself is informative -- it reveals the formal/informal price gap
- Report ranges and confidence intervals, not false precision. "Chicken: $4.00-5.00/kg (formal retail); $3.00-4.00/kg (informal market reports)" is more honest and more useful than "$4.37/kg"

### The Shelter Problem

Rental data in Venezuela is extraordinarily opaque. As discussed above, rent control distorted the formal market, the informal market operates through private negotiation, and online listings skew toward the higher-end formal market.

Honest approach:

- Scrape online rental platforms (TuInmueble, MercadoLibre, Corotos) and report formal market asking rents
- Clearly label this as "online-listed formal rental asking prices," not as representative of all housing costs
- Track over time: trends in formal market rents still provide useful information about direction and magnitude of shelter cost changes, even if the level may not match the median Venezuelan's actual housing cost
- In Colombia, the same approach applies with FincaRaiz and Metrocuadrado, validated against DANE's shelter CPI component

This is a known gap. It should be documented, not hidden.

### Shrinkflation

Package size reduction at constant nominal prices is a global phenomenon but is particularly prevalent in economies with price sensitivity and informal price controls. Tracking it requires:

- Recording package sizes alongside prices (which e-commerce platforms usually provide)
- Computing per-unit prices (price per kg, per liter, per unit)
- Flagging instances where the same brand/product reduces package size
- Reporting a "shrinkflation index" -- the percentage of tracked products that have reduced package sizes over a given period

### Geographic Variation

Prices in Caracas are not prices in Maracaibo. Prices in Maracaibo are not prices in Merida. And prices in any major city are not prices in a border town like San Cristobal or a rural area in Barinas state.

The sources of geographic price variation include:

- **Transportation costs**: Getting goods from ports (primarily Puerto Cabello and La Guaira) to inland cities adds cost that varies with distance, road quality, and fuel availability
- **Local supply conditions**: Agricultural production varies by region. Barinas and Portuguesa states produce much of Venezuela's agriculture; prices there may differ from purely import-dependent cities
- **Dollarization levels**: Border regions and oil-producing regions may be more dollarized than central areas, affecting the currency denomination of prices
- **Local market structure**: The degree of formal versus informal commerce, the number of competitors, and the presence of large retail chains all vary by city

The econOS approach:

- Produce separate indexes for each major city where data coverage allows
- Report the national index as a weighted average of city indexes (weighted by population or estimated economic activity)
- Flag cities with insufficient data coverage, rather than imputing prices from better-covered cities
- Use the Colombia/DANE comparison to calibrate how much geographic variation actually matters: DANE publishes city-level CPI, so the Colombian data can reveal how much city-level indexes diverge from the national average, and this divergence pattern can inform expectations for Venezuela

---

## What This Enables for Allocation

The theoretical argument is that better price information improves resource allocation. Here are the concrete channels through which a real-time price index changes behavior:

### Wage Negotiation

A Venezuelan worker in the formal sector is told by their employer that a 10% bolivar raise is generous. Without current price data, the worker can only push back with anecdotal impressions. With a real-time price index, the worker can say: "The cost of the cesta basica has risen 18% in the past three months. A 10% raise is a real wage cut." This is not hypothetical. Venezuelan workers' primary complaint during the crisis -- echoed by CENDA, by unions, and by ordinary workers on social media -- was that wages did not keep up with prices. The problem was not just that wages were low; it was that workers could not precisely quantify how low, because the inflation data was either absent or contested.

A transparent, independent, real-time price index shifts the information asymmetry in wage bargaining. It does not guarantee higher wages. But it gives workers the data to demand them, and it gives employers the data to understand what a competitive wage actually looks like.

### Business Pricing

A small business owner in Venezuela -- a restaurant, a bakery, a tienda -- must set prices every day, sometimes multiple times per day in volatile periods. Setting the price too high loses customers. Setting it too low means selling below replacement cost. The owner needs to know:

- What are competitors charging?
- What did my inputs cost this week versus last week?
- What is the exchange rate doing?

A real-time price index that includes competitor prices (via delivery app and web scraping data), input cost trends (via wholesale food price tracking), and the exchange rate (via Binance P2P) gives the business owner a dashboard for their most critical daily decision. This is the "BI view for the economy" concept from the investment allocation optimization document, applied at the micro level.

### Remittance Optimization

An estimated 7-8 million Venezuelans in the diaspora send money home. The World Bank estimates remittance flows to Venezuela at $3-5 billion annually, but actual flows (including informal channels) may be significantly higher.

A diaspora family in Bogota, Lima, or Miami sending $200 per month to relatives in Maracaibo wants to know: What does $200 buy this month? Is it more or less than last month? Should we send more this month because prices spiked? Should we advise our family to buy rice in bulk now because the price is about to rise?

Currently, this information travels through phone calls, WhatsApp messages, and anecdote. The price index makes it systematic: a Maracaibo cost-of-living figure, updated weekly, expressed in dollars, showing trends. The diaspora family can see that $200 buys 85% of last month's basket, and adjust accordingly.

At scale, this price transparency may also affect remittance corridors. If the cost of living in Ciudad Guayana is rising faster than in Merida, the aggregate flow of remittances may shift, redistributing diaspora support toward higher-need areas. This is resource reallocation driven by information.

### Migration Decisions

The Venezuelan migration crisis is the largest displacement in the Western Hemisphere's recent history. Migration decisions are driven by many factors -- safety, family, legal status, opportunity -- but economic calculation is central. A Venezuelan considering emigration is implicitly comparing:

- The real value of their income in Venezuela (income divided by local prices)
- The expected real value of their income at the destination (expected wages divided by destination prices)
- The costs of migration (travel, legal, social)

A real-time, multi-city price index that covers both Venezuelan cities and major destination cities (Bogota, Lima, Santiago, Madrid) enables this calculation with actual data rather than guesswork. It does not make the decision -- there are non-economic factors that no price index captures -- but it ensures the economic dimension of the decision is informed.

### Independent Economic Signal

Perhaps the most important function: a transparent, independent, methodologically documented price index provides a signal that cannot be suppressed or manipulated by the government.

When the BCV stopped publishing CPI in 2015, it created an information vacuum that served the government's interest in obscuring the severity of the crisis. An independent price index -- produced from publicly observable data, with published methodology, maintained by a distributed team, and hosted on infrastructure outside government control -- is resistant to this kind of suppression. The data exists because the prices exist. As long as retailers post prices online, as long as Binance P2P operates, as long as Venezuelans share prices on WhatsApp, the inputs to the index are available. No government decision can make the data disappear.

For economists, journalists, opposition politicians, international organizations, and ordinary citizens, this independent signal is a tool for accountability. It answers the question "how are things actually going?" with data rather than narrative.

---

## Technical Architecture: From Data Sources to Published Index

### Data Collection Pipeline

```
Layer 1: Web Scraping (daily)
  MercadoLibre VE/CO, Farmatodo, supermarket chains, Exito, Jumbo
  → Raw prices with product identifiers, timestamps, currency denomination, seller location
  → Stored: raw HTML + extracted structured data

Layer 2: Exchange Rate (continuous/hourly)
  Binance P2P API, Monitor Dolar, BCV official rate, DolarToday
  → Bid/ask rates, volumes, timestamps
  → Stored: time series database

Layer 3: Social Media (daily/as available)
  WhatsApp/Telegram group monitoring, Instagram business accounts, Twitter/X
  → Unstructured text and images → NLP/OCR processing → structured price observations
  → Stored: raw content + extracted observations with confidence scores

Layer 4: Delivery Apps (daily)
  Yummy, PedidosYa, Rappi
  → Structured product prices, restaurant prices, category data
  → Stored: structured data with timestamps and geographic markers

Layer 5: Institutional (monthly/as published)
  DANE CPI, BCV releases, CENDA canasta alimentaria, IMF estimates
  → Structured official data
  → Stored: official statistics database
```

### Product Matching and Classification

Each price observation must be mapped to a standardized product category. The classification should follow COICOP (Classification of Individual Consumption According to Purpose) at the top level, for comparability with official CPI baskets, with finer-grained subcategories as data allows.

Product matching uses:

- SKU/barcode matching where available (e-commerce platforms often include this)
- Brand + product name + size matching for packaged goods
- Category-level matching for products without specific identifiers (e.g., "chicken breast, per kg")
- Machine learning models trained on the product matching task, improving over time

### Index Construction

The basic methodology follows standard price index construction, adapted for the multi-source, multi-currency context:

1. **Compute category-level price changes**: For each product category, compute the percentage change in the median (or geometric mean) price from the previous period. Use the median rather than the mean to reduce sensitivity to outliers (a single misreported price).

2. **Weight categories**: Use expenditure weights that approximate Venezuelan and Colombian household spending patterns. For Venezuela, where no current household expenditure survey exists, weights must be estimated from the best available sources -- CENDA's food basket composition, Econoanalitica's estimates of spending shares, and cross-country comparisons with Colombia's ENPH survey (adjusted for Venezuela's different consumption patterns). For Colombia, DANE's ENPH-derived weights serve as the benchmark.

3. **Compute sub-indexes**: Separate sub-indexes for food, housing, transportation, services, and other categories. These are individually useful (food inflation is the most important single number for most Venezuelan households).

4. **Compute currency-specific indexes**: Separate indexes for bolivar-denominated prices and dollar-denominated prices. A blended index weighted by estimated transaction shares in each currency.

5. **Aggregate to city-level and national indexes**: City-level indexes for cities with sufficient data coverage. National index as a population-weighted average of city indexes.

6. **Report with uncertainty**: Every index value accompanied by a confidence range reflecting the number of price observations, the cross-source consistency, and the estimated coverage of the product category.

### Publication

- **Daily index values**: Published to a public website and API
- **Weekly summary**: A human-readable report covering the week's price movements, notable changes, and exchange rate dynamics
- **Monthly comparison**: A formal comparison of the econOS index against DANE CPI (Colombia) and BCV releases (Venezuela, when available)
- **Full methodology document**: Publicly available, version-controlled, updated when methodology changes
- **Raw data access**: API access to individual price observations (anonymized by source where necessary) for researchers and journalists

---

## What Comes Next: From Price Index to Price Infrastructure

A real-time price index is the first step. Over time, the data infrastructure it creates enables increasingly sophisticated applications:

**Price prediction**: With sufficient historical data (6-12 months minimum), time-series models can forecast short-term price movements. This is useful for businesses planning purchases, for families timing major expenditures, and for the exchange rate (where short-term predictability, even modest, has value for remittance timing).

**Price dispersion analysis**: Not just "what is the price?" but "how much does the price vary across sources, cities, and time?" High price dispersion indicates market fragmentation and opportunities for arbitrage. Low dispersion indicates competitive, well-connected markets. Tracking dispersion over time measures whether markets are integrating or fragmenting.

**Relative price tracking**: Not just "are prices rising?" but "which prices are rising relative to others?" If food prices rise 20% while electronics prices fall 5%, the relative price has shifted, signaling changes in supply, demand, or cost structures that affect production and consumption decisions.

**Cross-border price comparison**: Systematic, product-level price comparison between Venezuelan and Colombian cities. This is the data layer needed for the migration and remittance BI views described in the highest-leverage areas document.

**Informal economy price intelligence**: As the social media and WhatsApp data layers mature, they provide insight into informal market prices that no formal data source captures. Over time, this creates a unique dataset on the informal economy's price dynamics -- a contribution to economic knowledge that currently does not exist for any country.

---

## Honest Assessment of Limitations

This document has described a methodology. Here is what it will not achieve:

**It will not measure the full cost of living.** A price index based on observable market prices cannot capture queuing costs (time spent searching for goods), quality degradation (services that nominally exist but function poorly), or the welfare loss from goods that are simply unavailable. During Venezuela's worst period, these non-price costs were enormous. They are diminishing as the economy stabilizes, but they remain real.

**It will underrepresent the poorest households.** The data sources -- online retail, delivery apps, social media groups -- all require internet access and some level of digital engagement. The poorest Venezuelans, particularly in rural areas and in urban informal settlements with weak connectivity, are the least likely to generate data and the most likely to face different prices (often higher, due to transportation costs and limited competition in underserved areas). The index will be more representative of the urban, digitally connected majority than of the rural or deeply informal poor.

**It will not capture services well.** Healthcare costs, education costs, legal services, home repair -- these are difficult to track through any automated method. Delivery apps capture some restaurant and pharmacy services, but the broader service economy remains hard to measure. This is also a limitation of the BPP and of BLS CPI (which relies on labor-intensive field collection for services).

**The social media layer is experimental.** Extracting structured price data from WhatsApp group messages and Instagram posts using NLP and OCR is feasible with current technology but noisy. The error rate will be higher than for web-scraped e-commerce data. This layer should be treated as supplementary and experimental until the processing pipeline is validated.

**Venezuela's data environment can deteriorate again.** The current moment -- where online retail is functioning, Binance P2P is active, and social media price reporting is widespread -- reflects a period of relative stabilization. A renewed economic crisis, increased government internet censorship, or platform shutdowns (Binance has faced regulatory pressure in multiple countries) could degrade the data sources. The system must be designed for resilience: multiple sources, no single point of failure, data archived continuously.

These limitations are real. They should be documented alongside every published index value. Transparent methodology that acknowledges what it cannot measure is infinitely more valuable than opaque methodology that claims to measure everything.

---

## The Argument in Summary

Prices are the most fundamental signal in any market economy. Hayek's entire framework rests on the proposition that prices encode dispersed information into a form that enables decentralized coordination. When prices are visible and current, allocation improves -- automatically, without anyone directing it, through millions of individual responses to the price signal. When prices are obscured, distorted, or destroyed, allocation degrades just as automatically.

Venezuela experienced the most extreme episode of price signal destruction in the modern Western Hemisphere. Price controls broke the signaling function. Currency controls broke the exchange rate signal. The statistical blackout eliminated even the measurement of the damage. The result was a 75% GDP contraction -- not because resources disappeared, but because the information system that coordinates resources collapsed.

Rebuilding that information system -- starting with the most fundamental signal, prices -- is not an academic exercise. It is rebuilding the market itself. A real-time, multi-source, multi-currency price index for Venezuela, validated against Colombia's functional statistical infrastructure, is the single highest-leverage data product that econOS can build. It serves the worker negotiating wages, the business owner setting prices, the diaspora family calibrating remittances, the potential migrant comparing cost of living, and the economist tracking recovery. It provides an independent signal that cannot be suppressed. It fills a void that no institution currently fills.

The methodology is proven. The Billion Prices Project demonstrated a decade ago that web-scraped daily price indexes work -- that they track official CPI in stable countries and provide superior information in unstable ones. The data sources are richer today than they were when the BPP operated: delivery apps, social media price networks, cryptocurrency exchange platforms, and mobile payment systems provide coverage that was unavailable in 2008.

What is missing is the infrastructure to collect this data systematically, aggregate it transparently, and publish it as a public good. That is what this document specifies. The price index is the beating heart of econOS -- the foundation on which every other measurement depends, the proof of concept that establishes credibility, and the tool that delivers immediate, tangible value to the people who need it most.
