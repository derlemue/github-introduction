# 7-0- Der GitHub Marketplace 🛍️

[🏠 Home](../../README.md) | [◀️ Zurück](./7--bonus-intro.md) | [▶️ Nächstes: Webhooks & Chat](./7-1-webhooks-discord.md)

---

## Der App Store für deinen Code

Oben im GitHub-Menü findest du den Punkt **Marketplace**. Hier gibt es Tools für fast alles, um deinen Workflow zu automatisieren und zu verbessern.

### Unsere Top-Empfehlungen für lemueIO

#### 1. Sicherheit: Dependabot 🛡️
Ein absolutes Muss. Dependabot prüft deine Abhängigkeiten (z.B. npm Pakete) auf bekannte Sicherheitslücken.
*   **Was es tut:** Es erstellt automatisch Pull Requests, um unsichere Pakete zu aktualisieren.
*   **Aktivierung:** In den Repo-Settings unter **Code security and analysis**.

#### 2. Hygiene: Stale Bot 🧹
Nichts ist schlimmer als hunderte offene Tickets, die 2 Jahre alt sind.
*   **Was es tut:** Der "Stale"-Bot markiert Issues und PRs als "inaktiv", wenn sich lange nichts tut, und schließt sie später automatisch.

---

### Apps vs. Actions
*   **Actions:** Kleine Skripte für deine Pipeline (haben wir in Kapitel 5 genutzt).
*   **Apps:** Vollwertige Integrationen, die oft Rechte auf deinem ganzen Account brauchen.

> **⚠️ WICHTIGE WARNUNG:**
> Installiere Apps niemals blind!
> Viele Apps fordern umfangreiche Rechte (z.B. "Read/Write all code"). Ein böswilliger App-Entwickler könnte theoretisch deinen Code stehlen.
> **Regel bei lemueIO:** Nur Apps von **verifizierten Herausgebern** (blauer Haken) installieren oder vorher Rücksprache halten!
