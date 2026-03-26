# ============================================================
# 📖 Lektion 5: Atomic Commits
# ============================================================
#
# Ein "Atomic Commit" bedeutet, dass jeder Commit genau
# EINE Sache macht – nicht mehr und nicht weniger.
# Das ist eine der wichtigsten Gewohnheiten für gutes
# Arbeiten mit Git!
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 5.1 Was ist ein Atomic Commit?
## ────────────────────────────────────────────────────────────

"Atomic" kommt vom griechischen Wort "atomos" = unteilbar.

Ein **Atomic Commit** ist ein Commit, der:
- ✅ Genau **eine logische Änderung** enthält
- ✅ In sich abgeschlossen ist (nichts fehlt, nichts ist kaputt)
- ✅ Eine klare Commit-Nachricht hat

> 💡 **Merke:** Ein Commit = Eine Sache. Nicht mehr, nicht weniger.


## ────────────────────────────────────────────────────────────
## 5.2 Warum sind Atomic Commits wichtig?
## ────────────────────────────────────────────────────────────

Stell dir vor, du hast diesen einen großen Commit:

```
"Login-Seite gebaut, Farben geändert, Bug gefixt, README aktualisiert"
```

Probleme dabei:
- ❌ Wenn der Bug-Fix falsch war, musst du ALLES rückgängig machen
- ❌ Niemand versteht, was genau passiert ist
- ❌ Code Review wird zum Albtraum

### Besser – Atomic Commits:

```bash
git commit -m "Login-Formular erstellt"
git commit -m "Hintergrundfarbe auf Blau geändert"
git commit -m "Fehler bei E-Mail-Prüfung behoben"
git commit -m "README mit Login-Anleitung ergänzt"
```

Jetzt kann man:
- ✅ Jeden Schritt einzeln verstehen
- ✅ Einzelne Änderungen rückgängig machen
- ✅ Code Review ist einfach und klar


## ────────────────────────────────────────────────────────────
## 5.3 Wie macht man Atomic Commits?
## ────────────────────────────────────────────────────────────

### Regel: Arbeite an EINER Sache, dann committe!

```bash
# Schritt 1: Eine Sache machen (z.B. neue Datei erstellen)
echo "# Mein Projekt" > README.md

# Schritt 2: NUR diese Änderung auf die Bühne stellen
git add README.md

# Schritt 3: Committen mit klarer Nachricht
git commit -m "README Datei erstellt"

# Schritt 4: Nächste Sache machen...
```

### Einzelne Dateien gezielt adden:

Wenn du mehrere Dateien geändert hast, aber sie zu verschiedenen
Änderungen gehören:

```bash
# NICHT git add . verwenden!
# Stattdessen gezielt adden:

git add login.html
git commit -m "Login-Formular erstellt"

git add styles.css
git commit -m "Hintergrundfarbe auf Blau geändert"
```


## ────────────────────────────────────────────────────────────
## 5.4 Faustregeln für Atomic Commits
## ────────────────────────────────────────────────────────────

1. **Kann ich die Änderung in einem kurzen Satz beschreiben?**
   - ✅ Ja → Guter Commit!
   - ❌ Nein, ich brauche "und" → Aufteilen!

2. **Würde der Code nach diesem Commit funktionieren?**
   - ✅ Ja → Guter Commit!
   - ❌ Nein → Noch nicht committen, erst fertig machen!

3. **Gehören alle Änderungen zum selben Thema?**
   - ✅ Ja → Guter Commit!
   - ❌ Nein → In mehrere Commits aufteilen!


## ────────────────────────────────────────────────────────────
## 5.5 Beispiel: Guter vs. Schlechter Workflow
## ────────────────────────────────────────────────────────────

### ❌ Schlechter Workflow:

```bash
# 3 Stunden lang an verschiedenen Sachen arbeiten...
git add .
git commit -m "Viele Änderungen"
```

### ✅ Guter Workflow:

```bash
# 1. Feature bauen
git add feature.py
git commit -m "Suchfunktion implementiert"

# 2. Bug fixen
git add utils.py
git commit -m "Fehler bei Datumsformatierung behoben"

# 3. Doku aktualisieren
git add README.md
git commit -m "Suchfunktion in README dokumentiert"
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- **Atomic Commit** = Ein Commit macht genau EINE Sache
- Jeder Commit soll in sich abgeschlossen sein (nichts kaputt)
- Lieber viele kleine Commits als ein riesiger
- Benutze `git add datei.txt` statt `git add .` wenn nötig
- Frage dich: "Kann ich das in einem Satz beschreiben?"
- Gute Atomic Commits machen Teamarbeit und Code Review viel einfacher!
