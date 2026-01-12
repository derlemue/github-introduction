# 3-0- Branches verstehen 🌿

[🏠 Home](../../README.md) | [◀️ Zurück](./3--kollaboration-intro.md) | [▶️ Nächstes: Pull Requests](./3-1-pull-requests.md)

---

## Warum nicht einfach alles auf `main`?

Stell dir `main` als die Live-Version deiner Webseite vor. Wenn du dort einen Fehler machst (z.B. ein Komma löschst), stürzt die Seite für alle Besucher ab. 💥

Deshalb arbeiten wir auf **Branches** (Ästen).

### Visualisierung

```text
main:      O ─── O ─── O ─── O  (Sauber & Stabil)
                 \
feature-x:        A ─── B ─── C  (Deine Baustelle)
```

Du zweigst bei Commit `O` ab, baust deine Commits `A`, `B` und `C`. Währenddessen funktioniert `main` weiter perfekt. Erst am Ende führen wir `C` wieder zurück zu `main`.

---

## Die Praxis: Branching in 3 Schritten

### 1. Erstellen & Wechseln (Switch)
Früher nutzte man `checkout`, heute ist der Befehl `switch` moderner und verständlicher.

```bash
# Erstellt (-c = create) einen Branch und wechselt sofort hin
git switch -c feature/neues-design
```

> **💡 Best Practice:** Nutze sprechende Namen!
> *   `feature/login-page`
> *   `fix/header-bug`
> *   `docs/readme-update`
> Vermeide Namen wie `test` oder `michaels-branch`.

### 2. Arbeiten
Du änderst Dateien, addest und committest wie gewohnt.
Der Clou: Wenn du jetzt `ls` (Dateien anzeigen) machst, siehst du deine neuen Dateien.

Wechsle spaßeshalber zurück zu main:
```bash
git switch main
```
😱 **Schreck:** Deine Dateien sind weg!
😅 **Entwarnung:** Sie sind nicht weg, nur im anderen Branch. Git tauscht die Dateien auf deiner Festplatte blitzschnell aus, je nachdem, in welchem Branch du bist.

### 3. Hochladen (Push)
Ein neuer Branch existiert erst mal nur lokal. GitHub kennt ihn nicht.

```bash
git push -u origin feature/neues-design
```

Das `-u` (upstream) ist wichtig beim ersten Mal: Es sagt Git, dass dieser lokale Branch fest mit dem Branch auf GitHub verbunden sein soll. Danach reicht ein einfaches `git push`.

---
*Dein Branch ist live auf GitHub. Aber wie kommt er jetzt in den sicheren Hafen (main)? Das klären wir im nächsten Schritt.*
