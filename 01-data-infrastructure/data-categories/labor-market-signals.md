# Labor Market Signals: Real-Time Labor Market Intelligence for Venezuela and Colombia

## 1. Why Labor Market Signals Have the Highest Allocation Impact

Of all the resource allocation decisions an economy makes, labor allocation is the most consequential. A machine placed in the wrong factory can be moved. Inventory shipped to the wrong warehouse can be redirected. Capital invested in the wrong asset can be sold. But a human being who spends five years in the wrong city, working in the wrong occupation, at a fraction of their productive potential -- that is a compounding loss that cannot be recovered. The years are gone.

Labor misallocation is the most expensive form of waste in any economy because it compounds over entire careers. A petroleum engineer selling empanadas in Maracaibo is not just losing today's wage differential between engineering work and street food. He is losing the human capital accumulation he would gain from practicing engineering, the professional network he would build, the promotions he would earn, the savings he would generate, and the contributions he would make to a sector that needs his skills. Multiply that by ten years and the lifetime cost is staggering. Multiply it by the hundreds of thousands of Venezuelans in similar positions and the cost to the economy is a measurable fraction of GDP.

This is not hypothetical. Venezuela's crisis produced the most visible mass labor misallocation event in modern Latin American history:

- **Doctors driving taxis.** Venezuelan physicians who trained for a decade earn more driving for hire in Lima or Bogota than practicing medicine in Caracas. Some who stayed switched to informal commerce entirely. The country hemorrhaged medical professionals while simultaneously facing a healthcare crisis.

- **Engineers selling street food.** PDVSA's collapse eliminated the single largest employer of technical talent in the country. Engineers, geologists, and skilled technicians who spent careers in the oil industry had no comparable employer remaining. Many transitioned to survival commerce.

- **Teachers earning starvation wages.** Public school teachers who remained in formal employment earned the equivalent of $3-10 per month at various points during the crisis. The rational economic response was to abandon the classroom for any informal work that paid more -- which was essentially everything. Those who stayed taught while simultaneously working second and third jobs to survive.

- **Nurses cleaning houses abroad.** Venezuelan nurses who migrated to Colombia, Peru, or Chile often could not get their credentials recognized. A nurse who would earn formal sector wages in a hospital instead earns informal wages cleaning houses -- not because she lacks the skill, but because she lacks the information, documentation, or connection to find the appropriate job.

These are not edge cases. They are the dominant labor market story of Venezuela over the past decade. And the underlying cause, in every case, includes an information failure: people did not know where the jobs were, what they paid, what the cost of living was at potential destinations, or whether their skills would be recognized.

### The Migration Decision as the Ultimate Allocation Choice

For the 7+ million Venezuelans who emigrated, the decision of where to go is the single highest-stakes economic allocation decision of their lives. It determines their income, their career trajectory, their children's education, and their family's economic future for years or decades.

Consider a 30-year-old Venezuelan nurse in Caracas in 2019, watching the economy collapse around her. She has a decision to make:

- **Stay in Caracas.** She keeps her social network, her apartment, her family nearby. But her formal salary is worthless, the hospital she works at lacks supplies, and the economy shows no signs of recovery.
- **Go to Bogota.** Colombia has a temporary protection framework for Venezuelans (ETPV). There are hospitals, there is demand for healthcare workers. But she does not know what nurses earn in Bogota, whether her Venezuelan nursing degree will be recognized, what rent costs in a neighborhood where she could live, or whether she would end up cleaning houses because the credential recognition process takes years.
- **Go to Lima.** Peru has absorbed millions of Venezuelans. The nursing labor market there might be different. But she knows even less about Lima than about Bogota.
- **Go to Santiago.** Chile is farther, more expensive to reach, but salaries are higher. The trade-offs are unclear.
- **Go to Miami.** If she has any connection to a US visa pathway, the wage differential is enormous. But so are the barriers.

Today, in 2026, this nurse makes this decision based on what her cousin told her, what she read in a WhatsApp group, and what she heard from a friend of a friend who went to Bogota two years ago. She is making a decision that will shape the next decade of her life based on anecdote and rumor, because no systematic information exists to help her.

**This is the killer use case for econOS.** Not an academic exercise in economic measurement. A tool that helps real people make the most important economic decision they will ever face, with actual data instead of word-of-mouth.

### The Compound Cost of Getting It Wrong

When the nurse goes to the wrong city, the cost is not just her lost income differential. It cascades:

- She earns less, so she sends smaller remittances home, so her family in Caracas has less to invest in her younger brother's education.
- She is underemployed, so she does not build the professional capital she would accumulate in a well-matched position, so her earnings trajectory is permanently lower.
- She occupies a low-skill job in the destination economy that a local worker could fill, while a nursing position elsewhere goes unfilled. Two labor markets are simultaneously worse off.
- Her negative experience (or her silence about a mediocre outcome) feeds back into the information network. The next nurse in Caracas hears that "Bogota didn't work out" and makes a different decision based on a single anecdote -- possibly an even worse one.

At the scale of 7 million emigrants, these compounding micro-misallocations add up to a macro-level drag on both Venezuela's diaspora productivity and the receiving countries' labor market efficiency. The aggregate cost is not calculable with precision, but it is enormous.

### Why This Is the Proving Ground for econOS

If econOS can demonstrably improve labor matching -- fewer people in the wrong city doing the wrong thing for the wrong wage -- then the core thesis is proven at the level of the economy's most important and most expensive resource. Labor is not one allocation problem among many. It is the allocation problem. An economy is, in the end, nothing more than what its people do with their time and skills. If you improve that allocation, everything else follows.

---

## 2. What We Need to Measure

To construct labor market intelligence that actually helps a Venezuelan nurse decide where to work, or a Colombian employer find the skills they need, or a student choose what to study, we need six categories of information, updated as continuously as possible.

### 2.1 Labor Demand by Sector and Geography

The most basic question: **where are the jobs?**

This means tracking, by city and by occupation/sector:
- How many open positions exist (or are being created)
- What sectors are hiring (healthcare, construction, technology, retail, logistics)
- Whether demand is growing or shrinking
- Whether the demand is formal (with contracts, benefits) or informal (day labor, gig work, self-employment opportunities)

For Venezuela, where the formal labor market collapsed and is unevenly recovering, demand signals are particularly sparse. For Colombia, where the formal sector is functional but nearly half of employment is informal, demand is partially visible but fundamentally incomplete.

### 2.2 Wage Levels by Occupation and City

Knowing that there are nursing jobs in Bogota is not enough. The nurse needs to know: **what do they pay?**

Wage data must be:
- Occupation-specific (a nurse, not "healthcare workers" as a category)
- City-specific (Bogota wages are different from Cucuta wages)
- Disaggregated by formality (formal wages vs. informal wages, which can differ by 2-3x)
- Denominated in meaningful terms (in Venezuela, wages must be expressed in dollar equivalents because bolivar figures are unintelligible without an exchange rate)
- Current (wage data from 2023 may be wildly outdated in a rapidly changing economy)

### 2.3 Cost of Living by City

A $600/month nursing salary in Bogota means something very different from a $600/month salary in Caracas. The wage only matters relative to what it buys.

Cost of living must be tracked at the city level across:
- Rent (the single largest expense for a migrant, and the most geographically variable)
- Food (basic basket costs)
- Transportation (commuting costs, which vary dramatically by city size and infrastructure)
- Utilities (electricity, water, phone/internet)
- Healthcare (out-of-pocket costs, which vary by country and insurance status)
- Education (if the worker has children)

The output metric is **real wages**: nominal wage minus cost of living, producing an estimate of actual purchasing power in each city. This is the number that matters for migration decisions.

### 2.4 Skills in Demand vs. Skills Available

The structural question: **what does the economy need that it doesn't have, and what does it have that it doesn't need?**

Skills mismatch measurement requires:
- What skills employers are requesting (visible in job postings)
- What skills the workforce possesses (visible in education data, professional registries, LinkedIn profiles)
- Where the gaps are (occupations with high demand and low supply, or high supply and low demand)
- How gaps vary by geography (a surplus of lawyers in Caracas and a shortage of electricians in Maracaibo are two different problems)

For the migration context, skills mismatch also includes **credential recognition**: a Venezuelan doctor has medical skills, but if Peru does not recognize her degree, she has zero formal medical skills in the Peruvian labor market. The gap between what a person can do and what the destination economy will let them do is itself a measurable friction.

### 2.5 Informal Economy Labor Conditions

The informal economy is not a footnote. It is where 40-60% of Venezuelans and nearly half of Colombians actually work. Ignoring it means ignoring the labor market reality for the majority.

What we need to know about informal labor:
- What kinds of informal work are available (street vending, domestic work, construction day labor, motorcycle taxi, gig platforms)
- What informal work actually pays (daily earnings, not monthly salaries, because informal work is often intermittent)
- What the working conditions are (hours, physical risk, instability)
- How informal earnings compare to formal employment for equivalent skill levels
- What the pathway from informal to formal looks like (is it possible? how long does it take? what does it require?)

This is the hardest category to measure because informal labor is, by definition, unregistered and largely invisible to digital systems. But it is also the most important for the populations who need econOS most.

### 2.6 Migration Flows and Outcomes

For the Venezuelan context specifically, migration is not a side topic. It is the central labor market event of the past decade.

Migration intelligence requires:
- Where Venezuelans are going (destination countries and cities, updated frequently)
- How they are doing economically once they arrive (employment rates, wages, formality status)
- What the legal pathway looks like (temporary protection, work permits, residency, citizenship timelines)
- How large the existing community is at each destination (community size affects job-finding, housing, and social support)
- What the return migration patterns look like (are people coming back to Venezuela? from where? why?)

---

## 3. Available Data Sources: Demand Side

### 3.1 Job Posting Platforms

Job posting platforms are the most accessible source of real-time labor demand data. They are imperfect, biased, and incomplete -- but they exist, they update daily, and they can be scraped.

**Computrabajo (computrabajo.com)**

Computrabajo is the dominant job board in Latin America. It operates in 19 countries, with particularly strong presence in Colombia (computrabajo.com.co), Venezuela (computrabajo.com.ve), Peru, Chile, Mexico, and Argentina. For the econOS labor market use case, Computrabajo is the single most important platform.

What Computrabajo provides:
- Job listings by city, sector, and occupation
- Required qualifications and experience levels
- Salary ranges (included in a meaningful minority of postings -- perhaps 30-40% in Colombia, less in Venezuela)
- Company names (which allows tracking of hiring activity by employer type and size)
- Posting dates (which allows tracking demand changes over time)

Computrabajo's coverage skews toward formal-sector, entry-to-mid-level positions. Administrative assistants, accountants, salespeople, call center operators, warehouse workers, and similar roles are heavily represented. Executive-level positions and highly technical roles are underrepresented relative to LinkedIn. Informal economy work is almost entirely absent.

In Colombia, Computrabajo is robust. Bogota alone typically has tens of thousands of active listings. Medellin, Cali, Barranquilla, and other major cities have thousands each. The platform captures a real cross-section of formal labor demand.

In Venezuela, Computrabajo coverage is thinner but growing as the economy partially recovers. Caracas listings dominate, with smaller numbers in Valencia, Maracaibo, and Barquisimeto. The Venezuelan recovery has created pockets of genuine formal hiring -- retail, food service, banking, telecommunications -- that are visible on the platform.

**Methodology for scraping:** Computrabajo listings can be collected through web scraping (the site does not have a public API), with daily or weekly collection cycles. Each listing should be parsed for: job title, sector, location (city, state), salary (if listed), experience level, education requirement, posting date, and company. Over time, this produces a panel dataset of labor demand that can be analyzed for trends, geographic shifts, and sectoral composition.

**elempleo.com (Colombia-specific)**

elempleo.com is the second-largest job platform in Colombia, with significant market share particularly among larger employers and more established companies. It tends to have higher representation of professional and managerial roles than Computrabajo. The combination of Computrabajo and elempleo.com covers the majority of formally posted jobs in Colombia.

**LinkedIn**

LinkedIn's penetration in Latin America has grown significantly. In Colombia, LinkedIn has an estimated 14-16 million members (in a country of 52 million), making it one of the most LinkedIn-active countries in Latin America. In Venezuela, penetration is lower but not negligible, and the diaspora is heavily represented.

LinkedIn data is valuable for:
- Professional and technical job postings (engineers, developers, analysts, managers)
- Skills demand signals (LinkedIn's "Skills in Demand" features and jobs data)
- Diaspora workforce profiles (Venezuelan professionals abroad list their skills, locations, and employment status)
- Salary insights (LinkedIn Salary, though coverage in Latin America is limited)

LinkedIn's limitation is its extreme skew toward formal, professional, educated, and urban workers. It tells you nothing about the informal economy. But for the professional labor market -- where some of the most painful misallocation occurs (the doctor driving a taxi) -- it is irreplaceable.

**Indeed (indeed.com)**

Indeed operates in both Colombia and Venezuela, aggregating postings from company career pages, other job boards, and direct employer submissions. Its coverage overlaps significantly with Computrabajo and elempleo.com but adds some unique listings, particularly from multinational companies posting across regions.

**Facebook Groups and Facebook Marketplace**

This is the unconventional source, and in the Venezuelan context, one of the most important.

Facebook is the dominant social media platform in Venezuela, with estimated penetration of 50-60% of the adult population. Venezuelan Facebook groups dedicated to employment are massive:
- Groups like "Empleos en Caracas," "Trabajo en Maracaibo," "Ofertas de Empleo Venezuela" have hundreds of thousands of members each.
- These groups contain a mix of formal job postings (employers or recruiters sharing openings), informal job offers (someone needing a house painter, a plumber, a nanny), and job-seeking posts (individuals describing their skills and availability).
- Unlike formal platforms, Facebook groups capture some of the informal and semi-formal labor market. A post offering $20/day for construction help is informal labor demand that would never appear on Computrabajo.

Scraping Facebook groups raises ethical and legal questions (discussed in Section 8), but the data they contain is genuinely unique: a window into the informal labor matching process that is invisible everywhere else.

In Colombia, Facebook job groups exist but are less central to the labor market because formal platforms (Computrabajo, elempleo.com) are more established and the formal economy is larger.

**WhatsApp Groups**

WhatsApp is the primary communication platform in both Venezuela and Colombia, and a significant amount of job referral and informal hiring happens through WhatsApp groups and individual messages. This data is essentially inaccessible for systematic collection -- WhatsApp is encrypted and private. It represents a known blind spot.

### 3.2 Gig Economy Platforms

Gig economy platforms provide a specific, visible window into a type of labor demand that sits between formal employment and pure informality.

**Rappi (Colombia, expanding regionally)**

Rappi is the dominant delivery and gig platform in Colombia, with operations also in Mexico, Brazil, Chile, Argentina, and Peru. In Colombian cities, Rappi riders (rappitenderos) are ubiquitous. The platform provides data signals on:
- Volume of delivery demand (a proxy for consumer spending and restaurant/retail activity)
- Number of active riders (a proxy for gig labor supply)
- Rider earnings (a proxy for informal gig wages)

Rappi does not publish granular data, but aggregate signals (delivery times as a proxy for rider availability, visible rider density in cities) provide indirect information.

**Uber and DiDi (ride-hailing)**

Uber operates in Colombia (major cities), and DiDi has entered the Colombian market. In Venezuela, Uber does not formally operate, but informal ride-hailing and car services exist through WhatsApp and direct referral. Ride-hailing platform activity in Colombia provides signals on both driver labor supply and consumer demand for transportation.

**PedidosYa (Colombia) and Yummy (Venezuela)**

Food delivery platforms that provide similar signals to Rappi. Yummy is the most prominent delivery platform operating within Venezuela.

**What gig platforms reveal:**

Gig platform activity is valuable not as a measure of total labor demand but as a **real-time indicator of economic activity** and as a measure of the "reservation wage" for informal workers. When Rappi is paying well and riders are scarce, it suggests the broader informal labor market is tight. When riders are abundant and deliveries are slow, it suggests surplus labor. The platforms themselves become thermometers of the informal labor market temperature.

### 3.3 Government and Institutional Job Listings

**Colombia:**
- The Servicio Publico de Empleo (SPE, Colombia's public employment service) posts vacancies and provides some aggregate labor market data. The SPE website (serviciodeempleo.gov.co) has job listings that can be scraped.
- Government entity hiring (convocatorias) is posted on various government websites and through the Funcion Publica portal.
- SENA (Servicio Nacional de Aprendizaje), Colombia's national vocational training institution, posts apprenticeship and training-linked employment opportunities.

**Venezuela:**
- There is no functioning public employment service. Government hiring in Venezuela is politicized and often occurs through partisan networks (carnet de la patria system) rather than open postings. This data is effectively inaccessible and unreliable as a market signal.

### 3.4 What Demand-Side Data Captures and What It Misses

| Source | What It Captures | What It Misses |
|--------|-----------------|----------------|
| Computrabajo/elempleo | Formal, posted, entry-to-mid-level demand | Informal economy, word-of-mouth hiring, executive roles |
| LinkedIn | Professional/technical demand, diaspora profiles | Non-professional work, informal economy |
| Facebook Groups | Semi-formal and some informal demand, job-seeking behavior | Cash-only day labor, illegal employment |
| Gig platforms (Rappi, Uber) | Platform gig demand, real-time activity | Non-platform informal gig work (the vast majority) |
| Government listings | Public sector formal demand | Politicized hiring, patronage employment |

The critical gap: **the majority of labor market matching in Venezuela and a large share in Colombia happens through personal networks, word-of-mouth, and physical presence** (showing up at a construction site, asking at a shop, knowing someone who knows someone). This is the invisible labor market that no digital source can fully capture. But the digital sources, combined, can illuminate the formal and semi-formal segments and provide directional signals about the broader market.

---

## 4. Available Data Sources: Supply Side

### 4.1 University Enrollment and Graduation Data

What skills are being produced? University systems are the primary pipeline for formal human capital.

**Venezuela:**
- The Ministerio de Educacion Universitaria, Ciencia y Tecnologia theoretically publishes enrollment and graduation statistics, but data availability has been erratic since the crisis began.
- ENCOVI (the independent household survey) has collected education data including enrollment by field.
- Key universities (UCAB, USB, UCV, LUZ) publish some enrollment data, but aggregation is difficult.
- The brain drain complicates interpretation: many enrolled students left the country before graduating, and many recent graduates emigrated immediately.
- Known oversupply: Venezuela historically overproduced lawyers, social communicators, and some business administration graduates relative to market demand. Known undersupply (post-crisis): technical trades, healthcare workers (many emigrated), oil sector engineers (PDVSA collapse dispersed them).

**Colombia:**
- The Sistema Nacional de Informacion de la Educacion Superior (SNIES), operated by the Ministerio de Educacion Nacional, publishes detailed enrollment and graduation data by institution, program, and field of study.
- The Observatorio Laboral para la Educacion (OLE) tracks graduate employment outcomes, including earnings and formality status by degree program. This is one of the best graduate-outcome tracking systems in Latin America.
- SENA publishes data on vocational and technical training enrollment and completion.

Colombia's education data infrastructure is genuinely useful. The OLE in particular provides a direct link between educational investment and labor market outcomes -- exactly the kind of human capital allocation signal that econOS needs.

### 4.2 Migration Statistics

The supply of Venezuelan labor in any given destination is determined by migration flows.

**UNHCR/IOM R4V Platform (r4v.info)**

The Inter-Agency Coordination Platform for Refugees and Migrants from Venezuela publishes periodic estimates of the Venezuelan population in each destination country and city. The latest figures (updated regularly but with some lag) place:
- Colombia: ~2.9 million
- Peru: ~1.5 million
- United States: ~1.0 million+ (estimates vary widely)
- Ecuador: ~475,000
- Chile: ~440,000
- Brazil: ~510,000
- Spain: ~400,000+
- Argentina: ~220,000

These are estimates, not census counts. The actual numbers are likely higher because undocumented migrants avoid registration.

**Colombian migration authorities (Migracion Colombia)**

Migracion Colombia publishes border crossing data, temporary protection permit (ETPV/PPT) issuance numbers, and some demographic information about the Venezuelan population. This is the most granular source on Venezuelan migration to any single destination country. As of recent reporting, approximately 2.4 million Venezuelans had applied for or received the Estatuto Temporal de Proteccion (Temporary Protection Status).

**DANE migration modules**

DANE has conducted specific GEIH migration modules that survey Venezuelan migrants on employment status, occupation, earnings, education, and legal status. This is the best survey source on Venezuelan migrant labor market outcomes in Colombia.

**Destination country statistical agencies**

Peru (INEI), Chile (INE Chile), Ecuador (INEC), and Brazil (IBGE) have varying levels of migration data. Most conducted special censuses or surveys during the peak of Venezuelan migration.

### 4.3 Social Media as Labor Supply Signal

**LinkedIn profiles**

LinkedIn profiles of Venezuelan professionals provide a large-scale, self-reported dataset on:
- Where the diaspora workforce is located (current city)
- What skills and occupations they claim
- What employment status they report (employed, seeking, freelancing)
- How skills match to their current work (an engineer listing their current role as "delivery driver" is visible misallocation)

This data is biased toward educated, professional workers. But for the professional labor supply question -- where are Venezuela's doctors, engineers, teachers, and accountants? -- LinkedIn is the closest thing to a real-time registry.

**Facebook job-seeking groups**

The inverse of demand-side Facebook groups: individuals posting their skills and availability. Groups like "Venezolanos en Bogota - Empleo" or "Venezolanos en Lima - Trabajo" contain thousands of posts from people describing their qualifications and seeking work. The volume and composition of these posts provide a real-time signal of labor supply in each destination city.

### 4.4 Remittance Patterns as Diaspora Distribution Proxy

Remittance flows to Venezuela -- estimated at $3-5 billion annually -- are a proxy for where the diaspora workforce is and how it is doing economically.

The logic: if remittances from Colombia to Venezuela increase, it means more Venezuelans in Colombia are earning enough to send money home. If remittances from Chile to Venezuela decline, it may mean Chilean economic conditions are worsening for Venezuelan workers.

The World Bank's bilateral remittance matrix, the Banco de la Republica's inbound remittance data (for Colombia), and platform-level data from Remitly, Wise, and Western Union provide partial visibility into these flows.

Remittance volume by source country is an indirect but meaningful measure of diaspora labor market conditions -- the employed send money, the unemployed do not.

---

## 5. Available Data Sources: Wages and Cost of Living

### 5.1 Job Posting Wage Data

A meaningful minority of job postings on Computrabajo, elempleo.com, and LinkedIn include salary ranges. In Colombia, an estimated 30-40% of Computrabajo postings include some salary information. In Venezuela, the percentage is lower and complicated by dual-currency pricing (some salaries quoted in bolivares, others in dollar equivalents).

When collected systematically over time, posted salary data provides:
- Occupation-specific wage levels by city
- Wage trends (are salaries rising or falling for nurses in Bogota?)
- Formal-informal wage gaps (by comparing posted formal wages to survey-based or anecdotal informal earnings)
- Cross-country wage comparisons (what does the same job pay in Bogota vs. Lima vs. Santiago?)

**Limitations:** Posted wages may not reflect actual wages paid (employers may offer less after negotiation). They represent only the formal job market. And they may be inflated to attract applicants or deflated to manage expectations.

**Methodology:** Scrape all job postings with salary data, classify by standardized occupation code (ISCO or national equivalent), and compute distributions (median, 25th percentile, 75th percentile) by occupation and city. Update weekly or monthly. Over time, this produces the most granular wage dataset available for the formal labor market.

### 5.2 Salary Transparency Platforms

**Glassdoor (glassdoor.com)**

Glassdoor has growing Latin American coverage, particularly in Colombia, Mexico, and Brazil. Company-specific salary reports, contributed by employees, provide an independent check on posted wage data. Coverage in Venezuela is minimal.

**Indeed Salaries**

Indeed's salary tool aggregates self-reported and scraped salary data for various occupations and companies in Colombia. Useful as a supplementary source.

**Salary Explorer, PayScale, and similar aggregators**

Various salary comparison websites aggregate data for Latin American countries. Quality varies, but they provide a baseline for occupational wage levels.

**DANE GEIH earnings data (Colombia)**

DANE's household survey collects detailed earnings data for employed workers, broken down by occupation, sector, city, formality status, and education level. This is published in microdata form (available to researchers) and in summary tables. It is the authoritative benchmark for Colombian wage levels, though with a 30-45 day publication lag.

**ENCOVI earnings data (Venezuela)**

The annual ENCOVI survey collects earnings data, but the sample size limits occupational and geographic granularity. It provides the best available benchmark for Venezuelan wage levels, which is not saying much.

### 5.3 Cost of Living: Rent Data

Rent is the single most important cost of living variable for a migrant considering relocation. It is also highly scrapeable.

**FincaRaiz (fincaraiz.com.co) -- Colombia**

FincaRaiz is one of Colombia's two dominant real estate platforms (alongside Metrocuadrado). It lists rental properties across Colombian cities with rent prices, neighborhood, property type, and size. Scraping FincaRaiz over time produces:
- Median rent by city and neighborhood
- Rent trends (rising or falling, and how fast)
- Geographic rent gradients (how rent varies across a city)
- Housing affordability ratios (when combined with wage data)

**Metrocuadrado (metrocuadrado.com) -- Colombia**

The other major Colombian real estate platform, owned by El Tiempo media group. Similar data to FincaRaiz, valuable as a complementary source.

**MercadoLibre Inmuebles (inmuebles.mercadolibre.com.ve) -- Venezuela**

MercadoLibre is the dominant classifieds and e-commerce platform in Venezuela (and much of Latin America). Its real estate section lists rentals in Venezuelan cities with prices, typically in dollar equivalents. Coverage is concentrated in Caracas, Valencia, Maracaibo, and Barquisimeto.

Scraping MercadoLibre Inmuebles over time provides the best available rent data for Venezuelan cities, though coverage is incomplete (many rentals in Venezuela are arranged informally and never listed online).

**Facebook Marketplace and rental groups**

In both countries, Facebook is used extensively for rental listings, particularly at lower price points that may not appear on formal real estate platforms. Groups like "Arriendo en Bogota" or "Alquiler en Caracas" contain thousands of listings.

### 5.4 Cost of Living: Goods and Services Prices

The price-tracking work described elsewhere in econOS (see `modern-data-sources/transaction-data.md` and the proof-of-concept section) directly feeds the cost of living calculation.

**Web-scraped retail prices:**
- Venezuelan online retailers (MercadoLibre, Farmatodo online, supermarket chains): food basket costs, personal care, household goods
- Colombian online retailers (Exito, Jumbo, Alkosto, Rappi catalog prices): same categories
- These produce city-level price indexes for basic consumption goods

**Transport costs:**
- Uber/DiDi fare estimates (accessible through their apps or APIs) provide standardized per-kilometer transport costs in Colombian cities
- Informal transport fares in Venezuela (bus, por puesto) are trackable through social media and periodic surveys
- Gasoline prices (relevant for cities where private transport or motorcycle is primary)

**Utilities:**
- Electricity, water, and natural gas tariffs are published by regulators in Colombia (CREG, CRA) and are relatively stable
- In Venezuela, utility costs have been historically negligible due to subsidies, though this is slowly changing
- Mobile phone and internet costs are trackable through provider websites

**Healthcare costs:**
- Out-of-pocket healthcare costs vary dramatically between countries and by insurance/coverage status
- For Venezuelan migrants in Colombia, access to the healthcare system depends on ETPV/PPT status and EPS (health insurance) enrollment
- Pharmacy prices (scrapeable from Farmatodo, Cruz Verde, Drogueria online catalogs) provide a proxy for healthcare costs

### 5.5 The Constructable Metric: Real Wages by City

Combining wage data and cost of living data produces the metric that actually matters for migration decisions: **real wages** -- what a given occupation pays in a given city, adjusted for what it costs to live there.

Example construction:

| City | Nursing wage (median, formal) | Rent (1BR, basic) | Food basket (monthly) | Transport (monthly) | Real disposable income |
|------|------|------|------|------|------|
| Caracas | $120/month | $150 | $100 | $15 | -$145 |
| Bogota | $550/month | $250 | $180 | $60 | $60 |
| Lima | $480/month | $200 | $160 | $50 | $70 |
| Santiago | $750/month | $350 | $220 | $80 | $100 |
| Miami | $3,500/month | $1,800 | $400 | $150 | $1,150 |

These numbers are illustrative, not current. The point is the structure: when you can populate this table with real, current data for a specific occupation, you have produced something that no institution currently provides and that millions of people desperately need.

The real wage calculation should include:
- Nominal wage (from job posting data, salary surveys, DANE/ENCOVI benchmarks)
- Housing cost (from rent scraping)
- Food cost (from price scraping)
- Transport cost (from platform data and fare schedules)
- Taxes and social contributions (where applicable in the formal sector)
- Remittance cost (the transaction fee for sending money home, which varies by corridor and method)

The residual is **disposable income after basic costs and remittances** -- the number that determines whether a migration decision makes economic sense.

---

## 6. The Construction: A Real-Time Labor Market BI View

The data sources described in Sections 3-5 are raw inputs. The value of econOS is in combining them into something actionable. This section describes how to construct the labor market BI view: the "Where should I work?" dashboard.

### 6.1 Architecture

The system has four layers:

**Layer 1: Data Collection**
- Daily scraping of job platforms (Computrabajo, elempleo.com, LinkedIn, Indeed, Facebook Groups)
- Weekly scraping of rental platforms (FincaRaiz, Metrocuadrado, MercadoLibre Inmuebles)
- Continuous price monitoring (online retailers, from the price-tracking module)
- Periodic ingestion of institutional data (DANE GEIH releases, UNHCR migration estimates, remittance data)
- Gig platform signal collection (Rappi delivery times, ride-hailing availability)

**Layer 2: Standardization and Classification**
- Job postings classified by standardized occupation code (mapped to ISCO-08 or CIUO-08 Colombian adaptation)
- Wages normalized to monthly USD equivalent (critical for cross-country comparison, especially for Venezuela where bolivar wages require exchange rate conversion)
- Cost of living components standardized by city and updated with each new data collection cycle
- Geographic standardization (all data tagged to city, with neighborhood-level where available)

**Layer 3: Index Construction**
- **Labor Demand Index** by occupation and city: composite of job posting counts, posting growth rate, and posting-to-population ratio. Updated weekly.
- **Wage Index** by occupation and city: median posted wage, supplemented by Glassdoor/survey data where available. Updated monthly.
- **Cost of Living Index** by city: composite of rent, food basket, transport, and utilities. Updated monthly.
- **Real Wage Index** by occupation and city: wage index minus cost of living index. This is the core output.
- **Skills Gap Index** by occupation and city: ratio of demand (job postings) to estimated supply (LinkedIn profiles, graduation data, migration population). Identifies where there are more jobs than workers (opportunity) vs. more workers than jobs (saturation).
- **Migration Corridor Index**: for each origin-destination pair (e.g., Caracas-to-Bogota), a composite score incorporating job availability, real wages, legal pathway status, community size, and migration cost.

**Layer 4: User-Facing BI Views**
- Pre-computed dashboards for specific user personas (see Section 7)
- Filterable by occupation, current location, and target cities
- Uncertainty bands explicitly shown (not false precision)
- Source transparency (every number links to its data source and methodology)
- Updated at least monthly, with some components updating weekly or daily

### 6.2 The Matching Engine

The core function: given a user's profile (occupation, skills, current location, preferences), find the best labor market match across available cities.

Inputs from the user:
- Current occupation/skills (mapped to standardized classification)
- Current location
- Willingness to migrate (domestic only, regional, international)
- Priority weighting (maximum income vs. lowest cost vs. largest community vs. shortest legal pathway)

Outputs to the user:
- Ranked list of cities with estimated job availability, wage, cost of living, and real disposable income for their occupation
- Skills gap data (is their occupation in demand or saturated in each city?)
- Migration corridor information (how to get there, legal requirements, estimated transition cost and time)
- Comparable profiles (people with similar backgrounds who made similar moves -- what happened to them, based on survey data or social media signals)

This is not a recommendation engine in the prescriptive sense. It does not say "go to Bogota." It says "here is what we know about the labor market for nurses in Bogota, Lima, Santiago, and Miami. Here are the numbers, here are the uncertainties, here is what we can see and what we cannot. You decide."

### 6.3 Update Cadence and Freshness

Different data sources update at different frequencies. The BI system must handle this gracefully:

| Component | Update frequency | Source lag |
|-----------|-----------------|------------|
| Job posting counts | Daily-weekly | Near real-time |
| Posted wages | Weekly-monthly | Near real-time |
| Rent prices | Monthly | Listings reflect current market |
| Food/goods prices | Weekly | From price-tracking module |
| DANE GEIH labor data | Monthly | 30-45 day lag |
| ENCOVI Venezuela data | Annual | 6-12 month lag |
| Migration stock estimates | Quarterly-annual | Variable lag |
| Remittance flows | Quarterly | 2-3 month lag (Colombia) |

The system should display freshness metadata for every component: "Wage data last updated: March 15, 2026. Cost of living last updated: March 22, 2026. Migration estimates based on Q4 2025 R4V data." Users need to know what is current and what is stale.

### 6.4 Cross-Validation and Quality Control

With no single authoritative benchmark (especially for Venezuela), quality control relies on cross-validation between independent sources:

- **Wage cross-validation:** Do Computrabajo posted wages for a given occupation in Bogota roughly match Glassdoor reports? DANE GEIH survey earnings? If they diverge by more than 30%, flag for investigation.
- **Cost of living cross-validation:** Do FincaRaiz rents match Metrocuadrado rents for the same neighborhoods? Do online food prices match the DANE consumer price index for the same categories?
- **Demand cross-validation:** Do job posting trends on Computrabajo align with trends on elempleo.com? If one platform shows surging demand in healthcare and the other shows flat demand, the signal is ambiguous.
- **Migration data cross-validation:** Do R4V population estimates for Colombians cities align with DANE GEIH migration module findings? Migracion Colombia registration data?

Where sources agree, confidence is high. Where they diverge, uncertainty bands widen. The system should never present a single number without context about how confident that number is.

---

## 7. The Migration Decision Support Tool

This is the single most impactful application of the labor market intelligence system. It deserves detailed treatment because it addresses the specific, urgent, life-altering decision that millions of Venezuelans have faced and continue to face.

### 7.1 The Decision Framework

A Venezuelan in Caracas considering emigration faces a multi-variable optimization problem that they currently solve with almost no data:

**Option A: Stay in Caracas**
- Current income: known (probably low)
- Current cost of living: known (from daily experience)
- Social network: intact
- Risk: continued economic stagnation, political instability
- Required action: none (default)

**Option B: Move to Bogota**
- Expected income: unknown (what do people like me earn there?)
- Expected cost of living: unknown (what does rent cost? food? transport?)
- Social network: some (how large is the Venezuelan community?)
- Risk: legal status uncertainty, discrimination, starting over
- Required action: border crossing, documentation, job search, housing search
- Migration cost: bus fare, first months' rent, living expenses during job search

**Option C: Move to Lima**
- Same unknowns as Bogota, but for Peru
- Different legal framework (Peru has been less welcoming than Colombia recently)
- Different labor market conditions
- Farther, more expensive to reach

**Option D: Move to Santiago**
- Higher wages, higher cost of living
- More distant, more expensive migration
- Different legal pathway
- Smaller Venezuelan community (historically)

**Option E: Explore a US pathway**
- Vastly higher wages
- Extremely difficult legal pathway
- Very high migration cost and risk
- Large Venezuelan community in some cities (Miami, Houston)

The migration decision support tool provides, for each option, the best available data on every variable. Not perfect data -- the best available data, with explicit uncertainty.

### 7.2 What the Tool Shows

For a Venezuelan nurse in Caracas considering Bogota:

**Job availability:**
- Number of nursing job postings in Bogota this month: [number from Computrabajo/elempleo scraping]
- Trend: increasing/decreasing/stable over the past 6 months
- Comparison: how does nursing demand in Bogota compare to Lima, Santiago?
- Credential note: Colombia's process for recognizing Venezuelan nursing degrees requires [X steps, estimated Y months, Z cost] through the Ministry of Health and the relevant Secretaria de Salud

**Expected wage:**
- Median posted nursing wage in Bogota: COP [X] / USD [Y] per month
- Range: 25th-75th percentile [A-B]
- Source: [N] job postings collected between [date range]
- Context: this is formal sector. Informal nursing work (home care, etc.) pays approximately [estimate if available]

**Cost of living:**
- Median rent for 1-bedroom apartment in affordable Bogota neighborhoods (Kennedy, Suba, Bosa, Engativa): COP [X] / USD [Y]
- Estimated monthly food cost for single person: [estimate from price tracking]
- Monthly transport (TransMilenio/SITP): COP [X]
- Total estimated basic monthly costs: [sum]

**Real economic position:**
- Estimated monthly disposable income after basic costs: [wage minus costs]
- Estimated remittance capacity: [disposable income minus personal expenses]
- Compare to current disposable income in Caracas: [if available]

**Community and support:**
- Estimated Venezuelan population in Bogota: [from Migracion Colombia/DANE data]
- Key neighborhoods with Venezuelan concentration: [from reports, community data]
- Venezuelan community organizations, churches, and support networks: [from publicly available information]

**Legal pathway:**
- Current status of ETPV/PPT (Temporary Protection Status): [current policy]
- Application process: [summary]
- Work authorization: [what the permit allows]
- Pathway to longer-term residency: [if applicable]

**Migration logistics:**
- Typical travel method and cost from Caracas to Bogota: [bus via Cucuta, approximate fare, travel time]
- Estimated setup cost (first month's rent, deposit, basic supplies): [estimate]
- Estimated time from arrival to first paycheck: [based on reported job search durations]

### 7.3 What Makes This Different from What Exists

Today, a Venezuelan considering migration can find:
- Anecdotal advice in WhatsApp groups and Facebook groups
- UNHCR/IOM informational guides that describe legal processes but not labor market conditions
- News articles about Venezuelan migration (usually focused on crisis narrative, not actionable economic data)
- Word-of-mouth from people who already migrated (useful but unsystematic, subject to survivorship bias)

What does not exist:
- A systematic comparison of labor market conditions by occupation across destination cities
- Real-wage calculations that account for cost of living differences
- Updated, occupation-specific job availability data for multiple cities
- A tool that combines all relevant decision variables in one view
- Anything that updates more frequently than annually

The migration decision support tool is not technologically exotic. It is a combination of web scraping, data standardization, and a basic BI interface. The components exist. The data sources exist. What does not exist is someone combining them into the tool that millions of people need.

### 7.4 Scale of Impact

Consider the following back-of-envelope calculation:

- 7+ million Venezuelans have emigrated
- Suppose 10% (700,000) made a significantly suboptimal location/occupation choice due to information failure -- went to a city where they earned 30% less than they would have in a better-matched destination
- Average annual income for these workers: $6,000 (a rough estimate for informal Venezuelan migrant workers in Latin America)
- Annual misallocation cost per person: $1,800 (30% of $6,000)
- Total annual cost of labor misallocation for this population: **$1.26 billion per year**

This is a rough estimate with wide uncertainty bands. But the order of magnitude is plausible. And it excludes:
- The millions who stayed in Venezuela in suboptimal employment because they didn't know what was available elsewhere
- The compounding cost over careers (10 years of $1,800/year misallocation is $18,000 per person)
- The productivity loss to destination economies from underemployment (a nurse cleaning houses instead of nursing)
- The knock-on effects on families, children's education, and community development

Even if the true number is a fraction of this estimate, it represents an enormous, addressable economic loss. And the cost of building the tool to address it is trivial by comparison -- a few engineers, a web scraping infrastructure, and a BI interface.

---

## 8. Limitations: What We Cannot See

Intellectual honesty requires a clear-eyed assessment of what this system cannot do.

### 8.1 The Informal Labor Market Remains Largely Invisible

The most critical limitation. In Venezuela, 40-60% of employment is informal. In Colombia, ~47%. This means the majority of the labor market operates through personal networks, physical presence, cash transactions, and word-of-mouth. No amount of job platform scraping can capture the day laborer who gets hired because he showed up at a construction site at 6 AM, or the domestic worker who found a family through a neighbor's recommendation.

What we can do:
- Use formal-sector data as a directional signal (if formal nursing demand in Bogota is growing, informal demand probably is too)
- Use gig platform data as a bridge (Rappi riders are semi-formal and generate data that correlates with broader informal activity)
- Use social media and Facebook group data to capture some semi-formal and informal market activity
- Use payment platform data (Pago Movil, Nequi) as a general economic activity proxy that captures some informal transactions

What we cannot do:
- Measure cash-only day labor
- Count informal job openings that are never posted anywhere
- Track wages paid in physical dollars from hand to hand
- Provide real-time data on the street vending economy, domestic work, or informal transport

The system should be explicit about this gap. Every BI view should include a note: "This data reflects the formal and semi-formal labor market. Approximately [X]% of employment in this city is informal and not captured by these sources."

### 8.2 Digital Platform Bias

Every data source skews toward certain populations:

- **Job platforms (Computrabajo, LinkedIn):** Skew toward educated, urban, formal-sector workers. A Colombian with a university degree searching for accounting work is well-represented. A Venezuelan without legal status looking for construction day labor is invisible.
- **Social media (Facebook, Instagram):** Skew toward younger, more connected populations. Older workers, rural workers, and the poorest populations are underrepresented.
- **Salary platforms (Glassdoor):** Skew toward formal-sector employees at established companies. Informal wages are unmeasured.
- **Rental platforms (FincaRaiz):** Skew toward formal rental market. Informal housing (shared rooms, subletting, informal settlements) is underrepresented.

The net effect: the system will be most accurate for the formal, educated, urban labor market and least accurate for the informal, less-educated, rural or peri-urban labor market. This is a serious equity concern. The people with the least access to information are also the people the system serves worst.

Mitigation strategies:
- Explicitly model and communicate the bias
- Supplement digital data with periodic surveys (partnering with ENCOVI, DANE migration modules, or conducting targeted surveys of informal workers)
- Use cross-validation with aggregate statistics that cover informal populations (DANE's informality measures, ENCOVI data)
- Design the system to flag when a user's profile suggests they are in a segment poorly covered by the data

### 8.3 Underemployment and Skills Mismatch Are Hard to Measure

The system can estimate whether nursing jobs exist in Bogota and what they pay. It is much harder to measure:
- How many of those posted jobs actually result in hires
- How many Venezuelans apply and are rejected due to credential issues
- How long the job search takes
- What percentage of qualified Venezuelan nurses in Bogota are actually working as nurses vs. doing survival work
- The psychological and social dimensions of occupational downgrading

The mismatch between skills held and skills utilized -- the doctor-driving-a-taxi phenomenon -- is visible in aggregate through surveys (DANE, ENCOVI) but not measurable in real time through digital data alone.

### 8.4 Credential Recognition Is a Non-Data Problem

One of the most painful labor market frictions for Venezuelan migrants is credential recognition. A Venezuelan doctor's medical degree is not automatically valid in Colombia, Peru, or Chile. The process for recognition involves paperwork, fees, exams, and time that can stretch from months to years.

This is not an information problem that econOS can solve by providing better data. It is a regulatory and institutional barrier. But econOS can:
- Document the credential recognition process for each destination country and occupation
- Estimate the time and cost of recognition based on reported experiences
- Factor credential recognition status into the migration decision tool (distinguishing between "jobs available if credentials are recognized" and "jobs you can actually get right now")

### 8.5 Privacy and Ethical Considerations

Building labor market intelligence from scraped data raises legitimate privacy concerns:

- **Job seeker privacy:** People posting their skills and job-seeking status on Facebook groups may not expect that information to be systematically collected and analyzed.
- **Migrant vulnerability:** Venezuelan migrants, particularly those without legal status, may face risks if their location, employment status, or job-seeking behavior is visible to authorities (Venezuelan, Colombian, or other).
- **Employer data:** Companies posting jobs may not want their hiring patterns systematically tracked.

Design principles:
- All data is aggregated and anonymized. Individual job seekers are never identified.
- No individual-level data is stored or displayed. All outputs are statistical: "there are approximately X nursing jobs in Bogota with a median wage of Y."
- Data collection adheres to platform terms of service where feasible, and uses public information only.
- The system does not share data with any government or law enforcement entity.
- Venezuelan migrants' data is treated with particular care given their vulnerability.

### 8.6 Political Sensitivity

In Venezuela, economic data is politically sensitive. A system that shows, with real-time data, that 60% of workers earn below subsistence, or that the formal labor market has not recovered, could be viewed as politically threatening by the government. This is not a hypothetical concern -- the Venezuelan government suppressed its own statistical agency's output for years.

In Colombia, the political sensitivity is lower but not zero. Data on Venezuelan migrant employment could be used to fuel anti-immigrant sentiment.

Design principles:
- Present data factually, without political framing
- Avoid government dependency (the system should not rely on any government for data access or permission)
- Distribute the system openly so that suppression is difficult
- Be transparent about methodology so that politically motivated criticism can be addressed with evidence

---

## 9. What This Proves for Allocation

If econOS can build and deploy the labor market intelligence system described in this document, it proves the core econOS thesis at the most important level.

### 9.1 The Micro-Level Proof

A Venezuelan nurse who uses the migration decision tool and chooses Bogota over Lima because the data shows better real wages for nursing in Bogota -- and who, six months later, is employed as a nurse earning the predicted wage -- is a single data point proving that better information produces better allocation. Multiply this by thousands of users and the aggregate allocation improvement is measurable.

### 9.2 The Meso-Level Proof

If the skills gap analysis shows a shortage of electricians in Medellin and this information reaches SENA (Colombia's vocational training system) or a private training provider, and they open an electrician training program in Medellin, and those graduates find employment -- that is the human capital allocation channel working. Information about demand reshaped the supply of skills.

### 9.3 The Macro-Level Proof

If labor market intelligence reduces the average duration of job search for Venezuelan migrants in Colombia -- measurable through DANE's GEIH migration modules over time -- the aggregate productivity gain is enormous. Every month of unemployment or underemployment for a million workers is roughly $500 million in lost output (at even modest wage assumptions). Cutting average job search duration by one month through better matching produces gains measured in hundreds of millions of dollars.

### 9.4 The Information Thesis in One Sentence

The Venezuelan labor crisis is not primarily a shortage of skills or a shortage of jobs. It is a shortage of information connecting the skills to the jobs. econOS fills that gap.

---

## 10. Implementation Priorities

### Immediate (0-3 months)

1. **Begin scraping Computrabajo** for Venezuela and Colombia. Daily collection of all job postings in major cities, parsed into standardized fields (occupation, city, wage, requirements). This is the single most actionable data collection step and requires only standard web scraping infrastructure.

2. **Begin scraping rental platforms** -- FincaRaiz and Metrocuadrado for Colombia, MercadoLibre Inmuebles for Venezuela. Monthly collection, parsed into city/neighborhood/price/type fields.

3. **Aggregate existing institutional data** -- DANE GEIH latest releases, UNHCR R4V latest migration estimates, World Bank remittance data, OLE graduate outcome data for Colombia. Consolidate into a standardized reference dataset.

4. **Construct a pilot real-wage comparison** for 5 occupations (nurse, engineer, accountant, teacher, software developer) across 5 cities (Caracas, Bogota, Lima, Santiago, Miami). Even rough estimates prove the concept.

### Short-term (3-6 months)

5. **Expand job scraping** to LinkedIn, elempleo.com, Indeed, and Facebook Groups (with appropriate ethical review for the last).

6. **Build the standardized occupation classifier** mapping job titles across platforms and countries to a common taxonomy.

7. **Integrate price-tracking data** from the consumer goods scraping module to produce automated cost of living indexes by city.

8. **Publish the first migration decision comparison** as a simple web tool: "Compare labor market conditions for [occupation] in [city A] vs. [city B]."

### Medium-term (6-12 months)

9. **Build the skills gap analysis** combining job demand data with education data (OLE, SNIES for Colombia; ENCOVI, university data for Venezuela) and migration population estimates.

10. **Add gig economy signals** -- Rappi and Uber data integration for real-time activity indicators.

11. **Develop the full migration decision support tool** with the multi-variable comparison described in Section 7.

12. **Validate against DANE GEIH** -- compare econOS labor demand and wage estimates to DANE's survey-based measures. Quantify the correlation and the divergences. Publish the methodology paper.

### Ongoing

13. **Maintain data freshness** -- the system is only valuable if it stays current. Job postings stale within weeks. Rent prices change monthly. The scraping infrastructure must run continuously.

14. **Expand city coverage** -- add Peruvian, Chilean, Ecuadorian, and Brazilian cities as destination comparisons.

15. **Build the feedback loop** -- survey users about outcomes. Did the nurse who went to Bogota based on the data find work as a nurse? At the predicted wage? How long did it take? This feedback is both validation data and product improvement input.

---

## Summary

Labor market intelligence is the highest-impact data product econOS can build. The reason is simple: labor is the most important resource in any economy, labor allocation decisions are the most consequential economic decisions individuals make, and the information available to support those decisions in Venezuela and Colombia ranges from sparse to nonexistent.

The data sources exist. Computrabajo lists jobs. FincaRaiz lists apartments. LinkedIn lists professionals. DANE publishes surveys. UNHCR counts migrants. Binance tracks exchange rates. Online retailers display prices. None of these sources is sufficient alone. All of them are partial, biased, and incomplete. But combined into a structured BI system -- standardized by occupation, geography, and currency; cross-validated across multiple sources; updated continuously; and presented through a user interface designed for the decisions people actually face -- they become something that does not exist today and that millions of people need.

The Venezuelan nurse in Caracas weighing whether to stay or go deserves better than WhatsApp rumors and a cousin's anecdote. She deserves a system that tells her: here are the nursing jobs in Bogota, here is what they pay, here is what rent costs, here is the credential recognition process, here is the size of the Venezuelan community, here is what the data says and here is what we don't know. She still makes the choice. But she makes it with information instead of blindness.

That is what labor market intelligence means for econOS. Not an academic exercise. Not a statistical report. A tool that helps real people make better decisions about the most important economic choice they will ever face. And if it works -- if even a fraction of the millions of misallocated Venezuelan workers find better matches -- the allocation gain is visible, measurable, and enormous.

This is how you prove that better information produces a better economy. Not in the abstract. In the lives of people who are currently deciding where to live, what to do, and how to survive, with almost nothing to guide them.
