# 1-1- SSH Keys einrichten 🔑

[🏠 Home](../../README.md) | [◀️ Zurück](./1-0-git-installation.md) | [▶️ Nächstes: Workflow](../2-basis-workflow/2--workflow-intro.md)

---

## 🔒 Warum Passwörter "out" sind

Früher hast du dich bei jedem Hochladen (`push`) mit Benutzername und Passwort angemeldet. Das ist nervig und unsicher.
Bei **lemueIO** nutzen wir **SSH-Keys**.

### Das Konzept: Schlüssel & Schloss
Stell dir vor, dein Computer hat einen **privaten Schlüssel** (Private Key), den nur er kennt.
GitHub bekommt das passende **Schloss** (Public Key).

Wenn du dich verbindest, prüft GitHub: *"Passt dein Schlüssel in mein Schloss?"*
Wenn ja, bist du drin. Ohne Passwort-Eingabe.

> **⚠️ Wichtig:** Gib deinen **Private Key** (das ist die Datei ohne Endung) niemals weiter! Der **Public Key** (endet auf `.pub`) darf (und muss) geteilt werden.

---

## Schritt 1: Schlüsselpaar generieren

Wir nutzen den modernen **Ed25519**-Standard (schneller & sicherer als das alte RSA).

Öffne dein Terminal (oder Git Bash) und gib ein:

```bash
ssh-keygen -t ed25519 -C "deine-email@lemue.io"
```

1.  Drücke **Enter**, um den Standard-Speicherort zu bestätigen.
2.  (Optional) Gib ein Passwort für den Schlüssel ein (extra Sicherheit) oder drücke **Enter** für keins.

## Schritt 2: Den öffentlichen Schlüssel kopieren

Jetzt müssen wir das "Schloss" kopieren, um es GitHub zu geben.

**Windows (PowerShell):**
```powershell
Get-Content ~/.ssh/id_ed25519.pub | Set-Clipboard
```

**Mac:**
```bash
pbcopy < ~/.ssh/id_ed25519.pub
```

**Linux:**
```bash
cat ~/.ssh/id_ed25519.pub
# -> Kopiere die Ausgabe (fängt an mit ssh-ed25519...)
```

## Schritt 3: Bei GitHub hinterlegen

1.  Geh auf GitHub.com oben rechts auf dein **Profilbild** -> **Settings**.
2.  Klicke links auf **SSD and GPG keys**.
3.  Klicke oben rechts auf **New SSH Key**.
4.  **Title:** Gib deinem Key einen Namen (z.B. "MacBook Pro Elliot").
5.  **Key:** Füge den kopierten Inhalt (`Strg+V` / `Cmd+V`) ein.
6.  Klicke **Add SSH key**.

---

## 🛠️ Troubleshooting

### Fehler: "Permission denied (publickey)"
Das ist der Klassiker. Er bedeutet, dass GitHub deinen Schlüssel nicht akzeptiert oder dein Computer ihn nicht anbietet.

**Lösung:** Prüfe, ob dein SSH-Agent läuft und den Key kennt:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### Fehler: "But I have an old rsa key?"
Kein Problem, aber wir empfehlen dringend ein Upgrade auf Ed25519. Alte RSA-Keys (unter 3000 bit) werden von GitHub teilweise gar nicht mehr akzeptiert.

---
*Glückwunsch! Deine Verbindung ist jetzt sicher und passwortfrei. Weiter geht's mit dem Workflow!*
