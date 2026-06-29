# Review Tracking

This folder tracks issues and improvements discovered while building the digital edition.

Each item should be tracked as its own Markdown file so it can be reviewed, discussed, resolved, and linked from the manuscript.

## Categories

```text
reviews/
├── technical/
├── pedagogy/
└── digital/
```

## Technical Errors

Use for objective technical problems in the original book:

- incorrect polarity
- wrong equation
- incorrect sign convention
- incorrect unit
- incorrect answer
- inaccurate figure
- inconsistent notation

File naming:

```text
reviews/technical/EE-0001.md
```

## Pedagogical Improvements

Use when the original content is technically correct but could be taught better:

- unclear explanation
- missing intuition
- weak example order
- better figure needed
- missing derivation step
- better analogy or application

File naming:

```text
reviews/pedagogy/PED-0001.md
```

## Digital Enhancements

Use for improvements made possible by a digital edition:

- interactive figures
- animations
- simulations
- hyperlinks
- collapsible derivations
- embedded calculators
- generated glossaries or indexes

File naming:

```text
reviews/digital/DIG-0001.md
```

## Standard Issue Template

```markdown
---
id: EE-0001
type: technical-error
status: open
priority: medium
location:
  chapter:
  section:
  page:
  figure:
reported_by: Bernard Hurtault
date_reported:
---

# Short Issue Title

## Issue

Describe the problem clearly.

## Evidence

Explain why this is an issue. Include equations, figure references, or reasoning.

## Recommendation

Describe the proposed correction or improvement.

## Resolution

Leave blank until resolved.
```
