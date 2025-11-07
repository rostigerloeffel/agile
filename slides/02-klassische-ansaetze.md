<!-- .slide: data-background="#FF5722" -->

# ⚠️ Warum klassische Ansätze scheitern

Die Probleme traditioneller Softwareentwicklung

Note:
Bevor wir in die agile Welt eintauchen, schauen wir uns an, welche Probleme traditionelle Ansätze haben und warum sie in komplexen Projekten oft scheitern.

---

## Das Wasserfall-Problem

**Klassisches Projekt:**

1. 📋 Anforderungen (3 Monate)
2. 🎨 Design (2 Monate)
3. 💻 Implementierung (6 Monate)
4. 🧪 Testing (2 Monate)
5. 🚀 Deployment (1 Monat)

**Erstes Feedback:** Nach 14 Monaten! 😱

Note:
Das Wasserfall-Modell bedeutet: Erst nach über einem Jahr sieht der Kunde das erste Ergebnis. Bis dahin können sich Anforderungen längst geändert haben. Die Kosten später Änderungen sind enorm.

---

## Die Kosten später Änderungen

| Phase | Kostenänderung | Beispiel |
|-------|----------------|----------|
| Anforderungen | **1x** | Feature-Idee ändern: 1 Tag |
| Design | **5x** | Architektur anpassen: 1 Woche |
| Implementierung | **10x** | Code umschreiben: 2 Wochen |

Note:
Studien zeigen: Ein Fehler in den Anforderungen kostet später ein Vielfaches! Frühes Feedback ist Gold wert.

--

## Die Kosten später Änderungen (2/2)

| Phase | Kostenänderung | Beispiel |
|-------|----------------|----------|
| Testing | **50x** | Retest & Bugfixes: 2 Monate |
| Produktion | **200x** | Migration & Support: 8+ Monate |

**Je später der Fehler, desto teurer!**

Note:
Ein Fehler in der Produktion kann das 200-fache kosten wie in der Anforderungsphase!

---

<!-- .slide: data-background-color="#0e1117" data-transition="fade" -->

# 💥 HealthCare.gov 2013

Der teuerste "Go-Live" der US-Geschichte

---

## HealthCare.gov: Der Katastrophen-Launch

> **"Am ersten Tag konnten sich exakt 6 Menschen anmelden."**

**Das Projekt:**
- 55 beteiligte Auftragnehmer
- $1,7 Milliarden Budget
- 3 Jahre Entwicklung
- Big-Bang-Go-Live am 1. Oktober 2013

**Das Ergebnis:**
- Sofortiger Absturz
- Langsame Ladezeiten, kaputte Formulare, Datenverlust

Note:
Stellen Sie sich vor: Drei Jahre Entwicklung, Dutzende Firmen, hunderte Entwickler – und am ersten Tag schaffen es genau sechs Menschen, sich einzuloggen. Das war HealthCare.gov, das US-Gesundheitsportal, 2013. Über 55 Auftragnehmer, monolithische Planung, kein durchgängiges Ownership. Alles sollte am Stichtag live gehen – Big Bang. Ergebnis: Komplettausfall.

---

## Die Rettung: Agile in der Krise

**"Tech Surge" Team:**
- Kleine, cross-funktionale Teams
- Iteratives Arbeiten
- Radikale Priorisierung
- Tägliche Releases
- 3 Monate intensive Arbeit

**Resultat:**
- System stabilisiert
- Daraus entstand der **U.S. Digital Service (USDS)**

Note:
Die Rettung kam nicht durch neue Meetings, sondern durch kleine, cross-funktionale Teams. Sie arbeiteten iterativ, priorisierten radikal, lieferten täglich aus. Das war echte Agilität – geboren aus Krise, nicht aus Zertifizierung.

---

## Lessons Learned

**Was hätte geholfen?**

1. **Komplexität schlägt Planbarkeit** - MVP statt Big Bang
2. **Verantwortung > Vertrag** - Ein Team, ein Ziel
3. **Feedbackzyklen sind überlebenswichtig** - Iterative Last-Tests
4. **Agilität entsteht aus Not** - Pragmatismus über Dogma

**Lehre:** Agilität ist die logische Antwort auf Komplexität!

Note:
Agilität ist kein Glaubenssatz, sondern eine pragmatische Reaktion auf die Realität komplexer Projekte.

---

## Traditionell vs. Agile (1/2)

| Aspekt | Traditionell | Agile |
|--------|--------------|-------|
| **Planung** | Alles im Voraus | Iterativ, adaptiv |
| **Anforderungen** | Festgeschrieben | Änderungen willkommen |
| **Feedback** | Am Ende | Kontinuierlich |

Note:
Der fundamentale Unterschied: Traditionelle Methoden versuchen, Unsicherheit zu eliminieren. Agile akzeptiert Unsicherheit und nutzt sie als Chance zum Lernen.

--

## Traditionell vs. Agile (2/2)

| Aspekt | Traditionell | Agile |
|--------|--------------|-------|
| **Risiko** | Hoch (Big Bang) | Niedrig (inkrementell) |
| **Team** | Spezialisiert, Silos | Cross-functional |
| **Erfolgsmaß** | Plan eingehalten? | Wert geliefert? |

Note:
Agile Teams fragen nicht "Haben wir den Plan eingehalten?", sondern "Haben wir Wert geliefert?"

---

## DO's: Projektstart

✅ **DO:**
- Kleine, lieferbare Inkremente planen
- Frühes und häufiges Feedback einholen
- Cross-funktionale Teams bilden
- Technische Exzellenz von Anfang an

Note:
Die richtigen Weichen am Anfang stellen! Details:
- Kleine Inkremente: 1-2 Wochen Zyklen, nicht monatelange Features
- Frühes Feedback: Stakeholder sollten alle 1-2 Wochen funktionierende Software sehen
- Cross-funktionale Teams: Alle Skills im Team (Frontend, Backend, Testing, UX)
- Technische Exzellenz: Tests, CI/CD, Code Reviews von Tag 1 an

--

## DON'Ts: Projektstart

❌ **DON'T:**
- 100 Seiten Anforderungsdokument schreiben
- "Später refactoren wir das"
- Erstes Deployment nach 6 Monaten
- Teams nach Technologie trennen

Note:
Vermeiden Sie Big Design Up Front und technische Schulden von Tag 1. Details:
- 100-Seiten-Dokument: Veraltet sofort, niemand liest es vollständig. Besser: User Stories + Prototypen
- "Später refactoren": Später kommt nie! Tech Debt wird nur größer
- 6 Monate bis Deployment: Viel zu spät für Feedback
- Tech-Silos: Führt zu Bottlenecks und Handoffs

---

## Zusammenfassung: Warum scheitern klassische Ansätze?

❌ **Hauptprobleme:**
- Spätes Feedback (Monate bis Jahre)
- Explodierende Kosten bei Änderungen
- Big Bang Deployment = hohes Risiko
- Silos & fehlende Zusammenarbeit
- Rigide Pläne statt Anpassungsfähigkeit

**➡️ Die Lösung:** Agile Software Development!

Note:
Klassische Ansätze funktionieren bei Unsicherheit und Komplexität nicht. Agile bietet eine bessere Alternative - schauen wir uns an wie!
