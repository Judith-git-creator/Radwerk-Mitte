# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Projektstand

Das Projekt ist ein Website-Relaunch für **Radwerk Mitte** (Fahrradhändler mit Werkstatt und B2b-Dienstrad-Leasing). Bisher gibt es noch keinen Code, kein Build-System und kein Git-Repository. Grundlagen:

- `PRD – Website-Relaunch Radwerk Mitte.pdf` (Stand 19.10.2026, Autorin: Judith): verbindlicher Umfang. Wenn sich PRD und diese Datei widersprechen, gilt das PRD.
- `Übung_Kundengespräch_Protokoll.pdf`: Protokoll des ersten Kundengesprächs mit Merle Vogelsang (Gesprächsführung: Steve, weitere Beiträge: Jonas, Chris). Die Fußnoten enthalten ein unsauberes Spracherkennungs-Transkript; Zitate daraus nicht wörtlich übernehmen. Das Protokoll liefert Hintergrund, das PRD die Entscheidungen.
- `Firmensteckbrief-Radwerk-Mitte-BTA.pdf`: Eckdaten, Geschichte, Ansprechpersonen und Haltung der Firma. Radwerk Mitte ist eine **fiktive Übungsfirma** aus dem Kurs „Vibe Engineering“; alle Personen, Zahlen und Kunden sind erfunden. Das Lila im Steckbrief ist das Kurslayout, nicht die Markenfarbe.

- `design/`: Ablage für alle Designvorlagen (Mockups, Logo, Farben, Typografie). Einstieg und Übersicht ist `design/DESIGN.md`, sie wird hier eingebunden: @design/DESIGN.md

Tech-Stack, Build-, Lint- und Test-Befehle sind noch nicht festgelegt. Sobald sie feststehen, hier ergänzen.

## Unternehmenskontext

### Eckdaten (aus dem Firmensteckbrief)

- **Radwerk Mitte GmbH**, gegründet 1989 in Kassel von Heiner Vogelsang (anfangs eine Werkstatt in einem Kasseler Hinterhof). Rund 120 Beschäftigte, etwa 28 Mio. € Umsatz.
- Standorte: zwei Filialen mit Werkstatt in **Kassel** und **Göttingen**, außerdem Onlineshop, Zentrallager und der Bereich Dienstrad-Leasing. Das Leasing wächst am schnellsten.
- Merle Vogelsang hat das Dienstrad-Leasing aufgebaut und führt die Firma seit zwei Jahren. Heiner Vogelsang leitet weiter die Werkstatt.
- Bestehende Geschäftskunden im Leasing: ein Klinikum, eine Stadtverwaltung und ein Pflegedienst. Sie brauchen klare Angebote und verlässliche Termine.
- **Haltung des Hauses:** „Erst anschauen, dann sagen.“ Zusagen werden gehalten, auch kleine. Verzögert sich etwas, meldet sich das Team vor dem Termin. Dieses Versprechen soll die Website glaubwürdig transportieren.

### Ansprechpersonen (relevant für Formular-Weiterleitung und Inhalte)

| Person | Rolle |
|---|---|
| Merle Vogelsang | Geschäftsführung, Ansprechpartnerin im Projekt, gibt Inhalte frei |
| Heiner Vogelsang | Gründer, Werkstattleitung (Thema „Werkstatt“) |
| Dilan Aydın | Vertrieb für Geschäftskunden (Thema „B2b“, Leasing-Anfragen) |
| Svenja Kowalczyk | E-Commerce und Marketing (Online-Shop, vermutlich auch Website-Pflege und Analytics) |
| Amara Osei | Kundenservice (die eine Person, die bisher alle Anfragen abfängt) |

Die Zuordnung der Formularthemen zu Personen ist abgeleitet und muss noch mit der Kundin bestätigt werden. Adressen gehören in die Konfiguration, nicht in den Code.

### Aus dem Kundengespräch

- Familienunternehmen mit Ausbildungsbetrieb an beiden Standorten. Langfristiges Ziel ist, alle Arbeitsplätze zu sichern.
- Wachstum soll vor allem über B2b kommen (E-Bike- und Dienstrad-Leasing für Unternehmen). B2c ist bereits gut aufgestellt und bleibt bestehen. Custom-Räder für das Luxussegment werden im nächsten Jahr separat getestet und gehören deshalb nicht auf die Website.
- **Alleinstellungsmerkmal, das die Website belegen soll:** über Jahre gewachsenes regionales Netzwerk, direkte Erreichbarkeit per Telefon, Service vor Ort aus einer Hand (Reparatur bis Ausstattung ganzer Firmen). Kunden merken das laut Kundin oft erst, nachdem sie große Anbieter ausprobiert haben. Die Seite soll es also mit konkreten Belegen zeigen, nicht nur behaupten.
- Wettbewerb: große Online-Händler (z. B. Upway).
- Regionale Partnerschaften und Zulieferer sind der Kundin wichtig und eignen sich als Vertrauensbeleg.
- Engpässe: Kundenservice (ein Mitarbeiter; B2b-Kunden rufen häufig an) und Werkstatt bei Spitzenlast. FAQ und Vorsortierung sollen beides entlasten.
- Blau/Orange sind auch auf den Firmenfahrzeugen, daher fest gesetzt. Auch der B2b-Bereich soll modern und nicht „altbacken“ wirken.
- Bisher gibt es keine Daten zur Absprungrate. Dass Nutzer abspringen, weil sie keine E-Mail schreiben wollen, ist nur aus Gesprächen bekannt.
- Partnerportal: Radwerk kann sich in Portale von Partnern einloggen, bietet selbst aber keines an. Im PRD ist das auf Stufe 2 verschoben.

## Ziele (Stufe 1)

Budget ca. 150.000 €, Basis für ca. 15 % Wachstum im Folgejahr. Die Website ersetzt eine veraltete WordPress-Seite.

1. **Mehr B2b-Anfragen:** Dienstrad-Leasing für Arbeitgeber steht im Mittelpunkt (Referenz: Klinikum mit 80 Rädern).
2. **Support entlasten:** Standardfragen beantwortet die Seite selbst, Anfragen kommen vorsortiert an (bisher fängt ein einziger Support-Mitarbeiter alles ab).
3. **Vertrauen zeigen:** moderner Auftritt in Blau/Orange, der Netzwerk und Service vor Ort belegt.
4. **Messbar werden:** erstmals Daten zu Besuchern, Absprungrate und Anfragen.

## Zielgruppen

- **Arbeitgeber** (Klinik, Kommune, Pflegedienst): Leasing-Angebot verstehen, schnell anfragen
- **Beschäftigte mit Dienstrad:** monatliche Kosten und Ablauf selbst ausrechnen
- **Privatkunden (B2c):** Antworten ohne Anruf, Weg zum Online-Shop
- **Radwerk-Team** (Vertrieb, Kundenservice): vorsortierte Anfragen, Inhalte selbst pflegen

## Funktionen und Akzeptanzkriterien

| Funktion | Fertig, wenn … |
|---|---|
| B2b-Bereich Dienstrad-Leasing | von der Startseite in 1 Klick erreichbar; das Anfrageformular landet sofort beim Vertrieb, der Absender erhält eine Eingangsbestätigung |
| Leasing-Kalkulator | zeigt nach Eingabe von Radpreis und Gehalt die monatliche Rate; die Werte kommen vom Leasingpartner (nicht selbst erfinden, sondern konfigurierbar hinterlegen) |
| FAQ | mindestens 20 häufigste Fragen (vom Support erhoben), durchsuchbar |
| Anfrage-Vorsortierung | das Formular fragt das Thema ab (B2b, Werkstatt, Kauf, Sonstiges) und leitet an die zuständige Stelle weiter |
| Online-Shop-Anbindung | der bestehende externe Shop ist von jeder Seite verlinkt und funktioniert durchgehend |
| Design & Technik | Farben Blau/Orange, mobil voll nutzbar, barrierefrei (WCAG 2.1 AA), DSGVO-konform |
| Pflege & Messung | das Team ändert Texte und Bilder ohne Entwickler (CMS nötig); ein Dashboard zeigt Besucher, Absprungrate und Anfragen |

## Nicht-Ziele (Stufe 1), nicht umsetzen

- kein Partnerportal mit Login (erst Stufe 2, nach Klärung der Schnittstellen)
- kein Custom-Rad- oder Luxusbereich
- kein neuer Shop und keine neue Warenwirtschaft, der externe Shop wird nur verlinkt
- kein neues Branding: Farben und Logo bleiben, sie werden nur moderner umgesetzt
- kein Chat, der berät, verkauft oder Termine zusagt

## Inhalte und Tonalität

- Ton: sachlich, hilfsbereit, Kunden werden mit **„Sie“** angesprochen. Die Freigabe erteilt Merle Vogelsang.
- Inhalte der alten WordPress-Seite dürfen übernommen werden (der Zugang wird über einen Fragebogen geklärt).
- FAQ-Inhalte und Vorsortierungsregeln liefert der Kundenservice, Kalkulatorwerte die Leasingpartner. Bis dahin klar markierte Platzhalter verwenden.
- Analytics und Formulare müssen DSGVO-konform sein (Einwilligung vor Tracking).

## Offene Punkte

- Inhalte der B2b-SLAs
- ob ein Partnerportal doch schon in Stufe 1 nötig ist
- welche Person bzw. welches Postfach welches Formularthema (B2b, Werkstatt, Kauf, Sonstiges) erhält
