# ============================================================
# 📖 Lektion 11: Rebase (Grundlagen)
# ============================================================
#
# Rebase ist eine Methode, um deinen Branch auf den neuesten
# Stand von main zu bringen. Es "verschiebt" deine Commits
# so, als hättest du erst jetzt angefangen zu arbeiten.
#
# Keine Sorge – GitHub macht das meiste für uns!
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 11.1 Was ist Rebase?
## ────────────────────────────────────────────────────────────

Stell dir vor, du hast angefangen zu arbeiten, während jemand anderes
auch Änderungen in `main` gemacht hat:

### Vorher (dein Branch ist "veraltet"):

```
main:          ●──●──●──●──●     (neue Commits von anderen)
                    \
dein-branch:        ●──●         (deine Commits)
```

### Nach einem Rebase:

```
main:          ●──●──●──●──●
                              \
dein-branch:                   ●──●    (deine Commits sind jetzt "obendrauf")
```

> 💡 **Merke:** Rebase "verschiebt" deine Commits ans Ende von main. Es sieht so aus, als hättest du erst jetzt angefangen.


## ────────────────────────────────────────────────────────────
## 11.2 Warum Rebase?
## ────────────────────────────────────────────────────────────

- ✅ Dein Branch ist immer auf dem **neuesten Stand**
- ✅ Die **Historie bleibt sauber** und linear (kein Zickzack)
- ✅ **Konflikte** werden früh erkannt und gelöst
- ✅ Dein **Pull Request** ist leichter zu reviewen


## ────────────────────────────────────────────────────────────
## 11.3 Wie macht man einen Rebase?
## ────────────────────────────────────────────────────────────

```bash
# 1. Sicherstellen, dass main aktuell ist
git checkout main
git pull origin main

# 2. Zurück zu deinem Branch wechseln
git checkout mein-branch

# 3. Rebase auf main
git rebase main
```

### Wenn alles gut geht:

```
Successfully rebased and updated refs/heads/mein-branch.
```

### Wenn es Konflikte gibt:

```bash
# Git zeigt dir, wo der Konflikt ist
# 1. Öffne die Datei und löse den Konflikt
# 2. Datei auf die Bühne stellen
git add datei.txt

# 3. Rebase fortsetzen
git rebase --continue
```

### Rebase abbrechen (wenn du unsicher bist):

```bash
git rebase --abort
```

> ⚠️ Das macht alles rückgängig – kein Schaden passiert!


## ────────────────────────────────────────────────────────────
## 11.4 Rebase vs. Merge
## ────────────────────────────────────────────────────────────

| | Rebase | Merge |
|---|--------|-------|
| **Historie** | Linear und sauber | Zeigt alle Verzweigungen |
| **Einfachheit** | Etwas komplizierter | Einfacher |
| **Wann?** | Branch aktualisieren | Branches zusammenführen |

Für den Alltag:
- **Rebase** → Um deinen Branch auf den neuesten Stand von main zu bringen
- **Merge** → Um Branches zusammenzuführen (passiert meistens über PR auf GitHub)


## ────────────────────────────────────────────────────────────
## 11.5 Push nach Rebase
## ────────────────────────────────────────────────────────────

Nach einem Rebase musst du mit **Force Push** hochladen, weil sich die
Commit-Geschichte geändert hat:

```bash
git push --force-with-lease origin mein-branch
```

> ⚠️ **Wichtig:** Benutze `--force-with-lease` statt `--force`!
> Das ist sicherer, weil es prüft, ob jemand anderes in der Zwischenzeit
> etwas auf dem Branch geändert hat.

> 🚫 **NIEMALS** einen Force Push auf `main` machen! Nur auf deinem eigenen Branch.


## ────────────────────────────────────────────────────────────
## 11.6 GitHub macht es einfach
## ────────────────────────────────────────────────────────────

Die gute Nachricht: GitHub bietet bei Pull Requests die Option
**"Rebase and merge"** an. Das macht den Rebase automatisch für dich!

Beim Mergen eines Pull Requests auf GitHub hast du drei Optionen:
1. **Create a merge commit** – Normaler Merge
2. **Squash and merge** – Alle Commits zu einem zusammenfassen
3. **Rebase and merge** – Rebase automatisch durchführen


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- **Rebase** verschiebt deine Commits ans Ende von main
- Das hält die Git-Historie sauber und linear
- `git rebase main` → Deinen Branch auf den neuesten Stand bringen
- Bei Konflikten: Lösen → `git add` → `git rebase --continue`
- `git rebase --abort` → Alles rückgängig machen (Notbremse!)
- Nach Rebase: `git push --force-with-lease` (nur auf deinem Branch!)
- GitHub bietet "Rebase and merge" bei Pull Requests an
