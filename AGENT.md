# Serien-Agent — Arbeitsanweisung

Der wöchentliche Lauf ist eine **Cloud-Routine** ("Serien-Wochenreport (Henning)",
Freitag 09:00 Europe/Berlin). Sie klont dieses Repo, arbeitet darin und committet
die Ergebnisse zurück. Henning braucht dafür keinen laufenden PC.

Änderst du hier etwas Grundsätzliches, sag Claude Bescheid — der Routine-Prompt
verweist auf diese Datei, muss aber bei strukturellen Änderungen mitgezogen werden.

## Dateien

| Datei | Zweck |
|---|---|
| `serien-profil.md` | Geschmack, Dienste, Lieblingsserien — von Henning bearbeitbar |
| `historie.md` | Was schon vorgeschlagen wurde + Hennings Feedback |
| `reports/JJJJ-MM-TT-report.md` | Ein Report pro Lauf |

## Ablauf pro Lauf

1. `serien-profil.md` und `historie.md` lesen. Das Profil ist die Wahrheit.
2. Heutiges Datum mit `date -u +%Y-%m-%d` ermitteln, nicht raten.
3. Websuche: neue Serienstarts und neue Staffeln der nächsten 2–4 Wochen in
   Deutschland. Sinnvolle Suchen z. B.:
   - "Serien Neustarts <Monat> <Jahr> Deutschland Streaming"
   - "neue Staffeln <Monat> <Jahr> Netflix Prime Disney+ Apple TV+ Paramount+"
   - gezielt für jede Serie unter "Serien, die ich aktuell verfolge"
   - "ARD Mediathek neue Serie <Monat>", "ZDF neue Serie <Monat>"
   Quellen notieren. Startdaten immer als "laut <Quelle>" kennzeichnen.
   Widersprechen sich Quellen, beide Termine nennen.
4. Gegen das Profil filtern: Treffen die drei Geschmackssäulen? Deutsche Fassung da?
5. Verfügbarkeit prüfen: Läuft der Titel auf einem von Hennings Diensten?
   Wenn nein → nur bei herausragender Passung, klar als "hast du nicht" markiert.
6. Titel aussortieren, die in `historie.md` unter "Bereits vorgeschlagen" stehen —
   außer es gibt echte Neuigkeiten (Termin verschoben, abgesetzt, Staffel bestätigt).
7. Report schreiben (Deutsch, kompakt, ~1 Seite): **Passt zu dir** ·
   **Neue Staffeln deiner Serien** (mit *Nachgeholt* und *Ausblick* bei Bedarf) ·
   **Könnte dich überraschen** (2–3 Titel) · **Quellen**.
8. Report unter `reports/JJJJ-MM-TT-report.md` ablegen **und** vollständig in der
   Antwort ausgeben, damit Henning ihn sofort sieht.
9. `historie.md` fortschreiben: alle genannten Titel mit Datum und Abschnitt.
10. **Alles committen und pushen** (siehe unten). Ohne Push ist die Arbeit verloren.

## Commit am Ende jedes Laufs

```
git add -A
git commit -m "Serien-Report <JJJJ-MM-TT>"
git push
```

Schlägt der Push fehl, einmal `git pull --rebase` und erneut pushen. Klappt es dann
noch nicht, den Fehler in der Antwort nennen und den Report trotzdem vollständig
ausgeben, damit Henning ihn nicht verliert.

## Feedback-Schleife

Henning schreibt sein Urteil in `historie.md` unter "Feedback". Jeder Lauf prüft, ob
dort etwas Neues steht, und arbeitet es in `serien-profil.md` ein:

- **"mehr davon"** → Merkmal (Säule, Tonfall, Herkunft, Showrunner) im Profil ergänzen
- **"das war nichts"** → Merkmal unter No-Gos ergänzen, Titel in der Historie als
  abgelehnt markieren

Bearbeitetes Feedback in der Historie als erledigt markieren, damit es nicht doppelt
einfließt. In der Antwort in einer Zeile sagen, was am Profil geändert wurde.

## Grenzen (ehrlich benennen)

- Keine TMDb-/JustWatch-API. Alles kommt aus der Websuche.
- Startdaten und Plattform-Zuordnungen ändern sich häufig — darum die Quellenangabe.
- Verfügbarkeit in Deutschland kann von internationalen Meldungen abweichen.
