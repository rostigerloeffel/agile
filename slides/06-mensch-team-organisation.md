<!-- .slide: data-background="#FF9800" -->

# 👥 Mensch, Team & Organisation

**Kern-Idee:** Autonomie ermöglicht Geschwindigkeit!

- 🏗️ **Autonome Teams:** Cross-funktional, End-to-End Ownership
- 📐 **Conway's Law:** Org-Struktur = Architektur
- 🎵 **Spotify-Modell:** Squads, Tribes, Chapters, Guilds

--

## Autonome Teams vs. Matrix-Organisation

**Matrix-Organisation:**
```
┌──────────┬──────────┬──────────┐
│ Frontend │ Backend  │ Database │
│  Team    │  Team    │  Team    │
└──────────┴──────────┴──────────┘
```
- ❌ Viele Handoffs
- ❌ Bottlenecks
- ❌ "Nicht meine Verantwortung"

**Autonome Product Teams:**
```
┌────────────────────────────────┐
│  Product Team A (Full-Stack)   │
│  Frontend, Backend, DB, QA     │
└────────────────────────────────┘
```
- ✅ End-to-End Ownership
- ✅ Schnelle Lieferung
- ✅ Weniger Koordination

Note:
Matrix-Organisation schafft Silos. Autonome Teams liefern Features Ende-zu-Ende!

--

## Conway's Law

> **"Organizations design systems that mirror their communication structure."**
> - Melvin Conway (1967)

**Beispiel:**
- 4 separate Teams → 4-schichtiges System
- 1 cross-funktionales Team → Modularer Monolith

**Lehre:** Organisationsstruktur = Architektur!

**Lösung:** "Inverse Conway Maneuver"
- Erst Architektur designen
- Dann Teams entsprechend organisieren

Note:
Conway's Law ist real! Wenn ihr Microservices wollt, braucht ihr autonome Teams.

--

## Spotify-Modell

**Squads** (5-9 Personen)
- Cross-funktional
- Eigene Mission
- Autonomie über WIE

**Tribes** (mehrere Squads, < 100 Personen)
- Gemeinsame Mission

**Chapters** (Fachdisziplin, z.B. Frontend)
- Wissensaustausch, Mentoring

**Guilds** (Interessensgruppen)
- Communities of Practice

Note:
Spotify-Modell balanciert Autonomie + Alignment. Nicht 1:1 kopierbar, aber Prinzipien sind wertvoll!

Squad: Kleines autonomes Team, z.B. Scrum, z.B. ein Produkt
Tribe: Mehrere Squads, verwandte Produkte
Chapter: Ähnliche Fachrichtungen innerhalb eines Tribes
Guild: Interessensgruppe, z.B. AI, Security usw.

-> Querschnittliche Kommunikation

---

## Kultur & Führung

**Kern-Idee:** Vertrauen ermöglicht Innovation!

- 🛡️ **Psychological Safety:** Fehler sind Lern-Chancen
- 🤝 **Blameless Culture:** System-Denken statt Schuldzuweisung
- 👤 **Servant Leadership:** Befähigen statt bestimmen
- 📊 **Data-Driven:** Daten > HiPPO

Note:
HiPPO = Highest Paid Person's Opinion
Die richtige Kultur ist der Schlüssel zu erfolgreichen agilen Teams.

--

## Verantwortung & Vertrauen

**Traditionell:**
- Micromanagement
- Command & Control
- "Check your brain at the door"

**Agil:**
- Ownership
- Trust & Empowerment
- "You are the expert"

Note:
Ohne Vertrauen keine Agilität! Teams brauchen Psychological Safety zum Experimentieren.

--

## Psychologische Sicherheit

**Was ist das?**
Umfeld, in dem man sich sicher fühlt, Risiken einzugehen

**Merkmale:**
- Fehler sind OK (Lern-Chancen!)
- Fragen stellen ist erwünscht
- Meinungen werden respektiert
- Keine Angst vor Bloßstellung

**Resultat:** Team experimentiert, innoviert, lernt

Note:
Psychological Safety ist Basis für Innovation. Ohne Sicherheit keine Kreativität!

--

## Google's Project Aristotle

**Frage:** Was macht Teams erfolgreich?

**Ergebnis (2015):**
1. **Psychological Safety** (wichtigster Faktor!)
2. Dependability
3. Structure & Clarity
4. Meaning
5. Impact

**Lehre:** Sicherheit > Smartness

Note:
Google analysierte 180 Teams. Ergebnis: Nicht WER im Team, sondern WIE Team zusammenarbeitet!

--

## Psychological Safety im Detail

**Was bedeutet das konkret?**
- Fehler ohne Blame
- Ideen ohne Ridicule
- Fragen ohne Judgment
- Risiken eingehen erlaubt
- Diverse Perspektiven willkommen

**Resultat:** Innovation & High Performance

Note:
Teams mit hoher Psychological Safety sind produktiver und innovativer. Sie teilen Wissen statt es zu horten!

--

## Blameless Culture

**Traditionell:**
- "Wer war's?" (Finger-Pointing)
- Bestrafung
- Angst vor Fehlern

**Blameless:**
- "Was ist passiert?" (System-Denken)
- Learning
- Fehler als Chance

**Wichtig:** Focus auf System, nicht Person!

Note:
"Human error" ist nie die Root Cause - es ist immer das System! Blame verhindert Lernen.

--

## Blameless Postmortem

**Ablauf nach Incident:**
1. Was ist passiert? (Timeline)
2. Warum konnte es passieren? (Root Cause)
3. Wie verhindern wir's? (Action Items)

**Beispiel:** Etsy Blameless Postmortems
- 100+ pro Jahr
- Kultur des Lernens
- Kontinuierliche Verbesserung

Note:
Blameless Postmortems schaffen Lernen statt Angst. Etsy hat das perfektioniert!

--

## Stakeholder-Management

**Herausforderung:**
- Viele Anfragen
- Alle "wichtig"
- Team überlastet

**Lösung: Product Owner als Filter!**
- PO sammelt Stakeholder-Input
- PO priorisiert (nicht jeder Stakeholder!)
- Team bleibt fokussiert

**Sprint Reviews:**
- Stakeholder sehen Fortschritt
- Feedback-Loop
- Erwartungs-Management

Note:
Stakeholder sind wichtig, aber direkter Zugriff aufs Team = Chaos! PO ist die Brücke.

--

## Stakeholder-Management: DO's

✅ **DO:**
- Sprint Reviews mit Stakeholdern
- Transparentes Backlog
- Roadmap kommunizieren (aber flexibel!)
- Frühes Feedback einholen

Note:
Stakeholder sind wichtig - regelmäßiges Engagement ist der Schlüssel.

--

## Stakeholder-Management: DON'Ts

❌ **DON'T:**
- Stakeholder ignorieren
- Überraschungs-Releases
- Jede Anfrage akzeptieren
- "We'll figure it out later"

Note:
Stakeholder-Management ist Balance: Engagement ohne Mikromanagement.

--

## Priorisierung & Entscheidungsfindung

**Wer entscheidet WAS?**
- **Product Owner:** WAS gebaut wird (Value)
- **Team:** WIE gebaut wird (Technical)
- **Stakeholder:** Input, kein Diktat

**Priorisierungs-Frameworks:**

**MoSCoW:**
- **M**ust have
- **S**hould have
- **C**ould have
- **W**on't have (this time)

Note:
Klare Verantwortlichkeiten vermeiden Konflikte. PO entscheidet WAS, Team entscheidet WIE!

--

## WSJF (Weighted Shortest Job First)

**Formel:**
```
WSJF = Cost of Delay / Job Size

Cost of Delay = Business Value + Time Criticality + Risk Reduction
```

**Beispiel:**
- Feature A: CoD=100, Size=10 → WSJF=10
- Feature B: CoD=50, Size=5 → WSJF=10
- Bug: CoD=200, Size=2 → WSJF=**100** (höchste Prio!)

**Lehre:** Kleine, wertvolle Items zuerst!

Note:
WSJF aus SAFe. Sehr nützlich für datengetriebene Priorisierung!

--

## Anti-Pattern: HiPPO

**HiPPO = Highest Paid Person's Opinion**

**Problem:**
- "Der CEO sagt, wir brauchen Feature X!"
- Keine Daten, nur Meinung
- Team frus

triert

**Lösung:**
- **Data-driven Decisions**
- A/B Tests
- User Research
- PO vertritt User, nicht Boss!

**Lehre:** Daten > Hierarchie

Note:
HiPPO ist Gift für Produktentwicklung! Daten + User Feedback schlagen Bauchgefühl.

--

## Führung in agilen Teams

**Traditionell:** Command & Control
- Manager gibt Tasks vor
- Micromanagement
- "Do as I say"

**Agil:** Servant Leadership
- Manager removed Blocker
- Coaching statt Controlling
- "How can I help?"

**Scrum Master als Servant Leader:**
- Dient dem Team
- Befähigt, nicht bestimmt
- Impediment Bulldozer

Note:
Servant Leadership ist Mindset-Shift! Führung heißt: Team zum Erfolg befähigen.

--

## Manager-Rolle in Agile

**Frage:** "Braucht Agile noch Manager?"

**Antwort:** Ja, aber anders!

**Manager-Aufgaben:**
- **Context geben** (Vision, Ziele, Constraints)
- **Team enablen** (Ressourcen, Tools, Training)
- **Impediments beseitigen** (organisatorisch)
- **Career Development** (Mentoring, Coaching)
- **Team schützen** (vor Chaos von außen)

**NICHT:**
- Task-Level Management
- Mikromanagement

Note:
Self-organizing ≠ no leadership! Teams brauchen Kontext und Support.

--

## Führung: DO's

✅ **DO:**
- Set goals, not tasks
- Empower decisions
- Coach, don't control
- Ask "How can I help?"
- Celebrate failures (= Learning!)

Note:
Gute Führung schafft Umfeld für Erfolg.

--

## Führung: DON'Ts

❌ **DON'T:**
- Task-Level Management
- Team bypassing (direkt Devs ansprechen)
- "I need status updates hourly"
- Blame bei Fehlern

Note:
Schlechte Führung schafft Bottlenecks und Micromanagement tötet Autonomie.

--

## Team-Praktiken: Definition of Done

**Warum wichtig?**
- Gemeinsames Verständnis von "Fertig"
- Verhindert "95% fertig"-Syndrom
- Qualitätsstandard

**Beispiel-DoD:**
- [ ] Code reviewed
- [ ] Tests (>80% Coverage)
- [ ] Akzeptanzkriterien erfüllt
- [ ] Deployed in Staging
- [ ] Von PO abgenommen

**Team-spezifisch & evolving!**

Note:
Jedes Team braucht seine eigene DoD. Wichtig: DoD muss realistisch, aber anspruchsvoll sein.

--

## Remote & Hybrid Work

**Herausforderungen:**
- Spontane Kommunikation fehlt
- Onboarding schwieriger
- Team-Bonding
- Timezone-Unterschiede

Note:
Remote funktioniert, braucht aber bewusste Kommunikation! Over-communicate ist OK.

--

## Remote: Best Practices

**Kommunikation:**
- **Daily Video-Calls** (Kamera an!)
- **Virtual Pairing** (Screen Sharing)
- **Async Communication** (Slack, Docs)
- **Over-Communicate** (mehr Info > weniger)
- **Regular Social Events** (Virtual Coffee)

**Tools:** Zoom, Miro, Mural, Slack

Note:
Remote-Teams brauchen bewusste Kommunikations-Strukturen. Async + Sync kombinieren!

---

## Zusammenfassung: Mensch, Team, Organisation

**Team-Struktur:**
- Autonome, cross-funktionale Teams > Matrix
- Conway's Law: Org-Struktur = Architektur

**Kultur:**
- Vertrauen > Kontrolle
- Psychological Safety > Smartness
- Blameless > Blame

**Stakeholder:**
- PO als Filter
- Sprint Reviews für Feedback

**Priorisierung:**
- Daten > HiPPO
- MoSCoW, WSJF

**Führung:**
- Servant Leadership
- Context geben, Team enablen

Note:
Menschen sind der Schlüssel! Prozesse und Tools sind nur Hilfsmittel.
