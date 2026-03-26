# ============================================================
# 📖 Lektion 10: Pull Requests & Code Review
# ============================================================
#
# Ein Pull Request (kurz PR) ist eine Anfrage, deinen Code
# in den main-Branch zu übernehmen. Bevor das passiert,
# schaut sich eine andere Person deinen Code an.
# Das nennt man Code Review.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 10.1 Was ist ein Pull Request?
## ────────────────────────────────────────────────────────────

Ein **Pull Request** (PR) ist eine Anfrage auf GitHub, die sagt:

> "Hey, ich habe auf meinem Branch etwas gemacht. Kann sich das jemand
> anschauen und dann in `main` übernehmen?"

### Der Ablauf:

```
1. Du arbeitest auf deinem Branch
2. Du pushst deinen Branch auf GitHub
3. Du erstellst einen Pull Request auf GitHub
4. Eine andere Person reviewed (überprüft) deinen Code
5. Nach der Freigabe wird dein Code in main gemerged
```


## ────────────────────────────────────────────────────────────
## 10.2 Einen Pull Request erstellen
## ────────────────────────────────────────────────────────────

### Schritt 1: Deinen Branch pushen

```bash
git checkout -b feature-neue-funktion
# ... Dateien bearbeiten ...
git add .
git commit -m "Neue Funktion implementiert"
git push -u origin feature-neue-funktion
```

### Schritt 2: Auf GitHub den PR erstellen

1. Gehe auf GitHub zu deinem Repository
2. Du siehst einen gelben Banner: "feature-neue-funktion had recent pushes"
3. Klicke auf **"Compare & pull request"**
4. Schreibe einen **Titel** und eine **Beschreibung**
5. Wähle einen **Reviewer** aus (die Person, die deinen Code prüft)
6. Klicke auf **"Create pull request"**

### Gute PR-Beschreibungen:

```
Titel: Login-Seite hinzugefügt

Beschreibung:
- Login-Formular mit E-Mail und Passwort erstellt
- Validierung für E-Mail-Format eingebaut
- Fehlermeldung bei falschem Passwort hinzugefügt

Getestet: Ja, manuell im Browser
```


## ────────────────────────────────────────────────────────────
## 10.3 Code Review – Warum?
## ────────────────────────────────────────────────────────────

> 🔑 **Regel bei uns:** Bevor Code in `main` kommt, muss eine zweite Person ihn überprüfen!

### Warum Code Review?

- 👀 **Vier Augen sehen mehr als zwei** – Fehler werden gefunden
- 📚 **Man lernt voneinander** – Du lernst von den Kommentaren
- ✅ **Qualität bleibt hoch** – Kein schlechter Code kommt in main
- 🤝 **Teamarbeit wird besser** – Alle wissen, was im Projekt passiert


## ────────────────────────────────────────────────────────────
## 10.4 Einen Code Review durchführen
## ────────────────────────────────────────────────────────────

Wenn du der Reviewer bist:

1. Gehe auf GitHub zum Pull Request
2. Klicke auf **"Files changed"** (Geänderte Dateien)
3. Schaue dir die Änderungen an
4. Du kannst **Kommentare** an bestimmten Zeilen hinterlassen
5. Am Ende wählst du:
   - ✅ **Approve** → "Sieht gut aus, kann gemerged werden"
   - 💬 **Comment** → "Ich habe Fragen/Anmerkungen"
   - ❌ **Request changes** → "Hier muss noch etwas geändert werden"

### Worauf achtet man beim Review?

- ✅ Ist der Code verständlich?
- ✅ Gibt es offensichtliche Fehler?
- ✅ Sind die Commit-Nachrichten gut?
- ✅ Fehlt etwas (z.B. Dokumentation)?
- ✅ Macht die Änderung Sinn?


## ────────────────────────────────────────────────────────────
## 10.5 Nach dem Review
## ────────────────────────────────────────────────────────────

### Wenn Änderungen gewünscht werden:

```bash
# 1. Feedback lesen und Änderungen machen
# 2. Neue Commits pushen – der PR aktualisiert sich automatisch!
git add .
git commit -m "Feedback eingearbeitet: Fehlermeldung verbessert"
git push
```

### Wenn alles freigegeben ist:

1. Klicke auf **"Merge pull request"** auf GitHub
2. Wähle **"Squash and merge"** oder **"Create a merge commit"**
3. Der Branch kann danach gelöscht werden ✅

### Nach dem Merge:

```bash
# Auf deinem PC: Zurück zum main-Branch und updaten
git checkout main
git pull origin main
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- Ein **Pull Request** ist eine Anfrage, Code in main zu übernehmen
- **Code Review** = Eine andere Person prüft deinen Code
- Workflow: Branch → Push → PR erstellen → Review → Merge
- Schreibe gute PR-Beschreibungen (Was? Warum? Wie getestet?)
- Als Reviewer: Code lesen, Kommentare schreiben, Approve/Request changes
- **Niemals ohne Review in main mergen!**
- Nach dem Merge: `git checkout main` und `git pull`
