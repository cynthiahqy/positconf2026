# Talk, posit::conf(2026)

**Date:** TBC
**Event:** TBC

📊 **Slides:** <https://cynthiahqy.github.io/positconf2026/>

## Reuse your custom ggplot2 with transparent helper functions!

## Abstract

> Wrapping 'ggplot2' code into plot helper functions is a common way to make
> multiple versions of a custom plot without copying and pasting the same code
> over and over again. Helper functions can replace long and complex 'ggplot2'
> code chunks with just a single function call. However, if that single function
> is not designed carefully, the initial convenience can often turn into
> frustration. While helper functions can reduce the amount of code needed to
> remake a complicated plot, they often mask the underlying layered grammar of
> graphics, complicating further customisation and tweaking of the plot. This
> talk addresses how to design effective 'ggplot2' plot helper functions that
> maximise reuse convenience whilst preserving access to the elegant flexibility
> of layered plot composition. By studying existing 'ggplot2' extensions for
> producing calendar plots, we identify a number of common pitfalls, including
> overly specific function arguments and hidden data manipulations. Then, propose
> a strategy for avoiding these pitfalls and retain the benefits of 'ggplot2' by:
> separating data preparation from plotting, utilising list arguments for
> customisation, and providing transparent documentation. We illustrate these
> strategies using examples from the design of the 'ggtilecal' package, which
> provides helper functions for plotting calendars using the `geom_tile()`
> geometry from ggplot2.

## Design principles

The talk builds to three principles for a *transparent* helper function:

1. **SEPARATE** data preparation from plot assembly, into modular internals.
2. **EXPOSE** ggplot2 components as list arguments, rather than burying them
   behind plot-specific arguments.
3. **DOCUMENT** the customisation pointers, so users know which seams they can
   reach into.

## Repository contents

| Path | What it is |
| --- | --- |
| `slides-v2.qmd` | The talk, as a Quarto reveal.js presentation |
| `_style.scss` | Custom slide styling (see the class reference below) |
| `assets/notability-v2/` | Hand-drawn sketches, trimmed and made transparent |
| `assets/code-blocks/` | Example plots from the calendar extensions compared |
| `slides.qmd` | Earlier version of this talk, given at MelbURN/SSA (2025-08-05) |

## Building

```bash
quarto render slides-v2.qmd
```

Outputs `slides-v2.html` (reveal.js) and `slides-v2.pptx`.

## Publishing

Slides are published to GitHub Pages from the `gh-pages` branch:

```bash
quarto publish gh-pages slides-v2.qmd
```

## Previous version

This talk was previously given as an invited talk at MelbURN/SSA on 2025-08-05,
under the title *Reusing 'ggplot2' code: how to design better plot helper
functions* — <https://www.statsoc.org.au/event-6260056>
