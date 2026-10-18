# Changelog

## 1.1.0 — 2026-10-18

Rechtsstand geprüft am 18.10.2026.

### Neu
- **Abschnitt „Vorab: Was gilt nach dem AI Act ab wann?“** — Zeitplan in der
  Fassung des „Digital Omnibus on AI“ (VO 2026/1744, in Kraft seit 27.07.2026):
  Hochrisiko-Pflichten ab 02.12.2027 (Anhang III) bzw. 02.08.2028 (Anhang I),
  Transparenzpflichten seit 02.08.2026, neue Verbote ab 02.12.2026.
- **1.4 Modellherkunft vs. Betriebsort** — für den Datenschutz zählt, wo das
  Modell rechnet, nicht woher es stammt.
- **3.3 Anbieter oder Betreiber?**
- **Abschnitt 7 „Cloud als bewusste Wahl“** — was beim Cloud-Assistenten das
  Haus verlässt (Frage, gefundene Stellen, Anhänge, Verlauf), wer die Cloud
  wählt (kein stiller Rückfall), AVV und Drittland, Speicherfristen
  (Zero Data Retention).
- `examples/beispiel-assessment.json` (fiktive Firma) und eine GitHub Action,
  die Schema und Beispiel bei jeder Änderung prüft.

### Geändert
- **1.2 Drittland:** EU-US Data Privacy Framework ergänzt (Angemessenheits-
  beschluss 2023, vom EU-Gericht am 03.09.2025 bestätigt, Rechtsmittel
  C-703/25 P anhängig). Vorher stand dort, US-Übermittlungen bräuchten immer
  SCC plus TIA.
- **3.1 / 3.2:** Verbote präzisiert (u. a. Emotionserkennung am Arbeitsplatz),
  Transparenzpflichten nach Art. 50 einzeln aufgeführt.
- **5.1:** KI-Kompetenz nach Art. 4 in der Fassung von 2026.
- **Glossar:** „AI Act seit August 2026 vollständig anwendbar“ korrigiert;
  Verarbeitungsverzeichnis, Schrems II, TIA präzisiert; neue Begriffe
  (Anbieter/Betreiber, Data Privacy Framework, Digital Omnibus, KI-Kompetenz,
  Zero Data Retention).
- `schema.json`: Abschnitt `cloud`, `checklisten_version` 1.1.0, JSON Schema
  2020-12 (passend zu `$defs`), `$id` auf die Datei im Repository.
- Kontakt und Verweise auf inntal-ki.eu umgestellt.

Bestehende Punkt-Nummern sind unverändert; neue Punkte haben neue Nummern.

## 1.0.0 — 2026-04-20

Erste Fassung.
