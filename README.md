# 🌿 Git Lernkurs

> Ein Schritt-für-Schritt Kurs um Git zu lernen – auf Deutsch, mit Erklärungen, Aufgaben und Lösungen.

---

## 📌 Worum geht's hier?

Dieser Kurs bringt dir **Git** bei – von den absoluten Grundlagen bis hin zum täglichen Arbeiten im Team. Jede Lektion ist wie ein Kapitel in einem Schulbuch aufgebaut: erst lesen und verstehen, dann üben, und wenn du nicht weiterkommst, gibt's die Lösung.

**So ist der Kurs aufgebaut:**

| Ordner       | Beschreibung |
|--------------|-------------|
| `docs/`      | 📖 **Lektionen** – Lies diese Dateien wie ein Schulbuch, Kapitel für Kapitel |
| `tasks/`     | 📝 **Aufgaben** – 4 Aufgaben pro Lektion zum Üben |
| `solutions/` | ✅ **Lösungen** – Erst selbst versuchen, dann hier nachschauen! |

---

## 📖 Lektionsübersicht

| Nr. | Lektion | Docs | Aufgaben | Lösung |
|-----|---------|------|----------|--------|
| 01 | Was ist Git? (Grundlagen) | [📖](docs/01_was_ist_git.md) | [📝](tasks/01_was_ist_git.md) | [✅](solutions/01_was_ist_git.md) |
| 02 | Repository erstellen & klonen (clone) | [📖](docs/02_clone.md) | [📝](tasks/02_clone.md) | [✅](solutions/02_clone.md) |
| 03 | Dateien tracken (add & status) | [📖](docs/03_add_und_status.md) | [📝](tasks/03_add_und_status.md) | [✅](solutions/03_add_und_status.md) |
| 04 | Änderungen speichern (commit) | [📖](docs/04_commit.md) | [📝](tasks/04_commit.md) | [✅](solutions/04_commit.md) |
| 05 | Atomic Commits | [📖](docs/05_atomic_commits.md) | [📝](tasks/05_atomic_commits.md) | [✅](solutions/05_atomic_commits.md) |
| 06 | Branches (Zweige) | [📖](docs/06_branches.md) | [📝](tasks/06_branches.md) | [✅](solutions/06_branches.md) |
| 07 | Was ist Origin? (Remote) | [📖](docs/07_origin_und_remote.md) | [📝](tasks/07_origin_und_remote.md) | [✅](solutions/07_origin_und_remote.md) |
| 08 | Push & Pull | [📖](docs/08_push_und_pull.md) | [📝](tasks/08_push_und_pull.md) | [✅](solutions/08_push_und_pull.md) |
| 09 | Fetch | [📖](docs/09_fetch.md) | [📝](tasks/09_fetch.md) | [✅](solutions/09_fetch.md) |
| 10 | Pull Requests & Code Review | [📖](docs/10_pull_requests.md) | [📝](tasks/10_pull_requests.md) | [✅](solutions/10_pull_requests.md) |
| 11 | Rebase (Grundlagen) | [📖](docs/11_rebase.md) | [📝](tasks/11_rebase.md) | [✅](solutions/11_rebase.md) |
| 12 | Git im Alltag (Tipps & Tricks) | [📖](docs/12_git_im_alltag.md) | [📝](tasks/12_git_im_alltag.md) | [✅](solutions/12_git_im_alltag.md) |

---

## 🚀 So fängst du an

### 1. Git installieren

```bash
# Linux (Ubuntu/Debian)
sudo apt install git

# macOS
brew install git

# Windows → https://git-scm.com/download/win
```

### 2. Git konfigurieren (einmalig)

```bash
git config --global user.name "Dein Name"
git config --global user.email "deine@email.de"
```

### 3. Kurs durcharbeiten

1. Öffne die Lektion in `docs/` und lies sie durch
2. Probiere die Beispiele im Terminal aus – tippe sie ab!
3. Öffne die passende Aufgabe in `tasks/`
4. Versuche die Aufgaben selbst zu lösen
5. Wenn du nicht weiterkommst → schau in `solutions/`

> ⚠️ **Wichtig:** Versuche die Aufgaben IMMER erst selbst zu lösen, bevor du in die Lösungen schaust!

---

## 👥 Code Review – So arbeiten wir im Team

> **Regel:** Bevor dein Code in den `main`-Branch kommt, muss eine zweite Person ihn überprüfen!

### Warum Code Review?
- 👀 Vier Augen sehen mehr als zwei
- 🐛 Fehler werden früh gefunden
- 📚 Man lernt voneinander
- ✅ Die Code-Qualität bleibt hoch

### So funktioniert's:
1. Du arbeitest auf deinem eigenen **Branch** (nicht auf `main`!)
2. Wenn du fertig bist, erstellst du einen **Pull Request** auf GitHub
3. Eine **zweite Person** schaut sich deinen Code an (= Code Review)
4. Der Reviewer gibt Feedback oder bestätigt mit ✅
5. Erst **nach der Freigabe** wird dein Code in `main` gemerged

> 🚫 **Niemals** direkt auf `main` pushen – immer über einen Pull Request mit Review!

---

## 🔗 Nützliche Links

- [Offizielle Git Webseite](https://git-scm.com/)
- [Git Dokumentation (Englisch)](https://git-scm.com/doc)
- [GitHub Docs (Englisch)](https://docs.github.com/)
- [Git Cheat Sheet (Deutsch)](https://training.github.com/downloads/de/github-git-cheat-sheet/)
- [Oh Shit, Git!?! – Häufige Fehler lösen](https://ohshitgit.com/de)

---

## 📂 Ordnerstruktur

```
git-learning--Janne/
├── README.md                ← Du bist hier!
├── docs/                    ← 📖 Lektionen (wie ein Schulbuch)
│   ├── 01_was_ist_git.md
│   ├── 02_clone.md
│   ├── 03_add_und_status.md
│   ├── 04_commit.md
│   ├── 05_atomic_commits.md
│   ├── 06_branches.md
│   ├── 07_origin_und_remote.md
│   ├── 08_push_und_pull.md
│   ├── 09_fetch.md
│   ├── 10_pull_requests.md
│   ├── 11_rebase.md
│   └── 12_git_im_alltag.md
├── tasks/                   ← 📝 Aufgaben (4 pro Lektion)
│   ├── 01_was_ist_git.md
│   ├── ...
│   └── 12_git_im_alltag.md
└── solutions/               ← ✅ Lösungen
    ├── 01_was_ist_git.md
    ├── ...
    └── 12_git_im_alltag.md
```

---

> 💡 **Tipp:** Git lernt man am besten durch Ausprobieren! Hab keine Angst Fehler zu machen – mit Git kann man (fast) alles rückgängig machen. 😄
