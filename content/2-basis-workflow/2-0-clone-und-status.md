# 2-0- Clone & Status 📥

[🏠 Home](../../README.md) | [◀️ Zurück](./2--workflow-intro.md) | [▶️ Nächstes: Add & Commit](./2-1-add-commit-push.md)

---

## 1. Clone: Das Projekt holen

Bevor du arbeiten kannst, musst du das Projekt auf deinen Computer holen. Das nennen wir **Clonen**.

### HTTPS vs. SSH (Der ewige Kampf)
Wenn du auf GitHub auf den grünen **Code** Button klickst, siehst du zwei wichtige Reiter:

1.  **HTTPS:** `https://github.com/lemueIO/projekt.git`
    *   *Vorteil:* Einfach, funktioniert immer.
    *   *Nachteil:* Fragt dich beim Pushen oft nach Credentials (wenn kein Credential Manager installiert ist).
2.  **SSH:** `git@github.com:lemueIO/projekt.git`
    *   *Vorteil:* **Unsere Empfehlung!** Nutzt den Key, den wir in Kapitel 1 eingerichtet haben. Sicherheit + Komfort.

**Der Befehl:**
Öffne dein Terminal, navigiere in deinen Ordner (z.B. `cd ~/Projekte`) und tippe:

```bash
git clone git@github.com:lemueIO/github-introduction.git
```

Jetzt hast du eine exakte Kopie des Projekts auf deiner Festplatte.

---

## 2. Status: Wo bin ich?

Der wohl wichtigste Befehl überhaupt. Wenn du dich fragst "Was habe ich gerade gemacht?", ist die Antwort immer:

```bash
git status
```

### Die Farben lesen lernen 🚥

Git spricht mit dir durch Farben (in den meisten Terminals):

*   **🔴 Rot (Untracked / Modified):**
    *   Du hast eine Datei geändert oder neu erstellt.
    *   Git weiß davon, hat sie aber noch *nicht* für den nächsten Versand vorgemerkt.
    *   *Metapher:* Das Produkt liegt im Regal, aber nicht im Einkaufswagen.

*   **🟢 Grün (Staged / Added):**
    *   Du hast `git add` benutzt.
    *   Die Datei liegt im "Warenkorb" (Staging Area).
    *   Sie ist bereit für den `commit` (Kaufabschluss).

*   **"Nothing to commit, working tree clean":**
    *   Alles ist synchron. Du hast keine offenen Änderungen. Entspann dich. ☕

### 💡 Pro-Tipp
Gewöhn dir an, **vor jedem** `commit` und **nach jedem** `add` einmal kurz `git status` zu tippen. Das verhindert peinliche Fehler ("Ups, ich hab die Config-Datei mit Passwort hochgeladen!").

---
*Datei rot? Dann ab zum nächsten Schritt: Wir legen sie in den Warenkorb!*
