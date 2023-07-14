# Search with Query - Text Embedding

### Einleitung
In diesem Bericht wird das durchgeführte Experiment erläutert, das zur Erstellung der
bereitgestellten Rangliste geführt hat. Das Ziel des Projekts bestand darin, ein Information
Retrieval System einzusetzen, um relevante Dokumente zu jeder Abfrage in einer Sammlung
von Dokumenten zu extrahieren. Dieser Bericht gibt einen Überblick über die verwendeten
Systeme, die Motivation hinter dem Experiment, die Struktur des Index, die Formulierung der
Abfragen und die Interpretation der Ergebnisse.

### Verwendete Systeme und Motivation
Für dieses Projekt wurde das Text-Embedding-Modell text-embedding-ada-002 von OpenAI
verwendet. Dieses vor-trainierte Text-Embedding-Modell bietet leistungsstarke
Möglichkeiten zur Darstellung von Textdaten in einem hochdimensionalen Raum. Die
Motivation für die Verwendung eines solchen Modells bestand darin, die in den Embeddings
codierten semantischen Informationen zu nutzen, um genauere Vergleiche und
Ähnlichkeitsmessungen zwischen Dokumenten und Abfragen zu ermöglichen.

### Index-Struktur
Der Index in diesem Projekt wurde unter Verwendung des Text-Embedding-Modells text-
embedding-ada-002 erstellt. Die erzeugten Text Embedding Vektoren sowohl für die
Dokumentensammlung als auch für die Abfrageliste dienten als Grundlage für den Index.
Jedes Dokument und jede Abfrage wurde in einen Vektor fester Länge von 1536
Dimensionen transformiert. Diese Vektoren erfassen die semantische Bedeutung und den
Kontext der jeweiligen Textelemente und ermöglichen einen effizienten Vergleich und Abruf.

### Rangliste
Um die Ähnlichkeiten zwischen den Dokumenten und den Abfragen zu bewerten, wurde die
Kosinus-Ähnlichkeit verwendet. Die Kosinus-Ähnlichkeit misst den Kosinus des Winkels
zwischen den Vektoren jedes Dokuments und jeder Abfrage und liefert eine Metrik zur
Bewertung ihrer Ähnlichkeit. Durch Berechnung der Kosinus-Ähnlichkeit zwischen den
Embeddingsvektoren jeder Abfrage und den Dokumenten wurde eine Rangliste von
Dokument-Abfrage-Paaren erstellt. Je höher der Wert der Kosinus-Ähnlichkeit ist, desto
ähnlicher werden das Dokument und die Abfrage betrachtet.

### Interpretation der Ergebnisse
Die generierte Rangliste liefert eine quantitative Bewertung der Ähnlichkeiten zwischen den
Dokumenten der Sammlung und den Abfragen. Höhere Werte der Kosinus-Ähnlichkeit
deuten auf eine stärkere semantische Ähnlichkeit zwischen Dokument-Abfrage-Paaren hin.
Folglich gelten Dokumente, die oben in der Rangliste stehen, als relevanter für die
entsprechende Abfrage.
