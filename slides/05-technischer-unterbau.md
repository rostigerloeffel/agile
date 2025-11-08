<!-- .slide: data-background="#E91E63" -->

# 💻 Technischer Unterbau

Ohne technische Exzellenz ist Agilität nur Theater

Note:
Agile Prozesse allein reichen nicht! Ohne solide technische Basis wird man langsam statt schnell. "You can't be agile with legacy code."

---

## Warum technische Exzellenz?

**Problem ohne Tech Excellence:**
- Änderungen dauern Wochen statt Tage
- Deployments sind riskant
- Bugs in Produktion häufen sich
- Team wird frustriert

Note:
Ohne solide technische Basis wird man langsam statt schnell.

--

## Warum technische Exzellenz? (2)

**Mit Tech Excellence:**
- Schnelle, sichere Änderungen
- Deployment ohne Angst
- Hohe Qualität
- Zufriedene Entwickler

**Lehre:** Ohne technischen Unterbau ist Agilität unmöglich!

Note:
Technische Exzellenz ist kein "Nice to Have" - es ist Voraussetzung für Agilität!

---

## Testing & CI/CD

**Kern-Idee:** Qualität von Anfang an!

- 🧪 **Testing:** Pyramid (70% Unit, 20% Integration, 10% E2E)
- 🔄 **CI:** Automated Build + Tests bei jedem Commit
- 🌿 **Trunk-Based Development:** Feature Branches < 2 Tage

Note:
Ohne Tests und CI ist Agilität unmöglich! Diese Praktiken sind das Fundament.

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
- ✅ Automated Build bei jedem Commit
- ✅ Automated Tests (< 10 Min)
- ✅ Build Status visible

**Regel:** Red Build = **höchste Priorität**!

**Tools:** GitHub Actions, GitLab CI, Jenkins

Note:
CI ist non-negotiable! Ohne CI habt ihr keine Agilität. Integration Hell ist real.

--

## Trunk-Based Development

**Prinzip:** Alle entwickeln auf einem Hauptzweig (main)

**Regeln:**
- Feature Branches: < 2 Tage
- Daily merges zu main
- Feature Flags für unfertiges

**Vorteile:**
- Weniger Merge-Konflikte
- Kontinuierliche Integration
- Schnelleres Feedback

Note:
Trunk-Based Development reduziert Integration Hell. Lange Feature Branches sind problematisch!

---

## Deployment & DevOps

**Kern-Idee:** Schnelle, sichere Releases durch Automation!

- 🚀 **CD:** Continuous Delivery/Deployment
- 🔵🟢 **Strategien:** Blue-Green, Canary, Feature Flags
- 👥 **DevOps:** "You build it, you run it" + IaC + Observability

Note:
Deployment darf keine Angst machen - mit den richtigen Praktiken wird es zur Routine.

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

**Beispiel:** Amazon deployed alle 11 Sekunden! 🚀

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

## Code Reviews

**Warum?**
- 👁️ 4-Augen-Prinzip
- 📚 Wissensaustausch
- 🐛 Bug-Prävention

**Best Practices:**
- Klein & häufig (< 400 Zeilen)
- Schnell (< 24h, besser < 4h)
- Konstruktiv (nicht arrogant!)

Note:
Code Reviews sind Gold wert! Aber sie müssen schnell sein - sonst blockieren sie.

--

## Code Review Checkliste

**Beim Review prüfen:**
- [ ] Tests vorhanden?
- [ ] Code verständlich?
- [ ] Sicherheit OK?
- [ ] Performance-Aspekte beachtet?
- [ ] Dokumentation aktualisiert?

**Tipp:** Checkliste im Pull Request Template!

Note:
Eine gute Checkliste macht Reviews systematisch und verhindert, dass etwas übersehen wird.

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

**Faustregel:** Start monolith, extract services bei Bedarf

Note:
Microservices sind kein Selbstzweck! Sie ermöglichen Team-Autonomie, bringen aber Komplexität.

--

## Decoupling für Autonomie

**Ziel:** Teams können unabhängig deployen

**Patterns:**
- **API-First Design:** Klare Schnittstellen
- **Database per Service:** Kein Shared DB
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

## DevOps-Praktiken

**Kernpraktiken:**
- Infrastructure as Code (IaC)
- Monitoring & Observability
- On-Call Rotation
- Automated Deployments
- Shared Metrics

**Ziel:** Schnelle, sichere Deployments durch Zusammenarbeit

Note:
Diese Praktiken ermöglichen schnelle, zuverlässige Releases. DevOps ist Team-Sport!

--

## Infrastructure as Code (IaC)

**Was:** Infrastruktur in Code definieren (Git!)

**Tools:**
- **Terraform:** Cloud-Provider-agnostisch
- **Kubernetes:** Container-Orchestrierung
- **Ansible:** Configuration Management

**Vorteile:**
- Versionierbar (Git!)
- Reproduzierbar
- Code Review für Infra!

**Beispiel:**
```terraform
resource "aws_instance" "web" {
  ami           = "ami-12345"
  instance_type = "t2.micro"
}
```

Note:
IaC macht Infrastruktur agil! Änderungen via Code Review + CI/CD.

--

## Monitoring & Observability

**Die 3 Säulen:**
1. **Metrics:** Zahlen (CPU, Memory, Response Time)
2. **Logs:** Events (Errors, Requests)
3. **Traces:** Request-Pfade (Distributed Tracing)

**Tools:**
- Prometheus + Grafana (Metrics)
- ELK Stack (Logs)
- Jaeger, Zipkin (Tracing)

**Wichtig:** Alerts mit Actionable Info!

**Beispiel:** Netflix Observability
- 100+ Microservices
- Distributed Tracing essential!

Note:
Ohne Observability ist Production ein Blackbox. "You can't improve what you can't measure."

--

## Technical Excellence: DO's

✅ **DO:**
- Tests in Definition of Done
- Refactoring in jedem Sprint
- Code Reviews vor Merge
- CI/CD Pipeline pflegen
- Pair Programming für komplexe Features
- Feature Flags nutzen

Note:
Technische Exzellenz ist Investment. Kurzfristig kostet es Zeit, langfristig spart es massiv!

--

## Technical Excellence: DON'Ts

❌ **DON'T:**
- "Keine Zeit für Tests"
- "Später refactoren"
- Technical Debt ignorieren
- Manuelle Deployments
- Code Reviews verzögern
- Broken Build ignorieren

**Red Flag:** "Wir müssen schneller sein, keine Zeit für Qualität!"

Note:
Ohne Qualität wird man langsamer, nicht schneller! "Go slow to go fast."

---

## Zusammenfassung: Technischer Unterbau

**Testing:** Pyramid (70% Unit, 20% Integration, 10% E2E)

**CI/CD:** Automated Tests + Deployments

**Deployment:** Blue-Green, Canary, Feature Flags

**Architektur:** Decoupling für Team-Autonomie

**DevOps:** "You build it, you run it" + IaC + Observability

**Lehre:** Technische Exzellenz = Voraussetzung für Agilität!

Note:
Ohne soliden technischen Unterbau scheitert Agile! Investiert in Tests, Automation, Architektur.
