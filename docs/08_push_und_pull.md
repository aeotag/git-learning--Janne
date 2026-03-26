# ============================================================
# 📖 Lektion 8: Push & Pull
# ============================================================
#
# Push und Pull sind die zwei wichtigsten Befehle, um
# Änderungen zwischen deinem PC und GitHub auszutauschen.
# Push = hochladen, Pull = herunterladen.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 8.1 Was ist Push?
## ────────────────────────────────────────────────────────────

**Push** = Deine Änderungen von deinem PC auf GitHub **hochladen**.

```
Dein PC ────push────▶ GitHub
```

```bash
git push origin main
```

Das bedeutet: "Lade meine Commits auf den Remote 'origin' hoch, Branch 'main'."


## ────────────────────────────────────────────────────────────
## 8.2 Was ist Pull?
## ────────────────────────────────────────────────────────────

**Pull** = Änderungen von GitHub auf deinen PC **herunterladen und einbauen**.

```
Dein PC ◀────pull──── GitHub
```

```bash
git pull origin main
```

Das bedeutet: "Lade die neuesten Änderungen vom Remote 'origin' herunter, Branch 'main'."

> 💡 `git pull` macht eigentlich zwei Dinge auf einmal:
> 1. `git fetch` – Änderungen herunterladen
> 2. `git merge` – Änderungen in deinen Code einbauen


## ────────────────────────────────────────────────────────────
## 8.3 Der typische Arbeitsablauf
## ────────────────────────────────────────────────────────────

So sieht ein normaler Arbeitstag mit Git aus:

```bash
# 1. Neueste Änderungen holen (falls jemand anderes etwas geändert hat)
git pull origin main

# 2. Neuen Branch erstellen für deine Arbeit
git checkout -b feature-meine-aufgabe

# 3. Arbeiten, Dateien bearbeiten...

# 4. Änderungen speichern
git add .
git commit -m "Meine Änderung beschreiben"

# 5. Deinen Branch auf GitHub hochladen
git push origin feature-meine-aufgabe
```


## ────────────────────────────────────────────────────────────
## 8.4 Push – Details
## ────────────────────────────────────────────────────────────

### Ersten Push machen (mit -u):

Wenn du einen Branch zum **ersten Mal** hochlädst:

```bash
git push -u origin mein-branch
```

Das `-u` steht für "upstream" und merkt sich die Verbindung.
Danach reicht ein einfaches:

```bash
git push
```

### Was passiert, wenn Push nicht klappt?

Wenn jemand anderes vor dir etwas hochgeladen hat, bekommst du
einen Fehler:

```
! [rejected]        main -> main (fetch first)
```

Lösung: Erst pullen, dann pushen!

```bash
git pull origin main
# Eventuelle Konflikte lösen...
git push origin main
```


## ────────────────────────────────────────────────────────────
## 8.5 Pull – Details
## ────────────────────────────────────────────────────────────

### Regelmäßig pullen!

Wenn du im Team arbeitest, solltest du **regelmäßig pullen**, um auf
dem neuesten Stand zu bleiben.

```bash
# Vor dem Arbeiten immer:
git pull
```

### Was passiert, wenn es Konflikte gibt?

Wenn du und jemand anderes die **gleiche Zeile** in der **gleichen Datei**
geändert haben, gibt es einen **Merge-Konflikt**. Git zeigt dir das so:

```
<<<<<<< HEAD
Deine Änderung
=======
Die Änderung der anderen Person
>>>>>>> origin/main
```

Du musst dann entscheiden, welche Version richtig ist, die Markierungen
löschen und neu committen. Keine Panik – das klingt schlimmer als es ist!


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- `git push` → Deine Änderungen auf GitHub hochladen
- `git pull` → Änderungen von GitHub herunterladen und einbauen
- `git push -u origin branch-name` → Erster Push eines neuen Branches
- **Immer erst `git pull` machen, bevor du mit der Arbeit anfängst!**
- Bei Konflikten: Ruhe bewahren, Datei öffnen, richtige Version behalten
- Workflow: pull → branch → arbeiten → add → commit → push
