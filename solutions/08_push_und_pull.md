# ============================================================
# ✅ Lösungen zu Lektion 8: Push & Pull
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 8.1:
## ────────────────────────────────────────────────────────────

```
git push: Lädt deine Commits (Änderungen) von deinem PC auf
GitHub hoch, damit andere sie sehen und herunterladen können.

git pull: Lädt die neuesten Änderungen von GitHub auf deinen PC
herunter und baut sie automatisch in deinen Code ein.
```


## ────────────────────────────────────────────────────────────
## Lösung 8.2:
## ────────────────────────────────────────────────────────────

```bash
git push -u origin feature-neu
```

```
Warum "-u"?
Das "-u" (upstream) merkt sich die Verbindung zwischen deinem lokalen
Branch und dem Branch auf GitHub. Danach reicht ein einfaches "git push"
ohne weitere Angaben, weil Git jetzt weiß, wohin es pushen soll.
```


## ────────────────────────────────────────────────────────────
## Lösung 8.3:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1: Neuesten Stand holen
git checkout main
git pull origin main

# Schritt 2: Neuen Branch erstellen
git checkout -b feature-meine-aufgabe

# Schritt 3: Arbeiten (Dateien bearbeiten)

# Schritt 4: Änderungen auf die Bühne stellen
git add betroffene-datei.txt

# Schritt 5: Commit erstellen
git commit -m "Klare Beschreibung der Änderung"

# Schritt 6: Auf GitHub hochladen
git push -u origin feature-meine-aufgabe
```


## ────────────────────────────────────────────────────────────
## Lösung 8.4:
## ────────────────────────────────────────────────────────────

```
Was ist passiert?
Jemand anderes hat vor dir Änderungen auf GitHub hochgeladen.
Dein lokaler Stand ist veraltet und GitHub lehnt den Push ab,
weil sonst die Änderungen der anderen Person verloren gehen würden.

Was musst du tun?
Zuerst "git pull origin main" ausführen, um die Änderungen der
anderen Person herunterzuladen. Eventuelle Konflikte lösen.
Danach nochmal "git push origin main" versuchen.
```
