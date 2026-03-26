# ============================================================
# 📖 Lektion 3: Dateien tracken (add & status)
# ============================================================
#
# Git überwacht nicht automatisch alle Dateien. Du musst Git
# erst sagen, welche Dateien es verfolgen soll. Das machst du
# mit "git add". Stell dir das wie eine Bühne vor:
# Erst stellst du Dateien auf die Bühne (Staging Area),
# dann machst du ein Foto davon (Commit).
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 3.1 Die drei Bereiche in Git
## ────────────────────────────────────────────────────────────

Git hat drei wichtige Bereiche:

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Working Dir     │────▶│  Staging Area   │────▶│   Repository    │
│  (Arbeitsordner) │     │  (Bühne)        │     │   (Gespeichert) │
│                  │     │                  │     │                  │
│  Hier arbeitest  │     │  Hier stehen     │     │  Hier ist alles │
│  du an Dateien   │     │  Dateien bereit  │     │  sicher         │
│                  │     │  zum Speichern   │     │  gespeichert    │
└─────────────────┘     └─────────────────┘     └─────────────────┘
       ▲                        ▲                        ▲
       │                        │                        │
   du bearbeitest           git add                  git commit
```

> 💡 **Merke:** Bevor du etwas speichern (committen) kannst, musst du es erst auf die Bühne stellen (adden)!


## ────────────────────────────────────────────────────────────
## 3.2 Dateien hinzufügen (git add)
## ────────────────────────────────────────────────────────────

### Eine einzelne Datei hinzufügen:

```bash
git add dateiname.txt
```

### Mehrere Dateien hinzufügen:

```bash
git add datei1.txt datei2.txt datei3.txt
```

### ALLE geänderten Dateien hinzufügen:

```bash
git add .
```

> ⚠️ **Achtung:** `git add .` fügt ALLES hinzu. Das ist bequem, aber sei vorsichtig, dass du nicht versehentlich Dateien hinzufügst, die du nicht willst!


## ────────────────────────────────────────────────────────────
## 3.3 Status prüfen (git status)
## ────────────────────────────────────────────────────────────

Mit `git status` siehst du immer, was gerade los ist:

```bash
git status
```

### Was die Farben bedeuten:

- 🔴 **Rot** = Datei wurde geändert, aber noch NICHT auf der Bühne (nicht ge-added)
- 🟢 **Grün** = Datei ist auf der Bühne und bereit zum Committen

### Beispiel:

```bash
# Du erstellst eine neue Datei oder via vs code sidebar
echo "Hallo Welt" > hallo.txt

git status
# → hallo.txt ist ROT (Untracked file – Git kennt die Datei noch nicht)

git add hallo.txt

git status
# → hallo.txt ist GRÜN (bereit zum Committen)
```


## ────────────────────────────────────────────────────────────
## 3.4 Dateien von der Bühne nehmen (git restore --staged)
## ────────────────────────────────────────────────────────────

Ups, du hast eine Datei ausversehen ge-added? Kein Problem:

```bash
git restore --staged dateiname.txt
```

Die Datei wird von der Bühne genommen, aber die Änderung bleibt erhalten!


## ────────────────────────────────────────────────────────────
## 3.5 Änderungen ansehen (git diff)
## ────────────────────────────────────────────────────────────

Du willst sehen, was du geändert hast?

```bash
git diff                  # Zeigt Änderungen die NICHT auf der Bühne sind
git diff --staged         # Zeigt Änderungen die auf der Bühne sind
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- Git hat 3 Bereiche: Working Directory → Staging Area → Repository
- `git add datei.txt` → Datei auf die Bühne stellen
- `git add .` → Alle Dateien auf die Bühne stellen
- `git status` → Zeigt den aktuellen Zustand (rot = nicht ge-added, grün = bereit)
- `git restore --staged datei.txt` → Datei von der Bühne nehmen
- `git diff` → Zeigt dir, was sich geändert hat
- **Immer zuerst `git status` prüfen!**
