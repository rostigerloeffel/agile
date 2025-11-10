<!-- .slide: data-background="#E91E63" -->

# 💻 Technischer Unterbau

Ohne technische Exzellenz ist Agilität nur Theater

Note:
Agile Prozesse allein reichen nicht! Ohne solide technische Basis wird man langsam statt schnell. "You can't be agile with legacy code."

---

## Warum technische Exzellenz?

- Änderungen dauern Wochen statt Tage
- Deployments sind riskant
- Bugs in Produktion häufen sich
- Team wird frustriert

**Lehre:** Ohne technischen Unterbau ist Agilität unmöglich!

Note:
Ohne solide technische Basis wird man langsam statt schnell.

--

## (Einige) Bausteine

- 🧪 **Testing/TDD:** Pyramid (70% Unit, 20% Integration, 10% E2E)
- 🌿 **Trunk-Based Development:** Feature Branches < 2 Tage
- 🔄 **CI/CD:** Automatisierter Build, Tests bei jedem Commit, automatisierte Deployments

Note:
Ohne Tests und CI ist Agilität unmöglich! Diese Praktiken sind das Fundament.

--

## Trunk-Based Development

**Prinzip:** Alle entwickeln auf einem Hauptzweig (main)

<div class="two-columns">

<div>

**Regeln:**
- Feature Branches: < 2 Tage
- Daily merges zu main
- Feature Flags für Unfertiges

</div>

<div>

**Vorteile:**
- Weniger Merge-Konflikte
- Kontinuierliche Integration
- Schnelleres Feedback

</div>

</div>

Note:
Trunk-Based Development reduziert Integration Hell. Lange Feature Branches sind problematisch!

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

## Test-Driven Development (TDD)

**Red-Green-Refactor:**
1. 🔴 **Red:** Test schreiben (fehlschlägt)
2. 🟢 **Green:** Code schreiben (Test besteht)
3. 🔵 **Refactor:** Code verbessern

Note:
DO's 
- Baby Steps, Tests als Spezifikation
DON'T
- Tests nachträglich, Refactoring überspringen

TDD fühlt sich anfangs langsam an, spart aber langfristig Zeit!

--

## Code Reviews

<div class="two-columns">

<div>

**Warum?**
- 👁️ 4-Augen-Prinzip
- 📚 Wissensaustausch
- 🐛 Bug-Prävention

</div>

<div>

**Best Practices:**
- Klein & häufig (< 100 Zeilen)
- Schnell (< 24h, besser < 4h)
- Konstruktiv, nüchtern, unemotional
- PR-Stacking: https://www.stacking.dev/

</div>

</div>

Note:
Code Reviews sind Gold wert! Aber sie müssen schnell sein - sonst blockieren sie.

Code Review Checkliste

Beim Review prüfen:
- [ ] Architektur-Guidelines beachtet?
- [ ] Tests vorhanden?
- [ ] Code verständlich?
- [ ] Sicherheit ok?
- [ ] Performance ok?
- [ ] Dokumentation aktualisiert?

Eine gute Checkliste macht Reviews systematisch und verhindert, dass etwas übersehen wird.

--

## Continuous Integration (CI)

- Automatisierte Builds bei jedem Commit
- Automatisierte Tests (< 10 Min)
- Build-Status sichtbar

**Tools:** Bitbucket Pipelines, GitHub Actions, GitLab CI, Jenkins

Note:
CI ist non-negotiable! Ohne CI habt ihr keine Agilität. Integration Hell ist real.

--

## Deployment & DevOps

**Kern-Idee:** Schnelle, sichere Releases durch Automatisierung!

- 🚀 **CD:** Continuous Delivery/Deployment
- 🔵🟢 **Strategien:** Blue-Green, Canary, Feature Flags
- 👥 **DevOps:** "You build it, you run it" + IaC + Observability

Note:
Deployment darf keine Angst machen - mit den richtigen Praktiken wird es zur Routine.

--

<div style="font-size: 0.85em;">

## Continuous Deployment (CD)

<div class="two-columns">

<div>

**Level 1: Continuous Delivery**
- Jeder Commit _könnte_ in Prod gehen
- Manual Deployment-Button

</div>

<div>

**Level 2: Continuous Deployment**
- Jeder Commit _geht_ automatisch in Prod
- Feature Flags für Unfertiges

</div>

</div>

**Vorteile:**
- Schnelles Feedback von echten Usern
- Kleine Deployments = weniger Risiko

**Beispiel:** Amazon deployed alle 11 Sekunden! 🚀

</div>

Note:
CD ist der heilige Gral! Aber: Braucht solide Tests, Monitoring, Feature Flags.

--

## Deployment-Strategien

**Blue-Green Deployment:**
- 2 identische Umgebungen (Blue = alt, Green = neu)
- Switch nach erfolgreichem Test
- Instant Rollback möglich

**Canary Release:**
- Neue Version für 5-10% der User
- Monitoring: Fehlerrate, Performance
- Bei OK: Rollout zu 100%

**Feature Flags:**
- Code deployed, Feature ausgeschaltet
- Schrittweise aktivieren (z.B. Beta-User)

**Beispiel:** Netflix nutzt alle drei!

Note:
Diese Strategien ermöglichen risikoarme Deployments. Feature Flags sind besonders mächtig!

--

## Technical Debt Management

**Was ist Tech Debt?**
- "Quick & dirty" Code
- Fehlende Tests
- Veraltete Dependencies

**Strategien:**
- **Boy Scout Rule:** Code besser hinterlassen
- **20% Zeit für Tech Debt** (Google's Regel)
- **Refactoring in jedem Sprint**

❌ **Anti-Pattern:** "Technical Debt Sprint" in 6 Monaten

**Lehre:** Tech Debt kontinuierlich abbauen!

Note:
Tech Debt ist wie Kreditkarte: OK in Maßen, aber Zinsen zahlen tut weh!

--

## Architektur für Agilität

**Monolith vs. Microservices:**

**Monolith:**
- ✅ Einfach zu starten
- ❌ Skalierung schwierig
- ❌ Teams blockieren sich

**Microservices:**
- ✅ Unabhängige Deployments
- ✅ Team-Autonomie
- ❌ Komplexität (Netzwerk, Monitoring)

**Faustregel:** Startet als Monolith, extrahiert Services nach Bedarf

Note:
Microservices sind kein Selbstzweck! Sie ermöglichen Team-Autonomie, bringen aber Komplexität.

--

## Decoupling für Autonomie

**Ziel:** Teams können unabhängig deployen

**Patterns:**
- **API-First Design:** Klare Schnittstellen
- **Datenbank pro Service:** Kein Shared DB
- **Event-Driven:** Asynchrone Kommunikation
- **Bounded Contexts:** (Domain-Driven Design)

**Beispiel:** Amazon (2-Pizza-Teams)
- Jedes Team: Eigener Service
- Eigene DB, eigenes Deployment
- APIs für Kommunikation

Note:
Decoupling ermöglicht unabhängige Teams. "You build it, you run it."

--

## DevOps-Kultur

**Traditionell:**
- Dev baut, Ops deployed
- "Throw it over the wall"
- Konflikte & Finger-Pointing

**DevOps:**
- **"You build it, you run it"** (Amazon)
- Teams verantwortlich für Prod
- Gemeinsame Metriken

Note:
DevOps ist Kulturwandel, nicht Tool-Sammlung! Es geht um gemeinsame Verantwortung.

--

## Zusammenfassung: Technischer Unterbau

**Testing:** Test-Driven Development, Testing Pyramid
**CI/CD:** Automated Tests + Deployments
**Deployment:** Blue-Green, Canary, Feature Flags
**Architektur:** Decoupling für Team-Autonomie
**DevOps** "You build it, you run it" + IaC + Observability
**Lehre:** Technische Exzellenz = Voraussetzung für Agilität!

Note:
Ohne soliden technischen Unterbau scheitert Agile! Investiert in Tests, Automation, Architektur.
