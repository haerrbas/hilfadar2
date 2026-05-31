# Projektdokumentation – Hilfadar

## Inhaltsverzeichnis

1. [Ausgangslage](#1-ausgangslage)
2. [Lösungsidee](#2-lösungsidee)
3. [Vorgehen & Artefakte](#3-vorgehen--artefakte)
    1. [Understand & Define](#31-understand--define)
    2. [Sketch](#32-sketch)
    3. [Decide](#33-decide)
    4. [Prototype](#34-prototype)
    5. [Validate](#35-validate)
4. [Erweiterungen [Optional]](#4-erweiterungen-optional)
5. [Projektorganisation [Optional]](#5-projektorganisation-optional)
6. [KI-Deklaration](#6-ki-deklaration)
7. [Anhang [Optional]](#7-anhang-optional)

> **Hinweis:** Massgeblich sind die im **Unterricht** und auf **Moodle** kommunizierten Anforderungen.

> **Live-Demo:** https://hilfadar.netlify.app · **Repository:** https://github.com/haerrbas/hilfadar

## 1. Ausgangslage
Im Alltag entstehen ständig kleine Aufgaben, bei denen kurzfristig Hilfe nützlich wäre – etwas tragen, ein Gerät reparieren, beim Umzug anpacken, eine Übersetzung, ein Fahrdienst. Gleichzeitig gibt es im näheren Umfeld viele Menschen mit genau den passenden Fähigkeiten und etwas freier Zeit. Die beiden finden heute aber kaum zusammen: Wer Hilfe braucht, weiss nicht, wer in der Nähe helfen kann und will; wer helfen würde, erfährt nichts von den offenen Aufgaben. Bestehende Plattformen lösen das meist über Geld (Gig-Economy) und erzeugen damit Druck, Hemmschwellen und eine rein transaktionale Beziehung.

- **Problem:** Menschen mit einem konkreten, kleinen Hilfebedarf und Menschen mit passenden Fähigkeiten und etwas Zeit finden im lokalen Umfeld nicht unkompliziert zueinander. Geldbasierte Lösungen passen für nachbarschaftliche, spontane Hilfe schlecht.
- **Ziele:**
  - Hilfesuchende und Helfende **anhand von Fähigkeiten (Skills)** schnell zusammenbringen (Matching).
  - Hilfe **ohne monetären Druck** ermöglichen – Verlässlichkeit entsteht über gegenseitige Bestätigung und Bewertung.
  - Den Ablauf so **einfach und transparent** halten, dass er auf dem Smartphone in wenigen Schritten funktioniert.
- **Primäre Zielgruppe:** Personen in einem lokalen Umfeld (z. B. Quartier/Campus/Gemeinde), die spontan oder geplant kleine Hilfeleistungen suchen oder anbieten möchten.
- **Weitere Stakeholder [Optional]:** Quartier-/Gemeindeorganisationen und Vereine, die nachbarschaftliche Hilfe fördern wollen.

## 2. Lösungsidee
**Hilfadar** ist eine mobile App, die zwei Rollen sauber trennt und über die untere Navigation jederzeit erreichbar macht: **Need** (Hilfe suchen) und **Give** (Hilfe anbieten). Über eine Kategorien-/Skill-Auswahl wird eine Anfrage gestartet; die App matcht Suchende und Helfende und führt beide über einen klaren, gegenseitig bestätigten Ablauf bis zum Abschluss.

- **Kernfunktionalität:**
  - **Need-Flow (Hilfe suchen):** Hilfekategorie wählen → Suche starten → Match prüfen (Profil der Person) → anrufen/kontaktieren → Auftrag abschliessen.
  - **Give-Flow (Hilfe anbieten):** Kategorie/Skills wählen → auf Match warten → Anfrage annehmen oder ablehnen → zur Person navigieren → Abschluss bestätigen.
  - **Gegenseitige Bestätigung:** Beide Flows enden mit einem Bestätigungsschritt – die helfende Person markiert den Auftrag als erledigt. Das schafft Verlässlichkeit ohne Geld.
- **Annahmen [Optional]:**
  - Vorhandene **Skills** sind das massgebliche Matching-Kriterium; Zeit/Verfügbarkeit ist zweitrangig, aber relevant.
  - Vertrauen lässt sich über **Name, Avatar und Sterne-Bewertung** aufbauen, sodass aus einer anonymen Anfrage eine konkrete, menschliche Begegnung wird.
- **Abgrenzung [Optional]:** Kein Bezahl-/Abrechnungssystem, keine Vermittlung kommerzieller Dienstleistungen. Der **Settings-Bereich** ist im aktuellen Prototyp bewusst als Platzhalter angelegt, da Need- und Give-Flow im Fokus stehen.

## 3. Vorgehen & Artefakte
Die Durchführung erfolgte phasenbasiert (Understand/Define → Sketch → Decide → Prototype → Validate). Nachfolgend die wichtigsten Ergebnisse je Phase.

### 3.1 Understand & Define
- **Zielgruppenverständnis:** Ausgangspunkt war der Problemraum «spontane, nachbarschaftliche Hilfe». Im Zentrum stehen zwei komplementäre Bedürfnisse: schnell passende Hilfe finden vs. eigene Fähigkeiten sinnvoll einbringen. Aus der Auseinandersetzung mit dem Problemraum entstanden die offenen Kernfragen (siehe «Kommentare»), die das Konzept geschärft haben.
- **Wesentliche Erkenntnisse (aus den Ideations-/Diskussionsnotizen):**
  - **Suchradius:** Wie weit soll die Suche räumlich gehen?
  - **Matching-Logik:** Genaues Matching vs. die Gefahr von «Racial Profiling» / unerwünschter Vorselektion – das Matching soll über Skills, nicht über persönliche Merkmale erfolgen.
  - **Skill-Definition:** Welche gesuchten Skills werden wie definiert und ausgewählt?
  - **Verfügbarkeit:** Verfügbarkeit für Aufgaben muss abgebildet werden.
  - **Zeitpunkt:** Hilfe «jetzt» vs. «auf Bestellung» (geplant).
- **Reflexion (Priorisierung):** Vorhandene Skills sind das stark massgebende Kriterium. Zeit kann zweitrangig sein – eine Aufgabe kann auch dann gut erledigt werden, wenn sie nicht sofort, aber von der/dem richtigen Skill-Träger:in übernommen wird. Die zentrale Abwägung lautet damit **Skills vs. Zeit**, mit klarem Vorrang der Skills.

### 3.2 Sketch
- **Variantenüberblick:** Zu Beginn wurden mehrere Richtungen handschriftlich skizziert: App-Icon-/Branding-Ideen, Kategorie-Icons (z. B. Reparatur, Natur/Garten, Wissen), unterschiedliche Layout-Raster für Listen und Profile sowie ein Storyboard des Such- und Match-Ablaufs.
- **Skizzen:**
  - **Icon-/Branding-Exploration:** verschiedene runde Icon-Motive zur Bildsprache der App.
  - **Storyboard / Screen-Raster:** Abfolge von Karten, Profil-/Avatar-Darstellungen und Listenelementen, aus denen die spätere Screen-Struktur abgeleitet wurde.
  - **«Swipe to search»-Mockup:** zentrale Such-Interaktion mit einer Skill-Auswahl (Checkboxen Skill 1–8) und einem Freitext-Feld «Beschreibung». Diese Skizze definiert den Einstieg in den Need-Flow.
  - Die Skizzen unterscheiden sich v. a. in der Anordnung der Suchauslösung (Button vs. Swipe-Geste) und in der Tiefe der Skill-Eingabe (reine Kategorie vs. Kategorie + Freitext).

> Die Original-Skizzen liegen im Repository unter [`/docs/sketches`](docs/) bzw. sind im Anhang referenziert.

### 3.3 Decide
- **Gewählte Variante & Begründung:** Gewählt wurde die Variante mit klarer **Bottom-Navigation (Need/Give)** und skill-basiertem Sucheinstieg («Swipe to search» + Skill-Auswahl). Entscheidkriterien:
  - **Klarheit der Rollen:** Need/Give als getrennte Tabs machen die zwei Kernrollen sofort sichtbar und reduzieren Verwechslungen.
  - **Fokus auf Skills:** Die Skill-Auswahl setzt die priorisierte Matching-Logik direkt um.
  - **Einfachheit/Mobile-First:** Wenige Schritte, grosse Touch-Ziele, schwarz-weisses Schema für maximalen Fokus auf Funktion.
- **End-to-End-Ablauf (User Journey):**
  - **Need (7 Screens):** Kategorie wählen → Suche starten («Searching…») → Match erhalten → Profil prüfen (Name, Avatar, Rating) → anrufen/kontaktieren → Status verfolgen («Susan will arrive in 5 min») → «Order done».
  - **Give:** Kategorie/Skills wählen → auf Match warten → Anfrage annehmen/ablehnen → zur wartenden Person navigieren → Abschluss bestätigen.
  - Beide Journeys treffen sich im **gemeinsamen Bestätigungsschritt** und enden im erledigten Auftrag.
- **Mockup:** Figma-Referenz-Mockup der gewählten Lösung: https://www.figma.com/community/file/1631066429495712411
  > TODO: 2–3 Screenshots der wichtigsten Mockup-Screens (Need-Einstieg, Match-Screen, Order-done) mit je einer kurzen Bildunterschrift einfügen.

### 3.4 Prototype

#### 3.4.1. Entwurf (Design)
- **Informationsarchitektur:** Zwei gleichwertige Hauptpfade über die Bottom-Navigation – **Need** und **Give** – plus ein (vorerst als Platzhalter angelegter) **Settings**-Bereich. Innerhalb von Need/Give führt jeweils ein linearer, schrittweiser Ablauf von der Kategorie-/Skill-Auswahl über das Matching bis zum Abschluss.
- **User Interface Design (zentrale Screens):**
  - **Sucheinstieg / Kategorieauswahl:** Skill-/Kategorieauswahl als Einstieg in den jeweiligen Flow.
  - **Such-/Matching-Status:** Statusmeldungen wie «Searching…» geben dem Prozess Transparenz und reduzieren Unsicherheit.
  - **Match-Screen:** Name, Avatar und Sterne-Rating der gematchten Person – aus der anonymen Anfrage wird eine menschliche Begegnung. Direktaktionen: anrufen/kontaktieren bzw. annehmen/ablehnen.
  - **Live-Status:** z. B. «Susan will arrive in 5 min».
  - **Abschluss:** «Order done» / Bestätigung durch die helfende Person.
  > TODO: Pro genanntem Screen einen Screenshot der **fertigen App** (nicht des Mockups) mit kurzer Erläuterung einfügen. Laut Raster sind «Screenshots inkl. Beschreibungen der fertigen App» Pflicht.
- **Designentscheidungen:**
  - **Schwarz-Weiss-Schema:** hält den Fokus auf Funktion statt Ästhetik.
  - **Grosse Schriftgrade & klare Kontraste:** Lesbarkeit auf kleinen Bildschirmen.
  - **Bottom-Navigation Need/Give:** trennt die zwei Kernrollen sofort sichtbar.
  - **Vertrauensaufbau über Name/Avatar/Rating** statt anonymer Anfrage.
  - **Transparente Statusmeldungen** zur Reduktion von Unsicherheit im Wartezustand.

#### 3.4.2. Umsetzung (Technik)
- **Technologie-Stack:** SvelteKit (HTML / CSS / JavaScript bzw. TypeScript).
  > TODO: Verwendete Bibliotheken ergänzen, falls genutzt (z. B. Icon-Set, Styling-Helfer).
- **Tooling:** Visual Studio Code als IDE; Git & GitHub für die Versionsverwaltung; Figma für das Mockup. Den KI-Einsatz siehe Kapitel **6. KI-Deklaration**.
- **Struktur & Komponenten:**
  > TODO: Kurz die SvelteKit-Routen/Seiten und die wichtigsten Komponenten/Stores auflisten (z. B. `src/routes/need/...`, `src/routes/give/...`, Komponenten für Match-Karte, Status, Bottom-Nav). Bitte an deine tatsächliche Ordnerstruktur anpassen.
- **Daten & Schnittstellen:**
  > TODO: Beschreiben, wie Daten im Prototyp gehalten werden (z. B. clientseitiger State/Stores, statische Beispieldaten/Mock-Daten). Falls eine Persistenz/DB genutzt wird, hier nennen.
- **Deployment:** Online deployt via **Netlify** unter https://hilfadar.netlify.app
- **Besondere Entscheidungen:** **Settings** ist bewusst als Platzhalter umgesetzt, um die verfügbare Zeit auf die beiden Kern-Flows (Need/Give) zu konzentrieren – eine bewusste Scope-Reduktion zugunsten der Kernfunktionalität.

### 3.5 Validate
- **URL der getesteten Version:** Stand **20.05.2026** der App unter https://hilfadar.netlify.app
  > TODO: Falls die getestete Fassung separat deployt wurde, hier die separate URL/den Commit-Stand (Tag/Branch vom 20.05.2026) eintragen. **Wichtig:** Der Test wurde auf der Version per 20.05. durchgeführt – das ist hier so vermerkt.
- **Ziele der Prüfung:** Sind die zwei Kern-Flows (Need/Give) selbsterklärend? Verstehen Nutzende den skill-basierten Sucheinstieg und das Match-/Bestätigungs-Prinzip? Wo entstehen Unsicherheiten (z. B. Suchradius, Verfügbarkeit, Zeitpunkt der Hilfe)?
- **Vorgehen:**
  > TODO: moderiert/unmoderiert, remote/on-site eintragen.
- **Stichprobe:**
  > TODO: Anzahl und Profil der Testpersonen eintragen (z. B. «n = X, Studierende / Quartierbewohner:innen»).
- **Aufgaben/Szenarien:**
  > TODO: Ausformulierte Testaufgaben eintragen, z. B. «Du brauchst Hilfe beim Tragen eines Möbelstücks – finde über Hilfadar jemanden und schliesse den Auftrag ab.» und das Give-Pendant.
- **Kennzahlen & Beobachtungen:**
  > TODO: Erfolgsquote, Zeitbedarf und qualitative Beobachtungen eintragen. Die folgenden Findings stammen aus der Auswertung/Diskussion und können hier als qualitative Beobachtungen einfliessen:
  - Offene Verständnisfragen rund um **Suchradius** («Wie weit soll die Suche gehen?»).
  - Wunsch nach klarer **Skill-Definition** und nach Abbildung der **Verfügbarkeit**.
  - Unterscheidung **«jetzt» vs. «auf Bestellung»** (sofortige vs. geplante Hilfe).
  - Risiko unerwünschter Vorselektion: Matching soll über **Skills**, nicht über persönliche Merkmale erfolgen.
- **Zusammenfassung der Resultate:** Die Grundidee der zwei Rollen (Need/Give) und der skill-basierte Ablauf wurden verstanden. Die wesentlichen offenen Punkte betreffen weniger die Bedienung als die **Logik des Matchings**: Suchradius, Skill-Definition, Verfügbarkeit sowie der Zeitpunkt der Hilfe. Bestätigt wurde die Priorisierung **Skills vor Zeit**.
- **Abgeleitete Verbesserungen (priorisiert):**
  1. **Suchradius sichtbar/einstellbar machen** – reduziert die häufigste Unsicherheit (hoher Nutzen, mittlerer Aufwand).
  2. **Verfügbarkeit & Zeitpunkt («jetzt» / «auf Bestellung») im Flow abbilden** – schärft das Matching.
  3. **Skill-Definition/-Auswahl präzisieren** – klarere Kategorien/Skills im Sucheinstieg.
  > Falls eine dieser Verbesserungen bereits im Prototyp umgesetzt wurde: in Kapitel 4 dokumentieren.

## 4. Erweiterungen [Optional]
> **Hinweis:** Jede Erweiterung ist separat nach dem folgenden Schema zu beschreiben.
> TODO: Nur ausfüllen, wenn du über den Mindestumfang hinausgegangen bist. Andernfalls dieses Kapitel leer lassen oder entfernen.

### _[4.x Kurzbeschreibung / Titel]_
- **Beschreibung & Nutzen:** _[…]_
- **Wo umgesetzt:** _[Frontend / Backend / Datenbank]_
- **Referenz:** _[Screenshot/Kapitel]_
- **Aus Evaluation abgeleitet?:** _[Ja/Nein – falls ja, welches Issue/Finding aus 3.5]_

## 5. Projektorganisation [Optional]
- **Repository & Struktur:** https://github.com/haerrbas/hilfadar
  > TODO: Kurze Strukturübersicht ergänzen (wichtigste Ordner/Dateien).
- **Issue-Management:**
  > TODO: Falls genutzt, kurz beschreiben (z. B. GitHub Issues/Projects).
- **Commit-Praxis:**
  > TODO: z. B. sprechende Commit-Messages.

## 6. KI-Deklaration
Die folgende Deklaration ist verpflichtend und beschreibt den Einsatz von KI im Projekt.

### 6.1 KI-Tools
- **Eingesetzte Tools:** Claude (Anthropic) zur Unterstützung bei der **Projektdokumentation** (Strukturierung und Textentwürfe dieser README).
  > TODO: Weitere im Projekt genutzte Tools ergänzen (z. B. GitHub Copilot / ChatGPT für Codevorschläge), inkl. Version/Variante, falls bekannt.
- **Zweck & Umfang:** KI wurde eingesetzt, um aus den eigenen Projektartefakten (Skizzen, Designentscheide, Workflows, Test-Findings) einen strukturierten Dokumentationsentwurf zu erstellen.
  > TODO: Falls KI auch für Code/Tests/Refactoring genutzt wurde, hier Art und Umfang ergänzen und kennzeichnen, welche Teile (ganz/teilweise) KI-unterstützt entstanden sind.
- **Eigene Leistung (Abgrenzung):** Konzept, Problemdefinition, Skizzen, Designentscheide, Workflows, Mockup, Implementierung und die Durchführung/Auswertung des Usability-Tests sind eigenständig erarbeitet. Die inhaltlichen Aussagen wurden geprüft und verantwortet.

### 6.2 Prompt-Vorgehen
Die Doku wurde erstellt, indem die eigenen Artefakte (PDFs der Abgaben, Skizzen, Test-Notizen) als Kontext bereitgestellt und die KI angewiesen wurde, **strikt entlang der vorgegebenen ZHAW-Vorlage** zu strukturieren, ohne Inhalte zu erfinden. Nicht belegbare Angaben (Testkennzahlen) wurden bewusst als offene Punkte markiert statt frei generiert. Anschliessend wurden die Texte fachlich geprüft und angepasst.
> TODO: Bei Bedarf 1–2 konkrete Beispiel-Prompts als Illustration ergänzen.

### 6.3 Reflexion
- **Nutzen:** Schnelle, konsistente Strukturierung der vorhandenen Inhalte entlang der Vorlage; Zeitersparnis bei der Formulierung.
- **Grenzen:** Die KI kennt weder die genaue technische Umsetzung noch die echten Testkennzahlen – diese müssen eigenständig ergänzt werden.
- **Risiken/Qualitätssicherung:** Gefahr erfundener Details (Konfabulation) wurde durch explizites Markieren offener Punkte und durch eigene Prüfung adressiert. Verantwortung für Korrektheit und Urheberrecht liegt bei der/dem Studierenden.

## 7. Anhang [Optional]
- **Quellen / Assets:**
  - Figma-Mockup (Community-Datei): https://www.figma.com/community/file/1631066429495712411
  > TODO: Verwendete Assets/Icons/Schriften inkl. Lizenz ergänzen.
- **Testskript & Materialien:**
  > TODO: Link/Datei zu Testaufgaben und -protokoll ergänzen.
- **Rohdaten/Auswertung:**
  > TODO: Link/Datei zu Notizen/Auswertung (Kommentare & Reflexion vom 20.05.2026) ergänzen.
