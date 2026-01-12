# 1-0- Git Installation & Konfiguration ⚙️

[🏠 Home](../../README.md) | [◀️ Zurück](./1--setup-intro.md) | [▶️ Nächstes: SSH Keys](./1-1-ssh-keys-einrichten.md)

---

## Schritt 1: Git herunterladen

Je nach Betriebssystem ist der Weg etwas anders:

* **Windows:** Lade [Git for Windows](https://git-scm.com/download/win) herunter und installiere es (klicke "Next" bei allen Standardeinstellungen).
* **Mac:** Öffne das Terminal und tippe `git --version`. Wenn es nicht installiert ist, fragt dein Mac, ob er es installieren soll. Bestätige das.
* **Linux:** `sudo apt-get install git` (Ubuntu/Debian) oder via Paketmanager deiner Wahl.

## Schritt 2: Der Test

Öffne ein Terminal (oder "Git Bash" auf Windows) und tippe:

```bash
git --version
```

Erscheint eine Nummer (z.B. `git version 2.30.0`), bist du bereit.

## Schritt 3: Visitenkarte hinterlegen

Git muss wissen, wer die Änderungen macht. Führe diese Befehle im Terminal aus (ersetze die Platzhalter):

```bash
git config --global user.name "Dein Vorname Nachname"
git config --global user.email "deine-email@lemue.io"
```

Pro-Tipp: Nutze am besten die E-Mail-Adresse, die du auch bei GitHub hinterlegt hast, damit dein Profilbild korrekt neben deinen Änderungen angezeigt wird.