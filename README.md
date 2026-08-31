# JOB REDESIGN LAB

Interaktiver Demonstrator zur Studie Job Redesign der kantonalen Verwaltung Zürich.
Aufgaben verstehen, Betroffenheit bewerten, Zukunft gestalten.

**Live:** https://y8arman.github.io/job-redesign-lab/

## Drei Einstiege

- **Erleben** (ohne Anmeldung): Der Aufgaben-Kompass bewertet eine Aufgabe über neun Dimensionen und zeigt live Wirkung, Machbarkeitsstatus, Zeithorizont und Betroffenheit. Die Betroffenheitslandkarte stellt 48 synthetische Aufgabentypen aus sechs Funktionsfamilien dar, umschaltbar über drei Szenarien.
- **Workshop** (Live-Session): Die Moderation stellt aus fünf Modultypen eine Playlist zusammen, Teilnehmende treten per QR-Code oder Session-Code mit einem frei gewählten Alias bei.
- **Demo**: Der komplette Workshop-Ablauf mit zwölf simulierten Teilnehmenden, ohne Verbindung und ohne Speicherung.

## Workshop-Module

- **Stimmungsbild**: Meinungsfragen ohne richtig oder falsch, Balken wachsen live.
- **Wortwolke**: Ein bis drei Begriffe pro Person, häufige Begriffe werden grösser.
- **Kompass gemeinsam**: Alle bewerten dieselbe Aufgabe auf fünf Dimensionen. Der Gruppen-Median trifft auf das Bibliotheksprofil, Spannweiten machen Dissens sichtbar statt ihn wegzumitteln.
- **Wissens-Challenge**: Vier Runden mit je sechs Fragen, Countdown, Punkten und fachlicher Auflösung.
- **Betroffenheits-Voting**: Betroffenheit mal Zeithorizont als live wachsendes Raster.

Jedes Modulergebnis lässt sich als PNG sichern. Sessions können nach dem Workshop mit einem Klick gelöscht werden.

## Methodik

Das Regelwerk (Wirkungslogik Automatisieren, Augmentieren, Menschlich stärken, der vierstufige Machbarkeitsstatus bis hin zu bewusst nicht automatisieren, Zeithorizonte und Szenarien konservativ, ausgewogen, ambitioniert) entspricht dem Excel-Simulationstool der Studie. Eine Inhaltsprüfung beim Laden verifiziert Bibliothek, Fragenpools und Regelwerk gegen fixe Erwartungswerte und sperrt bei Abweichungen den Workshop-Teil.

## Technik

- Eine einzige `index.html`, Vanilla JS, kein Build-Schritt.
- Backend: Firebase Realtime Database (compat SDK via CDN), Region europe-west1.
- QR-Erzeugung: qrcodejs (MIT-Lizenz, in die Datei eingebettet).
- Keine Cookies, kein Tracking, Auswertung ausschliesslich auf Gruppenebene.
- Respektiert prefers-reduced-motion.

## Selbst betreiben

Datei forken, in der Firebase-Konsole ein Projekt mit Realtime Database anlegen, die Datenbankregeln publizieren und die Werte im markierten CONFIG-Block der `index.html` eintragen. Wichtig: Das Feld `databaseURL` fehlt im automatisch erzeugten Konsolen-Snippet und muss von Hand ergänzt werden.

## Bedienung für die Moderation

Workshop starten, Playlist anpassen, Session erstellen. In der Lobby erzeugt die Taste **B** fünfzehn Test-Bots, die alle Module wie echte Teilnehmende bespielen. Vor einem Echteinsatz einmal die komplette Playlist mit Bots durchspielen.
