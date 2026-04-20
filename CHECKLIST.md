# DSGVO-KI-Checkliste

> Stand: April 2026 · basiert auf DSGVO (EU 2016/679) und EU AI Act (VO 2024/1689)

Gehen Sie die Punkte **vor** der Einführung eines KI-Systems durch. Jeder Punkt
hat drei Teile: **Frage**, **Warum das zählt**, **Typische Antworten**.
Markieren Sie Ihren Stand mit `[x]` für erledigt, `[?]` für offen, `[-]` für
nicht zutreffend.

---

## 1. Datenflüsse verstehen

### 1.1 Welche personenbezogenen Daten fließen in das KI-System?
- [ ] Kundendaten (Namen, Adressen, E-Mails)
- [ ] Mitarbeiterdaten (Personalakten, Leistungsbewertungen)
- [ ] Gesundheitsdaten, Finanzdaten, andere besondere Kategorien (Art. 9 DSGVO)
- [ ] Nur anonymisierte/pseudonymisierte Daten
- [ ] Keine personenbezogenen Daten

**Warum das zählt:** Besondere Kategorien nach Art. 9 DSGVO (Gesundheit,
Religion, Gewerkschaft, Biometrie etc.) erfordern eine explizite Rechtsgrundlage
und oft eine Datenschutz-Folgenabschätzung.

### 1.2 Wohin werden die Daten zur Verarbeitung gesendet?
- [ ] Bleiben auf eigener Hardware (On-Premise, lokaler Server)
- [ ] EU-Cloud (Anbieter in EU, Vertragssitz EU, keine US-Mutter mit CLOUD Act)
- [ ] US-Cloud (OpenAI, Anthropic, Google, Microsoft) mit SCC
- [ ] Drittland ohne Angemessenheitsbeschluss

**Warum das zählt:** Drittlandübermittlung nach Schrems II erfordert
Standardvertragsklauseln **plus** Transfer Impact Assessment. US-Cloud ist
nicht per se verboten, aber dokumentationspflichtig.

### 1.3 Werden Eingaben (Prompts) und Ausgaben gespeichert?
- [ ] Nein, keine Speicherung
- [ ] Ja, lokal, mit Löschfrist ___ Tage
- [ ] Ja, beim KI-Anbieter (Opt-out möglich?)

**Warum das zählt:** Prompts enthalten oft unbeabsichtigt personenbezogene
Daten. Ungewolltes Logging ist ein häufiger DSGVO-Verstoß.

---

## 2. Rechtsgrundlage und Dokumentation

### 2.1 Welche Rechtsgrundlage nutzen Sie?
- [ ] Einwilligung (Art. 6 Abs. 1 lit. a)
- [ ] Vertragserfüllung (Art. 6 Abs. 1 lit. b)
- [ ] Berechtigtes Interesse (Art. 6 Abs. 1 lit. f) — mit Interessenabwägung
- [ ] Gesetzliche Verpflichtung (Art. 6 Abs. 1 lit. c)

**Warum das zählt:** Ohne Rechtsgrundlage ist jede Verarbeitung unzulässig.
"Wir nutzen KI weil es modern ist" ist keine Rechtsgrundlage.

### 2.2 Ist das Vorhaben im Verarbeitungsverzeichnis (Art. 30 DSGVO) erfasst?
- [ ] Ja, mit Zweck, Datenkategorien, Empfängern, Löschfristen
- [ ] In Arbeit
- [ ] Noch nicht

### 2.3 Wurde eine Datenschutz-Folgenabschätzung (DSFA, Art. 35) geprüft?
- [ ] DSFA durchgeführt und dokumentiert
- [ ] DSFA geprüft und nicht erforderlich (begründet)
- [ ] Noch offen

**Warum das zählt:** Bei KI-Systemen mit voraussichtlich hohem Risiko (Scoring,
automatische Entscheidungen, systematische Überwachung) ist eine DSFA Pflicht.

### 2.4 Liegt ein Auftragsverarbeitungsvertrag (AVV) mit dem KI-Anbieter vor?
- [ ] Ja, unterzeichnet
- [ ] Entwurf liegt vor
- [ ] Nicht zutreffend (rein lokale Verarbeitung auf eigener Hardware)

---

## 3. EU AI Act: Risikoeinstufung

### 3.1 In welche Risikoklasse fällt der KI-Einsatz?
- [ ] **Verboten** (Art. 5) — Social Scoring, Echtzeit-Biometrie im öffentlichen Raum, emotionale Manipulation → _Vorhaben stoppen_
- [ ] **Hochrisiko** (Anhang III) — Personalauswahl, Kreditscoring, kritische Infrastruktur → _strenge Auflagen_
- [ ] **Begrenztes Risiko** — Chatbots mit Menschenkontakt, generative Systeme → _Transparenzpflicht_
- [ ] **Minimales Risiko** — interne Textzusammenfassung, Code-Vervollständigung → _keine besonderen Auflagen_

**Warum das zählt:** Hochrisiko-Systeme erfordern u.a. Konformitätsbewertung,
Risikomanagement, menschliche Aufsicht und detaillierte Dokumentation.

### 3.2 Bei generativen KI-Systemen: Kennzeichnungspflicht erfüllt?
- [ ] Nutzer wissen, dass sie mit einer KI interagieren
- [ ] KI-generierte Inhalte sind als solche erkennbar

---

## 4. Technische Absicherung

### 4.1 Wer hat Zugriff auf das KI-System?
- [ ] Rollenbasiert (nur autorisierte Mitarbeiter)
- [ ] Authentifizierung mit MFA
- [ ] Audit-Log über alle Zugriffe

### 4.2 Sind die Modelle und deren Herkunft dokumentiert?
- [ ] Modell-Karte (model card) liegt vor
- [ ] Trainingsdaten-Herkunft bekannt
- [ ] Lizenz des Modells erlaubt kommerzielle Nutzung

**Warum das zählt:** Manche "offenen" Modelle haben Einschränkungen (z.B.
Llama-Community-Lizenz >700M Nutzer). Modelle unbekannter Herkunft können
Urheberrechtsprobleme bergen.

### 4.3 Wie werden Daten bei lokaler Verarbeitung geschützt?
- [ ] Festplattenverschlüsselung auf dem Server
- [ ] Netzwerk-Segmentierung (KI-Server nicht im öffentlichen Netz)
- [ ] Regelmäßige Backups mit Verschlüsselung

### 4.4 Logging: Was wird protokolliert, wie lange, wer sieht es?
- [ ] Zweck der Logs dokumentiert (Sicherheit, Abrechnung, Debug)
- [ ] Löschfrist definiert
- [ ] Logs enthalten keine Prompt-Inhalte (oder gezielt pseudonymisiert)

---

## 5. Organisation

### 5.1 Wurden die Mitarbeiter geschult?
- [ ] Einführungsschulung (was darf ich in die KI eingeben, was nicht)
- [ ] Nutzungsrichtlinie dokumentiert und unterschrieben
- [ ] Ansprechpartner für Fragen benannt

### 5.2 Gibt es ein Incident-Response-Verfahren für KI-Vorfälle?
- [ ] Meldeweg bei Datenleck (72-Stunden-Frist nach Art. 33)
- [ ] Meldeweg bei Fehlfunktion/Halluzination mit Schaden
- [ ] Zuständigkeit für Pausieren/Abschalten des Systems geklärt

### 5.3 Betroffenenrechte umsetzbar?
- [ ] Auskunft (Art. 15) möglich
- [ ] Löschung (Art. 17) möglich — auch aus Vektor-Datenbanken
- [ ] Widerspruch gegen automatisierte Entscheidung (Art. 22) vorgesehen

**Warum das zählt:** Das Recht auf Löschung ist bei trainierten Modellen
technisch schwierig. Retrieval-Systeme (RAG) lassen sich leichter säubern als
fine-getunte Modelle.

---

## 6. Wirtschaftlichkeit und Abhängigkeit

### 6.1 Was kostet der Ausstieg?
- [ ] Daten-Export möglich (Prompts, Konfigurationen, Custom-Modelle)
- [ ] Alternative Anbieter evaluiert
- [ ] Lokale Fallback-Lösung verfügbar

### 6.2 Wie hoch ist die Abhängigkeit vom Anbieter?
- [ ] Austauschbare Standard-API (OpenAI-kompatibel)
- [ ] Proprietäre Schnittstelle mit hohem Wechselaufwand
- [ ] Anbieter könnte Preise oder Konditionen einseitig ändern

---

## Zusammenfassung

| Kategorie | Offen | Erledigt | Nicht zutreffend |
|-----------|-------|----------|------------------|
| Datenflüsse | | | |
| Rechtsgrundlage | | | |
| EU AI Act | | | |
| Technik | | | |
| Organisation | | | |
| Wirtschaftlichkeit | | | |

**Gesamturteil:** _(z.B. "Vorhaben kann starten nach Klärung von Punkt 2.3 und 4.4")_

---

_Diese Checkliste wird gepflegt unter https://github.com/inntal-ki/dsgvo-ki-checkliste._
_Hinweise und Verbesserungen willkommen — Issues und PRs sind der Weg._
