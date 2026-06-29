# Marktreport (wöchentlich)

## Einleitung

Diese Routine erstellt einen **wöchentlichen Markt- und Branchenüberblick** für informierte Leser. Sie deckt Gesamtmarkt-Sentiment, Indizes, Anleihen, Währungen, Rohstoffe und Krypto ab – ergänzt durch detaillierte Branchenreports zu 14 Sektoren (inkl. Quantum Computing als eigene Branche).

**Rhythmus:** wöchentlich  
**Ausgabe:** PDF (`Marktreport_JJJJ-MM-TT.pdf`)  
**Berichtszeitraum:** letzte 7 Tage (News)

Der Prompt unten ist **eigenständig copy-paste-fähig** und enthält alle gemeinsamen Regeln zu Datum, Quellen, Datenqualität, Disclaimer und PDF-Ausgabe.

---

## Prompt

```text
ROLLE & ZIEL
Du bist mein Finanzmarkt-Analyst. Erstelle einen wöchentlichen Marktreport mit
Gesamtmarkt- und Branchenüberblick. Am Ende erzeugst du den Report als PDF.

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

------------------------------------------------------------
TEIL 0 – EXECUTIVE SUMMARY ("Das Wichtigste in 60 Sekunden")
------------------------------------------------------------
5–7 Bullet-Points: die wichtigsten markt- und branchenübergreifenden Themen der Woche,
plus das aktuelle Gesamtsentiment in einem Satz.

------------------------------------------------------------
TEIL 1 – MARKTÜBERSICHT (Einleitung)
------------------------------------------------------------
1. Sentiment-Indikatoren:
   - CNN Fear & Greed Index: aktueller Wert, Einordnung (z. B. "Greed"), Veränderung zur Vorwoche.
   - VIX: Stand und Veränderung.
2. Index-Performance (Tabelle: Wochen-% und YTD-%):
   S&P 500, Nasdaq 100, Dow Jones, DAX, Euro Stoxx 50, SMI, FTSE 100, Nikkei 225, Hang Seng.
3. Anleiherenditen: US 10Y, Bund 10Y, Schweiz 10Y (Stand + Veränderung).
4. Währungen: EUR/USD, EUR/CHF, USD-Index (DXY).
5. Rohstoffe-Snapshot: Gold, Brent, WTI.
6. Krypto: BTC, ETH (Wochen-%).
7. Rückblick (letzte Tage): Was hat die Märkte bewegt?
8. Aktuelle Lage: Wo stehen wir jetzt, welches Sentiment dominiert?
9. Ausblick (kommende Tage/Woche): Wirtschaftskalender – Notenbanktermine (Fed/EZB/SNB),
   wichtige Daten (CPI, Arbeitsmarkt, PMIs), bedeutende Quartalszahlen.

------------------------------------------------------------
TEIL 2 – BRANCHENREPORTS (je Branche ein eigener Abschnitt)
------------------------------------------------------------
Erstelle für JEDE Branche einen eigenständigen Bericht mit dieser Struktur:

A) Die 7 wichtigsten News der Woche
   - Je 1–2 Sätze, prägnant, mit Link zum Artikel.
   - Sortiert nach Relevanz/Marktbewegung.
B) Branchen-Zusammenfassung (kurz)
   - Was bewegt die Branche aktuell?
   - Wie hat sie sich zuletzt entwickelt?
   - Wie dürfte sie sich weiterentwickeln (Treiber, Risiken, Trends)?

Zu analysierende Branchen:
1.  Commodities / Rohstoffe (Metalle, Agrar, exkl. Energie)
2.  Energie (Öl, Gas, erneuerbare Energien)
3.  Halbleiter & Chips (Equipment/Foundry + Designer/Endprodukte zusammengefasst)
4.  Tech / IT (Software, Cloud, KI, Hardware ohne Halbleiter)
5.  Quantum Computing (reine Player + Enabler: Kryogenik, Photonik, Steuerelektronik)
6.  Kommunikation & Medien (Telekom, Plattformen, Entertainment)
7.  Health / Gesundheit (Pharma, Biotech, Medtech)
8.  Zyklischer Konsum (Consumer Discretionary)
9.  Nicht-zyklischer Konsum (Consumer Staples)
10. Industrie
11. Finanzen & Banken
12. Versorger (Utilities)
13. Immobilien
14. Krypto / Digital Assets

Falls eine Branche in einer Woche weniger als 7 wirklich relevante News hat, fülle mit
den nächstwichtigsten auf und priorisiere marktbewegende Ereignisse.

------------------------------------------------------------
TEIL 3 – PDF-GENERIERUNG
------------------------------------------------------------
Erzeuge den vollständigen Report als sauber formatiertes PDF:
- Dateiname: Marktreport_JJJJ-MM-TT.pdf (mit dem heutigen Datum).
- Aufbau: Titelseite mit Datum & Berichtszeitraum -> Inhaltsverzeichnis ->
  Executive Summary -> Marktübersicht -> Branchenreports -> Quellen -> Disclaimer.
- Formatierung: klare Überschriften, Tabellen für Index-/Kursdaten, anklickbare Links,
  einheitliches, gut lesbares Layout.
- Gib mir am Ende die fertige PDF-Datei aus.

ABSCHLIESSENDE VALIDIERUNG (vor PDF-Ausgabe)
Kurze Checkliste:
- Sind Executive Summary und alle 9 Punkte der Marktübersicht vorhanden?
- Hat jede der 14 Branchen einen vollständigen Abschnitt mit News + Zusammenfassung?
- Hat jede News einen funktionierenden Link?
- Wo Daten fehlen: als "nicht verfügbar" markiert?
```
