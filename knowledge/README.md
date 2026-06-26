# Knowledge Base

This folder separates engineering knowledge from the linear book manuscript.

The `book/` or `chapters/` files preserve the textbook structure. The `knowledge/` folder organizes concepts, equations, figures, examples, and glossary terms so the material can be searched, reused, linked, and eventually turned into learning paths, reference pages, quizzes, or interactive lessons.

## Structure

```text
knowledge/
├── concepts/
├── equations/
├── examples/
├── figures/
├── glossary/
└── maps/
```

## Concept Files

Each concept should eventually have its own file:

```text
knowledge/concepts/thevenin-equivalent.md
knowledge/concepts/kirchhoffs-current-law.md
knowledge/concepts/phasor.md
```

Concept files should link back to the book sections where the concept appears.

## Equation Files

Important equations should eventually have their own files:

```text
knowledge/equations/ohms-law.md
knowledge/equations/kirchhoffs-current-law.md
```

## Figure Metadata Files

Figure artwork remains in `figures/`, while metadata and teaching notes live here:

```text
knowledge/figures/fig-1-1.md
```

## Maps

Maps describe relationships:

- concept prerequisites
- chapter-to-concept mapping
- equation dependencies
- figure usage
- review-item links

## Principle

The book is one presentation of the knowledge. The knowledge base is the reusable intellectual structure behind the book.
