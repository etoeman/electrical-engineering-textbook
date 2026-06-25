# Digital Edition Style Guide

This repository is a digital publishing project, not a scan archive.

## Source of Truth

GitHub is the master repository. Local copies and Obsidian vaults are working views.

## Manuscript Files

- Markdown files are the master manuscript files.
- Preserve the author's technical content.
- Preserve original section, figure, and equation numbering.
- Use semantic headings rather than visual imitation of page layout.
- Use Title Case for headings that appear in all caps in the print edition.

## Equations

- Use LaTeX for displayed equations.
- Preserve original equation numbers using `\tag{}`.
- Do not renumber equations.

## Figures

- Published figures should be SVG wherever practical.
- Circuit schematics use CircuitikZ as the editable source and are exported to SVG.
- Physical diagrams, flowcharts, and conceptual illustrations are recreated as hand-authored SVG.
- Do not use AI raster images as production assets unless explicitly approved.
- Every figure should be stored as a separate file.
- Captions remain in the Markdown manuscript, not baked into the figure, unless there is a special publishing reason.

## Source Pages

- Original page images are archival material used for verification.
- Source scans are not part of the finished digital edition.

## Chapter Organization

Each chapter should eventually have its own folder:

```text
chapters/01-basic-circuit-theory/chapter.md
figures/ch01/
figure-source/ch01/
source-pages/ch01/
```

## Editorial Rule

Improve digital presentation without changing the technical meaning.