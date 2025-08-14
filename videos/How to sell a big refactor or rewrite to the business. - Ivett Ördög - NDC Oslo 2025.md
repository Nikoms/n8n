# How to sell a big refactor or rewrite to the business? - Ivett Ördög - NDC Oslo 2025
![thumbnail](https://i.ytimg.com/vi/wdz90PQ2Ak4/maxresdefault.jpg)
[https://youtu.be/wdz90PQ2Ak4?si=4Gz3VnLq4olwP5r_](https://youtu.be/wdz90PQ2Ak4?si=4Gz3VnLq4olwP5r_)

## My thoughts

When to rewrite?

- Rewrites should focus on delivering customer value early and continuously, as per the Agile manifesto's highest priority.
- It’s important to approach rewrites incrementally, replacing parts of the system step-by-step rather than all at once.
- The strangling tree pattern is a useful strategy here: gradually growing new, improved parts around the old system until the legacy code can be fully replaced.
- Doing rewrites without delivering value during the process risks losing market share and getting shut down, so always align rewrites with feature delivery or critical platform transitions.

## TLDR;
- Viele Entwickler sind unzufrieden bei der Arbeit, hauptsächlich wegen schlechter Codequalität.
- Refaktorisierung ist unerlässlich, besonders bei von KI generiertem Code.
- Große Rewrites gelten als riskant, können aber unter bestimmten Voraussetzungen erfolgreich sein.
- Refaktorisierung ist klein und lokal, während Rewrites umfangreiche Neuerarchitekturen sind.
- Die Design-Stina-Hypothese beschreibt den Trade-off zwischen Designinvestition und Entwicklungsgeschwindigkeit.
- Erfolgreiche Startups haben oft Legacy-Code, da sie schnelle MVPs bevorzugen.
- Technische Schulden entstehen oft durch Vernachlässigung und sollten inkrementell angegangen werden.
- Rewrites scheitern häufig bei „Alles-oder-Nichts“-Ansatz ohne kontinuierlichen Geschäftswert.
- Fallstudien zeigen erfolgreiche Rewrites durch inkrementelle Migration oder neue Produktentwicklung:
  - Flash-Migration zu einem geschäftsorientierten Produkt
  - Schrittweiser Ersatz von Import- und Workflowsystemen
  - Entwicklung von VS Code als schlankes Produkt für einen neuen Markt
  - Teilweiser Frontend-Umstieg für bessere UX
- Erfolgreiche Strategien: Interne Konkurrenz schaffen oder inkrementell mit Kundenwert ersetzen.
- Rewrites sollten nicht als solche verkauft werden, sondern als Feature-Entwicklung.
- KI-Assistenz erleichtert, ersetzt aber nicht die Notwendigkeit von Refaktorisierung.
- Agile Prinzipien wie kontinuierliche Wertlieferung sollten Rewrites leiten.
- Audience-Fragen bestätigen, dass inkrementelle Wertschöpfung und Wettbewerbsdruck Erfolg fördern.
- Motivation steigt durch messbare Verbesserungen der Entwicklererfahrung (z.B. Shopify).
- Selbst ohne aktuellen Wettbewerb sollte man mit Konkurrenz rechnen.




## Content

### Einführung: Warum sprechen wir über Rewrites und Refaktorisierung?
Ich bin Evette und freue mich, heute über ein Thema zu sprechen, das allen Entwicklern bekannt ist: große Rewrites und Refaktorisierungen.

> „Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.“ – Agile Manifesto

Diese Zielsetzung ist der Leitfaden, wenn wir darüber nachdenken, wie wir Code und Produkte weiterentwickeln.

### Die Code-Qualitätskrise: Warum sind so viele Entwickler unglücklich?
Studien, wie die von Stack Overflow, zeigen, dass nur etwa 20 % der Entwickler zufrieden sind, während etwa ein Drittel mit einem Jobwechsel liebäugelt. Hauptgrund ist die schlechte Codequalität, die viele als frustrierend empfinden. Besonders heute sehen wir, wie KI-Programme oft schwer wartbaren Code erzeugen, deshalb ist Refaktorisierung ein wichtiger Schritt, um Qualität sicherzustellen.

> „Je mehr KI-Code erzeugt wird, desto größer ist leider auch der Anteil an Bugs und Redundanzen.“ – Diverse Studien

### Refactoring versus Rewrite: Was ist der Unterschied?
- **Refactoring** bedeutet kleine, lokale Verbesserungen am Code, oft ohne große Aufwände oder Bekanntmachung.
- **Rewrite** ist die umfassende Neuerstellung eines Systems ohne bewusst Verhaltensänderungen, oft risikoreich und aufwändig.

Rewrites werden oft negativ bewertet, z.B. Joski bezeichnete den Netscape-Rewrite als „schlechtesten strategischen Fehler“. Trotzdem träumen viele Entwickler von Rewrites, lernen aber schnell, wie komplex diese sind.

### Die Design Stina Hypothese: Investment und Geschwindigkeit
Martin Fowler stellte die Hypothese vor, dass zu wenig Design die Produktivität senkt, aber zu viel Design anfangs den Fortschritt bremst. Startups bevorzugen schnelle MVPs vor perfektem Design, was alte Systeme mit Legacy-Code erklärt.

> „Technical Debt ist oft eigentlich Technical Neglect.“ – Kevlin Henney

Das bedeutet: Viele technische Schulden entstehen durch Nicht-Bezahlung der notwendigen Wartung.

### Warum sind Rewrites riskant?
Rewrites sind riskant, weil sie häufig als „Alles-oder-Nichts“-Projekte betrieben werden, bei denen während der Arbeit kein echter Mehrwert für Kunden entsteht. Dadurch droht die Konkurrenz schneller zu sein, und das Projekt scheitert.

### Fallstudien: Erfolgreiche Rewrites trotz Risiken
- **Migration von Adobe Flash:** Statt sofort alles neu zu schreiben, begann man mit einem minimalistischen Produkt für Geschäfts-Kunden und erweiterte es sukzessive.
- **Monolithische Workflow-Systeme:** Schrittweise wurde problematischer Code ersetzt, trotz Fehlern und Herausforderungen.
- **Täglicher Datenimport:** Für Schlüsselkunden wurde eine 25-Stunden-Prozedur auf 5 Sekunden reduziert, anschließend inkrementeller Rollout.
- **Plattform mit externen APIs:** Neue APIs und Microservices wurden Stück für Stück eingeführt und gleichzeitig refaktoriert.
- **VS Code:** Kein Ersatz für Visual Studio, sondern ein neues, schlankes Produkt für einen neuen Markt mit maßgeblichem Erfolg.
- **Limp Poker Frontend:** Alte und neue Frontend-Komponenten liefen parallel, um Risiken zu minimieren.

### Erkenntnisse: Erfolgsfaktoren für Rewrites
1. Rewrites müssen Wert schaffen und nicht nur internen Code erneuern.
2. Ein inkrementeller Ansatz ist erfolgsentscheidend – „Alles-oder-Nichts“ führt meist zum Scheitern.

> „Verkauft keine Rewrite-Projekte als Rewrite – verkauft Features und Verbesserungen." 

### Strategien für erfolgreiche Rewrites
- **Interne Konkurrenz schaffen:** Z.B. entwickeln neuer Produkte für andere Märkte (Flash, VS Code).
- **Inkrementeller Ersatz:** Schrittweiser Austausch problematischer Systemteile (Strangler Fig Pattern).

### Weitere Überlegungen und Fallstricke
Die Kombination aus inkrementeller Entwicklung und Kundenfokus maximiert die Chancen. Tools und KI können beschleunigen, ersetzen aber nicht die kritische Bewertung und Refaktorisierung.

> „KI kann Entwickler bis zu 30-40 % schneller machen, aber Code-Qualität bleibt entscheidend.“

### Fazit
Rewrites sind keine Tabu-Themen, wenn sie mit Strategie, Kundenorientierung und schrittweisem Vorgehen umgesetzt werden. Refaktorisierung bleibt essenziell, gerade auch im Zeitalter von KI-gestützter Programmierung.

### Ausblick und Ressourcen
- Folge meinem YouTube-Kanal für weitere technische Insights.
- Melde dich für mein Coaching-Programm an, um Präsentationen und technische Kommunikation zu verbessern.

Fragen sind jederzeit willkommen – sprich mich gern an!
