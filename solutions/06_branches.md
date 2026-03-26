# ============================================================
# ✅ Lösungen zu Lektion 6: Branches (Zweige)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 6.1:
## ────────────────────────────────────────────────────────────

```bash
git branch
```

```
Auf welchem Branch bist du? main (mit einem * davor markiert)

Ausgabe:
* main
```


## ────────────────────────────────────────────────────────────
## Lösung 6.2:
## ────────────────────────────────────────────────────────────

```bash
# Erstellen und Wechseln:
git checkout -b feature-test

# Prüfen:
git branch

# Ergebnis:
  main
* feature-test     ← Der Stern zeigt, dass du hier bist
```


## ────────────────────────────────────────────────────────────
## Lösung 6.3:
## ────────────────────────────────────────────────────────────

```bash
# Auf feature-test Branch:
echo "Mein Feature" > feature.txt
git add feature.txt
git commit -m "Feature-Datei erstellt"

# Zurück zu main wechseln:
git checkout main

# Prüfen:
ls
# → feature.txt ist NICHT da!
```

```
Existiert feature.txt auf main? Nein!

Warum nicht? Weil die Datei nur auf dem Branch "feature-test"
committed wurde. Branches sind voneinander getrennt – Änderungen
auf einem Branch sind auf anderen Branches nicht sichtbar,
bis sie zusammengeführt (gemerged) werden.
```


## ────────────────────────────────────────────────────────────
## Lösung 6.4:
## ────────────────────────────────────────────────────────────

```
a) "test"                        → SCHLECHT – zu ungenau, was wird getestet?
b) "feature-login-seite"         → GUT – beschreibt klar, woran gearbeitet wird
c) "asdf"                        → SCHLECHT – nichtssagend
d) "fix-fehler-bei-anmeldung"    → GUT – beschreibt genau den Bug-Fix
e) "mein-branch"                 → SCHLECHT – sagt nichts über den Inhalt aus
f) "update-readme-mit-anleitung" → GUT – klar und beschreibend
```
