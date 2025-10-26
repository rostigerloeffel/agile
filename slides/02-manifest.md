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

## Wert 1: Praxisbeispiele

✅ **DO:**
- **Daily Stand-up** am Kanban Board
  - Team synchronisiert sich in 15 Min
  - Blocker werden sofort angesprochen
- **Pair Programming**
  - Wissenstransfer in Echtzeit
  - Höhere Code-Qualität
- **Face-to-Face Kommunikation**
  - Videocall statt E-Mail-Kette
  - Schnellere Entscheidungen

❌ **DON'T:**
- "Steht so im Prozess" als Totschlagargument
- Tool-Gläubigkeit: "Jira löst unsere Probleme"
- Alle Kommunikation nur über Tickets
- "Nicht meine Abteilung"-Mentalität

Note:
Beispiel: Ein Team hatte 3 Tage E-Mail-Ping-Pong. Ein 15-minütiger Call löste das Problem. Prozesse sollen Menschen unterstützen, nicht einschränken.

--

## Real-World: Spotify's Squad Model

**Beispiel:** Spotify organisiert sich in **Squads** (kleine, autonome Teams)
- 6-12 Personen
- Cross-functional (Design, Dev, QA, Product)
- Eigenes Mission & KPIs
- **Minimale Prozess-Vorgaben**

**Resultat:**
- Schnelle Entscheidungen
- Hohe Ownership
- Innovation durch Autonomie

**Lehre:** Menschen > Organigramme

Note:
Spotify zeigt: Wenn man den Menschen vertraut und ihnen Freiraum gibt, entstehen großartige Produkte. Nicht der Prozess macht's, sondern die Menschen.

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

## Wert 2: Praxisbeispiele

✅ **DO:**
- **Working Demo** im Sprint Review
  - Stakeholder sehen echte Features
  - Sofortiges Feedback
- **Living Documentation**
  - API-Docs aus Code generiert
  - Tests als Spezifikation
- **README über Architecture Decision Records**
  - Knapp, aktuell, relevant

**Angemessene Doku:**
- API-Dokumentation (Swagger/OpenAPI)
- Architecture Decision Records (ADRs)
- Onboarding-Guides
- Runbooks für Operations

Note:
Gute Dokumentation veraltet nicht, weil sie nah am Code ist. Tests sind oft die beste Dokumentation - sie lügen nie.

--

## Wert 2: Praxisbeispiele (Fortsetzung)

❌ **DON'T:**
- **100-Seiten Pflichtenheft** vor der ersten Zeile Code
  - Veraltet sofort
  - Niemand liest es vollständig
- **Dokumentation statt Demo**
  - "Die Funktion ist fast fertig, hier die PowerPoint"
  - Stakeholder sehen nichts Greifbares
- **Duplicate Information**
  - Doku sagt eins, Code macht was anderes
  - Wartungsalptraum

**Red Flag:** Wenn mehr Zeit für Doku als für Code draufgeht!

Note:
Faustregel: Dokumentiere Entscheidungen (Warum), nicht Implementierung (Was/Wie - das steht im Code). Code erklärt das "Was", Tests das "Wie", Doku das "Warum".

--

## Real-World: Amazon's "Working Backwards"

**Beispiel:** Amazon startet neue Features mit einem **Press Release**
- 1 Seite Produkt-Ankündigung (für Kunden)
- Beschreibt Kundennutzen, nicht Features
- Dann erst: Entwicklung

**Plus:** FAQ & Mock-Ups - aber keine umfassende Spezifikation!

**Resultat:**
- Fokus auf Kundenwert
- Klare Vision
- Minimale Up-Front Doku

**Lehre:** Dokumentation muss einen Zweck haben

Note:
Amazon dreht es um: Erst das Endergebnis beschreiben (Press Release), dann entwickeln. Das zwingt zu Klarheit über den Wert. Keine Spezifikation, sondern Vision.

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

## Wert 3: Praxisbeispiele

✅ **DO:**
- **Product Owner im Team**
  - Täglich verfügbar für Fragen
  - Nimmt an Sprint Reviews teil
  - Priorisiert Backlog gemeinsam mit Team
- **Sprint Reviews mit echten Usern**
  - Nicht nur Stakeholder, auch End-User
  - Sofortiges, ehrliches Feedback
- **User Story Mapping Sessions**
  - Team und Kunde mappen Journey gemeinsam
  - Gemeinsames Verständnis

**Beispiel:** Online-Shop
- Product Owner: Täglich im Slack-Channel
- Alle 2 Wochen: Demo mit echten Shop-Betreibern
- Feedback fließt sofort in nächsten Sprint

Note:
Ein guter Product Owner ist Gold wert! Sie oder er ist die Brücke zwischen Business und Tech - und sollte täglich verfügbar sein.

--

## Wert 3: Praxisbeispiele (Fortsetzung)

❌ **DON'T:**
- **Fixed-Price, Fixed-Scope Verträge**
  - "Alle Features stehen fest, keine Änderungen"
  - Realität: Anforderungen ändern sich IMMER
  - Resultat: Change Requests, Konflikte
- **"Fence Throwing"**
  - Anforderungen über den Zaun werfen
  - Monate später: "So habe ich das nicht gemeint"
- **Nur am Anfang und Ende involviert**
  - Kickoff → 6 Monate Stille → Präsentation
  - Keine Chance für Korrekturen

**Red Flag:** "Der Kunde will uns nicht stören"

Note:
Der Kunde MUSS "stören" dürfen! Besser jede Woche kleine Korrekturen als nach 6 Monaten die große Katastrophe. Agile Verträge arbeiten mit Time & Material oder Money-for-Nothing.

--

## Real-World: Gov.uk Digital Service

**Beispiel:** UK Government Digital Service (GDS)
- Entwickelt öffentliche Websites agil
- **User Researchers** im Team
- Jede Woche: Tests mit echten Bürgern
- Iterative Verbesserung

**Resultat:**
- gov.uk von 3.000 auf 1 Website konsolidiert
- Nutzerzufriedenheit: 90%+
- £1,7 Mrd. Einsparungen in 5 Jahren

**Lehre:** User Feedback > Expertenmeinungen

Note:
Die britische Regierung zeigt: Auch im öffentlichen Sektor funktioniert agiles Vorgehen. Durch kontinuierliches User Testing entstand eine der besten Regierungs-Websites der Welt.

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

## Wert 4: Praxisbeispiele

✅ **DO:**
- **Sprint Planning mit Flexibilität**
  - Commitment für Sprint, nicht für 6 Monate
  - Anpassung nach jedem Sprint
- **Pivots sind OK**
  - Markt ändert sich? → Prioritäten anpassen
  - Technologie veraltet? → Stack wechseln
- **A/B Tests & Experimente**
  - Feature ausrollen, messen, lernen
  - Bei Misserfolg: Schnell stoppen

**Beispiel:** E-Commerce Feature
- Hypothese: "Kunden wollen 1-Click-Checkout"
- Sprint 1: MVP implementieren
- Messung: Conversion -5% (!)
- Reaktion: Feature entfernen, anderen Ansatz testen

Note:
Das ist der Kern empirischen Arbeitens: Hypothese aufstellen, testen, messen, lernen, anpassen. Misserfolge sind Lern-Chancen, keine Katastrophen.

--

## Wert 4: Praxisbeispiele (Fortsetzung)

❌ **DON'T:**
- **Jahres-Roadmaps mit fixen Features**
  - "Q3 2024: Feature X, Q4 2024: Feature Y"
  - Realität: Markt, Technik, Prioritäten ändern sich
- **"Scope Creep" als Feindbild**
  - Änderungen als Problem sehen
  - "Steht nicht im Vertrag!"
- **Ignorieren von Feedback**
  - "Wir haben schon 6 Monate investiert, jetzt ziehen wir durch"
  - Sunk Cost Fallacy

**Red Flag:** "Das haben wir so geplant, das machen wir so!"

Note:
Rigide Pläne sind eine Illusion von Kontrolle. Die Welt ändert sich - gute Teams ändern sich mit. Das berühmte Zitat: "Plans are worthless, but planning is everything" (Eisenhower).

--

## Real-World: Spotify's Bet Model

**Beispiel:** Spotify arbeitet mit **Bets statt Plänen**
- Keine Feature-Roadmap, sondern Wetten/Hypothesen
- "Wir glauben, dass Feature X Problem Y löst"
- Timeboxed: 4-8 Wochen
- Erfolgskriterien definiert
- **Bei Misserfolg: Stoppen!**

**Resultat:**
- 30% der Bets werden gestoppt
- Ressourcen fließen zu erfolgreichen Initiativen
- Kultur des Experimentierens

**Lehre:** Pläne sind Hypothesen, keine Versprechungen

Note:
Spotify macht's vor: Behandle Features als Experimente. Manche scheitern - das ist OK und sogar gewünscht, denn es bedeutet, man lernt schnell.

---

## Die 12 Prinzipien (Überblick)

Das Agile Manifest hat auch **12 Prinzipien** - hier die wichtigsten:

1. **Kundennutzen** - Frühe, kontinuierliche Auslieferung wertvoll Software
2. **Änderungen willkommen** - Auch spät in der Entwicklung
3. **Häufige Lieferung** - Alle paar Wochen/Monate
4. **Tägliche Zusammenarbeit** - Business & Entwickler arbeiten täglich zusammen
5. **Motivierte Individuen** - Vertrauen, Unterstützung, Umfeld geben
6. **Face-to-Face Kommunikation** - Effizienteste Methode

Note:
Wir gehen nicht alle 12 durch (das wäre zu viel), aber schauen uns die praxisrelevantesten an.

--

## Die 12 Prinzipien (Fortsetzung)

7. **Funktionierende Software** - Primäres Fortschrittsmaß
8. **Nachhaltige Entwicklung** - Gleichmäßiges Tempo auf Dauer
9. **Technische Exzellenz** - Continuous Attention to Excellence
10. **Einfachheit** - Kunst, Arbeit die nicht getan werden muss zu maximieren
11. **Selbstorganisation** - Beste Architekturen/Designs von selbstorganisierten Teams
12. **Regelmäßige Reflexion** - In Abständen reflektieren und Verhalten anpassen

Note:
Diese Prinzipien sind zeitlos. Sie gelten genauso heute wie 2001 - weil sie fundamentale Wahrheiten über Softwareentwicklung beschreiben.

---

## Praxisrelevante Prinzipien: Deep Dive

Schauen wir uns 3 besonders wichtige Prinzipien genauer an:

--

## Prinzip 8: Nachhaltiges Tempo

> **"Agile Prozesse fördern nachhaltige Entwicklung. Die Auftraggeber, Entwickler und Benutzer sollten ein gleichmäßiges Tempo auf unbegrenzte Zeit halten können."**

**Was heißt das konkret?**

✅ **DO:**
- **40-Stunden-Woche** als Standard
- Überstunden sind Ausnahme, nicht Regel
- Urlaub wird genommen, nicht gehortet
- Burnout-Prävention durch Work-Life-Balance

❌ **DON'T:**
- **"Sprint-Heroics"** - Jeder Sprint mit Überstunden
- Vacation shaming ("Du nimmst schon wieder Urlaub?")
- "Crunch Time" als Dauerzustand
- Velocity durch Überlastung steigern

Note:
Software-Entwicklung ist ein Marathon, kein Sprint. Übermüdete Entwickler machen Fehler, die später teuer werden. Nachhaltigkeit ist langfristig produktiver.

--

## Prinzip 8: Real-World Beispiel

**Anti-Pattern: "Death March Project"**
- 6 Monate: 60-80 Stunden/Woche
- Team: Erschöpft, hohe Fluktuation
- Code-Qualität: Technische Schulden
- Resultat: Projekt fertig, Team kaputt

**Agile Alternative:**
- Realistische Sprint-Planung
- Velocity basiert auf 40h/Woche
- Bei Überlastung: Scope reduzieren, nicht Menschen überlasten
- Resultat: Langfristig höhere Produktivität

**Metric:** "Sustainable Pace" messen
- Überstunden tracken
- Krankheitstage beobachten
- Fluktuation im Auge behalten

Note:
Ein Team, das regelmäßig 60-Stunden-Wochen arbeitet, ist nicht "engagiert", sondern falsch geplant. Das Management muss Scope reduzieren, nicht Druck erhöhen.

--

## Prinzip 9: Technische Exzellenz

> **"Ständiges Augenmerk auf technische Exzellenz und gutes Design fördert Agilität."**

**Was heißt das konkret?**

✅ **DO:**
- **Test-Driven Development (TDD)**
- **Continuous Integration/Deployment**
- **Code Reviews** & Pair Programming
- **Refactoring** als Teil jedes Sprints
- **Definition of Done** beinhaltet Tests, Doku

❌ **DON'T:**
- "Erst Features, später Qualität"
- "Keine Zeit für Tests"
- "Technical Debt Sprint" in 6 Monaten
- Copy-Paste statt Refactoring

Note:
Technische Exzellenz ist kein Luxus, sondern Voraussetzung für Agilität. Schlechter Code macht Änderungen teuer und langsam - das Gegenteil von agil!

--

## Prinzip 9: Real-World Beispiel

**Google's 20% Zeit + Code Quality**
- Entwickler dürfen 20% Zeit für Tech Debt nutzen
- Strenge Code Review-Kultur
- Automated Testing als Standard
- Resultat: Hohe Qualität, schnelle Innovation

**Netflix's Chaos Engineering**
- "Chaos Monkey" testet Resilienz
- Production wird regelmäßig gestresst
- Resultat: 99,99% Uptime

**Lehre:** Investition in Qualität zahlt sich aus
- Weniger Bugs
- Schnellere Features (kein Legacy-Ballast)
- Weniger Stress im Team

Note:
Die besten Unternehmen behandeln Qualität nicht als Optional. Google, Netflix, Amazon - alle investieren massiv in technische Exzellenz. Das ist kein Zufall.

--

## Prinzip 10: Einfachheit

> **"Einfachheit -- die Kunst, die Menge nicht getaner Arbeit zu maximieren -- ist essenziell."**

**Das meistmissverstandene Prinzip!**

Nicht: "Einfache Lösungen bauen"
Sondern: **"Unnötige Arbeit vermeiden!"**

✅ **DO:**
- **YAGNI** (You Aren't Gonna Need It)
  - Nur Features bauen, die JETZT gebraucht werden
- **MVP** (Minimum Viable Product)
  - Kleinstmögliche Version, die Wert liefert
- **Kill Features**
  - Ungenutzte Features entfernen

Note:
Der größte Waste in Software: Features, die niemand benutzt. Studien zeigen: 45% aller Features werden nie oder selten genutzt. Das ist reine Verschwendung!

--

## Prinzip 10: Praxisbeispiele

❌ **DON'T:**
- **Over-Engineering**
  - "Was wenn wir das mal brauchen?"
  - Generische Frameworks für spezifische Probleme
- **Feature Bloat**
  - "Können wir nicht noch XYZ hinzufügen?"
  - Resultat: Komplexe, unübersichtliche Software
- **Premature Optimization**
  - "Das muss super-performant sein!" (aber niemand nutzt es)

✅ **DO:**
- **Start simple, grow as needed**
- **Feature Flags** für Experimente
  - Feature einschalten, messen, bei Misserfolg: AUS
- **Usage Analytics**
  - Welche Features werden WIRKLICH genutzt?

**Beispiel:** Basecamp removed 30% ihrer Features
- Analytics zeigten: <5% Nutzung
- Resultat: Einfachere, fokussiertere App

Note:
Die Kunst ist, NEIN zu sagen. Jedes Feature hat Kosten: Entwicklung, Wartung, Komplexität. Einfachheit bedeutet: Maximalen Wert mit minimalen Features.

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
