# ============================================================
# ✅ Lösungen zu Lektion 9: Fetch
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 9.1:
## ────────────────────────────────────────────────────────────

```
"git fetch" lädt die Änderungen von GitHub nur herunter, baut sie
aber NICHT in deinen Code ein. Deine Dateien bleiben unverändert.
"git pull" macht beides: herunterladen UND einbauen.
Fetch ist also die vorsichtigere Variante, weil man erst schauen
kann, was sich geändert hat, bevor man es übernimmt.
```


## ────────────────────────────────────────────────────────────
## Lösung 9.2:
## ────────────────────────────────────────────────────────────

```
| Befehl      | Herunterladen | Einbauen |
|-------------|:------------:|:--------:|
| git fetch   |      ✅      |    ❌    |
| git pull    |      ✅      |    ✅    |
```


## ────────────────────────────────────────────────────────────
## Lösung 9.3:
## ────────────────────────────────────────────────────────────

```bash
# Befehl 1 (herunterladen ohne einzubauen):
git fetch origin

# Befehl 2 (Historie anschauen):
git log origin/main --oneline

# Befehl 3 (Unterschiede anzeigen):
git diff main origin/main
```


## ────────────────────────────────────────────────────────────
## Lösung 9.4:
## ────────────────────────────────────────────────────────────

```
Beispiel 1:
Wenn ich in einem großen Projekt arbeite und erst schauen will,
was andere geändert haben, bevor ich meine Dateien verändere.
So kann ich prüfen, ob es Konflikte geben könnte.

Beispiel 2:
Wenn ich gerade mitten in der Arbeit bin und nicht will, dass
sich meine Dateien plötzlich ändern. Mit fetch kann ich die
Informationen holen und sie später in Ruhe einbauen.
```
