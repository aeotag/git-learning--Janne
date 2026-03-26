# ============================================================
# ✅ Lösungen zu Lektion 5: Atomic Commits
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 5.1:
## ────────────────────────────────────────────────────────────

```
Ein Atomic Commit ist ein Commit, der genau eine einzige logische
Änderung enthält – nicht mehr und nicht weniger. Er ist wichtig,
weil man so einzelne Änderungen leicht verstehen, rückgängig machen
und im Code Review prüfen kann.
```


## ────────────────────────────────────────────────────────────
## Lösung 5.2:
## ────────────────────────────────────────────────────────────

```
Commit 1: "Startseite erstellt"
Commit 2: "Farben angepasst"
Commit 3: "Tippfehler korrigiert"
Commit 4: "README aktualisiert"
```


## ────────────────────────────────────────────────────────────
## Lösung 5.3:
## ────────────────────────────────────────────────────────────

```bash
echo "<h1>Hallo</h1>" > seite.html
git add seite.html
git commit -m "HTML-Startseite erstellt"

echo "body { color: blue; }" > stil.css
git add stil.css
git commit -m "CSS-Datei mit Grundstil erstellt"

echo "Das ist ein Testprojekt." > info.txt
git add info.txt
git commit -m "Info-Datei mit Projektbeschreibung erstellt"
```


## ────────────────────────────────────────────────────────────
## Lösung 5.4:
## ────────────────────────────────────────────────────────────

```
a) NEIN – Wenn die Nachricht "und" enthält, macht der Commit
   wahrscheinlich zu viele Dinge auf einmal. Dann sollte man
   ihn aufteilen.

b) NEIN – Ein Commit sollte immer in sich abgeschlossen sein.
   Der Code sollte nach jedem Commit funktionieren.

c) JA – Viele kleine Commits sind besser als ein großer,
   weil man so einzelne Änderungen besser verstehen und
   bei Bedarf rückgängig machen kann.
```
