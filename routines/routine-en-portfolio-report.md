# Portfolio Report (fixed stock list)

## Introduction

This routine creates a **detailed portfolio report** for a predefined list of stocks. For each ticker it researches price data in EUR, price changes, analyst ratings, and the seven most price-relevant news items from the past week.

**Cadence:** on demand (e.g. weekly alongside the Market Report)  
**Output:** PDF (`Portfolio_Report_YYYY-MM-DD.pdf`)  
**Reporting window:** last 7 days (news)  
**Stocks:** 9 tickers (MSFT, NVDA, AMZN, GOOG, ASML, AVGO, KLAC, LRCX, AMAT)

The prompt below is **self-contained and copy-paste-ready** and includes all shared rules for dates, sources, data quality, disclaimers, and PDF output.

---

## Prompt

```text
ROLE & GOAL
You are my equity analyst. Create a detailed portfolio report for the stocks listed below
and generate it at the end as a cleanly formatted PDF.

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

STOCK LIST
MSFT  (Microsoft, US5949181045)
NVDA  (Nvidia, US67066G1040)
AMZN  (Amazon, US0231351067)
GOOG  (Alphabet, US02079K1079)
ASML  (ASML Holding, NL0010273215)
AVGO  (Broadcom, US11135F1012)
KLAC  (KLA, US4824801009)
LRCX  (Lam Research, US5128073062)
AMAT  (Applied Materials, US0382221051)

RESEARCH PER STOCK
1. Top 7 news items from the last 7 days
   - Price-relevant items only, sorted by relevance.
   - 1–2 sentences each in English, with URL to the original article.
2. Analyst ratings
   - Number of Buy / Hold / Sell and consensus (Buy/Hold/Sell).
   - Source: MarketBeat, TipRanks, or CNN Business (name source per stock).
   - If available: average price target.
3. Current price in EUR (with as-of date). If the stock is primarily quoted in USD,
   convert USD price to EUR and state the exchange rate used.
4. Price change in %: 1 week, 1 month, 6 months, 1 year, YTD.

REPORT FORMAT (PDF)
Title: Portfolio Report – [today's date]; note reporting window and data as-of date.

Optional at the start: overview table of all 9 stocks
(price EUR, 1W%, YTD%, consensus rating) for quick comparison.

One section per stock:

  [Name] ([Ticker]) – [ISIN]
  Price: [X] EUR (as of [date])
  Change: 1W: X% | 1M: X% | 6M: X% | 1Y: X% | YTD: X%
  Analyst Ratings: Buy: X | Hold: X | Sell: X | Consensus: BUY/HOLD/SELL
  (Avg. price target: [X], source: [...])

  Top 7 News:
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]
  - Summary in 1–2 sentences. [URL]

Layout: clear headings, clickable links, consistent tables, easy to read.
Filename: Portfolio_Report_YYYY-MM-DD.pdf

FINAL VALIDATION (before PDF output)
Check systematically and list the result as a short checklist:
- Does each of the 9 stocks have a complete section?
- Does each stock have exactly 7 news items with working links?
- Are price (EUR), all 5 change values, and analyst ratings present?
- Where something is missing: clearly marked as "not available"?
Only output the finished PDF once the checklist is complete.
```
