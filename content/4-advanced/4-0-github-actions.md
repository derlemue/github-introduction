# 4-0- GitHub Actions & Automatisierung ⚡

[🏠 Home](../../README.md) | [◀️ Zurück](./4--advanced-intro.md) | [🏁 Abschluss & Roadmap](../../ROADMAP.md)

---

## Was ist eine "Action"?

Eine **Action** ist ein kleines Skript, das GitHub automatisch ausführt, wenn ein bestimmtes Ereignis eintritt (z.B. ein `push` oder ein `pull request`).

Diese Skripte liegen in deinem Repository im Ordner `.github/workflows/` und sind in der Sprache **YAML** geschrieben.

## Dein erster Workflow

Stell dir vor, wir wollen jedes Mal, wenn jemand Code hochlädt, eine Begrüßung ins Protokoll schreiben.

### Die Struktur einer YAML-Datei

Erstelle (theoretisch) eine Datei `.github/workflows/hallo.yml`:

```yaml
name: Hallo Welt
on: [push]  # Wann soll es passieren? Bei jedem Push.

jobs:
  begruessung:
    runs-on: ubuntu-latest  # Wo soll es laufen? Auf einem Linux-Server von GitHub.
    steps:
      - uses: actions/checkout@v3 # Schritt 1: Code herunterladen
      - name: Sag Hallo
        run: echo "Hallo lemueIO! Code wurde erfolgreich hochgeladen." # Schritt 2: Befehl ausführen
```

## Warum ist das wichtig für lemueIO?

Mit deiner verifizierten Domain können wir später eine Action bauen, die sagt:

> "Wenn Code auf `main` landet -> Baue die Webseite -> Lade sie auf lemue.io hoch."

Das bedeutet: Du änderst nur Text in einer Datei, drückst "Push", und 2 Minuten später ist deine Webseite aktualisiert. Ohne FTP-Programme, ohne manuelles Kopieren.

---
**Herzlichen Glückwunsch! Du hast den theoretischen Teil des Guides abgeschlossen. 🎉**
