# ============================================================
# ✅ Lösungen zu Lektion 7: Was ist Origin? (Remote)
# ============================================================


## ────────────────────────────────────────────────────────────
## Lösung 7.1:
## ────────────────────────────────────────────────────────────

```
Ein Remote ist eine Version deines Repositories auf einem anderen
Computer, meistens auf einem Server wie GitHub. "origin" ist der
Standard-Name für diesen Remote – es ist einfach ein Spitzname für
die GitHub-URL deines Projekts.
```


## ────────────────────────────────────────────────────────────
## Lösung 7.2:
## ────────────────────────────────────────────────────────────

```bash
git remote -v
```

Ausgabe (Beispiel):
```
origin  https://github.com/be-storaged/git-learning--Janne.git (fetch)
origin  https://github.com/be-storaged/git-learning--Janne.git (push)
```


## ────────────────────────────────────────────────────────────
## Lösung 7.3:
## ────────────────────────────────────────────────────────────

```
"main" ist der Branch auf deinem eigenen PC (lokal).
"origin/main" ist der Branch auf GitHub (remote).
Die beiden können unterschiedlich sein, z.B. wenn jemand anderes
etwas auf GitHub geändert hat, das du noch nicht heruntergeladen hast.
```


## ────────────────────────────────────────────────────────────
## Lösung 7.4:
## ────────────────────────────────────────────────────────────

```bash
git remote add origin https://github.com/dein-name/mein-neues-projekt.git
```
