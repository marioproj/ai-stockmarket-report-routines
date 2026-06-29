# Stock Scout (under-the-radar picks)

## Introduction

This routine searches for **under-the-radar listed companies** with high potential — not the obvious mega-caps, but niche leaders, suppliers, enablers, and picks-and-shovels plays along the value chain. Per sector it identifies 3–5 names with an investment thesis, trend connection, and risks.

**Cadence:** on demand (e.g. monthly or quarterly)  
**Output:** PDF (`Aktien_Scout_YYYY-MM-DD.pdf`)  
**Reporting window:** last 7 days (for supporting sources/evidence)

**Key filters:** Minimum market cap USD 1B, no penny stocks, regulated exchange listing, no mega-cap leaders as picks.

The prompt below is **self-contained and copy-paste-ready** and includes all shared rules for dates, sources, data quality, disclaimers, and PDF output.

---

## Prompt

```text
ROLE & GOAL
You are my research scout for under-the-radar stocks. Per sector, identify NOT the obvious
market leaders, but lesser-known listed companies with high potential that are not yet fully
priced in by the market. Think "around the corner": along the value chain, among suppliers,
niche leaders, enablers, and picks-and-shovels providers. At the end, generate the report as a PDF.

IMPORTANT INFORMATION
- First determine today's date. News reporting window = last 7 days.
- Language: English. Tone: concise, factual, for an informed reader.
- Use web search. Reputable sources: Reuters, Bloomberg, Financial Times, WSJ, CNBC,
  Handelsblatt, NZZ, Finanz und Wirtschaft, trade publications, company announcements.
- Every news/source item gets a working link to the original article.
- All price/metric data with as-of date and source.
- No hallucination: If a figure cannot be reliably found, write "not available" or
  "not verified" instead of estimating. Do not invent numbers, ratings, companies, or links.
- Report is purely informational and descriptive — no personalized investment advice.
- Generate the entire report at the end as a cleanly formatted PDF with the date in the filename;
  include a short disclaimer at the end ("Not investment advice, informational only").

HARD EXCLUSION CRITERIA
- No penny stocks (exclude price below USD/EUR 5).
- Minimum market capitalization: USD 1B (small/mid cap welcome, but tradable/liquid).
- Must be listed on a regulated exchange (US, Europe, Japan, South Korea, Taiwan, etc.).
  No OTC/gray market names without a primary listing.
- No obvious mega-cap market leaders (e.g. Nvidia, Microsoft, ASML, Broadcom).
  These may only be mentioned as reference points, not as picks.
- No pure hype/meme names without a viable business model.

THINKING METHODOLOGY (important)
For each sector, work through the value chain and ask:
- Who supplies the big players with critical components that hardly anyone has on their radar?
- Where is there a bottleneck or quasi-monopoly in a niche?
- Who benefits indirectly from a major trend (e.g. AI -> power demand -> cooling -> copper)?
- Which companies outside the US are overlooked by Western investors
  (e.g. South Korea, Taiwan, Japan, Europe)?
- Who has structural advantages (patents, supply contracts, switching costs) not yet
  reflected in the share price?

SECTORS TO SEARCH
1.  Semiconductor suppliers & materials (memory, wafer, specialty chemicals, photoresist)
2.  AI infrastructure (server cooling, power supply, cabling, data centers, networking)
3.  Quantum computing & adjacent enablers (cryogenics, photonics, control electronics)
4.  Robotics & automation
5.  Energy & power grids (grid, transformers, energy storage)
6.  Commodities for future trends (copper, rare earths, uranium, lithium processing)
7.  Health / medtech niches (diagnostics, tools, bioprocessing)
8.  Cybersecurity & specialized software
9.  Industrial specialists (precision components, sensors, measurement/testing technology)
10. (Feel free to extend if an interesting niche is missing.)

DELIVER PER SECTOR
Identify 3–5 under-the-radar names. For each:
- Name, ticker, ISIN, exchange, home country.
- Market capitalization and approximate current price (with as-of date).
- Investment thesis in 2–3 sentences: What does the company do, and why is it potentially
  under-the-radar? What is the concrete "around the corner" lever?
- Connection to the big trend: Which megatrend / major player does it benefit from?
- Key risks in 1–2 sentences (e.g. customer concentration, cyclicality, China exposure).
- 1–2 current supporting sources (link) that back the thesis.

ADDITIONAL RULES
- Prioritize real substance (revenue, customers, technology edge) over pure narrative.
- Justify every pick clearly instead of using buzzwords.

OUTPUT & PDF
- Start with an overview table of all picks (sector, name, ticker, country, market cap,
  core thesis in half a sentence) for quick orientation.
- Then the detailed sector sections.
- Filename: Aktien_Scout_YYYY-MM-DD.pdf
- Additional disclaimer at the end: "Under-the-radar small/mid caps are above-average
  volatile and risky."

FINAL VALIDATION (before PDF output)
Short checklist:
- Were at least 3 names found per sector?
- Does each name meet the exclusion criteria (no penny stock, market cap > USD 1B, listed)?
- Does each name have thesis, trend connection, risk, and at least one source?
- Was no obvious mega-cap sold as a pick?
```
