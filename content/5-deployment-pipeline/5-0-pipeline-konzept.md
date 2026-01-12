# 5-0- Das Pipeline-Konzept 🧠

[🏠 Home](../../README.md) | [◀️ Zurück](./5--deployment-intro.md) | [▶️ Nächstes: Die Action bauen](./5-1-action-einrichten.md)

---

## Wie funktioniert CI/CD?

CI/CD steht für **Continuous Integration / Continuous Deployment**. Das klingt kompliziert, ist aber eigentlich ein einfacher Kreislauf:

### Der Ablauf bei lemueIO

1.  **Code:** Du schreibst Code auf deinem Laptop und machst einen `push`.
2.  **Trigger:** GitHub bemerkt: "Aha! Neuer Code auf dem `main` Branch!"
3.  **Action (Der Roboter):** GitHub startet einen unsichtbaren Linux-Server.
4.  **Checkout:** Der Roboter lädt deinen Code herunter.
5.  **Deploy:** Der Roboter verbindet sich mit deinem Webserver (per FTP/SFTP) und überschreibt die alten Dateien.

### Warum ist das besser?
*   **Keine Flüchtigkeitsfehler:** Der Roboter vergisst keine Dateien.
*   **Geschwindigkeit:** Es dauert meist unter 2 Minuten.
*   **Sicherheit:** Niemand muss Passwörter auf seinem Laptop speichern.
