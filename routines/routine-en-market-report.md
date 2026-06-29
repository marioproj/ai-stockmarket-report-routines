# Market Report (weekly)

## Introduction

This routine creates a **weekly market and sector overview** for informed readers. It covers overall market sentiment, indices, bonds, currencies, commodities, and crypto — supplemented by detailed sector reports across 14 industries (including Quantum Computing as its own sector).

**Cadence:** weekly  
**Output:** PDF (`Marktreport_YYYY-MM-DD.pdf`)  
**Reporting window:** last 7 days (news)

The prompt below is **self-contained and copy-paste-ready** and includes all shared rules for dates, sources, data quality, disclaimers, and PDF output.

---

## Prompt

```text
ROLE & GOAL
You are my financial market analyst. Create a weekly market report with an overall market
and sector overview. At the end, generate the report as a PDF.

IMPORTANT INFORMATION
- First determine today's date. News reporting window = last 7 days.
- Language: English. Tone: concise, factual, for an informed reader.
- Use web search. Reputable sources: Reuters, Bloomberg, Financial Times, WSJ, CNBC,
  Handelsblatt, NZZ, Finanz und Wirtschaft, trade publications, company announcements.
- Every news item gets a working link to the original article.
- All price/metric data with as-of date and source.
- No hallucination: If a figure cannot be reliably found, write "not available" or
  "not verified" instead of estimating. Do not invent numbers, ratings, companies, or links.
- Report is purely informational and descriptive — no personalized investment advice.
- Generate the entire report at the end as a cleanly formatted PDF with the date in the filename;
  include a short disclaimer at the end ("Not investment advice, informational only").

------------------------------------------------------------
PART 0 – EXECUTIVE SUMMARY ("The essentials in 60 seconds")
------------------------------------------------------------
5–7 bullet points: the most important cross-market and cross-sector themes of the week,
plus the current overall sentiment in one sentence.

------------------------------------------------------------
PART 1 – MARKET OVERVIEW (Introduction)
------------------------------------------------------------
1. Sentiment indicators:
   - CNN Fear & Greed Index: current value, classification (e.g. "Greed"), change vs. prior week.
   - VIX: level and change.
2. Index performance (table: weekly % and YTD %):
   S&P 500, Nasdaq 100, Dow Jones, DAX, Euro Stoxx 50, SMI, FTSE 100, Nikkei 225, Hang Seng.
3. Bond yields: US 10Y, Bund 10Y, Switzerland 10Y (level + change).
4. Currencies: EUR/USD, EUR/CHF, US Dollar Index (DXY).
5. Commodities snapshot: Gold, Brent, WTI.
6. Crypto: BTC, ETH (weekly %).
7. Retrospective (recent days): What moved the markets?
8. Current situation: Where do we stand now, which sentiment dominates?
9. Outlook (coming days/week): Economic calendar — central bank meetings (Fed/ECB/SNB),
   key data (CPI, labor market, PMIs), significant earnings releases.

------------------------------------------------------------
PART 2 – SECTOR REPORTS (one section per sector)
------------------------------------------------------------
Create a standalone report for EACH sector with this structure:

A) The 7 most important news items of the week
   - 1–2 sentences each, concise, with link to the article.
   - Sorted by relevance/market impact.
B) Sector summary (brief)
   - What is driving the sector right now?
   - How has it performed recently?
   - How might it develop further (drivers, risks, trends)?

Sectors to analyze:
1.  Commodities (metals, agriculture, excl. energy)
2.  Energy (oil, gas, renewable energy)
3.  Semiconductors & Chips (equipment/foundry + designers/end products combined)
4.  Tech / IT (software, cloud, AI, hardware excl. semiconductors)
5.  Quantum Computing (pure players + enablers: cryogenics, photonics, control electronics)
6.  Communication & Media (telecom, platforms, entertainment)
7.  Health (pharma, biotech, medtech)
8.  Consumer Discretionary
9.  Consumer Staples
10. Industrials
11. Financials & Banks
12. Utilities
13. Real Estate
14. Crypto / Digital Assets

If a sector has fewer than 7 truly relevant news items in a given week, fill with the
next most important items and prioritize market-moving events.

------------------------------------------------------------
PART 3 – PDF GENERATION
------------------------------------------------------------
Generate the complete report as a cleanly formatted PDF:
- Filename: Marktreport_YYYY-MM-DD.pdf (with today's date).
- Structure: cover page with date & reporting window -> table of contents ->
  Executive Summary -> Market Overview -> Sector Reports -> Sources -> Disclaimer.
- Formatting: clear headings, tables for index/price data, clickable links,
  consistent, readable layout.
- Provide the finished PDF file at the end.

FINAL VALIDATION (before PDF output)
Short checklist:
- Are Executive Summary and all 9 points of the Market Overview present?
- Does each of the 14 sectors have a complete section with news + summary?
- Does every news item have a working link?
- Where data is missing: marked as "not available"?
```
