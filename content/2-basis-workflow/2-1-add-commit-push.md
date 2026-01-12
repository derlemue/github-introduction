# 2-1- Add, Commit, Push 📦

[🏠 Home](../../README.md) | [◀️ Zurück](./2-0-clone-und-status.md) | [▶️ Nächstes: Kollaboration](../3-kollaboration/3--kollaboration-intro.md)

---

Dieser Dreischritt ist dein tägliches Brot. Verstehe ihn einmal richtig, und du wirst nie wieder Probleme haben.

## 1. Add: Der Einkaufswagen (Staging) 🛒

Du hast Änderungen gemacht (Dateien sind **rot** in `git status`). Bevor du sie "kaufst", musst du sie in den Einkaufswagen legen.

```bash
git add dateiname.md
# Oder für Faule (alles hinzufügen):
git add .
```

*Warum dieser Zwischenschritt?*
Vielleicht hast du an 3 Dateien gearbeitet, willst aber nur 2 davon hochladen, weil die dritte noch experimentell ist. Mit der Staging-Area hast du die volle Kontrolle.

---

## 2. Commit: Der Kaufvertrag 📝

Jetzt wird es ernst. Ein **Commit** ist ein Schnappschuss deiner Änderungen, versehen mit einer Nachricht und deinem Namen. Es ist wie das Bezahlen an der Kasse: Du bekommst einen Kassenbon (Hash-ID).

```bash
git commit -m "feat: neues kapitel zur installation hinzugefügt"
```

### Die Kunst der Commit-Message
Eine gute Message erklärt das **WAS** und das **WARUM**.
*   ❌ *Schlecht:* "fix", "update", "asdf"
*   ✅ *Gut:* "fix: login button alignment crash on mobile"

> **💡 Pro-Tipp:** Wir bei lemueIO nutzen oft "Conventional Commits" (Prefixe wie `feat:`, `fix:`, `docs:`, `chore:`). Das hilft uns später, automatisch Changelogs zu generieren!

---

## 3. Push: Der Upload 🚀

Bisher ist alles nur auf **deinem** Computer passiert. Wenn deine Festplatte morgen kaputt geht, ist alles weg. Ein `commit` speichert nur lokal!

Um es sicher zu `origin` (GitHub Server) zu bringen:

```bash
git push
```

### ⚠️ Achtung: "Rejected - non-fast-forward"?
Das passiert, wenn jemand anderes (z.B. ein Kollege) in der Zwischenzeit etwas gepusht hat. Du darfst deine Änderungen nicht einfach drüberbügeln.

**Lösung:** Erst holen, dann senden.
```bash
git pull      # Hol dir die Änderungen der anderen
git push      # Jetzt darfst du deine drauflegen
```

---
*Damit hast du den Basic Loop gemeistert! Jetzt lass uns schauen, wie wir arbeiten, ohne uns gegenseitig zu überschreiben.*
