# ============================================================
# 📖 Lektion 7: Was ist Origin? (Remote)
# ============================================================
#
# Bisher haben wir nur auf unserem eigenen PC gearbeitet.
# Aber Git kann dein Projekt auch mit einem Server
# (z.B. GitHub) verbinden. Diese Verbindung nennt man
# "Remote" – und die Standard-Verbindung heißt "origin".
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 7.1 Was ist ein Remote?
## ────────────────────────────────────────────────────────────

Ein **Remote** ist eine Version deines Repos auf einem anderen Computer
(meistens auf GitHub).

Stell dir das so vor:

```
┌─────────────────┐                    ┌─────────────────┐
│  Dein PC         │  ◄──── push ─────▶ │  GitHub          │
│  (Lokal)         │  ◄──── pull ─────▶ │  (Remote)        │
│                  │                    │                  │
│  Hier arbeitest  │                    │  Hier liegt die  │
│  du am Code      │                    │  Online-Kopie    │
└─────────────────┘                    └─────────────────┘
```


## ────────────────────────────────────────────────────────────
## 7.2 Was ist "origin"?
## ────────────────────────────────────────────────────────────

**"origin"** ist einfach ein **Name** (ein Spitzname) für die GitHub-URL deines Repos.

Wenn du ein Repo klonst, wird automatisch ein Remote namens "origin" erstellt:

```bash
git clone https://github.com/be-storaged/mein-projekt.git
```

Jetzt gibt es:
- **origin** = `https://github.com/be-storaged/mein-projekt.git`

> 💡 **Merke:** "origin" ist nur ein Name! Es könnte auch "github" oder "server" heißen. Aber "origin" ist die Standardbezeichnung, die jeder benutzt.


## ────────────────────────────────────────────────────────────
## 7.3 Remotes anzeigen
## ────────────────────────────────────────────────────────────

```bash
# Alle Remotes anzeigen (nur Namen)
git remote

# Alle Remotes mit URLs anzeigen
git remote -v
```

Ausgabe:

```
origin  https://github.com/be-storaged/mein-projekt.git (fetch)
origin  https://github.com/be-storaged/mein-projekt.git (push)
```

- **(fetch)** = Von hier werden Änderungen heruntergeladen
- **(push)** = Hierhin werden Änderungen hochgeladen


## ────────────────────────────────────────────────────────────
## 7.4 Remote hinzufügen (bei git init)
## ────────────────────────────────────────────────────────────

Wenn du ein Repo mit `git init` erstellt hast, gibt es noch keinen Remote.
Du musst ihn manuell hinzufügen:

```bash
git remote add origin https://github.com/benutzername/repo-name.git
```

### Kompletter Workflow bei einem neuen Projekt:

```bash
# 1. Repo erstellen
mkdir mein-projekt
cd mein-projekt
git init

# 2. Erste Datei erstellen und committen
echo "# Mein Projekt" > README.md
git add README.md
git commit -m "Erstes Commit: README erstellt"

# 3. GitHub-Repo als Remote hinzufügen
git remote add origin https://github.com/benutzername/mein-projekt.git

# 4. Zum ersten Mal auf GitHub hochladen
git push -u origin main
```


## ────────────────────────────────────────────────────────────
## 7.5 Was bedeutet origin/main?
## ────────────────────────────────────────────────────────────

Du wirst manchmal `origin/main` sehen. Das bedeutet:

- `main` = Dein lokaler main-Branch (auf deinem PC)
- `origin/main` = Der main-Branch auf GitHub

Die können unterschiedlich sein! Zum Beispiel wenn jemand anderes
etwas auf GitHub geändert hat, das du noch nicht heruntergeladen hast.

```
Dein PC:                GitHub:
main ──●──●──●          origin/main ──●──●──●──●──●
              ▲                                    ▲
              │                                    │
          Du bist hier              Jemand hat hier weitergearbeitet
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- Ein **Remote** ist eine Online-Version deines Repos (z.B. auf GitHub)
- **"origin"** ist der Standard-Name für den Remote
- `git remote -v` → Zeigt alle Remotes mit URLs
- `git remote add origin URL` → Fügt einen Remote hinzu
- `main` = dein lokaler Branch, `origin/main` = der Branch auf GitHub
- Beim Klonen wird "origin" automatisch eingerichtet
