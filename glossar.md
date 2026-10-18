# Glossar

Kurzerklärungen der wichtigsten Begriffe. Ohne Anspruch auf juristische Vollständigkeit.
Stand: Oktober 2026.

## Angemessenheitsbeschluss
Feststellung der EU-Kommission, dass ein Drittland ein mit der EU vergleichbares
Datenschutzniveau hat. Ohne solchen Beschluss sind zusätzliche Garantien (z. B. SCC) nötig.
Für die USA gilt er nur für Unternehmen, die nach dem → Data Privacy Framework zertifiziert sind.

## Anbieter und Betreiber (AI Act)
*Anbieter* entwickelt ein KI-System oder bringt es unter eigenem Namen in Verkehr.
*Betreiber* setzt ein KI-System in eigener Verantwortung ein. Die meisten Pflichten
liegen beim Anbieter; KMU sind meist Betreiber.

## Auftragsverarbeitungsvertrag (AVV)
Vertrag nach Art. 28 DSGVO zwischen Verantwortlichem und Dienstleister, der die
Verarbeitung personenbezogener Daten im Auftrag regelt.

## Data Privacy Framework (DPF)
Angemessenheitsbeschluss der EU-Kommission für die USA vom Juli 2023. Gilt für
US-Unternehmen, die sich zertifiziert haben (Liste: dataprivacyframework.gov).
Vom EU-Gericht am 03.09.2025 bestätigt; Rechtsmittel beim EuGH anhängig
(C-703/25 P, Stand 18.10.2026).

## Datenschutz-Folgenabschätzung (DSFA)
Strukturierte Risikoanalyse nach Art. 35 DSGVO, verpflichtend bei voraussichtlich
hohem Risiko für Betroffene.

## Digital Omnibus on AI
Verordnung (EU) 2026/1744, in Kraft seit 27.07.2026. Ändert den AI Act: verschiebt
die Hochrisiko-Pflichten, fasst die KI-Kompetenz (Art. 4) neu, ergänzt Verbote
und vereinfacht einiges für KMU.

## EU AI Act
Verordnung (EU) 2024/1689, geändert durch den → Digital Omnibus on AI. Gilt
stufenweise seit Februar 2025; die Hochrisiko-Pflichten folgen am 02.12.2027
(Anhang III) und 02.08.2028 (Anhang I). Zeitplan: Abschnitt „Vorab“ der Checkliste.

## Fine-Tuning
Nachtraining eines vortrainierten Modells mit eigenen Daten. Die Daten werden
dabei implizit „gelernt“ und sind schwer wieder zu löschen.

## Halluzination
KI-Ausgabe, die plausibel klingt, aber faktisch falsch ist. Typisches Risiko bei
generativen Sprachmodellen.

## Hochrisiko-KI
Systeme nach Anhang III des AI Act (Personalauswahl, Kreditwürdigkeit, kritische
Infrastruktur etc., Pflichten ab 02.12.2027) oder KI in Produkten nach Anhang I
(ab 02.08.2028). Sie sind mit strengen Auflagen belegt.

## KI-Kompetenz (Art. 4 AI Act)
Pflicht für Anbieter und Betreiber seit 02.02.2025, Maßnahmen zu treffen, damit
ihr Personal KI sachkundig einsetzen kann. Seit 2026 klargestellt: kein
garantiertes Kompetenzniveau, aber nachweisbare Maßnahmen.

## LLM (Large Language Model)
Großes Sprachmodell. Es kann als Dienst eines Anbieters genutzt oder — bei offenen
Modellen — als Datei auf eigener Hardware betrieben werden.

## Lokal / On-Premise
Betrieb auf eigener Hardware im eigenen Netz. Gegensatz zu Cloud.

## Model Card
Datenblatt zu einem KI-Modell: Herkunft, Trainingsdaten, Einschränkungen,
vorgesehene Nutzung, Lizenz. Etabliert durch Google 2019.

## Prompt
Texteingabe an ein Sprachmodell. Kann unbeabsichtigt personenbezogene Daten enthalten.

## Pseudonymisierung
Ersetzen von Identifikatoren durch Kennungen, sodass eine Zuordnung nur mit
zusätzlichem Wissen möglich ist. Nicht gleich Anonymisierung.

## RAG (Retrieval-Augmented Generation)
KI-Architektur, die Dokumente zur Laufzeit aus einer Datenbank lädt und dem
Modell als Kontext mitgibt. Daten werden nicht im Modell gespeichert — leichter
zu löschen als Fine-Tuning. Bei einem Cloud-Modell gehen die gefundenen Stellen
mit jeder Anfrage an den Anbieter.

## Schrems II
EuGH-Urteil 2020, das den Privacy Shield kippte. Seit Juli 2023 gibt es mit dem
→ Data Privacy Framework einen neuen Angemessenheitsbeschluss; für nicht
zertifizierte Empfänger bleiben SCC plus TIA nötig.

## Standardvertragsklauseln (SCC)
Von der EU vorgegebene Mustervertragsklauseln für Drittlandübermittlungen.

## Transfer Impact Assessment (TIA)
Bewertung, ob im Empfangsland ein mit der EU vergleichbarer Schutz gewährleistet
ist. Nötig zusätzlich zu SCC, wenn kein Angemessenheitsbeschluss greift.

## Verarbeitungsverzeichnis
Dokumentation aller Datenverarbeitungen nach Art. 30 DSGVO. Die Ausnahme für
Unternehmen unter 250 Mitarbeitern greift nur, wenn die Verarbeitung gelegentlich
erfolgt, kein Risiko birgt und keine besonderen Kategorien betrifft — in der
Praxis selten. Eine geplante Lockerung (Schwelle 750, „Omnibus IV“) war am
18.10.2026 noch nicht beschlossen.

## Vektor-Datenbank
Speichert numerische Repräsentationen (Embeddings) von Texten für
Ähnlichkeitssuche. Teil typischer RAG-Systeme.

## Zero Data Retention
Zusage eines Cloud-Anbieters, Eingaben und Ausgaben nicht über die Bearbeitung
der Anfrage hinaus zu speichern. Oft eine eigene Vertragsoption, nicht der Standard.
