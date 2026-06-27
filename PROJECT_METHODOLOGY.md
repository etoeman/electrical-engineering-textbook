# Electrical Engineering Knowledge Database
## Project Methodology (v1.0)

---

# 1. Purpose

This document defines the repeatable workflows used to build the Electrical Engineering Knowledge Database.

`PROJECT_STANDARD.md` defines the project rules. `PROJECT_METHODOLOGY.md` defines how the work is performed.

---

# 2. Core Production Workflow

```text
Original Book -> Digital Recreation -> First-Pass Concept Extraction -> Knowledge Database -> Author Review and Refinement
```

---

# 3. Stage 1 — Digital Book Recreation

The first objective is to recreate the textbook as accurately as possible.

This includes text, equations, tables, figures, captions, section hierarchy, numbering, and formatting where practical.

The goal is faithful reproduction, not interpretation.

No concepts are extracted during this stage.

---

# 4. Stage 2 — First-Pass Concept Extraction

After a digital section has been completed and verified, the assistant performs the first-pass concept extraction.

For every completed section, the assistant shall identify engineering concepts, laws, principles, definitions, physical phenomena, mathematical models, sign conventions, engineering terminology, important assumptions, common misconceptions, and relationships between concepts.

The assistant shall create an initial set of atomic concept notes using the locked EEKB Concept Note Standard.

The objective is completeness. It is preferable to identify a concept that is later merged than to overlook an important concept.

---

# 5. Stage 3 — Author Review and Refinement

The first-pass extraction is not authoritative.

The author is responsible for refining the knowledge base by renaming concepts, splitting concepts, merging concepts, expanding explanations, adding engineering insight, incorporating material from additional textbooks, adding professional experience, improving pedagogy, strengthening conceptual understanding, and building links between concepts.

The final knowledge base represents the author's engineering understanding.

---

# 6. Figure Creation Workflow

## Electrical Circuit Diagrams

```text
CircuitikZ (.tex) -> SVG -> PNG
```

1. Create or edit the CircuitikZ `.tex` source.
2. Render the CircuitikZ source to SVG.
3. Render the SVG to PNG.
4. Reference only the PNG in Markdown.

## Non-Circuit Figures

```text
SVG -> PNG
```

1. Create or edit the SVG source.
2. Render the SVG to PNG.
3. Reference only the PNG in Markdown.

PNG files are never edited directly.

---

# 7. Figure Recreation Workflow

When the user provides an existing figure from a textbook, paper, or other source:

1. Use the uploaded figure as the visual reference.
2. Redraw the figure carefully as clean vector source.
3. Match geometry, proportions, spacing, line weights, typography, labels, and engineering notation.
4. Use tracing only as a reference aid for fidelity.
5. Do not treat auto-tracing as the final product.
6. Render the PNG only from the final master source.

Working principle:

```text
Use tracing to achieve accuracy, not as a shortcut.
```

---

# 8. GitHub Workflow

GitHub is the source of truth.

When GitHub access is available, project changes shall be made directly in:

```text
etoeman/electrical-engineering-textbook
```

After GitHub is updated, the user will synchronize the local Obsidian working copy using `git pull`.

---

# 9. Quality Assurance Workflow

Before considering a section complete:

- Digital recreation should be checked against the source.
- Figure references should point only to PNGs.
- Every PNG should have its master source.
- Knowledge notes should follow the locked concept template.
- Atomic concept notes should not duplicate existing concepts.

---

# 10. Version History

## v1.0

Initial locked project methodology.
