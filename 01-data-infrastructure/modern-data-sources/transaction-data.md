# Transaction Data as a Real-Time Economic Signal: Venezuela and Colombia

## 1. The Payment Landscape in Venezuela

Venezuela does not have a functioning card-dominated payment system in the way the United States does. What it has instead is a layered, improvised stack of payment methods that emerged from a decade of monetary collapse, hyperinflation, and the physical disappearance of cash.

Understanding this stack is essential. It is not a simplified version of a developed market payment system. It is a fundamentally different structure shaped by crisis.

### Pago Movil (Interbank Mobile Payments)

Pago Movil is the closest thing Venezuela has to a universal digital payment system. Launched by the Banco Central de Venezuela (BCV) in 2018, it allows person-to-person and person-to-merchant transfers between bank accounts using a phone number, national ID (cedula), and bank code. No card required.

Pago Movil became dominant for a specific reason: during the hyperinflation crisis (2017-2021), physical bolivar bills lost value faster than the central bank could print and distribute them. ATMs ran dry. Cash literally became unavailable. Pago Movil filled the void -- not because it was technologically superior, but because it was the only way to transact in bolivares at all.

The major banks through which Pago Movil flows:
- **Banesco** -- the largest private bank by customer base
- **Mercantil** -- major private bank with significant retail presence
- **Bancamiga** -- growing digital-first bank
- **Banco de Venezuela** -- state-owned, largest by branch count
- **BBVA Provincial** -- major presence, Spanish-owned

Every bank that operates in Venezuela's interbank system connects to Pago Movil. The transaction is settled in bolivares at whatever the bolivar happens to be worth that day. Settlement is near-instant for most transfers, though the system experiences congestion during peak hours and around holidays.

Pago Movil is used for everything from buying coffee to paying rent. Street vendors, taxi drivers, and small shops all accept it. The merchant does not need a POS terminal -- just a bank account and a phone. This gives Pago Movil penetration into economic segments that card networks never reached.

**Data signal**: Pago Movil transaction volumes and values, if accessible, would be the single best proxy for formal domestic economic activity in bolivares. The BCV has aggregate data on interbank transfer volumes. Whether this data is published in usable form is a different question (see Section 7).

### Zelle (USD Person-to-Person)

This is the most unusual feature of Venezuela's payment landscape. Zelle is a US domestic payment system operated by Early Warning Services, owned by a consortium of major US banks (JPMorgan Chase, Bank of America, Wells Fargo, etc.). It was designed for Americans to send money to each other.

Venezuelans adopted it as a de facto dollarized payment system.

Here is how it works in practice: Venezuelans with US bank accounts (often opened during periods of travel, through family abroad, or via intermediaries) use Zelle to send dollars to each other as payment for goods and services. Businesses in Caracas, Maracaibo, and other cities quote prices in "Zelle dollars." A restaurant might list a meal as "$12 Zelle." A landlord might set rent at "$400 Zelle per month."

The mechanism is simple but has profound implications:
- Buyer has a US bank account with Zelle capability
- Seller has a US bank account with Zelle capability
- Payment is sent in USD via Zelle
- The transaction settles through the US banking system, not the Venezuelan one
- Venezuelan authorities have no visibility into it

Zelle transactions in this context are completely invisible to Venezuelan financial infrastructure. They show up as domestic US transfers between US bank accounts. The economic activity they represent -- rent, retail purchases, services, wholesale transactions -- is happening in Venezuela but is recorded nowhere in Venezuelan data.

**Data signal**: Essentially zero from the Venezuelan side. From the US side, Zelle does not publish geographic or purpose-of-transaction data. This is a major blind spot.

### Binance P2P and Crypto Exchanges

Venezuela has consistently ranked among the top 5-10 countries globally for peer-to-peer crypto trading volume, particularly on Binance P2P. This is not because Venezuelans are crypto enthusiasts. It is because Binance P2P serves as a currency exchange platform.

The typical flow:
1. Person A has bolivares in a Venezuelan bank account
2. Person A wants dollars (USDT, a stablecoin pegged to USD)
3. Person A goes to Binance P2P, finds a counterparty (Person B) willing to sell USDT for bolivares
4. Person A sends bolivares to Person B via Pago Movil or bank transfer
5. Person B releases USDT to Person A's Binance wallet
6. Person A now holds dollar-equivalent value

This is the de facto foreign exchange market for most Venezuelans. The official exchange rate set by the BCV often diverges from the rate on Binance P2P, and the Binance rate is typically treated as the real market rate.

Other platforms used: LocalBitcoins (now defunct, was once dominant in Venezuela), Reserve (stablecoin app that gained traction in Venezuela), and various smaller exchanges. But Binance P2P dominates by volume.

**Data signal**: Binance P2P volume data is partially accessible through Binance's API and through third-party aggregators like Useful Tulips (usefultulips.org, which tracked LocalBitcoins volumes by country) and Coin Dance. The bolivar/USDT trading pair volume on Binance P2P is a real-time indicator of currency exchange pressure, dollarization demand, and economic activity. The spread between the BCV official rate and the Binance P2P rate is itself an economic signal -- wider spreads indicate greater distrust of official monetary policy.

### Cash (USD and Bolivares)

Physical US dollar bills circulate widely in Venezuela, particularly in border regions (Tachira state near Colombia), in the oil-producing Zulia state, and in informal markets everywhere. The denominations matter: $1, $5, $10, and $20 bills are common. $50 and $100 bills are less circulated and sometimes discounted because of counterfeiting concerns and difficulty making change.

Physical bolivar bills exist but in diminished relevance. After multiple redenominations (the most recent creating the "bolivar digital" in October 2021, removing six zeros), physical bills are used for very small transactions. Most bolivar transactions above trivial amounts go through Pago Movil.

**Data signal**: Cash transactions are invisible to digital systems. In Venezuela, where a significant share of economic activity -- street food, informal transport, domestic work, small-scale commerce -- transacts in physical dollars, this invisibility is a major limitation.

### Bank Transfers (Domestic, Non-Pago Movil)

Standard bank-to-bank transfers within the Venezuelan banking system still occur, particularly for larger transactions (business payments, payroll for formal sector employees). These flow through the BCV's payment infrastructure.

**Data signal**: Captured in banking system data but not typically disaggregated in public reporting.

---

## 2. The Payment Landscape in Colombia

Colombia's payment landscape is more conventional than Venezuela's but is undergoing rapid transformation driven by mobile payment platforms.

### Nequi (Bancolombia)

Nequi is a digital wallet and payment platform owned by Bancolombia, Colombia's largest bank. Launched in 2016, it has grown to over 17 million users (as of late 2023, in a country of ~52 million people). Nequi allows:
- Person-to-person transfers (free between Nequi accounts)
- Bill payments
- QR code payments at merchants
- Cash withdrawals at Bancolombia ATMs
- Savings pockets ("bolsillos")

Nequi's growth accelerated during COVID-19 and has continued. It is particularly popular among younger, urban Colombians. The platform processes billions of pesos in transactions monthly.

**Data signal**: Nequi transaction volumes would be a strong proxy for digital economy activity among Colombia's urban, banked, younger population. Bancolombia publishes some aggregate statistics but not granular transaction data.

### Daviplata (Banco Davivienda)

Daviplata is Banco Davivienda's mobile payment platform, launched in 2012 -- predating Nequi. It was initially designed for financial inclusion, targeting lower-income and rural populations. Daviplata was the platform through which the Colombian government distributed Ingreso Solidario (pandemic cash transfers) and other social programs.

Daviplata has over 16 million registered users. Its user base skews more toward lower-income segments than Nequi, making it a valuable complement.

**Data signal**: Daviplata transaction data, particularly combined with Nequi data, would provide a more representative picture of Colombian digital payments than either alone. The government transfer distribution function means Daviplata data also captures fiscal policy transmission.

### PSE (Pagos Seguros en Linea)

PSE is Colombia's online bank transfer system, operated by ACH Colombia. It enables direct bank-to-bank payments for e-commerce, bill payments, and government services. When a Colombian buys something online and pays via their bank account, it typically goes through PSE.

PSE processed over 400 million transactions in 2023. It is the backbone of formal e-commerce payment in Colombia.

**Data signal**: PSE aggregate volumes are published by ACH Colombia and provide a reasonable proxy for formal online economic activity.

### Cards (Visa, Mastercard, Domestic Networks)

Card penetration in Colombia is growing but remains well below US levels. As of 2023, there were approximately 17 million credit cards and 40+ million debit cards in circulation. Visa and Mastercard are the dominant networks. Redeban and Credibanco are the major acquirers/processors.

Card usage is concentrated in formal retail, supermarkets, and e-commerce. Most informal commerce -- which represents a large share of economic activity -- does not accept cards.

**Data signal**: Card transaction data in Colombia follows the same logic as in the US (see Section 8) but with much lower coverage of total economic activity.

### Cash (Colombian Pesos)

Cash remains the dominant payment method for the majority of transactions in Colombia by volume, even as digital payments grow. The Banco de la Republica (Colombia's central bank) estimates that cash is still used in over 80% of face-to-face retail transactions. Cash dominance is particularly pronounced in:
- Rural areas
- Informal markets and street vendors
- Small towns
- Transportation (buses, taxis outside of apps)
- Tiendas de barrio (neighborhood shops, which represent a significant share of retail)

**Data signal**: Invisible, same as everywhere. But in Colombia, "invisible" means the majority of transactions.

---

## 3. Remittance Flows as Economic Data

Remittances are not a peripheral data source for Venezuela and Colombia. They are a central economic flow.

### Venezuela

Venezuela receives an estimated $3-5 billion per year in remittances, though exact figures are unreliable because a large share flows through informal channels. The Venezuelan diaspora -- estimated at 7-8 million people, primarily in Colombia, Peru, Chile, the US, and Spain -- sends money home regularly.

Formal remittance channels:
- **Western Union** -- operates in Venezuela, though with limitations
- **Remitly, Wise (TransferWise), WorldRemit** -- digital remittance services that send to Venezuelan bank accounts
- **Zelle** -- as described above, functions as both a payment and remittance mechanism
- **Binance P2P** -- used for remittances by converting dollars to USDT, sending USDT, and having the recipient sell for bolivares on Binance P2P
- **Reserve app** -- stablecoin-based, was specifically marketed for Venezuelan remittances

Informal channels:
- Physical cash carried by travelers (especially on the Colombia-Venezuela border, where regular bus routes operate)
- Informal money transfer networks (similar to hawala systems) where a broker in Miami receives dollars and a partner in Caracas pays out bolivares
- Crypto transfers outside of major exchanges

**Data signal**: Formal remittance data is partially captured by the World Bank's bilateral remittance matrices, by central bank balance-of-payments data, and by the remittance companies themselves. The World Bank estimates total flows but with significant uncertainty for countries like Venezuela with large informal channels. Remittance volume, frequency, and geographic origin patterns are proxies for diaspora economic health, family dependency ratios, and labor market conditions in host countries.

Seasonality matters: remittances to Venezuela spike in December (holiday spending), around school enrollment periods, and during family emergencies. Tracking these seasonal patterns provides insight into household economic planning.

### Colombia

Colombia received approximately $10.5 billion in remittances in 2023, making it one of the top remittance-receiving countries in Latin America. The primary source countries are the US, Spain, Chile, and other Latin American countries.

Formal channels are better established and more dominant than in Venezuela:
- **Western Union, MoneyGram** -- large physical agent networks
- **Bancolombia (via Nequi), Davivienda (via Daviplata)** -- direct bank receipt
- **Digital platforms**: Remitly, Wise, WorldRemit

The Banco de la Republica publishes detailed remittance data with a lag of approximately 2-3 months, broken down by country of origin and recipient department (state). This is one of the best remittance datasets in Latin America.

**Data signal**: Colombia's formal remittance data is relatively strong. The challenge is incorporating informal flows, which are smaller as a percentage of total than in Venezuela but still significant, particularly along border regions.

---

## 4. What Transaction Data Can Measure in Latin America

Given the payment landscape described above, what can digital transaction data actually tell us?

### Formal Digital Economy Activity

Pago Movil volumes in Venezuela and Nequi/Daviplata/PSE volumes in Colombia provide a real-time pulse of formal digital economic activity. When Pago Movil transaction counts rise, more people are buying and selling through the banking system. When they fall, activity is contracting or migrating to other channels (cash, crypto).

This is not the same as measuring GDP. It measures the **banked, digital portion of economic activity**. But changes in this portion over time -- growth rates, seasonal patterns, shock responses -- are highly informative.

### Currency Preferences as an Economic Signal

In Venezuela, the ratio of bolivar transactions (Pago Movil) to dollar transactions (Zelle, crypto) is itself a macroeconomic indicator. When Venezuelans shift toward dollars, it signals declining confidence in monetary policy. When bolivar transaction volumes stabilize or grow relative to dollar alternatives, it may signal stabilization.

The Binance P2P bolivar/USDT spread over the BCV official rate is a daily, tradeable measure of monetary credibility. This is a signal that no government statistical agency publishes but that every Venezuelan who exchanges currency knows intimately.

### Price Signals Through Exchange Platforms

Crypto exchange data provides something that official statistics in Venezuela often cannot: reliable price signals. When the BCV publishes an official exchange rate that diverges from the Binance P2P rate, the Binance rate is the one that merchants use to set prices. Tracking the parallel rate through exchange platform data is tracking the actual pricing mechanism of the economy.

In Colombia, where the peso floats more freely and the gap between official and market rates is minimal, this signal is less critical. But cross-border exchange flows (peso/bolivar, peso/dollar) at border towns are still informative.

### Geographic Activity Patterns

Mobile payment data has geographic markers (bank branch, city, phone prefix). If accessible in aggregate form, this allows mapping economic activity intensity across regions -- something particularly valuable in Venezuela, where official regional economic statistics are essentially nonexistent.

---

## 5. What Transaction Data Misses

### The Informal Cash Economy

This is the single largest blind spot and it is enormous.

In Venezuela, street vendors (buhoneros), informal transport operators, domestic workers, day laborers, small-scale agriculture sellers, and a substantial portion of the service economy transact in physical cash -- primarily US dollars for anything above trivial amounts, and bolivares for the smallest transactions. None of this appears in any digital payment system.

In Colombia, the picture is similar. Tiendas de barrio (neighborhood corner stores, estimated at 250,000+ across the country), street food vendors, informal construction labor, domestic workers, and the vast informal transport sector operate predominantly in cash. Colombia's informal economy is estimated at 50-60% of total employment.

When digital transaction data shows "the economy," it is showing the formal, banked, digitized portion. In countries where 40-60% of economic activity is informal, this is a severe limitation.

### Street Vending and Micro-Commerce

A street vendor in Caracas selling arepas might do 50 transactions a day, all in cash (small bills, both dollars and bolivares). Total daily revenue might be $30-50. This vendor contributes to economic activity, employs themselves (and possibly family members), participates in supply chains (buying ingredients from wholesale markets), and serves consumer demand. None of this is captured.

Multiply this by the hundreds of thousands of informal vendors in Venezuelan and Colombian cities and the missing data is not marginal.

### Day Labor and Gig Work (Non-Platform)

Platform gig workers (Rappi riders in Colombia, for example) generate digital transaction trails. But the much larger pool of non-platform informal labor -- construction day workers, domestic cleaners paid in cash, informal mechanics, unlicensed taxi drivers -- generates no digital footprint.

### Barter and In-Kind Exchange

In the worst periods of Venezuela's crisis, barter became a real economic mechanism -- not metaphorically, but literally. People exchanged goods for goods. This has diminished as the dollar economy stabilized, but in-kind exchanges (labor for food, goods for services) still occur, particularly in rural areas and among the poorest populations.

---

## 6. Biases and Representativeness

The income bias problem with transaction data that exists in the United States is dramatically amplified in Venezuela and Colombia.

### Income Bias

In the US, the poorest 20% of the population still overwhelmingly has bank accounts and uses debit cards. The unbanked rate is approximately 4.5% (FDIC, 2021). The bias exists but is moderate.

In Venezuela, while bank account penetration is relatively high (Pago Movil pushed banking access), the quality of access varies enormously. Someone with a Banesco account and steady Pago Movil usage is visible. Someone earning cash dollars in the informal economy and spending cash dollars at informal vendors is completely invisible. The most economically precarious populations -- street vendors, day laborers, people in rural areas with unreliable phone service -- are the least visible in digital payment data.

In Colombia, the unbanked population is estimated at 10-15%, but "underbanked" (having an account but rarely using it for transactions) is much higher. Daviplata and Nequi have expanded access, but active digital payment usage still correlates strongly with income, education, and urbanization.

### The Poorest Are the Most Invisible

This is worth stating directly because it is the central representativeness problem for econOS in Latin America. The populations most in need of economic measurement -- the informal workers, the street vendors, the households surviving on cash remittances and day labor -- are the ones least captured by any digital transaction system. Building an economic measurement tool on digital payment data risks creating a system that measures the formal economy well and the informal economy not at all, which would systematically misrepresent economic reality in countries where informality is the norm, not the exception.

### Currency Bias

In Venezuela, measuring only bolivar-denominated transactions (Pago Movil, bank transfers) misses the dollarized economy. Measuring only dollar-denominated transactions (Zelle, crypto) misses the bolivar economy. The true picture requires combining both, with appropriate weighting that itself depends on estimates of dollarization levels.

### Platform Bias

Each payment platform has its own demographic skew:
- Nequi: younger, urban, middle-class Colombians
- Daviplata: lower-income, some rural, government transfer recipients
- Pago Movil: broad but skews toward those with stable banking relationships
- Zelle: Venezuelans with US bank access (a specific, non-representative subset)
- Binance P2P: tech-literate, typically younger, often with some dollar access

No single platform represents the economy. Any measurement system must combine multiple sources and explicitly model the biases of each.

---

## 7. Cost and Accessibility

Can the transaction data described above actually be obtained?

### Pago Movil / Venezuelan Banking System

The BCV publishes some aggregate statistics on interbank transactions, but the data is limited, irregularly updated, and not available through any API or structured feed. Individual banks (Banesco, Mercantil, Bancamiga) do not publish transaction volume data.

Venezuela's Superintendencia de las Instituciones del Sector Bancario (SUDEBAN) collects banking statistics, but public reporting is sparse and often delayed by months.

**Assessment**: Getting useful aggregate Pago Movil data would likely require either a direct institutional partnership with one or more Venezuelan banks, or access to BCV/SUDEBAN reporting that is currently not publicly available in usable form. This is a significant barrier.

### Nequi / Daviplata / Colombian Banking System

Colombia's Superintendencia Financiera publishes more regular and detailed banking statistics than Venezuela's equivalent. ACH Colombia publishes PSE transaction volumes. The Banco de la Republica publishes payment system statistics.

Bancolombia and Davivienda publish some aggregate data in quarterly reports and investor presentations. Nequi has published user count milestones but not detailed transaction data.

**Assessment**: Colombia's data environment is materially better than Venezuela's. Aggregate payment system data is obtainable through public sources. Granular data (by region, by transaction size, by merchant category equivalent) would require partnerships, but the institutional infrastructure for such partnerships exists.

### Crypto Exchange APIs

Binance provides a public API that includes some P2P trading data, though not comprehensive historical archives. Third-party sites have tracked P2P volumes by country (Useful Tulips tracked LocalBitcoins, Coin Dance tracks some exchanges). The bolivar/USDT pair on Binance P2P is trackable in near real-time.

**Assessment**: This is the most accessible data source for Venezuela. Crypto exchange data can be scraped, accessed via API, or obtained through third-party aggregators. It is not comprehensive, but it is real-time and accessible.

### Remittance Data

The World Bank publishes annual bilateral remittance estimates. The Banco de la Republica (Colombia) publishes quarterly remittance data by country of origin. Individual remittance companies do not publish transaction data, but some (Wise, for example) publish aggregate corridor data in transparency reports.

**Assessment**: Formal remittance data is available with moderate lag (quarterly to annual). Real-time remittance flow data would require partnerships with platforms like Remitly, Wise, or Western Union.

### Central Bank Reporting

The Banco de la Republica (Colombia) has a strong data publication program -- payment statistics, remittance data, monetary aggregates, and financial system reports are available through their website with structured data access.

The BCV (Venezuela) has historically published economic data but with increasing irregularity and credibility concerns. Basic monetary aggregates and some payment system data are published, but with significant lags and questions about reliability.

**Assessment**: Colombia's central bank is a viable data source. Venezuela's is not reliable for timely, granular transaction data.

---

## 8. Reference: How It Works in the US

For comparison, the US transaction data ecosystem is mature, deep, and expensive.

The US processes roughly 150-170 billion card transactions per year. Visa processed $14.8 trillion in payment volume in fiscal 2023; Mastercard processed approximately $8.9 trillion. The card networks do not sell raw transaction data but publish aggregated indexes: Visa Business and Economic Insights and Mastercard SpendingPulse provide spending trend data used by analysts and researchers.

A layer of fintech data aggregators -- Earnest Research (MarketAxess), Second Measure (Bloomberg), Yodlee (Envestnet), Plaid -- aggregate anonymized transaction data from banking partners. These products cost $100K-$500K+ per year and are used primarily by hedge funds and equity research.

Bank research arms (Bank of America Institute, JPMorgan Chase Institute) publish periodic analyses based on their internal transaction data, covering tens of millions of accounts each.

The landmark proof of concept was the Opportunity Insights Economic Tracker (Chetty et al., 2023), which used Affinity Solutions card data during COVID-19 to track real-time consumer spending by income group, geography, and category -- demonstrating that private transaction data, properly anonymized and aggregated, could provide economic insights faster and with more granularity than official statistics.

The US model is relevant as a reference point but is not directly replicable in Latin America. Card penetration, data provider ecosystems, and institutional norms around data sharing are fundamentally different. The lesson from the US is that transaction data works for economic measurement. The challenge in Venezuela and Colombia is that the transaction data infrastructure is different in kind, not just in degree.

---

## 9. The econOS Opportunity

The payment landscapes of Venezuela and Colombia, precisely because they are fragmented and unconventional, present an opportunity that is different from but potentially larger than the US case.

### Mobile Payments as the Backbone

In the US, econOS would need to negotiate with entrenched players (Visa, Mastercard, banks) who already monetize their data. In Venezuela, Pago Movil data is sitting in a banking system that has no existing data monetization infrastructure. The competitive dynamics are different. The barriers are institutional and political, not commercial.

If econOS can establish a data partnership with even one major Venezuelan bank -- Banesco, Mercantil, or Bancamiga -- it would gain access to a substantial share of formal domestic bolivar transactions. Combined with crypto exchange data (accessible via API) and remittance corridor data, this would constitute the most comprehensive real-time economic dataset for Venezuela in existence. There is no Bloomberg terminal, no Mastercard SpendingPulse, no Opportunity Insights tracker for Venezuela. The baseline is near zero.

In Colombia, the path is more conventional but still open. Nequi and Daviplata are growing fast and have not yet been fully leveraged for macroeconomic measurement. The Banco de la Republica already publishes good data. The opportunity is to integrate multiple Colombian data sources (Nequi/Daviplata volumes, PSE data, card data, remittance data, central bank statistics) into a unified real-time picture that currently does not exist in combined form.

### Multi-Source Integration

The real value proposition is not any single data source but the combination:

| Data Source | Coverage | Accessibility | Signal |
|---|---|---|---|
| Pago Movil (Venezuela) | Formal bolivar economy | Difficult -- requires bank partnerships | Domestic activity level |
| Zelle (Venezuela) | Dollarized formal transactions | Inaccessible from Venezuelan side | N/A without US-side data |
| Binance P2P (Venezuela) | Currency exchange, dollarization | Moderate -- API and scrapers | Exchange rate, dollarization demand |
| Nequi/Daviplata (Colombia) | Digital economy, younger/urban population | Moderate -- some public data, partnerships needed for granularity | Consumer spending, financial inclusion |
| PSE (Colombia) | Formal e-commerce | Good -- ACH Colombia publishes data | Online economic activity |
| Remittances (both) | Diaspora economic support | Moderate -- World Bank, central bank data, platform partnerships | External dependency, household income |
| Cash (both) | Informal economy | None | Blind spot |

### What "Real-Time Economic Measurement" Means Here

In the US, "real-time economic measurement" means beating the Census Bureau's retail sales report by two weeks. The improvement is marginal -- from a 14-day lag to a 1-day lag on an economic indicator that already exists.

In Venezuela, "real-time economic measurement" means producing economic indicators that do not currently exist in any reliable form. Venezuela has not published complete, credible GDP data in years. Inflation estimates come from independent sources (the National Assembly's finance commission, Ecoanalitica, the Johns Hopkins-Hanke index) rather than the BCV. Regional economic data is essentially nonexistent.

An econOS system that aggregates Pago Movil volumes, Binance P2P exchange data, and remittance flows would not be competing with existing statistics. It would be creating economic visibility where there currently is none. This is a fundamentally different value proposition than in developed markets.

### The Informal Economy Problem Is Not Solvable by Transaction Data Alone

This must be stated clearly. In economies where 40-60% of activity is informal and cash-based, digital transaction data cannot provide a complete picture. econOS in Venezuela and Colombia must be designed from the start to acknowledge and explicitly model the informal economy gap, using complementary approaches:

- Satellite imagery (nighttime lights, commercial activity indicators)
- Survey-based calibration (periodic informal economy surveys to estimate the digital-to-total activity ratio)
- Supply chain proxies (wholesale market volumes, import data for consumer goods)
- Mobile phone activity data (call/data usage as a general economic activity proxy)

Transaction data is the backbone, but it is not the whole skeleton.

### The Starting Point

Phase 1 for econOS in Venezuela should focus on what is immediately obtainable:

1. **Binance P2P bolivar/USDT data** -- accessible via API, provides daily exchange rate and volume signals
2. **Public central bank data** -- whatever the BCV and Banco de la Republica currently publish, standardized and integrated
3. **Remittance corridor data** -- World Bank annual data supplemented by whatever platform-level data can be obtained
4. **One banking partnership** -- a single Venezuelan or Colombian bank willing to share aggregate, anonymized transaction volume data

This is a minimal viable dataset. It does not solve the informal economy problem. It does not provide granular regional data. But it would produce something that does not currently exist: a structured, regularly updated, multi-source economic activity indicator for Venezuela.

That is the proof of concept.
