# ============================================================
# 📖 Lektion 4: Änderungen speichern (commit)
# ============================================================
#
# Ein Commit ist wie ein Foto deines Projekts zu einem
# bestimmten Zeitpunkt. Jeder Commit hat eine Nachricht,
# die beschreibt, WAS du geändert hast.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 4.1 Was ist ein Commit?
## ────────────────────────────────────────────────────────────

Ein **Commit** ist eine gespeicherte Änderung. Stell dir das so vor:

- Du arbeitest an einem Gemälde 🎨
- Ab und zu machst du ein **Foto** davon (= Commit)
- Wenn du später etwas vermasselt hast, kannst du zum letzten Foto zurückgehen

Jeder Commit enthält:
- ✅ Was wurde geändert (welche Dateien)
- ✅ Wer hat es geändert
- ✅ Wann wurde es geändert
- ✅ Eine Nachricht, die die Änderung beschreibt


## ────────────────────────────────────────────────────────────
## 4.2 Einen Commit erstellen
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1: Dateien auf die Bühne stellen
git add datei.txt

# Schritt 2: Commit erstellen mit Nachricht
git commit -m "Beschreibung der Änderung"
```

### Beispiel:

```bash
echo "Mein erstes Projekt" > README.md
git add README.md
git commit -m "README Datei erstellt"
```


## ────────────────────────────────────────────────────────────
## 4.3 Gute Commit-Nachrichten schreiben
## ────────────────────────────────────────────────────────────

Die Commit-Nachricht ist super wichtig! Sie soll kurz und klar beschreiben,
WAS du geändert hast.

### ✅ GUTE Commit-Nachrichten:

```bash
git commit -m "Login-Seite hinzugefügt"
git commit -m "Fehler bei der Passwort-Prüfung behoben"
git commit -m "README mit Installationsanleitung aktualisiert"
```

### ❌ SCHLECHTE Commit-Nachrichten:

```bash
git commit -m "update"           # Was wurde geupdated?
git commit -m "fix"              # Was wurde gefixt?
git commit -m "stuff"            # Was für stuff?
git commit -m "asdfjklö"         # 🤦
```

### Regeln für gute Commit-Nachrichten:

1. **Kurz und knapp** – maximal eine Zeile (ca. 50 Zeichen)
2. **Beschreibend** – Man soll verstehen, WAS geändert wurde
3. **Im Imperativ** – "Füge hinzu" statt "Hinzugefügt"
4. **Auf Englisch oder Deutsch** – Aber bleib bei einer Sprache!


## ────────────────────────────────────────────────────────────
## 4.4 Commit-Historie ansehen (git log)
## ────────────────────────────────────────────────────────────

Du willst sehen, welche Commits gemacht wurden?

```bash
git log
```

Das zeigt dir alle Commits mit:
- Commit-ID (ein langer Hash)
- Autor
- Datum
- Nachricht

### Kürzere Ansicht:

```bash
git log --oneline
```

Zeigt nur die Kurzversion:

```
a1b2c3d README Datei erstellt
e4f5g6h Login-Seite hinzugefügt
```


## ────────────────────────────────────────────────────────────
## 4.5 Der komplette Workflow
## ────────────────────────────────────────────────────────────

```bash
# 1. Dateien bearbeiten
# 2. Status prüfen
git status

# 3. Dateien auf die Bühne stellen
git add .

# 4. Commit erstellen
git commit -m "Beschreibung der Änderung"

# 5. Prüfen ob alles geklappt hat
git log --oneline
```

> 💡 **Tipp:** Committe oft und in kleinen Schritten! Lieber 10 kleine Commits als 1 riesiger.


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- Ein **Commit** ist ein Snapshot (Foto) deines Projekts
- `git commit -m "Nachricht"` → Änderungen speichern
- Schreibe **gute, beschreibende** Commit-Nachrichten
- `git log` → Zeigt die Commit-Historie
- `git log --oneline` → Kürzere Ansicht
- **Workflow:** bearbeiten → `git status` → `git add` → `git commit`
