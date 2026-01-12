# 6-1- Die eigene Domain nutzen 🔗

[🏠 Home](../../README.md) | [◀️ Zurück](./6-0-pages-aktivieren.md) | [🏁 Abschluss & Roadmap](../../ROADMAP.md)

---

## Von github.io zu lemue.io

Wir wollen, dass die Seite unter einer Subdomain deiner Organisation läuft, z.B. `docs.lemue.io` oder `projekt.lemue.io`.

### 1. Beim Domain-Provider (DNS)
Logge dich dort ein, wo du deine Domain gekauft hast. Erstelle einen **CNAME-Record**:
*   **Host/Name:** `docs` (oder wie die Subdomain heißen soll)
*   **Value/Ziel:** `lemueio.github.io.` (Wichtig: Auf den GitHub-Namen zeigen, nicht auf die IP!)

### 2. In GitHub
1.  Gehe wieder zu **Settings > Pages**.
2.  Scrolle zu **Custom domain**.
3.  Trage deine Domain ein: `docs.lemue.io`.
4.  Klicke **Save**.
5.  GitHub prüft nun die DNS-Einträge. Das kann kurz dauern.
6.  **WICHTIG:** Setze den Haken bei **Enforce HTTPS**, damit die Seite sicher ist.

🎉 **Glückwunsch!** Dein Projekt ist nun professionell gehostet.
