# 3-1- Pull Requests (PRs) 📥

[🏠 Home](../../README.md) | [◀️ Zurück](./3-0-branches-verstehen.md) | [🔜 Nächstes Kapitel (Advanced)](../4-advanced/4--advanced-intro.md)

---

Ein **Pull Request** ist mehr als nur "Code mergen". Es ist ein Qualitäts-Gate. Hier schauen 4 Augen mehr als 2.

## Der "Knigge" für perfekte PRs 🎩

Wenn du bei lemueIO einen PR erstellst, achte auf folgendes:

1.  **Aussagekräftiger Titel:** Nicht "Update", sondern "feat: Add dark mode toggle".
2.  **Beschreibung:** Fülle das Template aus!
    *   *Was* wurde gemacht?
    *   *Warum*? (Link zum Ticket/Issue)
    *   *Wie* kann man es testen?
3.  **Selbst-Review:** Schau dir deine eigenen Änderungen ("Files changed") an, BEVOR du Kollegen taggst. Oft findest du selbst noch Typos oder vergessene `console.log`.

## Review & Feedback
Wenn ein Kollege schreibt: *"Bitte Variable X umbenennen"*, dann ist das kein Angriff.
*   Antworte höflich.
*   Diskutiere, wenn du anderer Meinung bist.
*   Setze die Änderung um und schreibe "Done" oder "Fixed".

## Merge Strategien: Wie kommt es zusammen?

Wenn der PR grün ist (Approved), gibt es meistens 3 Optionen beim Merge-Button.

### 1. Merge Commit (Der Standard)
Behält alle deine einzelnen Commits (`typo`, `fix`, `wip`).
*   *Vorteil:* Historie ist exakt.
*   *Nachteil:* Kann unübersichtlich werden ("Spaghetti-History").

### 2. Squash and Merge (Unsere Empfehlung ⭐)
Git nimmt alle deine 20 kleinen Commits und presst sie in **einen einzigen** sauberen Commit zusammen.
*   *Vorteil:* Der `main`-Branch bleibt extrem sauber und lesbar. "Ein Feature = Ein Commit".

---

## 😱 Hilfe, Merge Conflict!

Manchmal sagt GitHub: *"This branch has conflicts that must be resolved"*.
Das heißt: Jemand anderes hat genau die gleichen Zeilen geändert wie du. Git weiß nicht, welche Version stimmt.

**Was tun?**
Du musst das lokal lösen (wirklich!).
1.  `git checkout main`
2.  `git pull` (Main aktualisieren)
3.  `git checkout dein-feature`
4.  `git merge main`
5.  Jetzt knallt es. Öffne die Dateien mit `<<<< HEAD`, entscheide was bleibt, speichere.
6.  `git add .` und `git commit`.

Konflikt gelöst? Dann wieder `git push`.

---
*Du hast jetzt das Rüstzeug für echte Teamarbeit. Ab hier beginnt der Profi-Bereich: Automatisierung!*
