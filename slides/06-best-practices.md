<!-- .slide: data-background="#00BCD4" -->

# ✨ Best Practices & Antipatterns

Learnings aus der Praxis

Note:
Jetzt wird's richtig praktisch! Wir schauen uns bewährte Praktiken an - und häufige Fehler, die ihr vermeiden solltet.

---

## Best Practices: Kategorien

Wir schauen uns an:

1. **Technical Excellence** - Code & Qualität
2. **Team Practices** - Zusammenarbeit
3. **Product Management** - Features & Backlog
4. **Häufige Antipatterns** - Was schiefgeht
5. **Tools & Techniken** - Werkzeuge
6. **Agile Transformation** - Kulturwandel

Note:
Diese Kategorien decken die wichtigsten Bereiche ab. Viele Learnings kommen aus realen Projekten - einschließlich Fehlern!

---

<!-- .slide: data-background="#E91E63" -->

# 💻 Technical Excellence

Code-Qualität als Fundament

Note:
"Ohne technische Exzellenz ist man nicht agil, sondern nur chaotisch schnell." Qualität ist nicht optional!

---

## Test-Driven Development (TDD)

**Warum?**
- Tests als Spezifikation
- Besseres Design (testbarer Code)
- Sicherheitsnetz für Refactoring
- Weniger Debugging

**Red-Green-Refactor:**
1. 🔴 Test schreiben (fails)
2. 🟢 Code schreiben (passes)
3. 🔵 Refactoring (tests stay green)

**Realität:** Nicht 100% TDD nötig, aber für Core-Logic!

Note:
TDD ist Investment: Anfangs langsamer, langfristig schneller. Besonders wichtig bei Business-kritischer Logik.

--

## Testing Pyramid

```
         ╱ ╲
        ╱ E2E╲       ← Wenige (10%)
       ╱───────╲
      ╱  Inte-  ╲    ← Einige (20%)
     ╱  gration  ╲
    ╱─────────────╲
   ╱  Unit Tests   ╲ ← Viele (70%)
  ╱─────────────────╲
```

**Faustregel:**
- **70% Unit Tests** (schnell, isoliert)
- **20% Integration Tests** (Module zusammen)
- **10% E2E Tests** (UI, langsam)

❌ **Anti-Pattern:** Ice Cream Cone (umgedreht!)

Note:
Die Test-Pyramide ist wichtig! Zu viele E2E-Tests = langsame Builds, flaky Tests. Unit Tests sind das Fundament.

--

## Continuous Integration (CI)

**Must-Haves:**
- ✅ **Automated Build** bei jedem Commit
- ✅ **Automated Tests** (Unit + Integration)
- ✅ **Fast Feedback** (< 10 Min)
- ✅ **Build Status visible** (Monitor, Slack)
- ✅ **Trunk-Based Development** (kurze Branches)

**Regel:** Red Build = höchste Priorität!

**Tools:** GitHub Actions, GitLab CI, Jenkins, CircleCI

Note:
CI ist non-negotiable! Ohne CI habt ihr keine Agilität. Integration Hell ist real - und verhindert schnelle Iterationen.

--

## Continuous Deployment (CD)

**Level 1: Continuous Delivery**
- Jeder Commit _könnte_ in Prod gehen
- Manual Deployment-Button

**Level 2: Continuous Deployment**
- Jeder Commit _geht_ automatisch in Prod
- Feature Flags für unfertiges

**Vorteile:**
- Schnelles Feedback von echten Usern
- Kleine Deployments = weniger Risiko
- Rollback einfacher

**Beispiel:** Amazon deployed alle 11 Sekunden! 🚀

Note:
CD ist der heilige Gral! Aber: Braucht solide Tests, Monitoring, Feature Flags. Nicht jedes Team muss dort hin - aber Richtung stimmt!

--

## Code Reviews

**Warum?**
- 👁️ 4-Augen-Prinzip
- 📚 Wissensaustausch
- 🎓 Mentoring
- 🐛 Bug-Prävention

**Best Practices:**
- **Klein & häufig** (< 400 Zeilen)
- **Schnell** (< 24h, besser < 4h)
- **Konstruktiv** (nicht arrogant!)
- **Automatisierte Checks first** (Linting, Tests)

**Checkliste:**
- [ ] Tests vorhanden?
- [ ] Code verständlich?
- [ ] Sicherheit OK?
- [ ] Performance OK?

Note:
Code Reviews sind Gold wert! Aber sie müssen schnell sein - sonst blockieren sie. 4h-Regel: Niemand wartet gerne tagelang.

--

## Technical Debt Management

**Was ist Tech Debt?**
- Code der "quick & dirty" war
- Fehlende Tests
- Veraltete Dependencies
- Schlechte Architektur

**Strategien:**
- **Boy Scout Rule** - Hinterlasse Code besser als vorgefunden
- **Tech Debt Backlog Items** (sichtbar!)
- **20% Zeit für Tech Debt** (reservieren!)
- **Refactoring in jedem Sprint** (nicht "später")

❌ **Anti-Pattern:** "Technical Debt Sprint" in 6 Monaten

Note:
Tech Debt ist wie Kreditkarte: OK in Maßen, aber Zinsen zahlen tut weh! Lieber kontinuierlich abbezahlen als aufhäufen.

--

## Technical Excellence: DO's & DON'Ts

✅ **DO:**
- **Definition of Done** beinhaltet Tests
- **Refactoring** als Teil jedes Sprints
- **Code Reviews** vor Merge
- **CI/CD Pipeline** pflegen
- **Pair Programming** für komplexe Features
- **Automatisierte Tests** priorisieren

❌ **DON'T:**
- **"Keine Zeit für Tests"**
  - Tests sparen langfristig Zeit!
- **"Später refactoren"**
  - Später = Nie
- **Technical Debt ignorieren**
  - Wird nur größer!
- **Manuelle Deployments**
  - Fehleranfällig & langsam
- **Code Reviews verzögern**
  - Blockt Team!

Note:
Technische Exzellenz ist Investment. Kurzfristig kostet es Zeit, langfristig spart es massiv Zeit und Nerven!

---

<!-- .slide: data-background="#FF9800" -->

# 👥 Team Practices

Zusammenarbeit & Kommunikation

Note:
Agile ist Menschen-zentriert! Die besten Prozesse helfen nicht, wenn das Team nicht funktioniert.

---

## Definition of Done (DoD)

**Warum wichtig?**
- Gemeinsames Verständnis von "Fertig"
- Verhindert "Fast-Fertig"-Syndrom
- Qualitätsstandard

**Beispiel-DoD:**
- [ ] Code geschrieben & reviewed
- [ ] Unit Tests (>80% Coverage)
- [ ] Integration Tests geschrieben
- [ ] Akzeptanzkriterien erfüllt
- [ ] Dokumentation aktualisiert
- [ ] Deployed in Staging
- [ ] Von PO abgenommen
- [ ] Keine bekannten Bugs

**Team-spezifisch!**

Note:
Jedes Team braucht seine eigene DoD. Wichtig: DoD muss realistisch sein, aber auch anspruchsvoll genug für Qualität.

--

## Retrospektiven richtig machen

**Frequenz:** Nach jedem Sprint (Scrum) oder monatlich (Kanban)

**Format wechseln!** (alle 2-3 Retros)
- Start/Stop/Continue
- Glad/Sad/Mad
- 4 L's (Liked/Learned/Lacked/Longed for)
- Timeline
- Starfish

**Wichtig:**
- ✅ Psychologische Sicherheit!
- ✅ Konkrete Aktionen (max 1-2)
- ✅ Ownership + Deadline
- ✅ Follow-Up nächste Retro

❌ **Anti-Pattern:** Retros ohne Konsequenzen

Note:
Retros sind nutzlos, wenn nichts passiert! Lieber 1 Verbesserung umsetzen als 10 diskutieren und vergessen.

--

## Effective Dailies

**Ziel:** Synchronisation, nicht Status-Report!

**Format (optional):**
- Was habe ich gestern gemacht?
- Was mache ich heute?
- Gibt es Impediments?

**Alternative:** "Walk the Board"
- Von rechts nach links
- Fokus: Wo hängt's?

**Wichtig:**
- ⏱️ Max 15 Minuten!
- 🚫 Kein Problem-Solving (danach!)
- 🎯 Fokus auf Sprint Goal

Note:
Dailies sollten Energie geben, nicht rauben! Wenn sie langweilig sind, ändert das Format.

--

## Team Ownership & Autonomy

**Ownership:**
- Team ist verantwortlich für Erfolg/Misserfolg
- Nicht "Ich habe Feature X gemacht", sondern "Wir haben Sprint Goal erreicht"

**Autonomy:**
- Team entscheidet WIE (nicht Management!)
- Selbstorganisation bei Tasks
- Technische Entscheidungen beim Team

**Balance:**
- Autonomy braucht klare Ziele (Product Owner!)
- Ownership braucht Verantwortung (Definition of Done!)

Note:
Die besten Teams sind die mit hoher Autonomy + Ownership. Aber: Braucht Vertrauen von Management!

--

## Remote & Hybrid Work

**Challenges:**
- Weniger spontane Kommunikation
- Isolation
- Timezone-Unterschiede

**Best Practices:**
- **Video ON** in Meetings (Gesichter sehen!)
- **Async Communication** nutzen (Slack, Doku)
- **Overlap-Time** definieren (Core Hours)
- **Virtual Whiteboard** (Miro, Mural)
- **Remote-Friendly Retros** (Tools wie Retrium)
- **Pair Programming** remote (VS Code Live Share)

**Wichtig:** Kultur anpassen, nicht nur Tools!

Note:
Remote ist Realität! Teams müssen bewusst an Kultur arbeiten - virtueller Coffee Chat, Celebration-Channels, etc.

--

## Team Practices: DO's & DON'Ts

✅ **DO:**
- **Psychological Safety** schaffen
  - Fehler sind Lern-Chancen
- **Celebrate Wins** 🎉
  - Sprint Goal erreicht? Feiern!
- **Transparenz** über Probleme
  - Blocker früh ansprechen
- **Cross-Training**
  - Frontend lernt Backend & vice versa
- **Team-Building**
  - Gemeinsames Lunch, Games, etc.

❌ **DON'T:**
- **Blame Culture**
  - "Wer hat das verbockt?"
- **Hero Culture**
  - Einer rettet immer den Sprint
- **Meetings ohne Outcome**
  - Zeit verschwenden
- **Isolation**
  - Jeder vor sich hin entwickeln
- **Toxic Positivity**
  - Probleme schönreden

Note:
Team-Kultur ist entscheidend! Ein toxisches Team kann mit Scrum/Kanban nichts anfangen. Psychologische Sicherheit ist Fundament.

---

<!-- .slide: data-background="#4CAF50" -->

# 📦 Product Management

Backlog, User Stories, Priorisierung

Note:
Gutes Product Management ist entscheidend! Der beste Prozess hilft nicht, wenn am falschen Feature gearbeitet wird.

---

## User Stories: INVEST-Kriterien

| Kriterium | Bedeutung | Beispiel |
|-----------|-----------|----------|
| **I**ndependent | Unabhängig | Kann in beliebiger Reihenfolge umgesetzt werden |
| **N**egotiable | Verhandelbar | Details im Gespräch klären |
| **V**aluable | Wertvoll | Nutzen für User/Business |
| **E**stimable | Schätzbar | Team kann Aufwand einschätzen |
| **S**mall | Klein | 1-5 Tage |
| **T**estable | Testbar | Klare Akzeptanzkriterien |

**Format:**
> "Als [Rolle] möchte ich [Feature], um [Nutzen] zu erhalten."

Note:
INVEST hilft, gute User Stories zu schreiben. Wenn eine Story nicht INVEST ist, sollte sie refined werden!

--

## User Story: Good vs. Bad

❌ **Schlechte Story:**
> "Datenbank optimieren"

Warum schlecht?
- Kein Nutzer-Wert sichtbar
- Nicht testbar
- Zu technisch
- Kein "Warum"

✅ **Gute Story:**
> "Als Shop-Kunde möchte ich Suchergebnisse in < 1 Sekunde sehen, damit ich schnell Produkte finde."
>
> **Akzeptanzkriterien:**
> - [ ] Suche antwortet in < 1s (95. Perzentil)
> - [ ] Relevanz-Ranking bleibt gleich
> - [ ] Tests für Performance

Note:
Der Unterschied: Nutzer-Perspektive + messbares Ziel + Kontext. Das Team versteht das WHY!

--

## Backlog Priorisierung

**Methoden:**
1. **Business Value** (ROI)
2. **Risk Reduction** (Unsicherheit früh adressieren)
3. **Dependencies** (Blocker zuerst)
4. **MoSCoW:**
   - **M**ust have
   - **S**hould have
   - **C**ould have
   - **W**on't have

**WSJF (SAFe):**
- Weighted Shortest Job First
- (Business Value + Risk + Time Criticality) / Job Size

**Wichtig:** Explizite Kriterien, nicht "Bauchgefühl"!

Note:
Priorisierung ist die wichtigste Aufgabe des Product Owners! Falsche Prio = verschwendete Entwicklungszeit.

--

## Minimum Viable Product (MVP)

**Was ist ein MVP?**
> Das kleinste Product, das Wert liefert & Lernen ermöglicht.

**Nicht:** "Schlechte Version des finalen Produkts"
**Sondern:** "Hypothese testen mit minimalem Aufwand"

**Beispiel: Online Shop**
- ❌ MVP: Shop ohne Checkout
- ✅ MVP: Landing Page + "Interesse?"-Button → Messen: Wie viele klicken?

**Ziel:** Learn fast, fail fast!

Note:
MVP ist missverstanden! Es geht nicht darum, ein halbfertiges Produkt zu releasen, sondern schnell zu lernen ob die Richtung stimmt.

--

## Feature Flags

**Was?**
- Features "ausschaltbar" machen
- Deployment ≠ Release

**Use Cases:**
- **Unfertige Features** ausschalten
- **A/B Testing** (50% sehen Feature A, 50% Feature B)
- **Canary Releases** (5% bekommen neue Version)
- **Kill Switch** (Feature kaputt? Sofort aus!)

**Tools:** LaunchDarkly, Unleash, Split.io

**Wichtig:** Feature Flags aufräumen (Tech Debt!)

Note:
Feature Flags entkoppeln Deployment von Release. Ihr könnt täglich deployen, aber Features kontrolliert freigeben. Game-Changer!

--

## Product Management: DO's & DON'Ts

✅ **DO:**
- **User Research**
  - Mit echten Usern reden!
- **Data-Driven** entscheiden
  - A/B Tests, Analytics
- **Outcomes > Outputs**
  - "Conversion +10%" nicht "5 Features gebaut"
- **Kill Features**
  - Ungenutzte Features entfernen
- **Transparenz** über Roadmap
  - Team weiß wohin die Reise geht

❌ **DON'T:**
- **Feature-Factory**
  - Nur Output zählen
- **HiPPO** (Highest Paid Person's Opinion)
  - Boss entscheidet ohne Daten
- **Keine User-Tests**
  - "Wir wissen was User wollen" (nein!)
- **Feature Bloat**
  - Immer mehr Features, nie aufräumen
- **Wasserfall-Roadmap**
  - 2-Jahres-Plan ohne Flexibilität

Note:
Gutes Product Management ist hart! Es bedeutet auch NEIN sagen zu Features, die nicht wertvoll sind.

---

<!-- .slide: data-background="#F44336" -->

# 🚫 Häufige Antipatterns

Was schiefgeht - und wie vermeiden

Note:
Jetzt die "Hall of Shame" - häufige Fehler, die agile Transformationen scheitern lassen. Lernt aus den Fehlern anderer!

---

## Antipattern 1: "Agile Theater"

**Symptome:**
- Daily Stand-ups? ✅
- Sprints? ✅
- Scrum Master? ✅
- **ABER:** Wasserfall-Mentalität bleibt!

**Beispiele:**
- "Agile" Namen, aber Top-Down Entscheidungen
- Sprints, aber keine Working Software
- Retros, aber keine Änderungen

**Lösung:** Fokus auf **Mindset**, nicht nur Praktiken!

Note:
Agile Theater = "Wir machen die Rituale, aber nicht den Wandel". Das ist wie Yoga-Hose ohne Yoga - sieht aus wie, ist aber nicht.

--

## Antipattern 2: "Wagile"

**Definition:** Wasserfall + Agile = Wagile 😱

**Symptome:**
- 6 Monate Requirements-Phase
- Dann: "Jetzt machen wir Sprints!"
- Am Ende: Big Bang Release

**Problem:** Man bekommt Nachteile von beiden!
- Wasserfall: Langsam, unflexibel
- Agile: Overhead von Events

**Lösung:** Entweder richtig agil oder ehrlich Wasserfall!

Note:
Wagile ist das Schlimmste aus beiden Welten. Häufig in großen Orgas, die "agil werden müssen" aber nicht wirklich wollen.

--

## Antipattern 3: "Scrum Master als Projektmanager"

**Symptome:**
- SM verteilt Tasks
- SM trackt Stunden
- SM "managt" das Team
- SM schreibt Status-Reports für Management

**Problem:** Team verliert Selbstorganisation!

**Lösung:**
- SM ist **Coach**, nicht Manager
- Team verteilt Tasks selbst
- SM entfernt Impediments, managt nicht!

Note:
Der häufigste Fehler! Viele Ex-Projektmanager werden Scrum Master und machen weiter wie vorher. Das tötet Agilität.

--

## Antipattern 4: "Dark Scrum"

**Definition:** Scrum als Druckmittel missbrauchen

**Symptome:**
- Velocity als Performance-Metrik
- "Warum schafft ihr nur 30 Points?"
- Überlastung durch unrealistische Commitments
- Schuldzuweisungen bei verfehlten Goals

**Problem:**
- Team hat Angst vor Metriken
- Burnout
- Qualität leidet

**Lösung:** Metriken für Team-Verbesserung, nicht für Bewertung!

Note:
Dark Scrum entsteht, wenn Management Scrum falsch versteht. Velocity ist kein KPI! Es ist ein Team-Tool zur Planung.

--

## Antipattern 5: "Zombie Scrum"

**Definition:** Scrum ohne Purpose

**Symptome:**
- Events laufen mechanisch ab
- Niemand weiß warum
- Kein echtes Engagement
- "Wir machen das halt so"

**Problem:** Team sieht keinen Wert mehr

**Lösung:**
- Retro: "Warum machen wir das?"
- Experimente: Events anpassen
- WHY hinter Praktiken erklären

Note:
Zombie Scrum = Scrum ohne Seele. Das Team macht die Bewegungen, aber versteht nicht mehr warum. Das tötet Motivation.

--

## Antipattern 6: "Death by Meeting"

**Symptome:**
- 6h Meetings pro Tag
- Entwickler kommen nicht zum Coden
- Meeting um Meetings zu planen
- Keine Deep Work Time

**Problem:** Produktivität stirbt!

**Lösung:**
- **No-Meeting Blocks** (z.B. Dienstag Nachmittag)
- Meetings challengen: "Brauchen wir das?"
- Timeboxing strikt einhalten
- Async Kommunikation nutzen

Note:
Agile bedeutet NICHT "mehr Meetings". Im Gegenteil: Effiziente Kommunikation. Wenn Entwickler nicht entwickeln können, läuft was falsch!

--

## Antipattern 7: "Agile Only in IT"

**Symptome:**
- IT arbeitet in Sprints
- **ABER:** Andere Abteilungen (Marketing, Legal, HR) nicht
- IT wartet auf Freigaben von Wasserfall-Prozessen
- Bottleneck außerhalb IT

**Problem:** IT kann nur so agil sein wie die Organisation!

**Lösung:**
- **Business Agility** (ganze Organisation)
- Stakeholder in agile Praktiken einbinden
- Cross-funktionale Teams (inkl. Legal, Marketing, etc.)

Note:
Das ist ein Organisations-Problem! IT alleine kann nicht agil sein, wenn der Rest der Firma im Wasserfall ist. Das braucht Change Management.

---

## Tools & Techniken

**Project Management:**
- Jira, Azure DevOps, Linear, Trello
- Wichtig: Tool folgt Prozess, nicht umgekehrt!

**Collaboration:**
- Slack, Microsoft Teams
- Miro, Mural (Virtual Whiteboard)
- Confluence, Notion (Doku)

**CI/CD:**
- GitHub Actions, GitLab CI, Jenkins
- Docker, Kubernetes

**Monitoring:**
- Datadog, New Relic, Grafana
- Feature Flags: LaunchDarkly

**Wichtig:** Tools sind Mittel, kein Ziel!

Note:
Es gibt tausende Tools. Wichtiger als das perfekte Tool: Das Team muss es nutzen und verstehen. Simple Tools gut genutzt > komplexe Tools schlecht genutzt.

---

## Agile Transformation: Tipps

**1. Start Small**
- Pilot-Team, nicht ganze Organisation
- Erfolge zeigen, dann skalieren

**2. Training & Coaching**
- Investiert in Ausbildung!
- Externe Coaches für Anfang

**3. Management Buy-In**
- Ohne Support von oben: Scheitern
- Management muss Mindset ändern

**4. Geduld**
- Agile Transformation dauert Jahre, nicht Wochen
- Kulturwandel ist langsam

**5. Experimentieren**
- Kein Framework ist perfekt
- Adaptiert an euren Kontext!

Note:
Agile Transformation ist Marathon, kein Sprint. Die meisten Firmen brauchen 2-3 Jahre für echten Kulturwandel. Das ist OK!

---

## Zusammenfassung: Best Practices

**Technical Excellence:**
- TDD, CI/CD, Code Reviews, Tech Debt Management

**Team Practices:**
- DoD, effektive Retros & Dailies, Psychological Safety

**Product Management:**
- INVEST User Stories, Priorisierung, MVP, Feature Flags

**Antipatterns vermeiden:**
- Agile Theater, Wagile, Dark Scrum, Zombie Scrum

**Wichtigste Lehre:**
> Agile ist Mindset, nicht Checkliste!

Note:
Am Ende des Tages: Agile bedeutet kontinuierliches Lernen und Anpassen. Kein Team, kein Produkt ist gleich - adaptiert!
