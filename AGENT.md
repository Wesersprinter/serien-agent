# Serien-Agent — Arbeitsanweisung

Diese Datei beschreibt, was der wöchentliche Lauf tut. Der geplante Task
(`serien-wochenreport`, Freitag 09:00, Europe/Berlin) enthält dieselbe Anweisung
in Kurzform. Änderst du hier etwas Grundsätzliches, sag Claude Bescheid, damit
der Task-Prompt mitgezogen wird.

## Dateien

| Datei | Zweck |
|---|---|
| `serien-profil.md` | Geschmack, Dienste, No-Gos — von Henning bearbeitbar |
| `historie.md` | Was schon vorgeschlagen wurde + Hennings Feedback |
| `reports/JJJJ-MM-TT-report.md` | Ein Report pro Lauf |

## Ablauf pro Lauf

1. `serien-profil.md` und `historie.md` lesen.
2. Websuche: neue Serienstarts und neue Staffeln der nächsten 2–4 Wochen in
   Deutschland. Sinnvolle Suchen z. B.:
   - "Serien Neustarts <Monat> <Jahr> Deutschland Netflix Prime Disney"
   - "neue Staffeln <Monat> <Jahr> Streaming Deutschland"
   - "Apple TV+ / Paramount+ / Magenta TV Neuheiten <Monat>"
   - gezielt für Titel aus "Serien, die ich aktuell verfolge"
   Quellen notieren. Startdaten immer als "laut <Quelle>" kennzeichnen.
3. Gegen das Profil filtern: Genres, No-Gos, deutsche Fassung vorhanden?
4. Verfügbarkeit prüfen: Läuft der Titel auf einem von Hennings Diensten?
   Wenn nein → nur bei sehr hoher Passung erwähnen, klar als "hast du nicht" markieren.
5. Titel aussortieren, die in `historie.md` schon unter "Bereits vorgeschlagen"
   stehen — es sei denn, es gibt echte Neuigkeiten (Termin verschoben, Trailer, Abbruch).
6. Report schreiben (Deutsch, kompakt, max. ~1 Seite) mit genau drei Abschnitten:
   - **Passt zu dir** — je Titel: Startdatum, Plattform, ein Satz Begründung
   - **Neue Staffeln deiner Serien**
   - **Könnte dich überraschen** — 2–3 Titel abseits des üblichen Geschmacks,
     je mit Begründung, warum sie trotzdem zum Profil passen
   Am Ende: Quellenliste.
7. Report unter `reports/JJJJ-MM-TT-report.md` ablegen **und** vollständig im
   Chat ausgeben, damit Henning ihn sofort sieht.
8. `historie.md` fortschreiben: alle genannten Titel unter "Bereits vorgeschlagen"
   mit Datum und Abschnitt eintragen.

## Feedback-Schleife

Henning schreibt sein Urteil in `historie.md` unter "Feedback" — oder sagt es
Claude direkt ("das war nichts" / "mehr davon"). Daraus wird gelernt:

- **"mehr davon"** → Merkmal (Genre, Tonfall, Herkunft, Showrunner) in
  `serien-profil.md` unter Lieblingsgenres bzw. Referenzpunkte ergänzen.
- **"das war nichts"** → Merkmal in `serien-profil.md` unter No-Gos ergänzen
  oder abschwächen, Titel in der Historie als abgelehnt markieren.

## Grenzen (ehrlich benennen)

- Keine TMDb-/JustWatch-API im Einsatz. Alles kommt aus der Websuche.
- Startdaten und Plattform-Zuordnungen ändern sich häufig — darum die Quellenangabe.
- Verfügbarkeit in Deutschland kann von internationalen Meldungen abweichen.
