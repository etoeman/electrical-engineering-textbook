# Electrical Engineering Knowledge Database
## Project Methodology (v1.1)

---

# 1. Purpose

This document defines the repeatable workflows used to build the Electrical Engineering Knowledge Database.

`PROJECT_STANDARD.md` defines the project rules. `PROJECT_METHODOLOGY.md` defines how the work is performed.

---

# 2. Core Production Workflow

```text
Original Book -> Digital Recreation -> Error/Pedagogic Fixes -> Enhanced Edition -> Knowledge Database -> Author Review and Refinement
```

The production flow is sequential. Each stage depends on the previous stage.

- The **Digital Recreation** preserves the source material faithfully.
- The **Error/Pedagogic Fixes** stage records issues found in the Digital Recreation and proposed fixes.
- The **Enhanced Edition** applies approved fixes and pedagogical improvements.
- The **Knowledge Database** is extracted from the Enhanced Edition, not directly from the Digital Recreation.
- **Author Review and Refinement** is the final authority for the knowledge base.

---

# 3. Stage 1 — Digital Book Recreation

The first objective is to recreate the textbook as accurately as possible.

This includes text, equations, tables, figures, captions, section hierarchy, numbering, and formatting where practical.

The goal is faithful reproduction, not interpretation.

No concepts are extracted during this stage.

Digital Recreation files use the base section filename:

```text
<section-slug>.md
```

Example:

```text
1.3-current-and-kirchhoffs-current-law.md
```

---

# 4. Stage 2 — Error/Pedagogic Fixes

After a digital section has been completed and checked against the source, the assistant shall create an intermediate Error/Pedagogic Fixes file.

This stage documents issues to be corrected before creating the Enhanced Edition. It is not the Enhanced Edition itself.

For every completed section, the companion file shall use the suffix:

```text
-error-pedagogic-fixes.md
```

Example:

```text
1.3-current-and-kirchhoffs-current-law-error-pedagogic-fixes.md
```

The Error/Pedagogic Fixes file records:

- Technical errors.
- Ambiguous explanations.
- Weak or incomplete pedagogy.
- Notation inconsistencies.
- Figure deficiencies.
- Missing conceptual bridges.
- Outdated terminology or engineering practice.
- Proposed corrections.
- Rationale for each change to be incorporated into the Enhanced Edition.

The Error/Pedagogic Fixes file is the change-control bridge between the faithful Digital Recreation and the improved Enhanced Edition.

---

# 5. Stage 3 — Enhanced Edition

The Enhanced Edition is created only after the Error/Pedagogic Fixes stage.

The Enhanced Edition applies approved corrections and pedagogical improvements from the Error/Pedagogic Fixes file while preserving the technical meaning of the original source.

Enhanced Edition files use the suffix:

```text
-enhanced.md
```

Example:

```text
1.3-current-and-kirchhoffs-current-law-enhanced.md
```

---

# 6. Stage 4 — Knowledge Database Extraction

After an Enhanced Edition section has been completed and verified, the assistant performs knowledge extraction.

Concepts are extracted from the Enhanced Edition, not directly from the Digital Recreation.

For every completed enhanced section, the assistant shall identify engineering concepts, laws, principles, definitions, physical phenomena, mathematical models, sign conventions, engineering terminology, important assumptions, common misconceptions, and relationships between concepts.

The assistant shall create an initial set of atomic concept notes using the locked EEKB Concept Note Standard.

The objective is completeness. It is preferable to identify a concept that is later merged than to overlook an important concept.

---

# 7. Stage 5 — Author Review and Refinement

The first-pass extraction is not authoritative.

The author is responsible for refining the knowledge base by renaming concepts, splitting concepts, merging concepts, expanding explanations, adding engineering insight, incorporating material from additional textbooks, adding professional experience, improving pedagogy, strengthening conceptual understanding, and building links between concepts.

The final knowledge base represents the author's engineering understanding.

---

# 8. Figure Creation Workflow

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

# 9. Figure Recreation Workflow

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

# 10. GitHub Workflow

GitHub is the source of truth.

When GitHub access is available, project changes shall be made directly in:

```text
etoeman/electrical-engineering-textbook
```

After GitHub is updated, the user will synchronize the local Obsidian working copy using `git pull`.

---

# 11. Quality Assurance Workflow

Before considering a section complete:

- Digital recreation should be checked against the source.
- Error/Pedagogic Fixes should document issues and proposed corrections before Enhanced Edition work begins.
- Enhanced Edition should incorporate approved fixes from the Error/Pedagogic Fixes file.
- Knowledge extraction should be performed from the Enhanced Edition.
- Figure references should point only to PNGs.
- Every PNG should have its master source.
- Knowledge notes should follow the locked concept template.
- Atomic concept notes should not duplicate existing concepts.

---

# 12. Version History

## v1.1

Added the Error/Pedagogic Fixes stage between Digital Recreation and Enhanced Edition. Clarified that Knowledge Database extraction is performed from the Enhanced Edition.

## v1.0

Initial locked project methodology.
