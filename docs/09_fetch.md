# ============================================================
# 📖 Lektion 9: Fetch
# ============================================================
#
# Fetch ist der "vorsichtige Bruder" von Pull. Er lädt
# Änderungen herunter, baut sie aber NICHT automatisch ein.
# So kannst du erst schauen, was sich geändert hat, bevor
# du es übernimmst.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 9.1 Was ist Fetch?
## ────────────────────────────────────────────────────────────

**Fetch** = Änderungen von GitHub **herunterladen**, aber noch **NICHT einbauen**.

Vergleich:

| Befehl | Herunterladen | Einbauen |
|--------|:------------:|:--------:|
| `git fetch` | ✅ | ❌ |
| `git pull`  | ✅ | ✅ |

> 💡 **Merke:** `git pull` = `git fetch` + `git merge`

Stell dir das so vor:
- **Fetch** = Du schaust in den Briefkasten und siehst, dass Post da ist
- **Pull** = Du schaust in den Briefkasten, nimmst die Post raus und liest sie


## ────────────────────────────────────────────────────────────
## 9.2 Wann benutzt man Fetch?
## ────────────────────────────────────────────────────────────

Fetch ist nützlich, wenn du:

1. **Erst schauen willst**, was andere geändert haben
2. **Nicht sofort** deine Dateien verändern willst
3. **Sicher sein willst**, dass nichts kaputt geht

### Beispiel:

```bash
# Änderungen herunterladen (ohne einzubauen)
git fetch origin

# Schauen, was sich auf GitHub geändert hat
git log origin/main --oneline

# Unterschiede zwischen deinem Code und GitHub anzeigen
git diff main origin/main

# Wenn alles gut aussieht → jetzt einbauen
git merge origin/main
```


## ────────────────────────────────────────────────────────────
## 9.3 Fetch in der Praxis
## ────────────────────────────────────────────────────────────

```bash
# Alle Änderungen von allen Remotes holen
git fetch --all

# Nur von origin holen
git fetch origin

# Einen bestimmten Branch holen
git fetch origin main
```

### Was passiert nach einem Fetch?

Nach `git fetch` hast du die neuesten Informationen, aber dein
Arbeitsordner hat sich NICHT verändert:

```
Dein PC (main):           ●──●──●          ← unverändert!
Origin (origin/main):     ●──●──●──●──●    ← heruntergeladen, aber nicht eingebaut
```


## ────────────────────────────────────────────────────────────
## 9.4 Fetch vs. Pull – Wann was?
## ────────────────────────────────────────────────────────────

### Benutze `git fetch` wenn:
- ✅ Du erst sehen willst, was sich geändert hat
- ✅ Du vorsichtig sein willst
- ✅ Du in einem komplexen Projekt arbeitest

### Benutze `git pull` wenn:
- ✅ Du weißt, dass es keine Konflikte gibt
- ✅ Du schnell auf den neuesten Stand kommen willst
- ✅ Du am Anfang deines Arbeitstages bist

> 💡 Für den Alltag reicht `git pull` meistens aus. Aber es ist gut zu wissen, dass `git fetch` existiert, wenn du mal vorsichtiger sein willst!


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- `git fetch` → Änderungen herunterladen, aber NICHT einbauen
- `git pull` = `git fetch` + `git merge` (herunterladen UND einbauen)
- Fetch ist die "sichere" Variante – du kannst erst schauen, dann entscheiden
- `git fetch --all` → Von allen Remotes holen
- `git diff main origin/main` → Unterschiede nach Fetch anzeigen
- Für den Alltag: `git pull` reicht meistens, `git fetch` wenn du vorsichtig sein willst
