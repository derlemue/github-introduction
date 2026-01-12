# 3-0- Branches verstehen & nutzen 🌿

[🏠 Home](../../README.md) | [◀️ Zurück](./3--kollaboration-intro.md) | [▶️ Nächstes: Pull Requests](./3-1-pull-requests.md)

---

## Was ist ein Branch?

Ein **Branch** ist wie ein Speicherstand in einem Videospiel, den du kopierst, um ein riskantes Level auszuprobieren. Wenn du stirbst (Code kaputt machst), lädst du einfach den alten Speicherstand (`main`) wieder.

## Die Befehle

### 1. Einen neuen Branch erstellen

Wir erstellen einen Branch namens `feature/neue-seite` und wechseln sofort hinein.

```bash
git checkout -b feature/neue-seite
```

(Der Schalter `-b` steht für "create branch".)

### 2. Arbeiten

Jetzt kannst du Dateien ändern, löschen oder hinzufügen. Alles passiert nur in diesem Branch! Der `main`-Branch bleibt unberührt.

Führe wie gewohnt deine Speicher-Befehle aus:

```bash
git add .
git commit -m "Neue Seite erstellt"
```

### 3. Zurückwechseln (optional)

Willst du sehen, wie es vorher aussah? Wechsel zurück zum Hauptstrang:

```bash
git checkout main
```

Deine Änderungen sind jetzt "weg" (aber sicher im anderen Branch gespeichert).

### 4. Branch hochladen

Das erste Mal Hochladen eines neuen Branches braucht einen speziellen Befehl:

```bash
git push -u origin feature/neue-seite
```

(Das `-u` verknüpft deinen lokalen Branch mit dem auf GitHub).
