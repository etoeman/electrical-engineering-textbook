# Electrical Engineering Knowledge Database

This repository is the source of truth for the Electrical Engineering Knowledge Database and the related digital textbook project.

The project has four permanent outputs for each textbook section:

1. **Digital Edition** — faithful recreation of the original textbook section.
2. **Enhanced Edition** — corrected and improved teaching version.
3. **Section Review** — editorial review documenting errors, weaknesses, and improvements.
4. **Knowledge Database** — fine-grained atomic concept notes built from the section and expanded with additional engineering knowledge.

---

## Repository Philosophy

GitHub is the single source of truth.

The local Obsidian vault is the Git working copy. After GitHub is updated, the local vault is synchronized with:

```text
git pull
```

All project content belongs in GitHub. Personal Obsidian workspace state does not.

---

## Project Governance

The project is governed by two top-level documents:

```text
PROJECT_STANDARD.md
PROJECT_METHODOLOGY.md
```

`PROJECT_STANDARD.md` defines the rules.

`PROJECT_METHODOLOGY.md` defines the workflows.

New conversations about this project may begin with:

```text
EEKB
```

That command means: use this repository, follow the project standard and methodology, and preserve the locked architecture.

---

## Main Repository Folders

```text
chapters/       Digital and enhanced textbook sections
knowledge/      Digested atomic engineering concept notes
figures/        Figure folders containing source and published PNG files
front-matter/   Source front matter from the recreated textbook
references/     Bibliographic and source references
templates/      Reusable project templates
```

---

## Chapter Structure

Textbook chapters are organized by chapter folder.

Each book section is stored as its own Markdown file.

Example:

```text
chapters/
└── 01-basic-circuit-theory/
    ├── README.md
    ├── 1.3-current-and-kirchhoffs-current-law.md
    ├── 1.3-current-and-kirchhoffs-current-law-enhanced.md
    └── 1.3-current-and-kirchhoffs-current-law-review.md
```

The base section file is the faithful digital edition.

The `-enhanced.md` file is the corrected teaching edition.

The `-review.md` file is the editorial review.

---

## Knowledge Database Structure

The `knowledge/` folder contains the author's digested engineering understanding.

The textbook chapter and section sequence provides the learning pathway, but each section folder contains fine-grained atomic concept notes.

Example:

```text
knowledge/
└── ch01-basic-circuit-theory/
    └── 1.3-current-and-kirchhoffs-current-law/
        ├── Current.md
        ├── Conventional Current.md
        ├── Current Direction.md
        └── Kirchhoff's Current Law.md
```

Each concept note follows the locked EEKB concept note template in:

```text
templates/concept-note.md
```

---

## Figure Structure

All figures live under `figures/`.

Each figure has its own folder.

Example:

```text
figures/
└── ch01/
    └── fig-1-3/
        ├── fig-1-3.svg
        └── fig-1-3.png
```

Circuit diagrams use CircuitikZ as the source:

```text
figures/
└── ch02/
    └── fig-2-8/
        ├── fig-2-8.tex
        ├── fig-2-8.svg
        └── fig-2-8.png
```

Markdown references only PNG figures.

PNG files are generated from their source files. They are never edited directly.

---

## Production Workflow

Every textbook section follows this workflow:

```text
Original Textbook
        ↓
Digital Edition
        ├── Enhanced Edition
        ├── Section Review
        └── First-Pass Concept Extraction
                ↓
        Electrical Engineering Knowledge Database
                ↓
        Author Expansion and Refinement
```

---

## Working Rule

This repository is now governed by locked standards.

Repository architecture changes should occur only when explicitly approved and documented through the project standard.
