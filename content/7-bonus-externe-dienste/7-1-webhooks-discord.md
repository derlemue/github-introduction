# 7-1- Praxis: Benachrichtigungen (Discord/Slack) 💬

[🏠 Home](../../README.md) | [◀️ Zurück](./7-0-marketplace.md) | [🏁 Zurück zur Übersicht](../../README.md)

---

## "Ping! Neuer Code da."

Es ist motivierend für das Team, wenn man sieht, dass etwas passiert. Wir richten einen **Webhook** ein, der Updates in einen Chat-Kanal postet.

### Beispiel: Discord Integration

1.  **In Discord:**
    *   Gehe in deinen Server-Einstellungen auf **Integrationen** > **Webhooks**.
    *   Erstelle einen neuen Webhook und kopiere die **Webhook URL**.

2.  **In GitHub:**
    *   Gehe in dein Repo auf **Settings** > **Webhooks**.
    *   Klicke **Add webhook**.
    *   **Payload URL:** Füge die Discord-URL ein und hänge `/github` ans Ende an! (Wichtig für Discord).
    *   **Content type:** Wähle unbedingt `application/json`.
        *   *Info:* `application/x-www-form-urlencoded` ist ein älteres Format, das Discord oft nicht versteht. Wir brauchen JSON.
    *   **Which events?** Wähle "Just the push event" (für den Anfang).
    *   Klicke **Add webhook**.

### Testen & Debuggen 🐞

Mache eine kleine Änderung an einer Datei und pushe sie.
*Bling!* In deinem Discord-Channel sollte jetzt eine Nachricht von GitHub stehen.

**Kommt nichts an?**
Gehe in GitHub wieder auf den Webhook und klicke auf den Tab **Recent Deliveries**.
*   Siehst du einen ✅ grünen Haken? GitHub hat gesendet. (Fehler liegt bei Discord/URL).
*   Siehst du ein ❌ rotes Kreuz? Klicke darauf, um die Fehlermeldung (Response) zu sehen.

Das funktioniert fast identisch für Slack (dort gibt es eine offizielle GitHub-App).
