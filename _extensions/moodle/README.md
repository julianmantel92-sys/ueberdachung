# automatic-ai-engine

Eine maßgeschneiderte Quarto-Extension für interaktive Webseiten, moderne Fachinformations-Portale und Moodle-kompatible HTML-Lehrmaterialien mit Deep-Dive-Containern, Drag-and-Drop-Aufgaben und Vektor-Visualisierungen.

---

## 🛠️ 1. Erstmalige Einrichtung im Quarto-Projekt

### Schritt 1: In das gewünschte Quarto-Projekt wechseln
```bash
cd /Pfad/zu/deinem/quarto-projekt
```

### Schritt 2: Repository direkt als Extension `moodle` hineinklonen
```bash
git clone git@github.com:julianmantel92-sys/automatic-ai-engine.git _extensions/moodle
```

> **Hinweis:** Durch das Klonen direkt nach `_extensions/moodle` entfallen manuelle Ordnererstellungen (`mkdir`) und Symlinks. Quarto erkennt das Format `moodle-html` auf jedem System (macOS, Windows, Linux) sofort.

---

## 📄 2. Verwendung im QMD-Dokument

In jedem `.qmd`-Dokument dieses Projekts reicht nun der schlanke Zweizeiler im YAML-Frontmatter:

```yaml
---
title: "Titel des Dokuments"
subtitle: "Untertitel / Themenbereich"
date: last-modified
lang: de
toc-title: "Inhaltsübersicht"

format:
  moodle-html: default
---
```

---

## 🧩 3. Enthaltene Features

Das Format `moodle-html` bindet automatisch folgende Kernkomponenten ein:
- **Design & Theme:** Bereitstellung von `custom.scss` (moderne Typografie, Slate-/Indigo-Farbpalette, optimierte Tabellen und Callouts).
- **Interaktive Deep Dives:** Aufklappbare Accordion-Boxen via `::: {.details}` für Praxisfälle, Berechnungen und Gesetzestexte.
- **Interaktiver Header:** Sticky Navigation Header mit dynamischer Titelübernahme aus dem Dokument.
- **Drag- & Click-Übungen:** Interaktive Textlücken (`::: {.drag-exercise}`) für Lern- und Testmodule.
- **Inhaltsverzeichnis & Nummerierung:** Automatisches Inhaltsverzeichnis (`toc: true`) und saubere Gliederungsnummern (`number-sections: true`).
- **Autarkie:** Alle Skripte und Styles werden inline kompiliert (`self-contained: true`) – perfekt für den Upload in Moodle oder als Standalone-Webseite.

---

## 🔄 4. Updates der Extension einspielen

Wenn Sie Anpassungen an der Extension im GitHub-Repository vorgenommen haben, aktualisieren Sie diese in einem bestehenden Projekt einfach per:

```bash
cd _extensions/moodle
git pull
```

---

### 🚀 5. Eigene Änderungen hochladen (Workflow)

**In das Extension-Verzeichnis wechseln:**
```bash
cd _extensions/julianmantel92-sys/automatic-ai-engine
```
**Änderungen vorbereiten und commiten:**
```bash
git add .
git commit -m "Deine Nachricht"
```
**Online-Updates abholen und mergen:**
```bash
git pull origin main
```
**Eigene Änderungen hochladen:**
```bash
git push origin main
```
