# DSGVO-KI-Checkliste

> Stand: Oktober 2026 (Rechtsstand geprüft am 18.10.2026) · Version 1.1.0
> Grundlage: DSGVO (EU 2016/679) und EU AI Act (VO 2024/1689) in der Fassung
> des „Digital Omnibus on AI“ (VO 2026/1744)

Gehen Sie die Punkte **vor** der Einführung eines KI-Systems durch. Jeder Punkt
hat drei Teile: **Frage**, **Warum das zählt**, **Typische Antworten**.
Markieren Sie Ihren Stand mit `[x]` für erledigt, `[?]` für offen, `[-]` für
nicht zutreffend.

---

## Vorab: Was gilt nach dem AI Act ab wann?

Der „Digital Omnibus on AI“ (VO 2026/1744, in Kraft seit 27.07.2026) hat die
Hochrisiko-Pflichten **verschoben, nicht gestrichen**. Alles andere gilt wie
geplant.

| Seit / ab | Was gilt | Betrifft Ihr Vorhaben vor allem, wenn … |
|---|---|---|
| **02.02.2025** | Verbotene Praktiken (Art. 5) · KI-Kompetenz (Art. 4) | Sie KI überhaupt einsetzen (Art. 4 gilt für jeden Betreiber) |
| **02.08.2025** | Pflichten der Anbieter von KI-Modellen mit allgemeinem Verwendungszweck (Kap. V) · Sanktionsregeln | Sie selbst ein Modell anbieten (selten bei KMU) |
| **02.08.2026** | Transparenzpflichten (Art. 50): KI-Interaktion erkennbar machen, KI-Inhalte kennzeichnen | Sie einen Chatbot nach außen betreiben oder KI-Inhalte veröffentlichen |
| **02.12.2026** | Ende der Übergangsfrist für die maschinenlesbare Kennzeichnung (Art. 50 Abs. 2) bei Systemen, die vor dem 02.08.2026 in Verkehr waren · neue Verbote: intime Deepfakes ohne Einwilligung, Darstellungen sexuellen Kindesmissbrauchs (Art. 5 Abs. 1 lit. ba, bb) | Sie generative Bild-, Video- oder Audio-KI einsetzen |
| **02.12.2027** | Hochrisiko-Pflichten für Systeme nach Anhang III (z. B. Personalauswahl, Kreditwürdigkeit, Zugang zu Bildung) | Sie KI für Entscheidungen über Menschen nutzen |
| **02.08.2028** | Hochrisiko-Pflichten für KI in Produkten nach Anhang I (z. B. Maschinen, Medizinprodukte) | Sie KI in ein reguliertes Produkt einbauen |

**Begriffe:** *Anbieter* entwickelt ein KI-System oder bringt es unter eigenem
Namen in Verkehr. *Betreiber* setzt es in eigener Verantwortung ein. Die
meisten KMU sind Betreiber; wer einen eigenen Chatbot baut und auf die Website
stellt, kann zugleich Anbieter sein (→ 3.3).

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
- [ ] Cloud-Anbieter mit Rechenzentrum in der EU — Konzernmutter und Zugriffsrechte geprüft
- [ ] US-Anbieter, zertifiziert nach dem EU-US Data Privacy Framework
- [ ] US-Anbieter ohne Zertifizierung oder anderes Drittland — mit Standardvertragsklauseln (SCC) und Transfer Impact Assessment

**Warum das zählt:** Für US-Unternehmen, die nach dem EU-US Data Privacy
Framework (DPF) zertifiziert sind, gilt seit Juli 2023 ein
Angemessenheitsbeschluss — SCC und TIA sind dann nicht nötig. Das EU-Gericht
hat den Beschluss am 03.09.2025 bestätigt; ein Rechtsmittel beim EuGH
(C-703/25 P) ist anhängig (Stand 18.10.2026). Fällt der Beschluss, gelten
wieder SCC plus TIA — es lohnt sich, die SCC im AVV vorsorglich mitzuvereinbaren.
Ein Rechenzentrum in der EU allein klärt nicht, ob eine Muttergesellschaft im
Drittland auf die Daten zugreifen kann.

### 1.3 Werden Eingaben (Prompts) und Ausgaben gespeichert?
- [ ] Nein, keine Speicherung
- [ ] Ja, lokal, mit Löschfrist ___ Tage
- [ ] Ja, beim KI-Anbieter (Frist ___ Tage, Nutzung zum Training ausgeschlossen?)

**Warum das zählt:** Prompts enthalten oft unbeabsichtigt personenbezogene
Daten. Ungewolltes Logging ist ein häufiger DSGVO-Verstoß.

### 1.4 Wo rechnet das Modell — und woher stammt es?
- [ ] Offenes Modell auf eigener Hardware, ohne Verbindung nach außen
- [ ] Offenes Modell, betrieben bei einem Cloud-Anbieter
- [ ] Proprietäres Modell über die Schnittstelle (API) des Herstellers

**Warum das zählt:** Für den Datenschutz zählt der **Betriebsort**, nicht das
Herkunftsland des Modells. Ein offenes Modell ist eine Datei: Läuft es auf
eigener Hardware ohne Rückkanal, verlässt keine Eingabe das Haus — gleich, wo
es trainiert wurde. Umgekehrt schützt die Herkunft aus Europa nicht, wenn das
Modell bei einem Anbieter in einem Drittland rechnet. Die Herkunft bleibt
wichtig für Lizenz, Trainingsdaten und eingebaute Inhaltsfilter (→ 4.2).
Prüfen Sie bei „ohne Verbindung nach außen“ auch die Software rundherum:
sendet die Laufzeitumgebung Telemetrie oder lädt sie Inhalte nach?

---

## 2. Rechtsgrundlage und Dokumentation

### 2.1 Welche Rechtsgrundlage nutzen Sie?
- [ ] Einwilligung (Art. 6 Abs. 1 lit. a)
- [ ] Vertragserfüllung (Art. 6 Abs. 1 lit. b)
- [ ] Berechtigtes Interesse (Art. 6 Abs. 1 lit. f) — mit Interessenabwägung
- [ ] Gesetzliche Verpflichtung (Art. 6 Abs. 1 lit. c)

**Warum das zählt:** Ohne Rechtsgrundlage ist jede Verarbeitung unzulässig.
„Wir nutzen KI, weil es modern ist“ ist keine Rechtsgrundlage.

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

## 3. EU AI Act: Risikoeinstufung und Pflichten

### 3.1 In welche Risikoklasse fällt der KI-Einsatz?
- [ ] **Verboten** (Art. 5) — u. a. Social Scoring, manipulative Techniken, Emotionserkennung am Arbeitsplatz und in Bildungseinrichtungen, biometrische Echtzeit-Fernidentifizierung im öffentlichen Raum zur Strafverfolgung; ab 02.12.2026 auch intime Deepfakes ohne Einwilligung → _Vorhaben stoppen_
- [ ] **Hochrisiko** (Anhang III) — Personalauswahl, Kreditwürdigkeit, kritische Infrastruktur → _strenge Auflagen ab 02.12.2027_
- [ ] **Transparenzpflichtig** (Art. 50) — Chatbots mit Menschenkontakt, generierte Bilder, Videos, Audio und Texte → _Kennzeichnung seit 02.08.2026_
- [ ] **Minimales Risiko** — interne Textzusammenfassung, Code-Vervollständigung → _keine besonderen Auflagen außer KI-Kompetenz (→ 5.1)_

**Warum das zählt:** Hochrisiko-Systeme erfordern u. a. Konformitätsbewertung,
Risikomanagement, menschliche Aufsicht und detaillierte Dokumentation. Die
Verschiebung durch den Digital Omnibus gibt Zeit, ändert aber nichts an den
Anforderungen.

### 3.2 Transparenzpflichten nach Art. 50 erfüllt?
- [ ] Menschen, die mit dem System sprechen, erfahren, dass es eine KI ist (z. B. Chatbot auf der Website)
- [ ] Generierte Bilder, Videos, Audio und Texte sind maschinenlesbar als KI-generiert markiert — Pflicht des Anbieters; bei eigenen Systemen, die vor dem 02.08.2026 in Verkehr waren, bis 02.12.2026
- [ ] Deepfakes, die Sie veröffentlichen, sind als künstlich erzeugt offengelegt
- [ ] KI-generierte Texte, die die Öffentlichkeit über Angelegenheiten von öffentlichem Interesse informieren, sind offengelegt — außer ein Mensch hat sie geprüft und trägt die redaktionelle Verantwortung

**Warum das zählt:** Diese Pflichten gelten seit 02.08.2026 und wurden durch
den Digital Omnibus nicht verschoben.

### 3.3 Sind Sie Anbieter oder Betreiber?
- [ ] Betreiber — wir nutzen ein fertiges System eines Anbieters
- [ ] Anbieter — wir entwickeln ein System oder bringen es unter eigenem Namen in Verkehr (z. B. eigener Chatbot für Kunden)
- [ ] Beides

**Warum das zählt:** Anbieter tragen die meisten Pflichten (Kennzeichnung nach
Art. 50 Abs. 1 und 2, bei Hochrisiko die Konformitätsbewertung). Wer ein
System wesentlich verändert oder unter eigenem Namen anbietet, kann vom
Betreiber zum Anbieter werden.

---

## 4. Technische Absicherung

### 4.1 Wer hat Zugriff auf das KI-System?
- [ ] Rollenbasiert (nur autorisierte Mitarbeiter)
- [ ] Authentifizierung mit MFA
- [ ] Audit-Log über alle Zugriffe

### 4.2 Sind die Modelle und deren Herkunft dokumentiert?
- [ ] Modell-Karte (model card) liegt vor
- [ ] Trainingsdaten-Herkunft bekannt
- [ ] Lizenz des Modells erlaubt die geplante Nutzung (auch kommerziell)

**Warum das zählt:** „Offen“ heißt nicht immer frei: Manche Modelllizenzen
schränken die Nutzung ab einer Nutzerzahl ein, verlangen Namensnennung oder
verbieten bestimmte Einsatzzwecke. Lesen Sie die Lizenz auf der Modellkarte,
nicht die Zusammenfassung eines Dritten. Modelle unbekannter Herkunft können
Urheberrechtsprobleme bergen.

### 4.3 Wie werden Daten bei lokaler Verarbeitung geschützt?
- [ ] Festplattenverschlüsselung auf dem Server
- [ ] Netzwerk-Segmentierung (KI-Server nicht im öffentlichen Netz)
- [ ] Regelmäßige Backups mit Verschlüsselung

### 4.4 Logging: Was wird protokolliert, wie lange, wer sieht es?
- [ ] Zweck der Logs dokumentiert (Sicherheit, Abrechnung, Fehlersuche)
- [ ] Löschfrist definiert
- [ ] Logs enthalten keine Prompt-Inhalte (oder gezielt pseudonymisiert)

---

## 5. Organisation

### 5.1 KI-Kompetenz: Wurden die Mitarbeiter geschult?
- [ ] Einführungsschulung (was darf ich in die KI eingeben, was nicht)
- [ ] Nutzungsrichtlinie dokumentiert und unterschrieben
- [ ] Ansprechpartner für Fragen benannt
- [ ] Maßnahmen und Teilnahme dokumentiert

**Warum das zählt:** Art. 4 AI Act verpflichtet Anbieter und Betreiber seit
02.02.2025, Maßnahmen zur KI-Kompetenz ihres Personals zu treffen. In der
Fassung von 2026 ist klargestellt, dass kein bestimmtes Kompetenzniveau
garantiert werden muss — Maßnahmen ergreifen und belegen können genügt, sie
müssen aber zum Einsatz passen.

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
- [ ] Ein Ausfall des Dienstes legt Arbeitsabläufe still

---

## 7. Cloud als bewusste Wahl

Nicht jede Aufgabe muss lokal laufen. Wenn ein Cloud-Assistent genutzt wird,
dann **bewusst** — für klar benannte Aufgaben, mit geklärtem Vertrag.

### 7.1 Was verlässt beim Cloud-Assistenten das Haus?
- [ ] Die Frage selbst (Prompt)
- [ ] Gefundene Stellen aus eigenen Dokumenten, die automatisch mitgeschickt werden (RAG)
- [ ] Angehängte Dateien
- [ ] Bisheriger Gesprächsverlauf
- [ ] Metadaten (Benutzerkennung, IP-Adresse, Zeitpunkt)

**Warum das zählt:** Mitarbeiter denken bei „ich frage die KI“ an ihre Frage.
Ein Assistent mit Zugriff auf Dokumente schickt aber oft ganze Textstellen mit,
die er selbst ausgewählt hat — und mit jeder Folgefrage meist den bisherigen
Verlauf.

### 7.2 Wer entscheidet, wann die Cloud genutzt wird?
- [ ] Der Mitarbeiter wählt den Cloud-Assistenten ausdrücklich (eigener Assistent, klar beschriftet)
- [ ] Freigabe nur für bestimmte Gruppen oder Aufgaben
- [ ] Kein automatischer Rückfall in die Cloud, wenn das lokale System ausgelastet oder ausgefallen ist

**Warum das zählt:** Ein stiller Rückfall macht aus einer lokalen Verarbeitung
unbemerkt eine Übermittlung an Dritte — ohne dass jemand die Daten vorher
bewertet hat.

### 7.3 Vertrag und Drittland geklärt?
- [ ] AVV nach Art. 28 DSGVO mit dem Cloud-Anbieter (→ 2.4)
- [ ] Unterauftragsverarbeiter bekannt (wer rechnet tatsächlich?)
- [ ] Rechtsgrundlage für Drittlandübermittlung (→ 1.2)
- [ ] Nutzung der Eingaben zum Training vertraglich ausgeschlossen

### 7.4 Wie lange speichert der Anbieter Eingaben und Ausgaben?
- [ ] Keine Speicherung über die Anfrage hinaus („Zero Data Retention“), vertraglich zugesichert
- [ ] Speicherung für ___ Tage (z. B. zur Missbrauchserkennung)
- [ ] Unklar

**Warum das zählt:** Auch ohne Training heben viele Anbieter Eingaben eine Zeit
lang auf, etwa zur Missbrauchserkennung. „Zero Data Retention“ ist oft eine
eigene Vertragsoption und nicht der Standard — fragen Sie nach, statt es
anzunehmen.

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
| Cloud | | | |

**Gesamturteil:** _(z. B. „Vorhaben kann starten nach Klärung von Punkt 2.3 und 4.4“)_

---

_Diese Checkliste wird gepflegt unter https://github.com/inntal-ki/dsgvo-ki-checkliste._
_Hinweise und Verbesserungen willkommen — Issues und PRs sind der Weg._
