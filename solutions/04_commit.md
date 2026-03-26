# ============================================================
# ✅ Lösungen zu Lektion 4: Änderungen speichern (commit)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 4.1:
## ────────────────────────────────────────────────────────────

```bash
echo "# Mein Test-Projekt" > README.md
git add README.md
git commit -m "README Datei erstellt"
```


## ────────────────────────────────────────────────────────────
## Lösung 4.2:
## ────────────────────────────────────────────────────────────

```
a) "update"                → SCHLECHT – Man weiß nicht, was geupdated wurde
b) "Login-Formular..."     → GUT – Klar und beschreibend
c) "fix"                   → SCHLECHT – Man weiß nicht, was gefixt wurde
d) "Fehler bei..."         → GUT – Beschreibt genau, was behoben wurde
e) "asdfgh"                → SCHLECHT – Komplett nichtssagend
f) "README mit..."         → GUT – Man weiß genau, was geändert wurde
```


## ────────────────────────────────────────────────────────────
## Lösung 4.3:
## ────────────────────────────────────────────────────────────

```bash
echo "Notizen" > notizen.txt
git add notizen.txt
git commit -m "Notizen-Datei erstellt"

echo "Kontakte" > kontakte.txt
git add kontakte.txt
git commit -m "Kontakte-Datei erstellt"

# Historie anzeigen:
git log --oneline
```

Ausgabe (Beispiel):
```
b3c4d5e Kontakte-Datei erstellt
a1b2c3d Notizen-Datei erstellt
f6g7h8i README Datei erstellt
```


## ────────────────────────────────────────────────────────────
## Lösung 4.4:
## ────────────────────────────────────────────────────────────

```
Schritt 1: git status              (prüfen, was geändert wurde)
Schritt 2: git add datei.txt       (Datei auf die Bühne stellen)
Schritt 3: git commit -m "Nachricht"  (Änderung speichern)
Schritt 4: git log --oneline       (prüfen, ob der Commit da ist)
```
