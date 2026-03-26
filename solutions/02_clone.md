# ============================================================
# ✅ Lösungen zu Lektion 2: Repository erstellen & klonen
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 2.1:
## ────────────────────────────────────────────────────────────

```bash
mkdir test-repo
cd test-repo
git init
```


## ────────────────────────────────────────────────────────────
## Lösung 2.2:
## ────────────────────────────────────────────────────────────

```bash
git clone https://github.com/be-storaged/git-learning--Janne.git
```


## ────────────────────────────────────────────────────────────
## Lösung 2.3:
## ────────────────────────────────────────────────────────────

```
"git init" erstellt ein komplett neues, leeres Repository auf deinem PC.
"git clone" kopiert ein bestehendes Repository von GitHub auf deinen PC,
inklusive aller Dateien und der kompletten Historie.
Man benutzt "git init" wenn man ein neues Projekt startet, und
"git clone" wenn man an einem bestehenden Projekt arbeiten will.
```


## ────────────────────────────────────────────────────────────
## Lösung 2.4:
## ────────────────────────────────────────────────────────────

```bash
cd test-repo
git status
```

Ergebnis:
```
On branch main
nothing to commit, working tree clean
```

Was bedeutet das:
```
Du bist auf dem Branch "main" und es gibt keine Änderungen.
Der Arbeitsordner ist sauber – alles ist gespeichert.
```
