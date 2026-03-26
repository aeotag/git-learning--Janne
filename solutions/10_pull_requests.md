# ============================================================
# ✅ Lösungen zu Lektion 10: Pull Requests & Code Review
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 10.1:
## ────────────────────────────────────────────────────────────

```
Ein Pull Request ist eine Anfrage auf GitHub, den eigenen Code in
den main-Branch zu übernehmen. Wir brauchen ihn, damit eine zweite
Person den Code vorher überprüfen kann (Code Review). So werden
Fehler früh gefunden und die Code-Qualität bleibt hoch.
Außerdem lernt man voneinander, wenn man sich gegenseitig Feedback gibt.
```


## ────────────────────────────────────────────────────────────
## Lösung 10.2:
## ────────────────────────────────────────────────────────────

```
Schritt 1 (Terminal): git checkout -b feature-neue-funktion
Schritt 2 (Terminal): Dateien bearbeiten, git add .
Schritt 3 (Terminal): git commit -m "Neue Funktion implementiert"
Schritt 4 (Terminal): git push -u origin feature-neue-funktion
Schritt 5 (GitHub):   Auf "Compare & pull request" klicken
Schritt 6 (GitHub):   Titel, Beschreibung schreiben und Reviewer zuweisen
Schritt 7 (GitHub):   Nach Freigabe auf "Merge pull request" klicken
```


## ────────────────────────────────────────────────────────────
## Lösung 10.3:
## ────────────────────────────────────────────────────────────

```
1. Ist der Code verständlich und gut lesbar?
2. Gibt es offensichtliche Fehler oder Bugs?
3. Sind die Commit-Nachrichten klar und beschreibend?
4. Fehlt etwas Wichtiges (z.B. Dokumentation, Tests)?
```


## ────────────────────────────────────────────────────────────
## Lösung 10.4:
## ────────────────────────────────────────────────────────────

```bash
# Schritt 1: Feedback lesen und die gewünschten Änderungen machen

# Schritt 2: Änderungen committen
git add .
git commit -m "Feedback eingearbeitet: [Beschreibung der Änderung]"

# Schritt 3: Erneut pushen (der PR aktualisiert sich automatisch!)
git push
```
