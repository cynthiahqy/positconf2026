# Invited Talk, MelbURN/SSA

2025-08-05

## Reusing ‘ggplot2’ code: how to design better plot helper functions

## Abstract

> Wrapping ‘ggplot2’ code into plot helper functions is a common way to make multiple versions of a custom plot without copying and pasting the same code over and over again. Helper functions can replace long and complex ‘ggplot2’ code chunks with just a single function call. However, if that single function is not designed carefully, the initial convenience can often turn into frustration. While helper functions can reduce the amount of code needed to remake a complicated plot, they often mask the underlying layered grammar of graphics, complicating further customisation and tweaking of the plot. This talk addresses how to design effective ‘ggplot2’ plot helper functions that maximise reuse convenience whilst preserving access to the elegant flexibility of layered plot composition. By studying existing ‘ggplot2’ extensions for producing calendar plots, we identify a number of common pitfalls, including overly specific function arguments and hidden data manipulations. Then, propose a strategy for avoiding these pitfalls and retain the benefits of ‘ggplot2’ by: separating data preparation from plotting, utilising list arguments for customisation, and providing transparent documentation. We illustrate these strategies using examples from the design of the ‘ggtilecal’ package, which provides helper functions for plotting calendars using the geom_tile() geometry from ggplot2.

