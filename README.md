# DSGVO-KI-Checkliste

**Self-Assessment für die Einführung von KI-Systemen in KMU — nach DSGVO und EU AI Act.**

[![Schema](https://github.com/inntal-ki/dsgvo-ki-checkliste/actions/workflows/validate.yml/badge.svg)](https://github.com/inntal-ki/dsgvo-ki-checkliste/actions/workflows/validate.yml)

**Stand:** Oktober 2026 · Version 1.1.0 · Rechtsstand geprüft am 18.10.2026 (inkl. „Digital Omnibus on AI“, VO 2026/1744)

Eine strukturierte Checkliste, mit der Sie vor der Einführung eines KI-Systems
(lokal oder Cloud) die wichtigsten rechtlichen und organisatorischen Fragen
durchgehen. Ohne Beratungsjargon, ohne Produktempfehlung.

## Für wen ist das?

- Geschäftsführer und IT-Verantwortliche in kleinen und mittleren Unternehmen
- Datenschutzbeauftragte, die ein KI-Vorhaben bewerten sollen
- Berater, die ihren Kunden eine strukturierte Vorarbeit abnehmen wollen

## Inhalt

- [`CHECKLIST.md`](CHECKLIST.md) — Die eigentliche Checkliste (Markdown)
- [`schema.json`](schema.json) — Maschinenlesbares Schema für Self-Assessment-Tools
- [`glossar.md`](glossar.md) — Begriffe kurz erklärt
- [`examples/beispiel-assessment.json`](examples/beispiel-assessment.json) — ausgefülltes Beispiel (fiktive Firma)
- [`CHANGELOG.md`](CHANGELOG.md) — was sich wann geändert hat

## Nutzung

### Manuell durchgehen

Kopieren Sie [`CHECKLIST.md`](CHECKLIST.md) und beantworten Sie die Punkte für
Ihr konkretes Vorhaben. Jeder Punkt hat eine kurze Erklärung, warum er zählt.

### Maschinell auswerten

Das Schema in [`schema.json`](schema.json) eignet sich, um die Antworten in
einem Formular oder einer kleinen Web-App zu erfassen. Ein ausgefülltes Beispiel
steht in [`examples/beispiel-assessment.json`](examples/beispiel-assessment.json);
bei jeder Änderung prüft eine GitHub Action Schema und Beispiel.

## Haftungsausschluss

Diese Checkliste ersetzt **keine juristische Beratung**. Sie ist ein
strukturiertes Werkzeug zur Vorarbeit, damit Sie mit dem Anwalt oder
Datenschutzbeauftragten effizienter sprechen können. DSGVO und EU AI Act sind
komplex; im Zweifelsfall ziehen Sie qualifizierten Rat hinzu.

## Beitragen

Fehler, Lücken oder zusätzliche Branchen-Spezifika? Issues und Pull Requests
willkommen. Siehe [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Lizenz

[MIT](LICENSE) — freie Nutzung auch kommerziell, keine Gewähr.

---

Teil der [inntal-ki](https://github.com/inntal-ki) Open-Source-Familie — ein
persönliches, nicht kommerzielles Projekt · [inntal-ki.eu](https://inntal-ki.eu)
