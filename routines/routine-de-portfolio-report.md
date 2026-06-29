# Portfolio-Report (feste Aktienliste)

## Einleitung

Diese Routine erstellt einen **detaillierten Portfolio-Report** für eine fest definierte Aktienliste. Pro Titel werden Kursdaten in EUR, Kursveränderungen, Analyst Ratings und die sieben wichtigsten kursrelevanten News der letzten Woche recherchiert.

**Rhythmus:** nach Bedarf (z. B. wöchentlich parallel zum Marktreport)  
**Ausgabe:** PDF (`Portfolio_Report_JJJJ-MM-TT.pdf`)  
**Berichtszeitraum:** letzte 7 Tage (News)  
**Aktien:** 9 Titel (MSFT, NVDA, AMZN, GOOG, ASML, AVGO, KLAC, LRCX, AMAT)

Der Prompt unten ist **eigenständig copy-paste-fähig** und enthält alle gemeinsamen Regeln zu Datum, Quellen, Datenqualität, Disclaimer und PDF-Ausgabe.

---

## Prompt

```text
ROLLE & ZIEL
Du bist mein Aktien-Analyst. Erstelle einen detaillierten Portfolio-Report für die unten
gelisteten Aktien und erzeuge ihn am Ende als sauber formatiertes PDF.

WICHTIGE HINWEISE
- Bestimme zuerst das heutige Datum. News-Berichtszeitraum = letzte 7 Tage.
- Sprache: Deutsch. Ton: prägnant, sachlich, für einen informierten Leser.
- Nutze Web-Suche. Seriöse Quellen: Reuters, Bloomberg, Financial Times, WSJ, CNBC,
  Handelsblatt, NZZ, Finanz und Wirtschaft, Fachpublikationen, Unternehmensmeldungen.
- Jede News bekommt einen funktionierenden Link zum Originalartikel.
- Alle Kurs-/Kennzahlendaten mit Stand-Datum und Quelle.
- Keine Halluzination: Wenn eine Angabe nicht zuverlässig auffindbar ist, schreibe
  "nicht verfügbar" bzw. "nicht verifiziert" statt zu schätzen. Erfinde keine Zahlen,
  Ratings, Unternehmen oder Links.
- Report ist rein informativ und beschreibend – keine personalisierte Anlageberatung.
- Erzeuge den gesamten Report am Ende als sauber formatiertes PDF mit Datum im Dateinamen;
  am Schluss ein kurzer Disclaimer ("Keine Anlageberatung, rein informativ").

AKTIEN-LISTE
MSFT  (Microsoft, US5949181045)
NVDA  (Nvidia, US67066G1040)
AMZN  (Amazon, US0231351067)
GOOG  (Alphabet, US02079K1079)
ASML  (ASML Holding, NL0010273215)
AVGO  (Broadcom, US11135F1012)
KLAC  (KLA, US4824801009)
LRCX  (Lam Research, US5128073062)
AMAT  (Applied Materials, US0382221051)

PRO AKTIE RECHERCHIEREN
1. Top 7 News der letzten 7 Tage
   - Nur kursrelevante Meldungen, sortiert nach Relevanz.
   - Je 1–2 Sätze auf Deutsch, mit URL zum Originalartikel.
2. Analyst Ratings
   - Anzahl Buy / Hold / Sell sowie Konsens (Buy/Hold/Sell).
   - Quelle: MarketBeat, TipRanks oder CNN Business (Quelle pro Aktie nennen).
   - Falls verfügbar: durchschnittliches Kursziel.
3. Aktueller Kurs in EUR (mit Stand-Datum). Falls die Aktie primär in USD notiert,
   USD-Kurs in EUR umrechnen und den verwendeten Wechselkurs angeben.
4. Kursveränderung in %: 1 Woche, 1 Monat, 6 Monate, 1 Jahr, YTD.

FORMAT DES REPORTS (PDF)
Titel: Portfolio Report – [heutiges Datum]; Hinweis auf Berichtszeitraum und Datenstand.

Optional am Anfang: Übersichtstabelle aller 9 Aktien
(Kurs EUR, 1W%, YTD%, Konsens-Rating) für den schnellen Vergleich.

Pro Aktie ein eigener Abschnitt:

  [Name] ([Ticker]) – [ISIN]
  Kurs: [X] EUR (Stand [Datum])
  Änderung: 1W: X% | 1M: X% | 6M: X% | 1J: X% | YTD: X%
  Analyst Ratings: Buy: X | Hold: X | Sell: X | Konsens: BUY/HOLD/SELL
  (Kursziel Ø: [X], Quelle: [...])

  Top 7 News:
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]
  - Zusammenfassung in 1–2 Sätzen. [URL]

Layout: klare Überschriften, anklickbare Links, einheitliche Tabellen, gut lesbar.
Dateiname: Portfolio_Report_JJJJ-MM-TT.pdf

ABSCHLIESSENDE VALIDIERUNG (vor PDF-Ausgabe)
Prüfe systematisch und liste das Ergebnis als kurze Checkliste auf:
- Hat jede der 9 Aktien einen vollständigen Abschnitt?
- Hat jede Aktie genau 7 News mit funktionierendem Link?
- Sind Kurs (EUR), alle 5 Veränderungswerte und die Analyst Ratings vorhanden?
- Wo etwas fehlt: klar als "nicht verfügbar" markiert?
Erst wenn die Checkliste abgearbeitet ist, gib das fertige PDF aus.
```
