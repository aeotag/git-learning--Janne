# ============================================================
# ✅ Lösungen zu Lektion 12: Git im Alltag (Tipps & Tricks)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 12.1:
## ────────────────────────────────────────────────────────────

```bash
# Befehl für eine Datei:
git restore datei.txt

# Befehl für alle Dateien:
git restore .
```


## ────────────────────────────────────────────────────────────
## Lösung 12.2:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1 (Änderungen zwischenspeichern):
git stash

# Schritt 2 (Branch wechseln):
git checkout anderer-branch
# ... dort arbeiten ...

# Schritt 3 (zurückwechseln und Änderungen zurückholen):
git checkout mein-branch
git stash pop
```


## ────────────────────────────────────────────────────────────
## Lösung 12.3:
## ────────────────────────────────────────────────────────────

Inhalt der `.gitignore`:

```
# Log-Dateien
*.log

# Node.js Abhängigkeiten
node_modules/

# Umgebungsvariablen (Geheimnisse!)
.env

# Temporäre Dateien
*.tmp
```


## ────────────────────────────────────────────────────────────
## Lösung 12.4:
## ────────────────────────────────────────────────────────────

```bash
# 1. Morgens - Neuesten Stand holen:
git checkout main
git pull origin main

# 2. Neuen Branch erstellen:
git checkout -b feature-meine-aufgabe

# 3. Arbeiten und committen (atomic commits!):
git add betroffene-datei.txt
git commit -m "Klare Beschreibung der Änderung"

# 4. Branch auf GitHub hochladen:
git push -u origin feature-meine-aufgabe

# 5. Was machst du auf GitHub?
# Einen Pull Request erstellen, Titel und Beschreibung schreiben,
# einen Reviewer zuweisen und auf Feedback warten.

# 6. Was passiert nach dem Merge?
git checkout main
git pull origin main
git branch -d feature-meine-aufgabe
# → Zurück zu main wechseln, neuesten Stand holen,
#   alten Branch löschen. Fertig! 🎉
```
