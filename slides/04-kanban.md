<!-- .slide: data-background="#9C27B0" -->

# 📊 Kanban

Visualize Work, Limit WIP, Manage Flow

Note:
Nach Scrum schauen wir uns Kanban an - ein anderes, flexibleres agiles Framework. Kanban kommt ursprünglich aus der Fertigung und ist perfekt für kontinuierlichen Flow.

---

## Was ist Kanban?

**Definition:**
> Kanban ist eine Methode zur **Visualisierung von Arbeit**, zur **Begrenzung laufender Arbeiten (WIP)** und zur **Maximierung von Effizienz (Flow)**.

**Ursprung:**
- 1940er: **Toyota Production System** (Taiichi Ohno)
- "Kanban" (看板) = Signalkarte
- 2007: David J. Anderson adaptiert für Software
-

**Kern-Idee:**
- Pull statt Push
- Visualisierung
- Continuous Flow (kein Sprint!)

Note:
Kanban kommt aus der Lean-Bewegung. Toyota nutzte Karten, um Material "zu ziehen" statt zu "pushen". In Software: Wir ziehen Tasks, wenn wir Kapazität haben.

---

## Kanban vs. Scrum: Unterschiede

| Aspekt | Scrum | Kanban |
|--------|-------|--------|
| **Iterationen** | Feste Sprints (1-4 Wochen) | Kontinuierlicher Flow |
| **Rollen** | PO, SM, Dev Team | Keine vorgeschrieben |
| **Planung** | Sprint Planning | Kontinuierlich |
| **Änderungen** | Innerhalb Sprint vermeiden | Jederzeit möglich |

Note:
Scrum = Rhythmus durch Sprints. Kanban = kontinuierlicher Flow. Beides hat Vor- und Nachteile.

--

## Kanban vs. Scrum: Unterschiede (2/2)

| Aspekt | Scrum | Kanban |
|--------|-------|--------|
| **Metriken** | Velocity, Burndown | Lead Time, Cycle Time |
| **Board** | Resettet nach Sprint | Kontinuierlich |
| **WIP Limits** | Implizit (Sprint Scope) | Explizit (pro Spalte) |

**Beide sind agil!** Nur unterschiedliche Ansätze.

Note:
Manche Teams nutzen auch Scrumban (Hybrid) - das Beste aus beiden Welten!

---

## Die 6 Kanban-Praktiken

David J. Anderson definiert **6 Kern-Praktiken**:

1. **Visualize the Workflow** - Mache Arbeit sichtbar
2. **Limit Work in Progress (WIP)** - Begrenze parallele Arbeit
3. **Manage Flow** - Optimiere den Fluss
4. **Make Process Policies Explicit** - Prozessregeln transparent
5. **Implement Feedback Loops** - Feedback-Schleifen
6. **Improve Collaboratively** - Experimentelle Evolution

Schauen wir uns jede Praktik an!

Note:
Diese 6 Praktiken sind das Herz von Kanban. Sie sind einfach zu verstehen, aber schwer zu meistern.

---

## Praktik 1: Visualize the Workflow

**Warum?**
- Menschen sind visuell
- Unsichtbare Arbeit = Unmanaged Arbeit
- Transparenz schafft Verständnis

**Wie?**
- **Kanban Board** mit Spalten
- Jede Spalte = ein Status
- Jede Karte = ein Work Item

Note:
"Was nicht sichtbar ist, kann nicht gemanaged werden." Das Kanban Board macht den gesamten Workflow transparent - für alle!

--

## Ein einfaches Kanban Board

```
┌─────────────┬─────────────┬─────────────┬─────────────┐
│   Backlog   │    To Do    │ In Progress │    Done     │
├─────────────┼─────────────┼─────────────┼─────────────┤
│ [Task E]    │ [Task C]    │ [Task A]    │ [Task X]    │
│ [Task F]    │ [Task D]    │ [Task B]    │ [Task Y]    │
│ [Task G]    │             │             │ [Task Z]    │
│ ...         │             │             │             │
└─────────────┴─────────────┴─────────────┴─────────────┘
```

**Simpel, aber effektiv!**

--

## Erweitertes Kanban Board

```
┌─────┬─────────┬──────────┬─────────┬──────────┬─────────┬──────┐
│Back-│Selected │  Dev     │  Code   │   Test   │  Deploy │ Done │
│ log │ for Dev │          │ Review  │          │         │      │
├─────┼─────────┼──────────┼─────────┼──────────┼─────────┼──────┤
│     │ WIP: 3  │ WIP: 2   │ WIP: 2  │  WIP: 3  │ WIP: 1  │      │
├─────┼─────────┼──────────┼─────────┼──────────┼─────────┼──────┤
│[T-E]│ [T-C]   │ [T-A] 🔴 │ [T-F]   │          │  [T-X]  │[T-Z] │
│[T-F]│ [T-D]   │ [T-B]    │         │  [T-G]   │         │[T-Y] │
│[T-G]│ [T-K]   │          │         │  [T-H]   │         │      │
│ ... │         │          │         │  [T-I]   │         │      │
└─────┴─────────┴──────────┴─────────┴──────────┴─────────┴──────┘

🔴 = Blocker
```

**Workflow spiegelt Realität!**

Note:
Dieses Board zeigt den echten Workflow: Dev → Code Review → Test → Deploy. Jede Spalte hat ein WIP Limit. Blocker sind rot markiert.

--

## Visualisierung: DO's & DON'Ts

✅ **DO:**
- **Workflow abbilden** wie er IST (nicht wie er sein sollte)
- **Spalten für jeden Status**
  - "Waiting for Deployment" als eigene Spalte (sichtbar!)
- **Blocker markieren** (rote Karten, Flaggen)
- **Classes of Service** (Optional)
  - Farben: Bug (rot), Feature (grün), Tech Debt (gelb)
- **Board für alle sichtbar**
  - Physisch: An der Wand
  - Digital: Großer Monitor im Büro

❌ **DON'T:**
- **Zu viele Spalten** (>10 = zu komplex)
- **Zu wenig Spalten** ("To Do → Done")
- **Board nicht aktualisiert**
- **Versteckte Arbeit** (Tasks nicht auf Board)

Note:
Ein gutes Board zeigt die Realität. Wenn viele Tasks in "Waiting for Deployment" hängen, ist das sichtbar → Problem wird adressiert!

---

## Praktik 2: Limit Work in Progress (WIP)

**Warum?**
- Multitasking tötet Produktivität
- Context Switching kostet 20-40% Effizienz
- WIP Limits erzwingen Fokus

**Wie?**
- **WIP Limit pro Spalte** festlegen
- Limit überschritten? → Kein neues Item ziehen!
- Stattdessen: Blocker beseitigen oder helfen

Note:
WIP Limits sind das Herz von Kanban! Sie sind unbequem (deshalb funktionieren sie). Wenn "In Progress" voll ist, MUSS man helfen oder Blocker beseitigen.

--

## WIP Limits: Beispiel

**Ohne WIP Limit:**
```
Dev A: Task 1 (20%), Task 2 (40%), Task 3 (10%), Task 4 (30%)
→ Nichts wird fertig! Hoher Context Switch
```

**Mit WIP Limit (Max 2):**
```
Dev A: Task 1 (100%) ✅, dann Task 2 (100%) ✅
→ Tasks werden abgeschlossen! Weniger Context Switch
```

**Resultat:**
- Schnellerer Durchsatz
- Weniger Stress
- Höhere Qualität

Note:
Die Magie von WIP Limits: Sie zwingen zu Fokus. Lieber 2 Tasks abschließen als 5 anstarten und nichts fertigbekommen.

--

## WIP Limits festlegen

**Faustregel:**
- **WIP Limit = Anzahl Personen in Spalte**
- Oder: **WIP Limit = Personen × 1,5**

**Beispiel:** 3 Entwickler
- WIP Limit "In Dev": 3-5

**Wichtig:**
- **Experimentieren!** Zu niedrig → Idle Time. Zu hoch → Überlastung
- **Anpassen** nach 2-3 Wochen

**Ziel:** Optimaler Flow!

Note:
Es gibt keine perfekte Formel. Teams müssen experimentieren. Startet konservativ (= niedriges Limit), dann adjustieren.

--

## WIP Limits: DO's & DON'Ts

✅ **DO:**
- **Limits einhalten** (!)
  - Wenn voll, dann stopp!
- **Bei Limit: Helfen**
  - "In Progress" voll → Hilf Kollegen beim Review!
- **Limits sichtbar machen**
  - Auf Board schreiben: "WIP: Max 3"
- **Blocker sofort adressieren**
  - Limit voll wegen Blocker? → Höchste Priorität!
- **Limits anpassen**
  - Nach 2-3 Wochen: Zu eng? Zu weit?

❌ **DON'T:**
- **Limits ignorieren**
  - "Nur diesmal..." → Slippery Slope!
- **Zu hohe Limits**
  - WIP: 10 bei 3 Personen → Sinnlos!
- **Limits nie anpassen**
  - Kontinuierliche Verbesserung!
- **Limits als Bestrafung**
  - "Wir haben Limit gerissen!" → Schuld
  - Limits sind Tool, keine Regel

**Red Flag:** Team ignoriert Limits regelmäßig

Note:
WIP Limits funktionieren nur, wenn sie respektiert werden. Sonst sind sie nutzlos. Das Team muss das WHY verstehen!

---

## Praktik 3: Manage Flow

**Ziel:** Arbeit fließt **schnell & gleichmäßig** durchs System

**Wie Flow messen?**
1. **Lead Time** - Gesamtzeit (Anfrage → Delivered)
2. **Cycle Time** - Entwicklungszeit (Started → Done)
3. **Throughput** - Items pro Zeitraum (z.B. pro Woche)

**Optimierung:**
- Bottlenecks identifizieren
- Flow verbessern

Note:
Flow ist das Blut von Kanban. Guter Flow = Tasks fließen ohne Stau durchs System. Schlechter Flow = Tasks stapeln sich, lange Wartezeiten.

--

## Lead Time vs. Cycle Time

```
Request → Backlog → Selected → Dev → Test → Deploy → Done
←────────────── Lead Time ─────────────────────────→
                            ←─ Cycle Time ─→
```

**Lead Time:** Kunde macht Anfrage bis Feature live
**Cycle Time:** Team startet Arbeit bis Feature fertig

**Beide wichtig!**
- Lead Time = Kundenperspektive
- Cycle Time = Team-Effizienz

Note:
Lead Time ist oft viel länger als Cycle Time - weil Items lange im Backlog warten. Beide Metriken sind wichtig!

--

## Cumulative Flow Diagram (CFD)

**Das wichtigste Kanban-Diagramm!**

```
     │
Items│     Done
     │   ╱╱╱╱╱╱╱╱
     │  Test
     │ ╱╱╱╱╱╱╱
     │Dev
     │╱╱╱╱╱
     │Backlog
     └────────────→ Zeit
```

**Ablesen:**
- **Horizontale Breite** = Cycle Time
- **Steigung** = Throughput
- **Stau** sichtbar (aufbauende Bereiche)

Note:
CFD ist der Röntgenblick auf euren Workflow! Ihr seht sofort: Wo staut es sich? Wie schnell liefern wir? Wie lange dauert's?

--

## Bottlenecks erkennen & beseitigen

**Bottleneck = Engpass, der Flow verlangsamt**

**Erkennungszeichen:**
- Spalte ist ständig am WIP Limit
- Spalte danach ist leer
- Items stauen sich davor

**Beispiel:**
```
Dev (voll) → Code Review (leer) → Test (voll)
```
→ Code Review ist Bottleneck!

**Lösungen:**
- Mehr Kapazität (z.B. mehr Reviewer)
- Pair Reviews
- Prozess optimieren (z.B. automatisierte Checks)

Note:
Bottlenecks zu finden ist Gold wert! Statt überall zu optimieren, fokussiert man auf den Engpass. Theory of Constraints (Goldratt).

--

## Flow: DO's & DON'Ts

✅ **DO:**
- **Metriken tracken**
  - Lead Time, Cycle Time, Throughput
- **Visualisieren** (CFD!)
- **Bottlenecks aktiv angehen**
  - Ist Code Review der Engpass? → Mehr Reviewer, Pair Reviews
- **Flow gleichmäßig** halten
  - Vermeiden: Montag 20 Tasks, Freitag 2 Tasks
- **Blocker SOFORT** adressieren
  - Jeder gestoppte Flow kostet Zeit!

❌ **DON'T:**
- **Nur messen, nicht handeln**
  - Metriken ohne Verbesserung = nutzlos
- **Vanity Metrics** fokussieren
  - "Wir haben 100 Tasks im Backlog!" (wen interessiert's?)
- **Batch-Arbeit**
  - Freitag alle Reviews machen
  - Lieber: Kontinuierlich

Note:
Flow zu messen bringt nichts, wenn man nicht handelt. Bottlenecks identifizieren → beseitigen → messen → wiederholen.

---

## Praktik 4: Make Process Policies Explicit

**Warum?**
- Transparenz über "Regeln des Spiels"
- Vermeidet Missverständnisse
- Basis für Verbesserung

**Beispiele:**
- **Definition of Done** pro Spalte
- **WIP Limits** sichtbar
- **Pull-Kriterien** ("Wann darf ich einen Task ziehen?")
- **Priorisierungsregeln** ("Bugs vor Features")

Note:
Implizite Regeln führen zu Konfusion. Explizite Regeln schaffen Klarheit. Am besten: Direkt aufs Board schreiben!

--

## Explizite Policies: Beispiele

**Policy 1: Definition of Ready**
> Ein Task darf nur in "Selected for Dev" gezogen werden, wenn:
> - Akzeptanzkriterien definiert
> - Abhängigkeiten geklärt
> - Geschätzt

**Policy 2: Code Review**
> Code Review muss innerhalb von 4h erfolgen.
> Bei Blocker: Im Daily eskalieren.

**Policy 3: Priorisierung**
> Reihenfolge: P0 (Critical Bugs) > P1 (Features) > P2 (Tech Debt)

**Wichtig:** Policies SICHTBAR machen (Board, Wiki)!

Note:
Diese Policies sollten am Board hängen oder im Team-Wiki stehen. Jeder muss sie kennen und verstehen!

--

## Explizite Policies: DO's & DON'Ts

✅ **DO:**
- **Gemeinsam definieren**
  - Team entscheidet Policies, nicht Management
- **Sichtbar machen**
  - Am Board, im Wiki
- **Regelmäßig überprüfen**
  - Retros: "Sind unsere Policies noch sinnvoll?"
- **Klar & kurz**
  - "Code Review in 4h" nicht "Code Review soll nach Möglichkeit..."

❌ **DON'T:**
- **Zu viele Policies**
  - 20-seitige Prozessdoku → niemand liest's
- **Policies verstecken**
  - Im Confluence-Graveyard
- **Policies aufzwingen**
  - Team muss Buy-in haben
- **Nie ändern**
  - Policies sind nicht in Stein gemeißelt!

Note:
Policies sollen helfen, nicht belasten. Haltet sie einfach, sichtbar und lebendig!

---

## Praktik 5: Feedback Loops

**Warum?**
- Empirismus! Inspect & Adapt
- Frühe Fehler-Erkennung
- Kontinuierliche Verbesserung

**Kanban Feedback Loops:**
1. **Daily Stand-up** (täglich)
2. **Replenishment Meeting** (wöchentlich) - Backlog auffüllen
3. **Kanban Review** (monatlich) - Metriken reviewen
4. **Retrospektive** (monatlich) - Prozess verbessern
5. **Service Delivery Review** (quartalsweise) - Stakeholder

Note:
Kanban hat weniger "Events" als Scrum, aber auch Feedback-Schleifen. Entscheidend: Regelmäßigkeit!

--

## Kanban Daily Stand-up

Ähnlich wie Scrum Daily, aber fokussiert auf **Flow**:

**Format: "Walk the Board" (Right to Left!)**
- Start rechts bei "Done" (Was ist fertig?)
- Dann links: Wo hängt's?
- Blocker besprechen

**Fragen:**
- "Was blockt uns?"
- "Wo können wir helfen?"
- "Brauchen wir mehr Items aus Backlog?"

**Wichtig:** Von rechts nach links (Pull-Fokus!)

Note:
Der Unterschied zu Scrum Daily: Fokus auf das Board, nicht auf Personen. "Wo hängt's?" ist wichtiger als "Was hast du gestern gemacht?".

--

## Replenishment Meeting

**Ziel:** Backlog mit neuen Items auffüllen

**Frequenz:** Wöchentlich oder bei Bedarf

**Teilnehmer:** Product Owner + Team (optional)

**Aktivitäten:**
- Neue Items hinzufügen
- Prioritäten anpassen
- Items schätzen (grob)
- Alte Items entfernen

**Output:** Gefüllter, priorisierter Backlog

Note:
Das Replenishment Meeting ist wie Sprint Planning, nur kontinuierlich. Das Team zieht Items nach Bedarf, deshalb muss der Backlog immer gefüllt sein!

--

## Kanban Review & Retro

**Kanban Review (Service Delivery Review):**
- Metriken besprechen (Lead Time, Throughput)
- Stakeholder-Feedback
- Quartalsweise

**Retrospektive:**
- Was lief gut? Was nicht?
- Prozess-Verbesserungen
- Monatlich (oder häufiger)

**Wichtig:** Auch ohne Sprints braucht es Feedback-Loops!

Note:
Kanban ohne Feedback-Loops wird stagnieren. Reviews und Retros sind essentiell!

---

## Praktik 6: Improve Collaboratively, Evolve Experimentally

**Kern-Idee:**
- Kleine, evolutionäre Änderungen
- Experimentieren, messen, lernen
- Team-basierte Verbesserung

**Kaizen:** Kontinuierliche Verbesserung (改善)

**Wichtig:** Nicht Big-Bang-Changes, sondern kleine Schritte!

Note:
Kanban ist evolutionär, nicht revolutionär. Man startet mit dem IST-Zustand und verbessert inkrementell. Kein "Wir machen jetzt alles anders!".

--

## Experimentelle Verbesserung: Beispiel

**Problem:** Code Reviews dauern zu lang (Ø 2 Tage)

**Hypothese:** "Pair Reviews sind schneller"

**Experiment:**
- 2 Wochen: Pair Reviews für 50% der PRs
- Metrik: Review-Zeit messen

**Ergebnis:**
- Pair Reviews: Ø 2h
- Solo Reviews: Ø 2 Tage
→ Experiment erfolgreich!

**Aktion:** Pair Reviews als Standard etablieren

Note:
Das ist wissenschaftliches Arbeiten! Hypothese → Experiment → Messen → Entscheiden. So verbessert man nachhaltig!

--

## Improve Collaboratively: DO's & DON'Ts

✅ **DO:**
- **Team entscheidet** über Verbesserungen
  - Nicht Top-down!
- **Kleine Experimente** (max 2 Wochen)
- **Messen** (Data > Meinungen)
- **Erfolge feiern** 🎉
  - "Cycle Time von 10d auf 5d reduziert!"
- **Fehler akzeptieren**
  - Experiment gescheitert? OK, nächstes!

❌ **DON'T:**
- **Big Bang Changes**
  - "Ab morgen machen wir alles anders!"
  - Risiko: Chaos
- **Ohne Messung**
  - "Fühlt sich besser an" reicht nicht
- **Top-down Veränderungen**
  - Management diktiert Prozess
- **Keine Follow-Ups**
  - Experiment läuft, aber keiner checkt Ergebnisse

Note:
Die besten Verbesserungen kommen vom Team selbst. Management sollte enablen, nicht diktieren!

---

## Kanban Metriken: Deep Dive

Kanban ist datengetrieben! Die wichtigsten Metriken:

**1. Lead Time**
- Zeit von Request bis Delivery
- Kundenperspektive

**2. Cycle Time**
- Zeit von Start bis Done
- Team-Effizienz

**3. Throughput**
- Items pro Zeitraum (z.B. pro Woche)
- Liefergeschwindigkeit

**4. Work in Progress (WIP)**
- Anzahl aktiver Items
- Überlastung vermeiden

Note:
Diese 4 Metriken sind das Kern-Dashboard. Alles andere ist optional.

--

## Metriken visualisieren

**Lead Time Distribution Chart:**
```
Anzahl │     ╭──╮
Items  │   ╭─╯  ╰─╮
       │ ╭─╯      ╰──╮
       │─┴─┴─┴─┴─┴─┴─┴─┴→ Tage
       0  5 10 15 20 25
```
→ Median Lead Time: 10 Tage
→ 85. Perzentil: 18 Tage

**Warum 85. Perzentil?**
- "85% aller Items sind in 18 Tagen fertig"
- Realistischere Vorhersagen als Durchschnitt

Note:
Lead Time Distribution ist wichtig für Vorhersagen! "Wann ist Feature X fertig?" → "Mit 85% Wahrscheinlichkeit in 18 Tagen."

--

## Metriken: DO's & DON'Ts

✅ **DO:**
- **Trends beobachten**, nicht Einzelwerte
  - Lead Time über 3 Monate
- **Für Verbesserung nutzen**
  - Cycle Time steigt? → Untersuchen warum!
- **Transparent teilen**
  - Dashboard für alle sichtbar
- **Kontext geben**
  - "Lead Time 15d" ist gut oder schlecht? Kommt drauf an!

❌ **DON'T:**
- **Als KPI für Performance-Reviews**
  - "Dein Cycle Time ist zu hoch!" → Angst
  - Metriken sind für Team-Verbesserung, nicht für Bewertung!
- **Cherry-Picking**
  - Nur gute Wochen zeigen
- **Metriken ohne Action**
  - Messen alleine bringt nichts

**Red Flag:** Metriken werden gegen Team verwendet

Note:
Metriken sind Tools, keine Waffen! Wenn Entwickler Angst vor Metriken haben, läuft was falsch.

---

## Kanban in der Praxis: Use Cases

**Wann Kanban statt Scrum?**

✅ **Kanban passt gut bei:**
- **Support-Teams** (kontinuierlicher Ticket-Strom)
- **Operations** (DevOps, Incident Management)
- **Maintenance** (Bugfixes, kleiner Änderungen)
- **Teams mit hoher Variabilität** (unterschiedliche Task-Größen)
- **Continuous Delivery**

✅ **Scrum passt gut bei:**
- **Produkt-Entwicklung** (große Features)
- **Teams, die Rhythmus brauchen**
- **Planbare Roadmap**

**Oder: Scrumban** (Hybrid!)

Note:
Es gibt kein "besser" - nur "passender". Viele Teams nutzen auch Scrumban: Scrum-Struktur mit Kanban-Praktiken.

--

## Real-World: Kanban bei GitHub

**GitHub nutzt Kanban intern:**
- Kein Sprint Planning
- Continuous Delivery
- WIP Limits pro Engineer (2-3 Tasks)
- Feature Flags für Experiments

**Resultat:**
- Mehrere Deployments pro Tag
- Schnelle Feature-Iteration
- Hohe Entwickler-Zufriedenheit

**Lehre:** Kanban ermöglicht Continuous Delivery!

Note:
GitHub deployed hunderte Male am Tag. Mit Sprints wäre das schwierig. Kanban + Feature Flags = perfekte Combo für CD.

---

## Scrumban: Das Beste aus beiden Welten

**Was ist Scrumban?**
- Scrum-Struktur (Sprints, Rollen, Events)
- Kanban-Praktiken (WIP Limits, Flow)

**Beispiel:**
- **Sprints** (2 Wochen)
- **Kanban Board** mit WIP Limits
- **Daily Stand-up** ("Walk the Board")
- **Sprint Retro** (Verbesserung)
- **Metriken:** Velocity + Cycle Time

**Vorteil:** Struktur + Flexibilität!

Note:
Scrumban ist sehr verbreitet! Viele "Scrum"-Teams nutzen eigentlich Scrumban. Das ist völlig OK - agile Frameworks sind Werkzeuge, keine Religionen.

--

## Scrumban: DO's & DON'Ts

✅ **DO:**
- **Das Beste kombinieren**
  - Scrum's Struktur + Kanban's Flow
- **Experimentieren**
  - "Wie wäre es mit WIP Limits im Sprint?"
- **Team entscheidet**
  - Welche Elemente passen zu uns?

❌ **DON'T:**
- **"Wir machen echtes Scrum!"** (aber nutzen Kanban-Elemente)
  - Dogmatismus hilft nicht
- **Alles wild mischen** ohne Verständnis
  - Verstehe WHY hinter jeder Praktik
- **Frameworks als Religion**
  - Scrum/Kanban sind Tools, keine Glaubenssysteme

Note:
Es gibt keine "Prozesspolizei". Nutzt, was funktioniert. Aber versteht das WHY hinter jeder Praktik!

---

## Zusammenfassung: Kanban

**6 Kern-Praktiken:**
1. 👁️ Visualize Workflow → Board
2. 🚦 Limit WIP → Fokus
3. 📊 Manage Flow → Metriken
4. 📜 Explicit Policies → Transparenz
5. 🔄 Feedback Loops → Inspect & Adapt
6. 🧪 Improve Collaboratively → Kaizen

**Vorteile:**
- Flexibel (kein Sprint-Zwang)
- Datengetrieben (Metriken!)
- Einfacher Einstieg (Start where you are)

**Kern-Metriken:**
- Lead Time, Cycle Time, Throughput

**Wann nutzen?**
- Support, Operations, Continuous Delivery

Note:
Kanban ist wunderbar flexibel und datengetrieben. Perfekt für Teams mit kontinuierlichem Arbeitsstrom. Weniger gut für teams die klare Sprints brauchen.
