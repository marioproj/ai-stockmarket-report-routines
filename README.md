# AI Stockmarket Report Routines

A set of three coordinated AI prompt routines for structured financial market research and reporting. Each routine is a self-contained, copy-paste-ready prompt designed for AI assistants that support web search and PDF generation — preferably **Claude Cowork**, but also Cursor or similar tools.

**You are free to use, modify, and share these routines** for personal or commercial purposes under the terms of the [MIT License](LICENSE).

---

## The Three Routines

All three routines share the same **Important Information** block (DE: *Wichtige Hinweise*) — consistent rules for dates, sources, data quality, disclaimers, and PDF output — so they produce reports with a uniform standard.

### 1. Market Report (weekly)

**File:** `routine-de-market-report.md` (DE) · `routine-en-market-report.md` (EN)

A **weekly market and sector overview** covering:

- Executive summary and overall market sentiment
- Indices, bonds, currencies, commodities, and crypto
- Detailed sector reports across 14 industries (including Quantum Computing as its own sector)
- Economic calendar and outlook

**Output:** `Marktreport_YYYY-MM-DD.pdf`  
**Cadence:** Weekly · **News window:** last 7 days

---

### 2. Portfolio Report (fixed stock list)

**File:** `routine-de-portfolio-report.md` (DE) · `routine-en-portfolio-report.md` (EN)

A **detailed report on a predefined list of stocks**. For each ticker it researches:

- Top 7 price-relevant news items from the past week
- Analyst ratings and consensus
- Current price in EUR and performance (1W, 1M, 6M, 1Y, YTD)

The default list covers 9 large-cap tech and semiconductor names (MSFT, NVDA, AMZN, GOOG, ASML, AVGO, KLAC, LRCX, AMAT) — you can adapt the list in the prompt to match your own portfolio.

**Output:** `Portfolio_Report_YYYY-MM-DD.pdf`  
**Cadence:** On demand (e.g. weekly alongside the Market Report) · **News window:** last 7 days

---

### 3. Stock Scout (under-the-radar picks)

**File:** `routine-de-stock-scout.md` (DE) · `routine-en-stock-scout.md` (EN)

A **research scout for lesser-known listed companies** with potential — not the obvious mega-caps, but niche leaders, suppliers, enablers, and picks-and-shovels plays along the value chain.

Per sector, it identifies 3–5 candidates with an investment thesis, trend connection, and risks. Hard filters apply: minimum market cap of USD 1B, no penny stocks, regulated exchange listing, no mega-cap leaders as picks.

**Output:** `Aktien_Scout_YYYY-MM-DD.pdf`  
**Cadence:** On demand (e.g. monthly or quarterly) · **News window:** last 7 days for supporting sources

---

## Languages

Routine files are available in **German** and **English** in the [`routines/`](routines/) folder:

| Routine | German | English |
|---------|--------|---------|
| Market Report | `routine-de-market-report.md` | `routine-en-market-report.md` |
| Portfolio Report | `routine-de-portfolio-report.md` | `routine-en-portfolio-report.md` |
| Stock Scout | `routine-de-stock-scout.md` | `routine-en-stock-scout.md` |

Each file contains a short introduction and the full prompt inside a copy-paste block.

---

## How to Use it with Claude
(You can use it as well with in combination with other LLMs)

1. Open the routine file in your preferred language.
2. Copy the entire prompt from the code block.
3. Open Claude Cowork on desktop
4. Open the **Scheduled** tab
5. Create a new task
6. Select **Set up manually**
7. Give the routine a name and description
8. Add the copied prompt
9. Set frequency to weekly and select time and date
10. Select model **Sonnet 4.6** and save
11. The assistant will research current data via web search and produce a formatted PDF report.

You may edit any prompt freely — adjust sectors, stock lists, language, output format, or filters to suit your needs.

---

## Disclaimer

**These routines and any reports they generate do not constitute financial advice, investment recommendations, or a solicitation to buy or sell any security.**

All content is for **informational and educational purposes only**. Past performance is not indicative of future results. Investing involves risk, including the possible loss of principal. Always do your own research and consult a qualified financial advisor before making investment decisions.

The author assumes no liability for any financial losses or decisions made based on content produced with these prompts.

---

## License

This project is released under the [MIT License](LICENSE). You may use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of these routines without restriction, provided the copyright notice and license terms are included.

---

Created by **[Mario Nüesch](https://mario.pm)** with love ❤️ · [woumba.com](https://woumba.com)

If you find these routines useful, you can support me with a coffee ☕ via [this link](https://wise.com/pay/r/ET8uFqtYCTm3Z7Y).
