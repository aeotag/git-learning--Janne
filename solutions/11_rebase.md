# ============================================================
# ✅ Lösungen zu Lektion 11: Rebase (Grundlagen)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 11.1:
## ────────────────────────────────────────────────────────────

```
"git rebase" verschiebt die eigenen Commits ans Ende von main,
sodass es aussieht, als hätte man erst jetzt angefangen zu arbeiten.
Das ist nützlich, weil die Git-Historie sauber und übersichtlich bleibt
und Konflikte früh erkannt werden.
```


## ────────────────────────────────────────────────────────────
## Lösung 11.2:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1 (main updaten):
git checkout main
git pull origin main

# Schritt 2 (zu deinem Branch wechseln):
git checkout feature-xyz

# Schritt 3 (rebase):
git rebase main
```


## ────────────────────────────────────────────────────────────
## Lösung 11.3:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1 (Konflikt lösen):
# Die betroffene Datei öffnen und die Konflikte manuell lösen
# (die <<<<<<, ======, >>>>>> Markierungen entfernen und
# die richtige Version behalten)

# Schritt 2 (Datei adden):
git add datei-mit-konflikt.txt

# Schritt 3 (Rebase fortsetzen):
git rebase --continue

# Befehl zum Abbrechen:
git rebase --abort
```


## ────────────────────────────────────────────────────────────
## Lösung 11.4:
## ────────────────────────────────────────────────────────────

```bash
git push --force-with-lease origin feature-xyz
```

```
Warum reicht normaler push nicht?
Weil der Rebase die Commit-Geschichte verändert hat. Die Commits
auf GitHub und die lokalen Commits passen nicht mehr zusammen.
Git denkt, du hättest Commits "verloren" und lehnt den normalen
Push ab. Mit --force-with-lease sagst du Git: "Ich weiß was ich
tue, überschreibe die alte Version." --force-with-lease ist
sicherer als --force, weil es prüft, ob jemand anderes in der
Zwischenzeit etwas geändert hat.
```
