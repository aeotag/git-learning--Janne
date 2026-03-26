# ============================================================
# 📖 Lektion 12: Git im Alltag (Tipps & Tricks)
# ============================================================
#
# In dieser letzten Lektion lernst du nützliche Befehle und
# Tipps, die dir den Alltag mit Git erleichtern.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 12.1 Änderungen rückgängig machen
## ────────────────────────────────────────────────────────────

### Datei zurücksetzen (noch nicht committed):

```bash
# Eine Datei auf den letzten Commit-Stand zurücksetzen
git restore datei.txt

# ALLE Änderungen rückgängig machen
git restore .
```

### Letzten Commit rückgängig machen:

```bash
# Commit rückgängig, aber Änderungen behalten (auf der Bühne)
git reset --soft HEAD~1

# Commit rückgängig, Änderungen behalten (nicht auf der Bühne)
git reset HEAD~1

# ⚠️ Commit UND Änderungen komplett löschen (VORSICHT!)
git reset --hard HEAD~1
```

> 💡 `HEAD~1` bedeutet "ein Commit zurück". `HEAD~3` wäre drei Commits zurück.


## ────────────────────────────────────────────────────────────
## 12.2 Stash – Änderungen zwischenspeichern
## ────────────────────────────────────────────────────────────

Manchmal musst du den Branch wechseln, aber du hast noch unfertige
Änderungen. Mit **Stash** kannst du sie kurz zur Seite legen:

```bash
# Änderungen zwischenspeichern
git stash

# Andere Sachen machen, Branch wechseln, etc.
git checkout main
# ...
git checkout mein-branch

# Änderungen wieder zurückholen
git stash pop
```

### Stash anzeigen:

```bash
# Alle Stashes anzeigen
git stash list

# Stash anwenden, aber behalten
git stash apply
```

> 💡 Stell dir Stash wie eine Schublade vor, in die du schnell etwas reinlegst, um es später weiterzumachen.


## ────────────────────────────────────────────────────────────
## 12.3 .gitignore – Dateien ignorieren
## ────────────────────────────────────────────────────────────

Nicht alle Dateien sollen von Git verfolgt werden (z.B. Passwörter,
temporäre Dateien). Dafür gibt es die `.gitignore`-Datei:

Erstelle eine Datei namens `.gitignore` im Hauptordner:

```bash
# Beispiel .gitignore:

# Temporäre Dateien
*.tmp
*.log

# Betriebssystem-Dateien
.DS_Store
Thumbs.db

# Passwörter und Geheimnisse
.env
secrets.yaml

# Build-Ordner
node_modules/
__pycache__/
```

> 💡 Erstelle die `.gitignore`-Datei **ganz am Anfang** deines Projekts!


## ────────────────────────────────────────────────────────────
## 12.4 Nützliche Git-Befehle
## ────────────────────────────────────────────────────────────

```bash
# Die letzten 5 Commits anzeigen
git log --oneline -5

# Zeigt, wer welche Zeile geschrieben hat
git blame datei.txt

# Zeigt eine schöne Grafik der Branches
git log --oneline --graph --all

# Zeigt die Änderungen eines bestimmten Commits
git show commit-id

# Datei aus einem anderen Branch holen
git checkout anderer-branch -- datei.txt
```


## ────────────────────────────────────────────────────────────
## 12.5 Git Aliases – Abkürzungen
## ────────────────────────────────────────────────────────────

Du kannst dir Abkürzungen für häufige Befehle erstellen:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
git config --global alias.lg "log --oneline --graph --all"
```

Jetzt kannst du:

```bash
git st          # statt: git status
git co main     # statt: git checkout main
git br          # statt: git branch
git cm "msg"    # statt: git commit -m "msg"
git lg          # statt: git log --oneline --graph --all
```


## ────────────────────────────────────────────────────────────
## 12.6 Der komplette tägliche Workflow
## ────────────────────────────────────────────────────────────

Hier ist der komplette Workflow, den du jeden Tag benutzen wirst:

```bash
# 1. ☀️ Morgens: Neuesten Stand holen
git checkout main
git pull origin main

# 2. 🌿 Neuen Branch für deine Aufgabe erstellen
git checkout -b feature-meine-aufgabe

# 3. 💻 Arbeiten: Dateien bearbeiten...

# 4. 📸 Änderungen committen (atomic commits!)
git add betroffene-datei.txt
git commit -m "Klare Beschreibung der Änderung"

# 5. 🔄 Branch auf neuesten Stand bringen (optional aber empfohlen)
git fetch origin main
git rebase origin/main

# 6. 🚀 Branch auf GitHub pushen
git push -u origin feature-meine-aufgabe

# 7. 🔍 Pull Request auf GitHub erstellen
# → Reviewer zuweisen
# → Auf Feedback warten

# 8. ✅ Nach dem Merge: Aufräumen
git checkout main
git pull origin main
git branch -d feature-meine-aufgabe
```


## ────────────────────────────────────────────────────────────
## 12.7 Häufige Fehler und Lösungen
## ────────────────────────────────────────────────────────────

| Problem | Lösung |
|---------|--------|
| "Ich habe auf main committed!" | `git reset HEAD~1` und dann auf einem neuen Branch committen |
| "Ich habe die falsche Datei ge-added!" | `git restore --staged datei.txt` |
| "Mein Push wird abgelehnt!" | `git pull` zuerst, dann nochmal `git push` |
| "Ich bin auf dem falschen Branch!" | `git stash`, dann Branch wechseln, dann `git stash pop` |
| "Ich will meinen letzten Commit ändern!" | `git commit --amend -m "Neue Nachricht"` |


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- `git restore` → Änderungen rückgängig machen
- `git reset` → Commits rückgängig machen
- `git stash` → Änderungen zwischenspeichern
- `.gitignore` → Dateien von Git ausschließen
- `git log --oneline --graph --all` → Schöne Übersicht
- Git Aliases sparen dir Tipparbeit
- **Der tägliche Workflow:** pull → branch → arbeiten → commit → push → PR → review → merge

---

> 🎉 **Glückwunsch!** Du hast den Git-Kurs durchgearbeitet! Du kennst jetzt alle wichtigen Grundlagen, um mit Git im Team zu arbeiten. Übung macht den Meister – je öfter du Git benutzt, desto natürlicher wird es sich anfühlen! 💪
