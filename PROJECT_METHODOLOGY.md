# Electrical Engineering Knowledge Database
## Project Methodology (v1.3)

---

# 1. Purpose

This document defines the repeatable workflows used to build the Electrical Engineering Knowledge Database.

`PROJECT_STANDARD.md` defines the project rules. `PROJECT_METHODOLOGY.md` defines how the work is performed.

---

# 2. Core Production Workflow

```text
Original Book -> Digital Recreation -> Text Fixes -> Enhanced Edition -> Knowledge Database -> Author Review and Refinement
```

The production flow is sequential. Each stage depends on the previous stage.

- The **Digital Recreation** preserves the source material faithfully.
- The **Text Fixes** stage records technical errors, pedagogic issues, and proposed fixes found in the Digital Recreation.
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

## Section Answers

Each section concludes with an **Answers** subsection that consolidates all publisher-provided answers associated with that section, including:

- Answers to **What If?** questions (including those provided later as footnotes).
- Answers to **Check Your Understanding** questions.
- Any other publisher-provided exercise answers belonging to that section.

The original textbook text remains unchanged. The **Answers** subsection is an editorial convenience that gathers the official answers into one location at the end of the section. No new solutions or explanations are added during the Digital Recreation stage.

---

# 4. Stage 2 — Text Fixes

After a digital section has been completed and checked against the source, the assistant shall create an intermediate Text Fixes file.

This stage documents issues to be corrected before creating the Enhanced Edition. It is not the Enhanced Edition itself.

For every completed section, the companion file shall use the suffix:

```text
-fixes.md
```

Example:

```text
1.3-current-and-kirchhoffs-current-law-fixes.md
```

The Text Fixes file records error and pedagogic fixes, including:

- Technical errors.
- Ambiguous explanations.
- Weak or incomplete pedagogy.
- Notation inconsistencies.
- Figure deficiencies.
- Missing conceptual bridges.
- Outdated terminology or engineering practice.
- Proposed corrections.
- Rationale for each change to be incorporated into the Enhanced Edition.

The Text Fixes file is the change-control bridge between the faithful Digital Recreation and the improved Enhanced Edition.

---

# 5. Stage 3 — Enhanced Edition

The remainder of the document is unchanged.
