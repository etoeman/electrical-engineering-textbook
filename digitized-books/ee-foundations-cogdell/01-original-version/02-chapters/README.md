# Chapters

This folder contains the digital textbook section files.

The chapter structure follows the locked EEKB production standard:

- one folder per chapter;
- one Markdown file per textbook section;
- separate artifacts for the Digital Edition, Enhanced Edition, and Section Review.

## Chapter Folder Pattern

```text
chapters/
└── 01-basic-circuit-theory/
    ├── README.md
    ├── 1.1-introduction-to-electrical-engineering.md
    ├── 1.1-introduction-to-electrical-engineering-enhanced.md
    ├── 1.1-introduction-to-electrical-engineering-review.md
    ├── 1.2-physical-basis-of-circuit-theory.md
    ├── 1.2-physical-basis-of-circuit-theory-enhanced.md
    └── 1.2-physical-basis-of-circuit-theory-review.md
```

## Digital Edition

The base section file is the faithful digital recreation of the original textbook section.

Example:

```text
1.3-current-and-kirchhoffs-current-law.md
```

The Digital Edition preserves the original wording, equations, examples, figures, notation, and technical claims except for transcription corrections.

## Enhanced Edition

The enhanced section file is the corrected and improved teaching version.

Example:

```text
1.3-current-and-kirchhoffs-current-law-enhanced.md
```

The Enhanced Edition may correct technical errors, improve explanations, add conceptual insight, improve notation, and add teaching support.

## Section Review

The review section file records editorial observations and recommended improvements.

Example:

```text
1.3-current-and-kirchhoffs-current-law-review.md
```

The Section Review explains why changes are made in the Enhanced Edition.

## Figure References

Markdown section files reference only PNG figures.

Figure source and published outputs live under `figures/` according to the locked figure standard.
