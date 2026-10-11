# Memory Market Research Guide

A source-first framework for researching DRAM, NAND flash, HBM, and memory modules without confusing product specifications, market layers, or company narratives.

This guide contains **no price dataset, proprietary forecast, private database extract, credentials, or website source code**. It is a research process and reading list, not a trading model.

## 1. Define the market before collecting data

Memory is not one market. Write a one-sentence scope before opening a spreadsheet:

> Analyze **[technology]** in **[form factor / density / generation]** for **[end market]** in **[geography]**, measuring **[spot / contract / producer / retail]** conditions over **[time horizon]**.

Keep these distinctions explicit:

| Dimension | Examples | Why it matters |
|---|---|---|
| Technology | DRAM, NAND flash, NOR flash, HBM | Different suppliers, cost curves, and demand drivers |
| Product | Die, packaged chip, wafer, module, SSD, managed NAND | Prices and lead times are not interchangeable |
| Generation | DDR4 vs. DDR5; legacy vs. advanced NAND; HBM generation | Transitions can tighten one segment while leaving another oversupplied |
| Market layer | Spot, contract, distributor, OEM, retail | Each layer has different volume, timing, and negotiation dynamics |
| End market | Data center, PC, mobile, automotive, industrial, consumer | Qualification cycles and demand elasticity vary widely |

## 2. Build a product taxonomy

Start with standards and vendor documentation rather than marketplace listings.

- [JEDEC standards catalog](https://www.jedec.org/standards-documents) — terminology and specifications for memory devices, modules, packages, and interfaces.
- [Micron product portfolio](https://www.micron.com/products) — vendor documentation across DRAM, NAND, managed storage, SSDs, and memory cards.
- [Samsung Semiconductor memory](https://semiconductor.samsung.com/dram/) — product families and technical documentation.
- [SK hynix](https://www.skhynix.com/) — official DRAM, NAND, SSD, and related product categories.

For every observed item, record at minimum: technology, generation, density or capacity, organization, speed grade, form factor, package, ECC/buffering, vendor tier, geography, unit, currency, incoterm or freight treatment, tax treatment, and observation time.

## 3. Map demand by end market

Do not use device shipments alone. Memory content per device can change faster than unit demand.

| End market | Useful questions | Example public indicators |
|---|---|---|
| Data center / AI | Server shipments, accelerator deployments, HBM content, enterprise SSD capacity, cloud capex | Company filings, hyperscaler disclosures, vendor earnings materials |
| PC | Unit shipments, DRAM per system, SSD attach rate and capacity, channel inventory | Vendor filings, public industry summaries, customs data |
| Smartphone | Units, flagship mix, DRAM/NAND content, launch timing, channel inventory | Vendor disclosures, customs data, public shipment summaries |
| Automotive / industrial | Qualification cycles, content growth, design wins, inventory digestion | Supplier filings and segment commentary |
| Consumer / graphics | Console and GPU cycles, discrete graphics memory, retail promotions | Company filings and product announcements |

A useful decomposition is:

**bit demand = device units × average memory content per device**

Treat both terms as estimates with ranges. Avoid presenting a single-point forecast without assumptions.

## 4. Model supply in bits, not only wafers

Track the mechanisms that change effective supply:

- wafer starts and cleanroom capacity;
- node migration and layers per NAND stack;
- yield and ramp timing;
- bits produced per wafer;
- allocation among DRAM, HBM, mobile, server, client, and legacy products;
- packaging, testing, substrates, and HBM-related bottlenecks;
- utilization, maintenance, power, water, and geopolitical constraints;
- inventory held by suppliers, distributors, OEMs, and customers.

Capital expenditure is a leading input, not a direct near-term supply measure. Separate building shell, equipment installation, qualification, yield ramp, and volume output.

## 5. Use primary sources first

### Industry and standards

- [World Semiconductor Trade Statistics](https://www.wsts.org/) — global semiconductor billings and historical industry tables.
- [Semiconductor Industry Association resources](https://www.semiconductors.org/resources/) — industry reports and policy context.
- [SEMI market data](https://www.semi.org/en/products-services/market-data) — fab, equipment, materials, and packaging research; access varies.
- [JEDEC](https://www.jedec.org/) — standards and terminology.

### Company disclosures

- [Micron quarterly results](https://investors.micron.com/financials/quarterly-results/default.aspx)
- [Samsung Electronics investor relations](https://www.samsung.com/global/ir/financial-information/)
- [SK hynix investor relations](https://www.skhynix.com/ir/UI-FR-IR16/)
- [SEC EDGAR](https://www.sec.gov/edgar/search/) for U.S.-listed issuers and depositary receipts

Read prepared remarks, earnings decks, filings, and call transcripts together. Extract management statements with their date and exact scope; label guidance, targets, and opinions as such.

### Independent context

- [FRED semiconductor manufacturing PPI](https://fred.stlouisfed.org/series/PCU334413334413) — a U.S. industry price index, not a substitute for product-level memory quotes.
- [UN Comtrade](https://comtradeplus.un.org/) — trade flows; verify HS codes and classification changes.
- [U.S. Census manufacturing data](https://www.census.gov/manufacturing/m3/) — shipments, inventories, and orders for broad manufacturing categories.
- Specialist research firms can add channel checks and forecasts, but clearly label paywalled estimates and never republish licensed tables.

## 6. Handle prices correctly

Before comparing two observations, verify that they share:

1. the same product specification and quality tier;
2. the same market layer and transaction basis;
3. the same geography, currency, taxes, and freight treatment;
4. compatible timestamps and publication lags;
5. sufficient volume and a documented collection method.

Report ranges, dispersion, and confidence where possible. A spot quote can move before contract negotiations, but it may also reflect a thin or stressed channel. Retail promotions can say more about inventory strategy than upstream replacement cost.

Never turn an index into a currency price, mix nominal and inflation-adjusted series without disclosure, or splice incompatible products into a continuous chart.

## 7. Run a repeatable weekly workflow

1. **Update the event log:** earnings, product launches, fab incidents, policy changes, capacity announcements, and channel checks.
2. **Refresh indicators:** demand units, content assumptions, inventories, lead times, utilization commentary, and price direction by market layer.
3. **Record provenance:** source URL, publication date, access date, unit, currency, product definition, and any transformation.
4. **Triangulate:** require at least one demand-side and one supply-side explanation for a major move.
5. **Write a falsifiable view:** base case, upside/downside triggers, disconfirming evidence, and the next observation that would change the conclusion.

### Minimal research table

| Date | Segment | Indicator | Direction | Source type | Confidence | What would invalidate it? |
|---|---|---|---|---|---|---|
| YYYY-MM-DD | Example: server DRAM | Describe the observation; do not paste licensed data | Up / flat / down | Filing / official data / channel check | Low / medium / high | Specific contrary evidence |

## 8. Common failure modes

- Treating all DRAM or NAND products as interchangeable.
- Mixing spot, contract, producer, distributor, and retail observations.
- Counting announced capacity as immediately available output.
- Using wafer starts without adjusting for node, yield, and bits per wafer.
- Reading supplier revenue as pure unit demand while ignoring mix and price.
- Double-counting inventory across suppliers, channels, and customers.
- Quoting a forecast as observed fact.
- Ignoring fiscal-calendar differences and revised historical data.
- Reposting licensed tables or confidential channel checks.

## Related market monitor

[Market Pulse Scope](https://marketpulsescope.com/?utm_source=github&utm_medium=referral&utm_campaign=memory_market_research_guide) offers multilingual market news and selected electronics indicators that can help with discovery and ongoing monitoring. Validate important conclusions against original filings, standards, and official datasets.

No Market Pulse Scope dataset is included in this repository.

## Suggested citation practice

For each claim, keep the publisher, document title, publication date, stable URL, page or section, access date, and whether the statement is observed, estimated, forecast, or management guidance. Link to the source rather than copying large tables.

## Disclaimer

This guide is for research and education. It does not provide financial, investment, procurement, or trading advice. Product definitions, access terms, and methodologies change; consult each publisher's current documentation and license.

