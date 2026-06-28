# Electrical Engineering Knowledge Database
## Project Standard (v1.0)

---

# 1. Project Identity

**Project Name:** Electrical Engineering Knowledge Database  
**Repository:** `etoeman/electrical-engineering-textbook`  
**Primary Authoring Environment:** Obsidian  
**Version Control:** GitHub  
**Startup Command:** `EEKB`

GitHub is the source of truth for this project. The local Obsidian vault reads the local Git working copy, which is synchronized from GitHub using `git pull`.

---

# 2. Project Purpose

The Electrical Engineering Knowledge Database is a permanent, structured engineering knowledge base dedicated to fundamental electrical engineering.

The project has two related but distinct assets:

1. A faithful digital recreation of the source textbook material.
2. A digested engineering knowledge base built from that source material and expanded with additional engineering knowledge.

The knowledge base is not a copy of the textbook. It is the author’s curated engineering understanding of electrical engineering concepts.

---

# 3. Guiding Philosophy

Every concept should answer four fundamental questions:

1. What is it?
2. Why does it exist?
3. How does it work?
4. Why should I believe it?

Concepts shall be developed from first principles whenever practical. Physical intuition comes before mathematics. Mathematics is used to explain engineering, not replace engineering understanding.

---

# 4. Governance Documents

The top-level governance files are:

```text
PROJECT_STANDARD.md
PROJECT_METHODOLOGY.md
README.md
```

`PROJECT_STANDARD.md` defines permanent project rules. `PROJECT_METHODOLOGY.md` defines repeatable workflows. `README.md` introduces the repository.

---

# 5. GitHub Access Procedure

At the beginning of any ChatGPT conversation related to this project, the AI shall attempt to establish access to:

```text
etoeman/electrical-engineering-textbook
```

If repository access has not yet been granted for the current conversation, the AI shall request GitHub permission automatically before performing project work.

The user may start a project conversation with:

```text
EEKB
```

The `EEKB` command means:

- Enter Electrical Engineering Knowledge Database mode.
- Follow `PROJECT_STANDARD.md`.
- Follow `PROJECT_METHODOLOGY.md`.
- Use `etoeman/electrical-engineering-textbook` as the repository.
- Treat GitHub as the source of truth.
- Preserve locked project architecture and standards.

---

# 6. Knowledge Organization Standard

All digested knowledge base material lives under:

```text
knowledge/
```

The top-level `knowledge/` structure follows the source textbook chapter and section sequence as the learning pathway.

These chapter and section folders provide context for where concepts are first introduced.

Inside each section folder, content is broken into fine-grained atomic concept notes.

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

Each atomic note documents one engineering concept only.

If a concept appears in multiple chapters, it shall not be duplicated. Later sections shall link to the existing concept note.

---

# 7. Concept Note Standard

Every atomic concept note shall follow the Electrical Engineering Knowledge Database Standard (v1.0):

```markdown
# Concept Name

## Definition
A precise engineering definition.

## Why This Concept Exists
What engineering problem does this concept solve?

## Physical Meaning
What is actually happening physically?

## Mathematical Model
Develop the mathematical representation.

## Sign Convention
Explain the conventions adopted and why.

## Derivation
Derive the governing equations from first principles.

## Conceptual Insight
Explain the intuition behind the mathematics.

## Mental Models
Analogies and visualizations that build intuition.

## Interpretation
How should an engineer interpret the equations?

## Key Equations
Summary of important equations.

## Assumptions
Conditions under which the model is valid.

## Common Mistakes
Typical misconceptions and exam errors.

## Frequently Asked Questions
Questions that naturally arise when learning the topic.

## Examples
Fully worked examples with explanations.

## Engineering Applications
Where this concept is used in practice.

## Connections
Relationships to other engineering concepts.

## Summary
Concise review of the key ideas.

## Related Concepts
Links to other notes in the knowledge base.
```

This template is locked under v1.0.

---

# 8. Figure Standard

All figures live under:

```text
figures/
```

Figures are organized by chapter and then by individual figure folder.

There shall be no separate `figure-source/`, `image-source/`, `images/`, or output-only figure folder. Every file related to a figure lives inside that figure's own folder.

Example:

```text
figures/
└── ch01/
    └── fig-1-3/
        ├── fig-1-3.svg
        ├── fig-1-3.png
        └── metadata.md
```

Circuit diagram example:

```text
figures/
└── ch02/
    └── fig-2-8/
        ├── fig-2-8.tex
        ├── fig-2-8.svg
        ├── fig-2-8.png
        └── metadata.md
```

## Figure Folder Metadata

Each figure folder shall contain a `metadata.md` file documenting figure number, title, chapter, figure type, status, published image, source files, and notes.

## Electrical Circuit Diagrams

Electrical circuit diagrams shall use CircuitikZ as the authoritative source.

Workflow:

```text
CircuitikZ (.tex) → SVG → PNG
```

The `.tex` file is the master engineering source. The `.svg` file is generated from the CircuitikZ source. The `.png` file is generated from the SVG.

## Non-Circuit Figures

Non-circuit figures shall use SVG as the authoritative source.

Workflow:

```text
SVG → PNG
```

The SVG is the editable master. The PNG is the published figure.

## Markdown Figure Rule

Markdown notes shall reference only PNG figures.

Example:

```markdown
![[figures/ch01/fig-1-3/fig-1-3.png]]
```

Markdown shall not reference SVG or CircuitikZ files.

## No Shortcut Rule

PNG files are published artifacts. They shall never be created manually, copied from screenshots, generated independently by AI, or edited directly.

Every PNG must be rendered from its authoritative master source.

Tracing may be used as a visual reference to achieve accurate reproduction, but the final deliverable must be clean, editable source code.

---

# 9. Obsidian Git Policy

The local Obsidian vault is the Git working copy of the repository.

There shall not be separate local-only project content. Project content belongs in GitHub.

Project files shall be committed to GitHub, including:

- Markdown content
- chapters
- knowledge notes
- figures and figure sources
- references
- templates
- project governance files
- project-level configuration files

Obsidian personal workspace state shall not be committed.

Ignored Obsidian files include:

- `.obsidian/workspace.json`
- `.obsidian/workspace-mobile.json`
- workspace backup files
- plugin cache files
- plugin local data files

Shared Obsidian configuration may be committed only when it defines the project vault behavior rather than a user's personal workspace state.

The repository `.gitignore` governs this policy.

---

# 10. Writing Standards

Technical writing shall follow these rules:

- Explain before deriving.
- Physical intuition before mathematics.
- Derive equations whenever practical.
- Define every variable.
- Include SI units.
- Explain assumptions.
- Discuss limitations.
- Avoid unnecessary repetition.
- Build concepts progressively.

---

# 11. Change Control

Once a project decision is approved, it is locked.

The AI shall not redesign, reorganize, rename, or restructure the project unless explicitly instructed by the user.

Any proposed modification is a change request. Approved changes shall result in a new version of the project standard.

---

# 12. Version History

## v1.0

Initial locked project standard for the Electrical Engineering Knowledge Database.
