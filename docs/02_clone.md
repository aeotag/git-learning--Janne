# ============================================================
# 📖 Lektion 2: Repository erstellen & klonen (clone)
# ============================================================
#
# Ein Repository (kurz "Repo") ist ein Projektordner, den
# Git überwacht. Du kannst ein neues Repo erstellen oder
# ein bestehendes von GitHub auf deinen PC kopieren.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 2.1 Ein neues Repository erstellen (git init)
## ────────────────────────────────────────────────────────────

Um einen Ordner zu einem Git-Repository zu machen, benutzt du:

```bash
mkdir mein-projekt       # Erstelle einen neuen Ordner
cd mein-projekt          # Gehe in den Ordner
git init                 # Mache daraus ein Git-Repository
```

Danach sagt Git:

```
Initialized empty Git repository in /pfad/zu/mein-projekt/.git/
```

> 💡 Git erstellt einen versteckten Ordner `.git/` – dort speichert Git alle Informationen. Diesen Ordner niemals löschen!


## ────────────────────────────────────────────────────────────
## 2.2 Ein Repository von GitHub klonen (git clone)
## ────────────────────────────────────────────────────────────

Wenn ein Repo schon auf GitHub existiert, kannst du es auf deinen PC kopieren:

```bash
git clone https://github.com/benutzername/repo-name.git
```

Das passiert dabei:
1. Git erstellt einen neuen Ordner mit dem Repo-Namen
2. Alle Dateien werden heruntergeladen
3. Die komplette Historie (alle Änderungen) wird heruntergeladen
4. Die Verbindung zu GitHub wird automatisch eingerichtet

### Beispiel:

```bash
git clone https://github.com/be-storaged/git-learning--Janne.git
cd git-learning--Janne
```

Jetzt bist du im Projekt und kannst loslegen!


## ────────────────────────────────────────────────────────────
## 2.3 Was ist der Unterschied? (init vs. clone)
## ────────────────────────────────────────────────────────────

| | `git init` | `git clone` |
|---|-----------|-------------|
| **Wann?** | Neues Projekt starten | Bestehendes Projekt kopieren |
| **Wo?** | Auf deinem PC | Von GitHub (oder anderem Server) |
| **Verbindung?** | Keine Verbindung zu GitHub | Automatisch mit GitHub verbunden |
| **Dateien?** | Leerer Ordner | Alle Dateien werden heruntergeladen |


## ────────────────────────────────────────────────────────────
## 2.4 Den Status prüfen
## ────────────────────────────────────────────────────────────

Nachdem du ein Repo erstellt oder geklont hast, kannst du den Status prüfen:

```bash
git status
```

Bei einem frischen Repo siehst du:

```
On branch main
nothing to commit, working tree clean
```

Das bedeutet: Alles ist sauber, es gibt keine Änderungen.

> 💡 `git status` ist dein bester Freund! Benutze es oft, um zu sehen, was gerade los ist.


## ────────────────────────────────────────────────────────────
## 2.5 Klonen mit SSH (für Fortgeschrittene)
## ────────────────────────────────────────────────────────────

Es gibt zwei Arten, ein Repo zu klonen:

```bash
# HTTPS (einfacher, braucht Passwort/Token)
git clone https://github.com/benutzername/repo-name.git

# SSH (sicherer, braucht SSH-Key)
git clone git@github.com:benutzername/repo-name.git
```

Für den Anfang reicht HTTPS völlig aus!


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- `git init` → Neues leeres Repository erstellen
- `git clone URL` → Bestehendes Repository von GitHub kopieren
- `git status` → Aktuellen Zustand des Repos prüfen
- Beim Klonen wird automatisch eine Verbindung zu GitHub hergestellt
- Der `.git/`-Ordner enthält alle Git-Informationen – niemals löschen!
