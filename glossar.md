# Glossar

Kurzerklärungen der wichtigsten Begriffe. Ohne Anspruch auf juristische Vollständigkeit.

## Angemessenheitsbeschluss
Feststellung der EU-Kommission, dass ein Drittland ein mit der EU vergleichbares
Datenschutzniveau hat. Ohne solchen Beschluss sind zusätzliche Garantien (z.B. SCC) nötig.

## Auftragsverarbeitungsvertrag (AVV)
Vertrag nach Art. 28 DSGVO zwischen Verantwortlichem und Dienstleister, der die
Verarbeitung personenbezogener Daten im Auftrag regelt.

## Datenschutz-Folgenabschätzung (DSFA)
Strukturierte Risikoanalyse nach Art. 35 DSGVO, verpflichtend bei voraussichtlich
hohem Risiko für Betroffene.

## EU AI Act
Verordnung (EU) 2024/1689. Risikobasierter Regulierungsrahmen für KI-Systeme.
Seit August 2026 vollständig anwendbar.

## Fine-Tuning
Nachtraining eines vortrainierten Modells mit eigenen Daten. Die Daten werden
dabei implizit "gelernt" und sind schwer wieder zu löschen.

## Halluzination
KI-Ausgabe, die plausibel klingt, aber faktisch falsch ist. Typisches Risiko bei
generativen Sprachmodellen.

## Hochrisiko-KI
Systeme nach Anhang III des AI Act, die mit strengen Auflagen belegt sind
(Personalauswahl, Scoring, kritische Infrastruktur etc.).

## LLM (Large Language Model)
Großes Sprachmodell. Beispiele: GPT-4, Claude, Llama, Qwen, Mistral.

## Lokal / On-Premise
Betrieb auf eigener Hardware im eigenen Netz. Gegensatz zu Cloud.

## Model Card
Datenblatt zu einem KI-Modell: Herkunft, Trainingsdaten, Einschränkungen,
vorgesehene Nutzung. Etabliert durch Google 2019.

## Prompt
Texteingabe an ein Sprachmodell. Kann unbeabsichtigt personenbezogene Daten enthalten.

## Pseudonymisierung
Ersetzen von Identifikatoren durch Kennungen, sodass eine Zuordnung nur mit
zusätzlichem Wissen möglich ist. Nicht gleich Anonymisierung.

## RAG (Retrieval-Augmented Generation)
KI-Architektur, die Dokumente zur Laufzeit aus einer Datenbank lädt und dem
Modell als Kontext mitgibt. Daten werden nicht im Modell gespeichert — leichter
zu löschen als Fine-Tuning.

## Schrems II
EuGH-Urteil 2020, das den Privacy Shield kippte. Seitdem sind
US-Datenübermittlungen nur mit zusätzlichen Garantien zulässig.

## Standardvertragsklauseln (SCC)
Von der EU vorgegebene Mustervertragsklauseln für Drittlandübermittlungen.

## Transfer Impact Assessment (TIA)
Bewertung, ob im Empfangsland ein mit der EU vergleichbarer Schutz gewährleistet
ist. Nötig zusätzlich zu SCC nach Schrems II.

## Verarbeitungsverzeichnis
Dokumentation aller Datenverarbeitungen nach Art. 30 DSGVO. Pflicht für
Unternehmen ab 250 Mitarbeitern und für risikoreiche Verarbeitungen.

## Vektor-Datenbank
Speichert numerische Repräsentationen (Embeddings) von Texten für
Ähnlichkeitssuche. Teil typischer RAG-Systeme.
