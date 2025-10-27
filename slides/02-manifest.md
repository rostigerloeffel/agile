<!-- .slide: data-background="#4CAF50" -->

# 📜 Das Agile Manifest

Werte und Prinzipien agiler Softwareentwicklung

Note:
Jetzt tauchen wir ins Herz von Agile ein: Das Manifest und seine 12 Prinzipien. Diese bilden die Grundlage ALLER agilen Frameworks.

---

## Die 4 Werte des Agile Manifests

> Wir erschließen bessere Wege, Software zu entwickeln, indem wir es selbst tun und anderen dabei helfen.
>
> Durch diese Tätigkeit haben wir diese Werte zu schätzen gelernt:

**[agilemanifesto.org](https://agilemanifesto.org/iso/de/manifesto.html)**

Note:
Wichtig: Das Manifest sagt nicht, dass die Dinge auf der rechten Seite wertlos sind. Aber die Dinge auf der linken Seite werden höher bewertet.

---

## Wert 1: Individuen & Interaktionen

### **Individuen und Interaktionen**
### mehr als Prozesse und Werkzeuge

**Was bedeutet das?**
- Menschen sind wichtiger als Prozesse
- Direkte Kommunikation > Dokumentierte Prozesse
- Problemlösung durch Zusammenarbeit

Note:
Der erste und wichtigste Wert! Software wird von Menschen für Menschen gemacht. Ein mittelmäßiger Prozess mit einem großartigen Team schlägt einen perfekten Prozess mit einem mittelmäßigen Team.

--

## Wert 1: DO's

✅ **DO:**
- **Daily Stand-up** am Board
  - 15 Min Synchronisation
- **Pair Programming**
  - Wissenstransfer in Echtzeit
- **Face-to-Face Kommunikation**
  - Videocall statt E-Mail-Kette

Note:
Prozesse sollen Menschen unterstützen, nicht einschränken. Erweiterte Erklärungen:
- Daily Stand-up am Kanban Board: Team synchronisiert sich in 15 Min, Blocker werden sofort angesprochen
- Pair Programming: Zwei Entwickler, ein Screen - Wissenstransfer in Echtzeit, höhere Code-Qualität
- Face-to-Face: Ein 15-Min Videocall kann 3 Tage E-Mail-Ping-Pong ersetzen. Schnellere Entscheidungen, weniger Missverständnisse

--

## Wert 1: DON'Ts

❌ **DON'T:**
- "Steht so im Prozess"
- Tool-Gläubigkeit
- Nur Ticket-Kommunikation
- "Nicht meine Abteilung"

Note:
Ein 15-Min Call kann 3 Tage E-Mail-Ping-Pong ersetzen. Erweiterte Anti-Patterns:
- "Steht so im Prozess": Prozess als Totschlagargument statt pragmatischer Lösungen
- Tool-Gläubigkeit: "Jira löst unsere Probleme" - Tools sind Hilfsmittel, keine Lösung
- Nur Ticket-Kommunikation: Alle Kommunikation nur über Tickets führt zu Verzögerungen
- "Nicht meine Abteilung"-Mentalität: Silodenken verhindert Zusammenarbeit und schnelle Lösungen

--

## Real-World: Spotify Squads

**Squads** = Kleine, autonome Teams
- 6-12 Personen
- Cross-functional
- Eigene Mission & KPIs
- Minimale Prozess-Vorgaben

**Lehre:** Menschen > Organigramme

Note:
Spotify zeigt: Vertrauen + Freiraum = großartige Produkte.

---

## Wert 2: Funktionierende Software

### **Funktionierende Software**
### mehr als umfassende Dokumentation

**Was bedeutet das?**
- Lauffähiger Code ist der beste Beweis
- Dokumentation nur wo nötig
- "Show, don't tell"

Note:
Nicht: "Keine Dokumentation!" Sondern: Dokumentation muss Wert liefern. Ein funktionierendes Feature sagt mehr als 100 Seiten Spezifikation.

--

## Wert 2: DO's

✅ **DO:**
- **Working Demo** im Sprint Review
- **Living Documentation**
  - API-Docs aus Code generiert
- **ADRs** (Architecture Decisions)
  - Knapp, aktuell, relevant

Note:
Gute Dokumentation bleibt nah am Code.

--

## Wert 2: Angemessene Doku

**Was dokumentieren?**
- API-Dokumentation (Swagger)
- Architecture Decision Records (ADRs)
- Onboarding-Guides
- Runbooks für Operations

Note:
Tests sind oft die beste Dokumentation - sie lügen nie.

--

## Wert 2: DON'Ts

❌ **DON'T:**
- 100-Seiten Pflichtenheft vor Code
- Dokumentation statt Demo
- Doku ≠ Code (Duplicate Information)

**Red Flag:** Mehr Zeit für Doku als für Code!

Note:
Faustregel: Dokumentiere Entscheidungen (Warum), nicht Implementierung (Was/Wie). Details:
- 100-Seiten Pflichtenheft: Veraltet sofort nach Fertigstellung, niemand liest es vollständig
- Dokumentation statt Demo: "Die Funktion ist fast fertig, hier die PowerPoint" - Stakeholder sehen nichts Greifbares
- Duplicate Information: Doku sagt eins, Code macht was anderes - Wartungsalptraum
- Code erklärt das "Was", Tests das "Wie", Dokumentation das "Warum"

--

## Real-World: Amazon's "Working Backwards"

**Ansatz:** Neue Features starten mit **1-seitigem Press Release**
- Kundennutzen, nicht Features
- FAQ & Mock-Ups
- Dann erst: Entwicklung

**Lehre:** Vision > umfassende Spezifikation

Note:
Amazon dreht es um: Erst das Endergebnis beschreiben, dann entwickeln. Details:
- 1-seitige Produkt-Ankündigung für Kunden (nicht interne Spezifikation)
- Beschreibt Kundennutzen, nicht technische Features
- Plus: FAQ & Mock-Ups zeigen die Vision
- Aber: Keine umfassende technische Spezifikation up front
- Das zwingt zu Klarheit über den Wert und hält den Fokus auf Kundenbedürfnissen
- Dokumentation muss einen Zweck haben - Vision statt Bürokratie

---

## Wert 3: Zusammenarbeit mit dem Kunden

### **Zusammenarbeit mit dem Kunden**
### mehr als Vertragsverhandlung

**Was bedeutet das?**
- Kunde ist Teil des Teams
- Kontinuierliches Feedback
- Gemeinsame Verantwortung für Erfolg

Note:
Der klassische Ansatz: Vertrag aushandeln, dann entwickeln, am Ende liefern. Agile: Kunde ist kontinuierlich dabei, gibt Feedback, passt Prioritäten an.

--

## Wert 3: DO's

✅ **DO:**
- **Product Owner im Team**
  - Täglich verfügbar
- **Sprint Reviews mit End-Usern**
  - Sofortiges Feedback
- **User Story Mapping**
  - Gemeinsames Verständnis

Note:
Ein guter Product Owner ist Gold wert!

--

## Wert 3: Beispiel Online-Shop

**Product Owner Einbindung:**
- Täglich im Slack-Channel
- Alle 2 Wochen: Demo mit echten Betreibern
- Feedback sofort im nächsten Sprint

Note:
PO ist die Brücke zwischen Business und Tech.

--

## Wert 3: DON'Ts

❌ **DON'T:**
- Fixed-Price, Fixed-Scope Verträge
- "Fence Throwing" (Anforderungen über Zaun)
- Nur Kickoff + Enddemo

**Red Flag:** "Der Kunde will uns nicht stören"

Note:
Der Kunde MUSS "stören" dürfen! Besser wöchentliche Korrekturen als 6-Monats-Katastrophe.

--

## Real-World: Gov.uk

**UK Government Digital Service:**
- User Researchers im Team
- Wöchentliche Tests mit Bürgern
- Iterative Verbesserung

**Resultat:**
- 3.000 → 1 Website
- 90%+ Zufriedenheit
- £1,7 Mrd. Einsparungen

**Lehre:** User Feedback > Expertenmeinungen

Note:
Auch im öffentlichen Sektor funktioniert agiles Vorgehen.

---

## Wert 4: Reagieren auf Veränderung

### **Reagieren auf Veränderung**
### mehr als Befolgen eines Plans

**Was bedeutet das?**
- Pläne sind wichtig, aber nicht in Stein gemeißelt
- Änderungen sind normal und wertvoll
- Empirisches Vorgehen: Inspect & Adapt

Note:
Der klassische Plan sagt: "So wird's gemacht, Punkt." Agile sagt: "Das ist unsere aktuelle beste Annahme - wir passen an, sobald wir mehr wissen."

--

## Wert 4: DO's

✅ **DO:**
- **Sprint Planning mit Flexibilität**
  - Commitment für Sprint, nicht Monate
- **Pivots sind OK**
  - Markt ändert sich? → Anpassen!
- **A/B Tests & Experimente**
  - Ausrollen, messen, lernen

Note:
Empirisches Arbeiten: Hypothese → Testen → Lernen → Anpassen.

--

## Wert 4: Beispiel E-Commerce

**Feature-Experiment:**
- Hypothese: "1-Click-Checkout"
- Sprint 1: MVP
- Messung: Conversion -5% ❌
- Reaktion: Feature entfernen

Note:
Misserfolge sind Lern-Chancen, keine Katastrophen.

--

## Wert 4: DON'Ts

❌ **DON'T:**
- Jahres-Roadmaps mit fixen Features
- "Scope Creep" als Feindbild
- Feedback ignorieren (Sunk Cost Fallacy)

**Red Flag:** "Das haben wir so geplant!"

Note:
Rigide Pläne = Illusion von Kontrolle. "Plans are worthless, but planning is everything" (Eisenhower).

--

## Real-World: Spotify Bets

**Bets statt Plänen:**
- Wetten/Hypothesen statt Roadmap
- Timeboxed: 4-8 Wochen
- **Bei Misserfolg: Stoppen!**

**Resultat:**
- 30% werden gestoppt
- Ressourcen zu Erfolgen
- Kultur des Experimentierens

**Lehre:** Features sind Hypothesen

Note:
Behandle Features als Experimente. Manche scheitern - das ist OK!

---

## Die 12 Prinzipien (1/3)

Das Agile Manifest hat **12 Prinzipien**:

1. **Kundennutzen** - Frühe Auslieferung
2. **Änderungen willkommen**
3. **Häufige Lieferung** - Alle paar Wochen
4. **Tägliche Zusammenarbeit**

Note:
Wir schauen uns die praxisrelevantesten an.

--

## Die 12 Prinzipien (2/3)

5. **Motivierte Individuen** - Vertrauen geben
6. **Face-to-Face Kommunikation**
7. **Funktionierende Software** - Primäres Fortschrittsmaß
8. **Nachhaltige Entwicklung** - Gleichmäßiges Tempo

Note:
Diese Prinzipien sind zeitlos.

--

## Die 12 Prinzipien (3/3)

9. **Technische Exzellenz**
10. **Einfachheit** - Arbeit maximieren, die NICHT getan werden muss
11. **Selbstorganisation**
12. **Regelmäßige Reflexion** - Anpassen

Note:
Fundamentale Wahrheiten über Softwareentwicklung.

---

## Praxisrelevante Prinzipien: Deep Dive

Schauen wir uns 3 besonders wichtige Prinzipien genauer an:

--

## Prinzip 8: Nachhaltiges Tempo

> **"Gleichmäßiges Tempo auf unbegrenzte Zeit halten können."**

✅ **DO:**
- 40-Stunden-Woche als Standard
- Urlaub wird genommen
- Burnout-Prävention

Note:
Software-Entwicklung ist ein Marathon, kein Sprint.

--

## Prinzip 8: DON'Ts

❌ **DON'T:**
- "Sprint-Heroics" (jeder Sprint Überstunden)
- Vacation shaming
- "Crunch Time" als Dauerzustand

Note:
Übermüdete Entwickler machen teure Fehler.

--

## Prinzip 8: Anti-Pattern

**"Death March Project"**
- 6 Monate: 60-80h/Woche
- Resultat: Projekt fertig, Team kaputt

**Agile Alternative:**
- Velocity basiert auf 40h/Woche
- Bei Überlastung: Scope reduzieren!

Note:
60h-Wochen = falsche Planung. Scope reduzieren, nicht Druck erhöhen.

--

## Prinzip 9: Technische Exzellenz

> **"Technische Exzellenz fördert Agilität."**

✅ **DO:**
- Test-Driven Development (TDD)
- Continuous Integration/Deployment
- Code Reviews & Pair Programming
- Refactoring in jedem Sprint

Note:
Technische Exzellenz = Voraussetzung für Agilität.

--

## Prinzip 9: DON'Ts

❌ **DON'T:**
- "Erst Features, später Qualität"
- "Keine Zeit für Tests"
- "Technical Debt Sprint" in 6 Monaten

Note:
Schlechter Code macht Änderungen teuer - das Gegenteil von agil!

--

## Prinzip 9: Beispiele

**Google:** 20% Zeit für Tech Debt
**Netflix:** Chaos Engineering

**Resultat:**
- Hohe Qualität
- Schnelle Innovation
- Weniger Bugs

**Lehre:** Qualität ist keine Option

Note:
Top-Unternehmen investieren massiv in technische Exzellenz.

--

## Prinzip 10: Einfachheit

> **"Die Kunst, die Menge nicht getaner Arbeit zu maximieren."**

**Nicht:** "Einfache Lösungen"
**Sondern:** "Unnötige Arbeit vermeiden!"

✅ **DO:**
- YAGNI (You Aren't Gonna Need It)
- MVP (Minimum Viable Product)
- Kill Features (ungenutzte entfernen)

Note:
45% aller Features werden nie/selten genutzt!

--

## Prinzip 10: DON'Ts

❌ **DON'T:**
- Over-Engineering
- Feature Bloat
- Premature Optimization

Note:
Jedes Feature hat Kosten: Entwicklung, Wartung, Komplexität.

--

## Prinzip 10: DO's

✅ **DO:**
- Start simple, grow as needed
- Feature Flags für Experimente
- Usage Analytics nutzen

**Beispiel:** Basecamp entfernte 30% der Features (<5% Nutzung)

Note:
Die Kunst ist, NEIN zu sagen.

---

## Häufige Missverständnisse über Agile

Es gibt viele **Mythen** über Agile. Räumen wir auf:

--

## Mythos 1: "Agile = Keine Planung"

❌ **Mythos:**
"Agile Teams planen nicht, sie improvisieren!"

✅ **Realität:**
Agile Teams planen **kontinuierlich**!
- Sprint Planning alle 2 Wochen
- Backlog Refinement regelmäßig
- Release Planning für größere Horizonte

**Unterschied:** Nicht 1x für 12 Monate planen, sondern alle 2 Wochen adjustieren.

**Zitat:** *"Plans are worthless, but planning is everything."* - Eisenhower

Note:
Agile plant sogar MEHR als Wasserfall - nur in kürzeren Zyklen. Der Plan wird ständig an neue Erkenntnisse angepasst.

--

## Mythos 2: "Agile = Keine Dokumentation"

❌ **Mythos:**
"Agile Teams dokumentieren nichts!"

✅ **Realität:**
Agile Teams dokumentieren **angemessen**!
- User Stories → Anforderungen
- Architecture Decision Records → Design-Entscheidungen
- API Docs (Swagger) → Schnittstellen
- README → Onboarding

**Unterschied:** Dokumentation hat Zweck, bleibt aktuell, lebt nah am Code.

**Red Flag:** Doku, die nach 1 Woche veraltet ist.

Note:
"Funktionierende Software über umfassende Dokumentation" heißt nicht "keine Doku". Es heißt: Doku wo sinnvoll, nicht als Selbstzweck.

--

## Mythos 3: "Agile = Chaos / Keine Struktur"

❌ **Mythos:**
"Agile ist chaotisch, jeder macht was er will!"

✅ **Realität:**
Agile hat **klare Strukturen**!
- Scrum: Rollen, Events, Artefakte
- Kanban: WIP Limits, Pull-System
- XP: Engineering Practices

**Unterschied:** Struktur dient dem Team, nicht umgekehrt.

**Beispiel:** Daily Scrum
- Feste Zeit (z.B. 9:00 Uhr)
- Feste Dauer (15 Min)
- Festes Format (3 Fragen)
→ Das ist Struktur!

Note:
Agile ist hochstrukturiert - aber die Struktur ist leichtgewichtig und dient der Effizienz, nicht der Kontrolle.

--

## Mythos 4: "Agile = Nur für Software"

❌ **Mythos:**
"Agile funktioniert nur in Software-Entwicklung!"

✅ **Realität:**
Agile funktioniert überall, wo **Komplexität + Unsicherheit** herrschen!

**Beispiele außerhalb IT:**
- **Marketing:** Sprint-basierte Kampagnen (Agile Marketing)
- **HR:** Iteratives Recruiting, OKRs
- **Hardware:** Tesla's iterative Entwicklung (OTA Updates)
- **Bildung:** Agile Lehrpläne, Retrospektiven mit Schülern
- **Bauwesen:** Lean Construction

**Lehre:** Die Prinzipien sind universell.

Note:
Agile ist ein Mindset, kein Software-Tool. Überall, wo man in komplexen, unsicheren Umgebungen arbeitet, hilft agiles Vorgehen.

---

## Zusammenfassung: Agile Manifest

**Die 4 Werte:**
1. 👥 Individuen & Interaktionen > Prozesse & Werkzeuge
2. ✅ Funktionierende Software > Umfassende Dokumentation
3. 🤝 Zusammenarbeit mit Kunden > Vertragsverhandlung
4. 🔄 Reagieren auf Veränderung > Befolgen eines Plans

**Wichtigste Prinzipien:**
- Frühe & kontinuierliche Lieferung
- Änderungen willkommen
- Nachhaltiges Tempo
- Technische Exzellenz
- Einfachheit (YAGNI)

**Wichtig:** Agile ist ein **Mindset**, kein Rezept!

Note:
Das Manifest ist nur 2 Seiten lang - aber es hat die Softwareentwicklung revolutioniert. Die Werte und Prinzipien sind zeitlos und gelten auch 20+ Jahre später.
