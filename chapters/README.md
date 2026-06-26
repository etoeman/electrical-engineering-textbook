# Chapter Manuscript Policy

Each chapter may contain two manuscript tracks.

## Original Track

```text
original.md
```

This file preserves the original book as faithfully as possible:

- original wording
- original section order
- original figure numbering
- original equation numbering
- original technical claims, even when questionable

Corrections are not silently inserted into this file. If an error is suspected, create a review item under `reviews/technical/`.

## Improved Track

```text
improved.md
```

This file is the revised teaching edition:

- clearer explanations
- corrected known errors
- improved examples
- better sequencing where appropriate
- links to digital resources
- references to review items when changes are based on identified issues

## Current Transitional Files

Some early work may use:

```text
chapter.md
```

Those files should be treated as transitional drafts until split into `original.md` and `improved.md`.

## Recommended Chapter Folder

```text
chapters/01-basic-circuit-theory/
├── original.md
├── improved.md
└── README.md
```
