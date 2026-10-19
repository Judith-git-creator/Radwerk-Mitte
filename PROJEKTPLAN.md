# Projektplan – Website-Relaunch Radwerk Mitte

## Kontext

Radwerk Mitte ersetzt die veraltete WordPress-Seite durch einen Relaunch (Budget ca. 150.000 €, Basis für ca. 15 % Wachstum im Folgejahr). Bisher existiert weder Code noch ein Tech-Stack, nur Entscheidungsgrundlagen: PRD (verbindlich), Kundengespräch-Protokoll, Firmensteckbrief und ein noch leeres `design/`-Verzeichnis (Farbwerte und Logo-Dateien fehlen noch als Platzhalter). Ziel dieses Plans ist, die vier PRD-Ziele – mehr B2b-Anfragen, entlasteter Support, sichtbares Vertrauen, messbare Daten – in eine ausführbare Reihenfolge von Phasen zu bringen, inklusive der Abhängigkeiten von Kunde und Drittparteien (Leasingpartner, Kundenservice, alte WordPress-Inhalte), die den Start sonst blockieren würden.

Format: relative Phasen (keine Kalenderdaten, da kein Launch-Termin im PRD steht), mit Aufgabenliste je Phase, Tech-Stack-Auswahl ist Teil von Phase 1.

**Leitplanken, die in jeder Phase gelten:**
- Budget 150.000 € gilt für Stufe 1; Erweiterungen nur nach Rücksprache mit dem Team.
- Nicht-Ziele bleiben draußen: Partnerportal-Login, Custom-Rad/Luxusbereich, neuer Shop/neue Warenwirtschaft, neues Branding, beratender/verkaufender Chat.
- Fehlende Inhalte (Hex-Farben, Logo-Dateien, FAQ, Kalkulatorwerte, SLA-Texte) werden mit klar markierten Platzhaltern überbrückt, nie erfunden.
- Freigabe aller Inhalte durch Merle Vogelsang; Tonalität sachlich, per „Sie".

## Rollen (laut Firmensteckbrief, Zuordnung mit Kundin zu bestätigen)

| Person | Rolle im Projekt |
|---|---|
| Merle Vogelsang | Geschäftsführung, finale Freigabe aller Inhalte |
| Heiner Vogelsang | Werkstatt-Content, Formularthema „Werkstatt" |
| Dilan Aydın | B2b-Vertriebstexte, Formularthema „B2b" (Leasing-Anfragen) |
| Svenja Kowalczyk | Online-Shop-Verlinkung, Analytics/Dashboard, vermutlich CMS-Pflege nach Launch |
| Amara Osei | FAQ-Erhebung aus Support-Anfragen, Formularthemen „Kauf"/„Sonstiges" |

## Phase 1 – Discovery & Tech-Stack-Entscheidung

Ziel: Grundlage schaffen, auf der Design und Entwicklung aufsetzen können; alle Blocker identifizieren, die sonst später Phasen verzögern.

- [ ] Kickoff mit Merle Vogelsang: Scope (PRD), Nicht-Ziele und Rollenverteilung bestätigen
- [ ] Tech-Stack entscheiden: CMS-fähig (Team pflegt Texte/Bilder ohne Entwickler), barrierefrei umsetzbar (WCAG 2.1 AA), DSGVO-konform hostbar
- [ ] Fragebogen zur alten WordPress-Seite an Kundin schicken, Content-Zugang klären
- [ ] Sitemap entwerfen: Startseite, B2b-Bereich (max. 1 Klick erreichbar), Werkstatt, Shop-Link, FAQ, Kontakt/Formular
- [ ] Analytics-/Dashboard-Lösung auswählen (DSGVO-konform, Consent vor Tracking)
- [ ] Offene Punkte an Kundin adressieren: Inhalte der B2b-SLAs, Partnerportal-Entscheidung Stufe 1 vs. 2, Formularthema-zu-Postfach-Zuordnung bestätigen

**Abhängigkeit/Risiko:** Ohne Antwort auf die drei offenen Punkte oben verzögert sich Phase 3 (B2b-Content) und Phase 4 (Formular-Routing).

## Phase 2 – Design

Ziel: Moderner Auftritt in Blau/Orange, der auf dem bestehenden Branding aufbaut, WCAG-AA-tauglich ist und mobil funktioniert.

- [ ] Exakte Hex-Werte für Blau/Orange von Kundin einholen (`design/DESIGN.md` Platzhalter auflösen)
- [ ] Logo-Dateien (SVG/PNG) von Kundin einholen
- [ ] Abgeleitete Farbtöne definieren (Hover, Hintergründe, Fehler/Erfolg), Kontrastprüfung Orange-auf-Weiß gegen WCAG 2.1 AA
- [ ] Typografie festlegen (Schriftarten, Größen, auch für B2b-Bereich „nicht altbacken")
- [ ] Bildstil festlegen: eigene Fotos von Team/Werkstatt/Standorten als Vertrauensbeleg (Shooting-Bedarf klären)
- [ ] Wireframes für Startseite, B2b-Bereich mit Kalkulator, FAQ, Formular
- [ ] `design/DESIGN.md` Vorlagen-Tabelle mit finalen Dateien aktualisieren
- [ ] Design-Review und Freigabe durch Merle Vogelsang

**Abhängigkeit:** Hex-Werte und Logo-Dateien sind Blocker für jede weitere Gestaltung – so früh wie möglich bei der Kundin anfragen.

## Phase 3 – Content & Fachinhalte

Ziel: Alle Texte und Daten beschaffen, die Entwicklung sonst nur mit Platzhaltern bauen kann.

- [ ] FAQ: mit Amara Osei mind. 20 häufigste Fragen aus Support-Anfragen erheben
- [ ] Vorsortierungsregeln (welches Thema → welche Stelle) mit Amara/Dilan/Heiner final abstimmen
- [ ] B2b-Leasing-Texte mit Dilan Aydın erarbeiten (Referenz Klinikum/80 Räder als Beleg nutzen)
- [ ] Leasing-Kalkulator-Werte vom Leasingpartner anfordern, konfigurierbar (nicht hartkodiert) hinterlegen
- [ ] Werkstatt-Inhalte mit Heiner Vogelsang abstimmen
- [ ] Vertrauensbelege sammeln: regionale Partnerschaften/Zulieferer, „Erst anschauen, dann sagen"-Haltung konkret belegen
- [ ] Übernahmefähige Inhalte der alten WordPress-Seite sichten und redaktionell anpassen (Sie-Form, sachlich)
- [ ] Platzhalter für noch fehlende Inhalte (B2b-SLAs) klar markieren, falls bis Entwicklungsstart nicht final

## Phase 4 – Entwicklung

Ziel: Alle Akzeptanzkriterien aus dem PRD technisch umsetzen.

- [ ] CMS-Setup, sodass Team Texte/Bilder ohne Entwickler ändern kann
- [ ] B2b-Bereich Dienstrad-Leasing: von Startseite in 1 Klick erreichbar
- [ ] Anfrageformular mit Themen-Abfrage (B2b, Werkstatt, Kauf, Sonstiges) und Routing an zuständige Postfächer/Personen
- [ ] Eingangsbestätigung an Absender bei B2b-Anfragen
- [ ] Leasing-Kalkulator: Eingabe Radpreis + Gehalt → monatliche Rate, Werte konfigurierbar aus Phase 3
- [ ] FAQ-Bereich durchsuchbar machen
- [ ] Online-Shop-Verlinkung von jeder Seite, Funktionsprüfung des externen Shops
- [ ] Analytics-Dashboard: Besucher, Absprungrate, Anfragen; Consent-Banner vor jeglichem Tracking
- [ ] Umsetzung Design-System aus Phase 2 (Farben, Typografie, Responsive/Mobile)

## Phase 5 – QA, Barrierefreiheit & DSGVO-Prüfung

Ziel: Alle Akzeptanzkriterien verifizieren, bevor der alte Auftritt abgelöst wird.

- [ ] WCAG 2.1 AA Audit (insbesondere Kontraste Blau/Orange, Tastaturbedienung, Screenreader)
- [ ] Mobile-Test auf gängigen Geräten/Breakpoints
- [ ] End-to-End-Test Formular-Routing je Thema (B2b/Werkstatt/Kauf/Sonstiges) inkl. Eingangsbestätigung
- [ ] Leasing-Kalkulator gegen Leasingpartner-Werte verifizieren
- [ ] DSGVO-Review: Einwilligung vor Tracking, Formulardaten, alte Inhalte auf personenbezogene Daten geprüft
- [ ] Shop-Verlinkung auf allen Seiten stichprobenartig prüfen
- [ ] Freigabe-Runde mit Merle Vogelsang

## Phase 6 – Launch

- [ ] Redirects von alten WordPress-URLs einrichten
- [ ] DNS-/Hosting-Umschaltung
- [ ] Team-Schulung: CMS-Pflege, Dashboard-Nutzung (vermutlich Svenja federführend)
- [ ] Monitoring der ersten Tage (Formular-Eingänge, Fehler, Ladezeiten)

## Phase 7 – Post-Launch & Messung

Ziel: Die vierte PRD-Zielsetzung („messbar werden") einlösen und Grundlage für Stufe 2 schaffen.

- [ ] Nach 4–6 Wochen erste Auswertung: Besucher, Absprungrate, B2b-Anfragen vs. Referenzwert (Klinikum-Fall)
- [ ] Rückmeldung von Amara/Dilan einholen: spürbare Entlastung bei Support/Vertrieb?
- [ ] Learnings dokumentieren, offene Stufe-2-Entscheidung (Partnerportal) mit tatsächlichen Nutzungsdaten neu bewerten
