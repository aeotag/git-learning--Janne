# ============================================================
# 📖 Lektion 6: Branches (Zweige)
# ============================================================
#
# Branches sind wie parallele Welten für deinen Code.
# Du kannst an verschiedenen Dingen arbeiten, ohne dass
# sie sich gegenseitig stören. Am Ende führst du sie
# wieder zusammen.
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 6.1 Was ist ein Branch?
## ────────────────────────────────────────────────────────────

Stell dir einen Baum vor 🌳:

```
            feature-login
           /
main ─────●──────●──────●
           \
            fix-bug-123
```

- Der **Stamm** ist der `main`-Branch (die Hauptversion)
- Die **Äste** sind andere Branches (Arbeitskopien)

Jeder Branch ist eine **eigene Kopie** deines Projekts. Du kannst dort
Änderungen machen, ohne den `main`-Branch zu beeinflussen.

> 💡 **Merke:** Auf `main` arbeiten wir **NICHT** direkt! Wir erstellen immer einen neuen Branch.


## ────────────────────────────────────────────────────────────
## 6.2 Branches anzeigen
## ────────────────────────────────────────────────────────────

```bash
# Alle lokalen Branches anzeigen
git branch

# Alle Branches anzeigen (auch auf GitHub)
git branch -a
```

Der aktive Branch wird mit einem `*` markiert:

```
* main
  feature-login
  fix-bug-123
```


## ────────────────────────────────────────────────────────────
## 6.3 Einen neuen Branch erstellen
## ────────────────────────────────────────────────────────────

```bash
# Neuen Branch erstellen
git branch mein-neuer-branch

# Neuen Branch erstellen UND direkt dorthin wechseln
git checkout -b mein-neuer-branch
```

> 💡 **Tipp:** Benutze `git checkout -b name` – das ist der häufigste Befehl, weil du meistens sofort auf dem neuen Branch arbeiten willst.

### Branch-Namen – Regeln:

Gute Branch-Namen beschreiben, woran du arbeitest:

```bash
# ✅ GUTE Branch-Namen:
git checkout -b feature-login-seite
git checkout -b fix-passwort-fehler
git checkout -b update-readme

# ❌ SCHLECHTE Branch-Namen:
git checkout -b test
git checkout -b asdf
git checkout -b mein-branch
```


## ────────────────────────────────────────────────────────────
## 6.4 Zwischen Branches wechseln
## ────────────────────────────────────────────────────────────

```bash
# Zu einem anderen Branch wechseln
git checkout branch-name

# Zum main-Branch zurückwechseln
git checkout main
```

> ⚠️ **Achtung:** Speichere (committe) deine Änderungen, bevor du den Branch wechselst! Sonst können Änderungen verloren gehen.


## ────────────────────────────────────────────────────────────
## 6.5 Branches zusammenführen (merge)
## ────────────────────────────────────────────────────────────

Wenn du mit deiner Arbeit auf einem Branch fertig bist, führst du ihn
zurück in `main`:

```bash
# 1. Wechsle zum main-Branch
git checkout main

# 2. Führe deinen Branch in main zusammen
git merge feature-login-seite
```

```
            feature-login
           /               \
main ─────●──────●──────●───●── (zusammengeführt!)
```

> 💡 In der Praxis machen wir das über **Pull Requests** auf GitHub (Lektion 10). Aber es ist gut zu wissen, wie es funktioniert!


## ────────────────────────────────────────────────────────────
## 6.6 Branch löschen
## ────────────────────────────────────────────────────────────

Wenn ein Branch nicht mehr gebraucht wird (weil er gemerged wurde):

```bash
# Lokalen Branch löschen
git branch -d feature-login-seite

# Branch auf GitHub löschen
git push origin --delete feature-login-seite
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- Ein **Branch** ist eine eigene Kopie deines Projekts
- `git branch` → Alle Branches anzeigen
- `git checkout -b name` → Neuen Branch erstellen und wechseln
- `git checkout name` → Zu einem Branch wechseln
- `git merge name` → Branch zusammenführen
- `git branch -d name` → Branch löschen
- **Niemals direkt auf `main` arbeiten!** Immer einen neuen Branch erstellen.
