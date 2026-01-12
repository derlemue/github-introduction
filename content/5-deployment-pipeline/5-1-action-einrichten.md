# 5-1- Die Action einrichten 🛠️

[🏠 Home](../../README.md) | [◀️ Zurück](./5-0-pipeline-konzept.md) | [🔜 Nächstes Hauptkapitel](../../content/6-github-pages/6--pages-intro.md)

---

## Schritt 1: Zugangsdaten sichern (Secrets) 🔒

Wir schreiben NIEMALS Passwörter in den Code. Jeder könnte sie lesen! Wir nutzen den GitHub-Tresor.

1.  Gehe in deinem Repo zu **Settings** > **Secrets and variables** > **Actions**.
2.  Klicke auf **New repository secret**.
3.  Erstelle folgende Geheimnisse (mit den Daten deines Webhosters):
    *   `FTP_SERVER` (z.B. ftp.lemue.io)
    *   `FTP_USERNAME` (Dein Benutzername)
    *   `FTP_PASSWORD` (Dein Passwort)

## Schritt 2: Den Roboter programmieren

Erstelle in deinem Projektordner (ganz oben) folgende Datei-Struktur, falls noch nicht vorhanden:
`.github/workflows/deploy.yml`

Kopiere diesen Inhalt hinein:

```yaml
name: 🚀 Deploy Website
on:
  push:
    branches:
      - main  # Feuert nur, wenn Code auf 'main' landet

jobs:
  web-deploy:
    name: 🎉 Deploy
    runs-on: ubuntu-latest
    steps:
    - name: 🚚 Get latest code
      uses: actions/checkout@v4
    
    - name: 📂 Sync files via FTP
      uses: SamKirkland/FTP-Deploy-Action@v4.3.4
      with:
        server: ${{ secrets.FTP_SERVER }}
        username: ${{ secrets.FTP_USERNAME }}
        password: ${{ secrets.FTP_PASSWORD }}
        server-dir: /html/  # Pfad auf deinem Server (oft /html/ oder /public_html/)
```

Sobald du diese Datei commitest und pushst, versucht GitHub sofort, den ersten Deploy zu starten!
