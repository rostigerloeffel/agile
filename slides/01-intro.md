# Agile Softwareentwicklung

Eine Einführung in agile Methoden und Praktiken

<small>Dauer: ca. 60 Minuten</small>

Note:
Willkommen zur Präsentation über Agile Softwareentwicklung. In den nächsten 60 Minuten lernen Sie die Grundlagen, Frameworks und Best Practices kennen - mit vielen Praxisbeispielen.

---

## Agenda

1. **Einführung & Historie** - Woher kommt Agile?
2. **Agile Manifest** - Werte & Prinzipien
3. **Scrum Framework** - Rollen, Events, Artefakte
4. **Kanban** - Visualisierung & Flow
5. **Weitere Frameworks** - XP, SAFe, LeSS
6. **Best Practices** - DO's, DON'Ts & Antipatterns
7. **Q&A** - Ihre Fragen

Note:
Heute decken wir ein breites Spektrum ab - von den historischen Wurzeln bis zu konkreten Praxistipps. Bringen Sie gerne Ihre eigenen Erfahrungen ein!

---

<!-- .slide: data-background="#2196F3" -->

# 🚀 Warum Agile?

Die Probleme traditioneller Entwicklung

Note:
Bevor wir in die agile Welt eintauchen, schauen wir uns an, welche Probleme traditionelle Ansätze haben.

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

--

## Die Kosten später Änderungen

| Phase | Kostenänderung | Beispiel |
|-------|----------------|----------|
| Anforderungen | **1x** | Feature-Idee ändern: 1 Tag |
| Design | **5x** | Architektur anpassen: 1 Woche |
| Implementierung | **10x** | Code umschreiben: 2 Wochen |
| Testing | **50x** | Retest & Bugfixes: 2 Monate |
| Produktion | **200x** | Migration & Support: 8+ Monate |

**Je später der Fehler, desto teurer!**

Note:
Studien zeigen: Ein Fehler in den Anforderungen kostet in der Produktion das 200-fache! Frühes Feedback ist Gold wert.

--

## Reales Beispiel: Healthcare.gov (2013)

❌ **Traditioneller Ansatz:**
- 3 Jahre Entwicklung
- $1,7 Milliarden Budget
- Launch: Kompletter Ausfall
- Nur 6 Anmeldungen am ersten Tag
- 3 Monate Reparatur notwendig

✅ **Hätte Agile geholfen?**
- Frühes Feedback durch MVP
- Iterative Last-Tests
- Kontinuierliche Verbesserung

Note:
Healthcare.gov ist ein Paradebeispiel für Big Bang Deployment. Mit agilem Vorgehen (MVP, iteratives Deployment) wären viele Probleme früh erkannt worden.

---

## Traditionell vs. Agile (1/2)

| Aspekt | Traditionell | Agile |
|--------|--------------|-------|
| **Planung** | Alles im Voraus | Iterativ, adaptiv |
| **Anforderungen** | Festgeschrieben | Änderungen willkommen |
| **Feedback** | Am Ende | Kontinuierlich |
| **Risiko** | Hoch (Big Bang) | Niedrig (inkrementell) |

Note:
Der fundamentale Unterschied: Traditionelle Methoden versuchen, Unsicherheit zu eliminieren.

--

## Traditionell vs. Agile (2/2)

| Aspekt | Traditionell | Agile |
|--------|--------------|-------|
| **Team** | Spezialisiert, Silos | Cross-functional |
| **Erfolgsmaß** | Plan eingehalten? | Wert geliefert? |
| **Dokumentation** | Umfassend | Angemessen |

Note:
Agile akzeptiert Unsicherheit und nutzt sie als Chance zum Lernen.

--

## DO's: Projektstart

✅ **DO:**
- Kleine, lieferbare Inkremente planen
- Frühes und häufiges Feedback einholen
- Cross-funktionale Teams bilden
- Technische Exzellenz von Anfang an

Note:
Die richtigen Weichen am Anfang stellen! Details zu den DO's:
- Kleine Inkremente: Nicht monatelange Features, sondern 1-2 Wochen Zyklen
- Frühes Feedback: Stakeholder sollten alle 1-2 Wochen funktionierende Software sehen
- Cross-funktionale Teams: Alle Skills im Team (Frontend, Backend, Testing, UX)
- Technische Exzellenz: Tests, CI/CD, Code Reviews von Tag 1 an - nicht "später refactoren wir das"

--

## DON'Ts: Projektstart

❌ **DON'T:**
- 100 Seiten Anforderungsdokument schreiben
- "Später refactoren wir das"
- Erstes Deployment nach 6 Monaten
- Teams nach Technologie trennen (Frontend/Backend/DB)

Note:
Vermeiden Sie Big Design Up Front und technische Schulden von Tag 1. Details:
- 100-Seiten-Dokument: Veraltet sofort, niemand liest es vollständig. Besser: User Stories + Prototypen
- "Später refactoren": Später kommt nie! Tech Debt wird nur größer. Quality muss von Anfang an sein
- 6 Monate bis Deployment: Viel zu spät für Feedback. Lieber nach 2 Wochen erste Version deployen
- Tech-Silos (Frontend-Team, Backend-Team): Führt zu Bottlenecks und Handoffs. Teams sollten Features Ende-zu-Ende liefern können

---

<!-- .slide: data-background="#4CAF50" -->

# 📜 Geschichte der Agilen Bewegung

Von Toyota bis Snowbird

Note:
Agile ist keine Erfindung der 2000er. Die Wurzeln reichen bis in die 1950er zurück.

---

## Timeline: Die Wurzeln von Agile

**1950er** 🏭 **Toyota Production System**
- Taiichi Ohno entwickelt Lean Manufacturing
- Just-in-Time Produktion
- Kanban-Karten zur Steuerung
- *"Eliminate waste, empower workers"*

Note:
Die Prinzipien entstanden in der Fertigung! Toyota erkannte: Verschwendung eliminieren, Mitarbeiter befähigen, kontinuierlich verbessern.

--

## Timeline: Scrum wird geboren

**1986** 📄 **"The New New Product Development Game"**
- Takeuchi & Nonaka (Harvard Business Review)
- Rugby-Analogie: "Scrum"
- Cross-funktionale Teams
- Overlapping Phasen

Note:
Diese Ideen wurden später auf Software übertragen.

--

## Timeline: Software-Methoden (1/2)

**1991** 🔄 **RAD (Rapid Application Development)**
- James Martin
- Prototyping & iterative Entwicklung

**1995** 🔵 **Scrum**
- Ken Schwaber & Jeff Sutherland
- Erste formale Beschreibung

Note:
In den 90ern entstanden parallel viele "leichtgewichtige" Methoden.

--

## Timeline: Software-Methoden (2/2)

**1996** 🔶 **Extreme Programming (XP)**
- Kent Beck
- Technische Praktiken im Fokus

**1997-2000** 🌐 **DSDM, FDD, Crystal**
- Dynamic Systems Development Method
- Feature-Driven Development
- Crystal Clear (Alistair Cockburn)

Note:
Gegenbewegung zu schwerfälligen Prozessen wie RUP.

--

## 2001: Das Agile Manifest

**📍 Snowbird Ski Resort, Utah**
**📅 12.-14. Februar 2001**
**👥 17 Software-Entwickler**

**Ergebnis:** Das Agile Manifest + 12 Prinzipien

Note:
Diese 17 Personen trafen sich, um Gemeinsamkeiten ihrer Methoden zu finden.

--

## Die Autoren

Darunter:
- Kent Beck (XP)
- Ken Schwaber & Jeff Sutherland (Scrum)
- Alistair Cockburn (Crystal)
- Martin Fowler (Refactoring)
- Robert C. Martin (Clean Code)

Note:
In 2 Tagen entstand eines der einflussreichsten Dokumente der Softwareentwicklung.

--

## Agile wird Mainstream (1/2)

**2000er** 📈 **Verbreitung**
- 2002: Scrum Alliance gegründet
- 2003: "Agile Software Development with Scrum"
- 2005: Agile in großen Unternehmen

**2010er** 🌍 **Dominanz**
- 2011: SAFe 1.0 (Scaled Agile Framework)
- Agile wird Standard
- DevOps-Bewegung entsteht

Note:
Von einer Nischen-Bewegung zum Standard.

--

## Agile wird Mainstream (2/2)

**Heute** 🚀 **New Normal**
- 71% aller Unternehmen nutzen agile Ansätze
  - State of Agile 2023
- Agile beyond Software:
  - Marketing, HR, Finance

Note:
Heute ist die Frage nicht mehr "Warum Agile?", sondern "Wie machen wir Agile richtig?".

---

## Lean Prinzipien → Agile Praktiken

Die DNA von Agile kommt aus **Lean Manufacturing**:

| Lean Prinzip | Agile Umsetzung |
|--------------|-----------------|
| **Verschwendung eliminieren** | Working Software > Dokumentation |
| **Qualität einbauen** | Test-Driven Development, CI/CD |
| **Wissen schaffen** | Retrospektiven, Pair Programming |
| **Entscheidungen verzögern** | Last Responsible Moment |
| **Schnell liefern** | Sprints, Continuous Delivery |
| **Menschen respektieren** | Selbstorganisierende Teams |
| **Ganzheitlich optimieren** | End-to-End Value Stream |

Note:
Agile ist angewandte Lean-Philosophie in der Softwareentwicklung. Wer Lean versteht, versteht auch Agile besser.

---

## Zusammenfassung: Warum Agile? (1/2)

✅ **Frühe Wertschöpfung**
- Funktionierende Software nach Wochen
- ROI beginnt früher

✅ **Risikominimierung**
- Kleine Iterationen → kleine Fehler
- Kontinuierliches Feedback

✅ **Flexibilität**
- Änderungen sind willkommen
- Anpassung an Markt

Note:
Agile adressiert fundamentale Probleme der Softwareentwicklung.

--

## Zusammenfassung: Warum Agile? (2/2)

✅ **Qualität**
- Tests & Integration von Anfang an
- Technische Exzellenz eingebaut

✅ **Teamzufriedenheit**
- Autonomie & Ownership
- Sichtbarer Impact

Note:
Agile ist kein Wundermittel, aber es hilft bei Unsicherheit, Komplexität und Veränderung.
