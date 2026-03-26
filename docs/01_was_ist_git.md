# ============================================================
# 📖 Lektion 1: Was ist Git?
# ============================================================
#
# Git ist ein Werkzeug, das dir hilft, Änderungen an Dateien
# zu verfolgen. Stell dir vor, du schreibst einen Aufsatz und
# willst jede Version speichern – Git macht genau das,
# aber viel besser!
#
# ============================================================


## ────────────────────────────────────────────────────────────
## 1.1 Was ist Versionskontrolle?
## ────────────────────────────────────────────────────────────

Stell dir vor, du arbeitest an einem Dokument:

```
Aufsatz_v1.docx
Aufsatz_v2.docx
Aufsatz_v2_final.docx
Aufsatz_v2_final_WIRKLICH_FINAL.docx
```

Kennst du das? 😄 Das ist chaotisch und unübersichtlich!

**Git** löst dieses Problem. Es speichert automatisch jede Änderung,
die du machst, und du kannst jederzeit zu einer älteren Version
zurückspringen.


## ────────────────────────────────────────────────────────────
## 1.2 Warum brauchen wir Git?
## ────────────────────────────────────────────────────────────

- 📁 **Änderungen verfolgen** – Du siehst genau, was wann geändert wurde
- ⏪ **Rückgängig machen** – Du kannst jederzeit zu einer alten Version zurück
- 👥 **Teamarbeit** – Mehrere Personen können gleichzeitig am selben Projekt arbeiten
- 🔒 **Sicherheit** – Dein Code geht nie verloren


## ────────────────────────────────────────────────────────────
## 1.3 Git vs. GitHub – Was ist der Unterschied?
## ────────────────────────────────────────────────────────────

Das wird oft verwechselt, ist aber ganz einfach:

| | Git | GitHub |
|---|-----|--------|
| **Was?** | Ein Programm auf deinem Computer | Eine Webseite im Internet |
| **Wofür?** | Änderungen lokal speichern | Code online teilen & zusammenarbeiten |
| **Wo?** | Läuft auf deinem PC | Läuft im Browser (github.com) |

> 💡 **Merke:** Git ist das Werkzeug. GitHub ist wie ein Online-Speicher für deine Git-Projekte.

Man kann sich das so vorstellen:
- **Git** = Dein Tagebuch, in dem du alles aufschreibst
- **GitHub** = Der Tresor, in dem du dein Tagebuch sicher aufbewahrst und mit anderen teilen kannst


## ────────────────────────────────────────────────────────────
## 1.4 Die wichtigsten Begriffe
## ────────────────────────────────────────────────────────────

Bevor wir loslegen, hier ein paar Begriffe, die du kennen solltest:

| Begriff | Erklärung |
|---------|-----------|
| **Repository (Repo)** | Ein Ordner/Projekt, das von Git überwacht wird |
| **Commit** | Eine gespeicherte Änderung (wie ein Foto deines Projekts) |
| **Branch** | Ein Zweig – eine eigene Kopie zum Arbeiten |
| **Remote** | Ein Repo auf einem Server (z.B. GitHub) |
| **Clone** | Ein Repo von GitHub auf deinen PC kopieren |
| **Push** | Deine Änderungen auf GitHub hochladen |
| **Pull** | Änderungen von GitHub herunterladen |

> 🎯 Du musst dir das nicht alles sofort merken! Wir gehen alles Schritt für Schritt durch.


## ────────────────────────────────────────────────────────────
## 1.5 Git installieren und prüfen
## ────────────────────────────────────────────────────────────

Prüfe, ob Git installiert ist:

```bash
git --version
```

Wenn eine Versionsnummer erscheint (z.B. `git version 2.39.0`), ist alles gut!

Falls nicht, installiere Git:

```bash
# Linux (Ubuntu/Debian)
sudo apt install git

# macOS
brew install git

# Windows → https://git-scm.com/download/win
```


## ────────────────────────────────────────────────────────────
## 1.6 Git einmalig konfigurieren
## ────────────────────────────────────────────────────────────

Bevor du Git benutzen kannst, musst du Git sagen, wer du bist:

```bash
git config --global user.name "Dein Name"
git config --global user.email "deine@email.de"
```

Diese Einstellung gilt für ALLE deine Projekte. Du musst das nur **einmal** machen.

Prüfe deine Einstellungen:

```bash
git config --list
```


## ────────────────────────────────────────────────────────────
## 📝 Zusammenfassung
## ────────────────────────────────────────────────────────────

- **Git** ist ein Werkzeug zur Versionskontrolle
- Es speichert jede Änderung und du kannst jederzeit zurückspringen
- **Git** läuft auf deinem PC, **GitHub** ist eine Webseite
- Ein **Repository** ist ein Projektordner, der von Git überwacht wird
- Mit `git --version` prüfst du, ob Git installiert ist
- Mit `git config` sagst du Git, wer du bist
