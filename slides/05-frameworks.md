<!-- .slide: data-background="#00BCD4" -->

# 🌐 Weitere Agile Frameworks

Beyond Scrum & Kanban

Note:
Scrum und Kanban sind die bekanntesten, aber es gibt weitere agile Frameworks! Schauen wir uns die wichtigsten an: XP, SAFe, und LeSS.

---

## Die Agile Framework-Landschaft

**Team-Level:**
- Scrum (am weitesten verbreitet)
- Kanban
- **Extreme Programming (XP)** ← Technische Praktiken
- Crystal, FDD (selten)

**Enterprise/Scale:**
- **SAFe** (Scaled Agile Framework)
- **LeSS** (Large-Scale Scrum)
- Spotify Model
- Nexus, Scrum@Scale

Wir fokussieren uns auf: **XP, SAFe, LeSS**

Note:
Es gibt dutzende agile Frameworks. Wichtig: Alle basieren auf dem Agile Manifest! Unterschiede sind meist im Kontext (Team vs. Enterprise) und Fokus (Prozess vs. Technik).

---

<!-- .slide: data-background="#E91E63" -->

# 🔶 Extreme Programming (XP)

Technical Excellence als Kern

Note:
XP ist das "technischste" agile Framework. Während Scrum Prozess-fokussiert ist, ist XP Technik-fokussiert.

---

## Was ist Extreme Programming?

**Erfinder:** Kent Beck (1996)

**Kern-Idee:**
> Wenn eine Praktik gut ist, mach sie **extrem**!
> - Code Reviews gut? → **Pair Programming** (continuous review)
> - Tests gut? → **Test-Driven Development** (tests first)
> - Integration gut? → **Continuous Integration** (mehrmals täglich)

**Fokus:** Technische Exzellenz + Kundenzufriedenheit

Note:
Der Name "Extreme" kommt von "take best practices to extreme levels". XP ist radikal in seinen Praktiken - aber genau das macht es effektiv!

---

## Die 5 Werte von XP

1. **Communication** 🗣️
   - Intensive Zusammenarbeit

2. **Simplicity** ✨
   - Einfachste Lösung, die funktioniert (YAGNI!)

3. **Feedback** 🔄
   - Schnelles, kontinuierliches Feedback

4. **Courage** 💪
   - Mut zu Refactoring, zu NEIN sagen

5. **Respect** 🤝
   - Gegenseitiger Respekt im Team

Note:
Diese Werte sind die Basis. Darauf bauen die 12 Praktiken auf.

---

## Die 12 XP-Praktiken (Überblick)

**Planning:**
- User Stories
- Release Planning
- Small Releases

**Design:**
- Simple Design
- Refactoring
- Metaphor

**Coding:**
- **Pair Programming** ⭐
- **Test-Driven Development (TDD)** ⭐
- Collective Code Ownership
- Coding Standards

**Integration:**
- **Continuous Integration** ⭐
- Sustainable Pace

Note:
Von diesen 12 sind die markierten 3 heute Standard in der Industrie! Schauen wir sie uns genauer an.

---

## XP-Praktik: Pair Programming

**Was?**
- 2 Entwickler, 1 Tastatur, 1 Monitor
- **Driver:** Tippt Code
- **Navigator:** Denkt strategisch, reviewed live

**Rotation:** Alle 15-30 Minuten

**Vorteile:**
- ✅ Kontinuierliches Code Review
- ✅ Wissensaustausch
- ✅ Weniger Bugs
- ✅ Besseres Design

Note:
Pair Programming fühlt sich anfangs ineffizient an ("2 Leute für 1 Task!"), aber Studien zeigen: 15% langsamer, aber 15% weniger Bugs. Netto: Effizienter!

--

## Pair Programming: DO's & DON'Ts

✅ **DO:**
- **Rollen wechseln** (alle 20 Min)
  - Verhindert Ermüdung
- **Thinking Out Loud**
  - "Ich überlege gerade..."
  - Transparent denken!
- **Pausen machen** (alle 90 Min)
- **Unterschiedliche Pairings**
  - Senior + Junior (Mentoring)
  - 2 Seniors (Komplexe Probleme)
  - 2 Juniors (Lernen zusammen)
- **Remote-Pairing** (Screen Sharing + Voice)

❌ **DON'T:**
- **Navigator am Handy**
  - Unrespectful!
- **Driver ignoriert Navigator**
  - "Lass mich einfach machen"
- **Permanent Pair**
  - Auch solo-Zeit ist wichtig
- **Erzwungenes Pairing**
  - Team muss es wollen

Note:
Pair Programming funktioniert nur mit gegenseitigem Respekt. Wenn einer dominiert oder der andere passiv ist, wird's ineffektiv.

--

## Real-World: Pair Programming bei Pivotal Labs

**Pivotal Labs** (später VMware Tanzu):
- **100% Pair Programming**
- 8h am Tag (mit Pausen!)
- Rotation: 2x täglich neue Pairs

**Ergebnisse:**
- Sehr hohe Code-Qualität
- Kein Wissensmonopol
- Schnelles Onboarding (Juniors lernen extrem schnell)

**Lehre:** Kann funktionieren, aber ist extrem!

Note:
Pivotal ist der Extremfall. Die meisten Teams machen 30-50% Pairing. Wichtig: Für komplexe/kritische Features pairen, nicht für alles.

---

## XP-Praktik: Test-Driven Development (TDD)

**Der Red-Green-Refactor-Zyklus:**

1. **🔴 Red:** Test schreiben (der fehlschlägt)
2. **🟢 Green:** Code schreiben (Test besteht)
3. **🔵 Refactor:** Code verbessern (Tests bleiben grün)

**Mantra:** *"Test first, code second"*

Note:
TDD dreht die normale Reihenfolge um: Statt Code → Tests macht man Tests → Code. Das erzwingt testbaren Code und klare Specs!

--

## TDD: Beispiel

**Aufgabe:** Funktion `isPrime(n)` schreiben

```javascript
// 1. RED - Test schreiben (fehlschlägt)
test('isPrime returns true for 2', () => {
  expect(isPrime(2)).toBe(true);
});
// → Test fails (isPrime doesn't exist yet)

// 2. GREEN - Minimaler Code
function isPrime(n) {
  return n === 2;
}
// → Test passes

// 3. REFACTOR - Mehr Tests, mehr Code
test('isPrime returns false for 4', () => {
  expect(isPrime(4)).toBe(false);
});
// → Improve isPrime() implementation

// ... iterate ...
```

Note:
TDD zwingt einen, über Spezifikation nachzudenken BEVOR man Code schreibt. Das führt zu besserer API und klareren Anforderungen.

--

## TDD: DO's & DON'Ts

✅ **DO:**
- **Baby Steps**
  - Kleine Tests, kleine Code-Änderungen
- **Refactor kontinuierlich**
  - Nicht "später", sondern im Zyklus!
- **Tests als Spezifikation**
  - Tests dokumentieren Verhalten
- **Red → Green → Refactor** einhalten
  - Disziplin ist wichtig!

❌ **DON'T:**
- **Zu große Schritte**
  - "Ich schreibe erstmal 10 Tests"
  - Lieber: 1 Test → Code → nächster Test
- **Tests nachträglich**
  - "Code fertig, jetzt Tests" = kein TDD!
- **Refactoring überspringen**
  - Resultat: Technische Schulden
- **100% Coverage erzwingen**
  - Coverage ist Mittel, kein Ziel
  - 80-90% ist meist genug

**Red Flag:** "Wir haben keine Zeit für TDD"

Note:
TDD fühlt sich anfangs langsam an. Aber langfristig spart es Zeit (weniger Debugging, weniger Bugs in Prod). Investment lohnt sich!

---

## XP-Praktik: Continuous Integration

**Was?**
- **Mehrmals täglich** Code integrieren
- **Automated Build + Tests** bei jedem Commit
- **Schnelles Feedback** (< 10 Minuten)

**Ziel:** Integration Hell vermeiden!

**Tools:** Jenkins, GitLab CI, GitHub Actions, CircleCI

Note:
"Integration Hell" = Wochenlang separat entwickeln, dann versuchen zu mergen → Chaos! CI vermeidet das durch häufige, kleine Integrationen.

--

## CI: DO's & DON'Ts

✅ **DO:**
- **Commit mindestens 1x täglich**
  - Am besten mehrmals!
- **Build schnell halten** (< 10 Min)
  - Sonst wartet niemand
- **Bei Red Build: FIX FIRST!**
  - Roter Build = höchste Priorität
- **Trunk-Based Development**
  - Feature Branches kurz (< 2 Tage)
- **Feature Flags**
  - Unfertiges Feature ausschalten

❌ **DON'T:**
- **Lange Feature Branches** (Wochen)
  - Integration wird zur Qual
- **Broken Build ignorieren**
  - "Ist nicht meiner..."
- **Langsame Build Pipeline** (> 30 Min)
  - Niemand wartet so lang
- **Tests disabled** weil sie "flaky" sind
  - Fix the tests!

**Red Flag:** Build ist seit Tagen rot

Note:
CI funktioniert nur, wenn das Team diszipliniert ist. Broken Build muss SOFORT gefixt werden. Sonst verliert CI seinen Wert.

---

## XP vs. Scrum: Kombination!

**Scrum:** Prozess-Framework
**XP:** Technische Praktiken

→ **Perfekte Kombination!**

**Scrum + XP:**
- Scrum Rollen (PO, SM, Team)
- Scrum Events (Sprints, Dailys, Retros)
- XP Praktiken (TDD, Pairing, CI)

**Viele erfolgreiche Teams nutzen beides!**

Note:
Scrum sagt "WAS" (Rollen, Events), aber nicht "WIE" (technische Umsetzung). XP füllt diese Lücke! Deshalb werden beide oft kombiniert.

---

<!-- .slide: data-background="#673AB7" -->

# 🏢 SAFe (Scaled Agile Framework)

Agile für große Organisationen

Note:
SAFe ist das bekannteste Framework für Agile-Skalierung. Es ist... komplex. Aber für große Orgas (100+ Personen) oft notwendig.

---

## Was ist SAFe?

**Scaled Agile Framework**
- Für **50-10.000+ Personen**
- Strukturiert Agile auf mehreren Ebenen
- Kombiniert Scrum, Kanban, XP, Lean

**Aktuell:** SAFe 6.0 (2023)

**Kritik:** "Too heavyweight", "Agile in name only"
**Fans:** "Funktioniert in großen Orgas!"

Note:
SAFe ist umstritten! Puristen sagen "zu komplex". Praktiker sagen "besser als Wasserfall in großen Firmen". Die Wahrheit liegt irgendwo dazwischen.

---

## SAFe: Die 4 Ebenen

```
┌────────────────────────────────────────┐
│     Portfolio (Strategy)               │ ← Epics, Budgets
├────────────────────────────────────────┤
│  Large Solution (>100 Personen)        │ ← Solution Trains
├────────────────────────────────────────┤
│  Program (50-125 Personen)             │ ← ARTs (Agile Release Trains)
├────────────────────────────────────────┤
│  Team (5-11 Personen)                  │ ← Scrum/Kanban Teams
└────────────────────────────────────────┘
```

**Wichtigste Ebene:** Program (ARTs)

Note:
SAFe ist wie ein Russisch-Nestdoll: Teams in ARTs in Solutions in Portfolio. Je nach Größe nutzt man 1-4 Ebenen.

---

## Agile Release Trains (ARTs)

**Das Herz von SAFe:**
- **50-125 Personen**
- **8-12 Scrum Teams**
- **Gemeinsamer Rhythmus** (Program Increment)
- **Gemeinsames Ziel**

**Metapher:** Zug fährt nach Fahrplan, alle steigen ein!

**Program Increment (PI):**
- 8-12 Wochen
- 4-6 Sprints
- Endet mit PI Planning

Note:
ARTs sind SAFe's Lösung für Team-Synchronisation. Statt 10 Teams, die unabhängig agieren, synchronisieren sich alle im ART.

--

## PI Planning (Program Increment Planning)

**Das wichtigste Event in SAFe!**

**Dauer:** 2 Tage (alle 8-12 Wochen)
**Teilnehmer:** ALLE (50-125 Personen!)

**Tag 1:**
- Business Context (Wo wollen wir hin?)
- Product Vision
- Team Breakouts (Planung)

**Tag 2:**
- Team Präsentationen
- Risk Management (ROAM Board)
- Confidence Vote
- Commit zu PI Objectives

**Output:** Gemeinsamer Plan für nächste 8-12 Wochen

Note:
PI Planning ist aufwändig (2 Tage, alle Leute!), aber extrem wertvoll. Es synchronisiert die gesamte Organisation. Alle wissen, woran alle anderen arbeiten!

--

## PI Planning: Realität

**Herausforderungen:**
- 100 Leute in einem Raum (oder Remote!)
- Logistik-Alptraum
- Sehr teuer (2 Tage × 100 Personen)

**Aber:**
- Schafft Alignment
- Dependencies werden sichtbar
- Gemeinsame Ziele

**Entscheidend:** Gute Vorbereitung!

Note:
PI Planning gut durchzuführen ist Kunst. Schlecht gemacht = verschwendete Zeit. Gut gemacht = Organisation zieht an einem Strang.

---

## SAFe: DO's & DON'Ts

✅ **DO:**
- **Start small**
  - 1 ART, dann skalieren
- **Training!**
  - SAFe ist komplex, Team braucht Schulung
- **Anpassen**
  - SAFe ist Framework, kein Gesetz
  - Nimm was passt, lass Rest weg
- **Metriken nutzen**
  - Flow Metrics, Velocity, Predictability

❌ **DON'T:**
- **Alles auf einmal**
  - Ganz SAFe von Tag 1 → Chaos
- **SAFe ohne Training**
  - Resultat: "Wagile" (Wasserfall + Agile Buzzwords)
- **Top-Down ohne Buy-In**
  - Management diktiert SAFe → Team-Widerstand
- **Dogmatisch**
  - "Das ist nicht SAFe-konform!" → Sinnlos

**Red Flag:** SAFe wird "verordnet" ohne Team-Input

Note:
SAFe kann funktionieren, aber nur mit Team-Buy-In und guter Umsetzung. Schlecht gemacht ist es bürokratischer als Wasserfall!

---

<!-- .slide: data-background="#4CAF50" -->

# 📈 LeSS (Large-Scale Scrum)

Scrum für viele Teams - aber einfacher als SAFe

Note:
LeSS ist die Alternative zu SAFe: Weniger Struktur, mehr Agilität. "Scrum, aber mit mehr Teams".

---

## Was ist LeSS?

**Large-Scale Scrum** (Craig Larman & Bas Vodde)

**Kern-Idee:**
> "Scrum scaling is about scaling up Scrum itself, not scaling up a new framework."

**2 Varianten:**
- **LeSS:** 2-8 Teams (10-50 Personen)
- **LeSS Huge:** 8+ Teams (50+ Personen)

**Philosophie:** **More with Less** (weniger Rollen, weniger Artefakte, weniger Prozess)

Note:
LeSS ist radikal minimalistisch: Ein Product Backlog, ein Product Owner, eine Definition of Done - für ALLE Teams!

---

## LeSS Prinzipien (1/2)

**Die 10 LeSS-Prinzipien:**
1. **Large-Scale Scrum is Scrum**
2. **Empirical Process Control**
3. **Transparency**
4. **More with Less**
5. **Whole Product Focus**

Note:
LeSS ist das Gegenteil von SAFe: Statt mehr Struktur, WENIGER Struktur. Vertrauen auf Selbstorganisation.

--

## LeSS Prinzipien (2/2)

**Die 10 LeSS-Prinzipien (Fortsetzung):**

6. **Customer-Centric**
7. **Continuous Improvement**
8. **Lean Thinking**
9. **Systems Thinking**
10. **Queuing Theory**

**Kern:** Scrum-Werte beibehalten, nicht komplex machen!

Note:
LeSS setzt auf Einfachheit und minimalen Overhead.

---

## LeSS vs. SAFe (1/2)

| Aspekt | SAFe | LeSS |
|--------|------|------|
| **Komplexität** | Hoch (viele Rollen/Events) | Niedrig (minimalistisch) |
| **Product Owners** | Mehrere (pro Team) | **1 PO** für alle Teams |
| **Backlog** | Mehrere | **1 Backlog** für alle |

Note:
SAFe = "Hier ist der Prozess, folgt ihm." LeSS = "Hier sind Prinzipien, adaptiert selbst."

--

## LeSS vs. SAFe (2/2)

| Aspekt | SAFe | LeSS |
|--------|------|------|
| **Koordination** | ARTs, PI Planning | Gemeinsame Events |
| **Größe** | 50-10.000+ | 10-500 |
| **Philosophie** | Structured, Prescriptive | Minimalist, Adaptive |

**SAFe:** Mehr Struktur, mehr Guidance
**LeSS:** Weniger Struktur, mehr Freiheit

Note:
Beides hat Vor- und Nachteile. Wählt basierend auf eurer Organisation!

---

## Wann welches Framework?

**Team-Level (5-10 Personen):**
→ **Scrum** oder **Kanban**

**Mehrere Teams (10-50):**
→ **Scrum of Scrums** oder **LeSS**

**Viele Teams (50-500):**
→ **LeSS** oder **SAFe**

**Sehr große Organisation (500+):**
→ **SAFe** (oder **Spotify Model** für autonome Tribes)

**Wichtig:** Kontext matters!

Note:
Es gibt kein "bestes" Framework. Es kommt auf Kontext an: Größe, Kultur, Industrie, Compliance-Anforderungen, etc.

---

## Framework-Auswahl: Entscheidungshilfe

**Fragen:**
1. **Wie viele Leute?**
   - <10: Scrum/Kanban
   - 10-50: LeSS
   - 50+: SAFe oder LeSS Huge

2. **Wie komplex ist das Produkt?**
   - Einfach: Kanban
   - Komplex: Scrum

3. **Braucht ihr starke Governance?**
   - Ja (z.B. Finance, Healthcare): SAFe
   - Nein: LeSS

4. **Wie agil ist eure Kultur?**
   - Sehr agil: LeSS, Spotify
   - Traditionell: SAFe (als Brücke)

Note:
Frameworks sind Werkzeuge! Wählt basierend auf Kontext, nicht auf Hype. Und seid bereit zu adaptieren!

---

## Zusammenfassung: Frameworks

**Extreme Programming (XP):**
- Technische Praktiken (TDD, Pairing, CI)
- Kombiniert gut mit Scrum!

**SAFe:**
- Für große Organisationen (50+)
- Strukturiert, prescriptive
- ARTs + PI Planning

**LeSS:**
- Scrum-Skalierung (10-500 Personen)
- Minimalistisch
- 1 PO, 1 Backlog

**Lehre:** Frameworks sind Mittel zum Zweck, nicht Dogma!

Note:
Am Ende des Tages: Alle Frameworks basieren auf dem Agile Manifest. Wählt, was zu euch passt, adaptiert, und verbessert kontinuierlich!
