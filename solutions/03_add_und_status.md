# ============================================================
# ✅ Lösungen zu Lektion 3: Dateien tracken (add & status)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 3.1:
## ────────────────────────────────────────────────────────────

```bash
cd test-repo
echo "Hallo Welt!" > hallo.txt
git status
```

```
Farbe der Datei: Rot

Was bedeutet das: Die Datei ist "untracked" – Git kennt sie noch
nicht und sie wurde noch nicht zur Staging Area (Bühne) hinzugefügt.
```


## ────────────────────────────────────────────────────────────
## Lösung 3.2:
## ────────────────────────────────────────────────────────────

```bash
git add hallo.txt
git status
```

```
Farbe der Datei jetzt: Grün

Die Datei ist jetzt auf der Staging Area (Bühne) und bereit
zum Committen.
```


## ────────────────────────────────────────────────────────────
## Lösung 3.3:
## ────────────────────────────────────────────────────────────

```bash
echo "Inhalt 1" > datei1.txt
echo "Inhalt 2" > datei2.txt
git add datei1.txt
git status
```

```
Welche Datei ist grün? datei1.txt (wurde ge-added)
Welche Datei ist rot? datei2.txt (wurde NICHT ge-added)
```


## ────────────────────────────────────────────────────────────
## Lösung 3.4:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1 - Alles adden (der "Fehler"):
git add .

# Schritt 2 - datei2.txt von der Bühne nehmen:
git restore --staged datei2.txt

# Schritt 3 - Status prüfen:
git status
# → datei1.txt ist grün (auf der Bühne)
# → datei2.txt ist rot (nicht mehr auf der Bühne, aber die Datei existiert noch)
```
