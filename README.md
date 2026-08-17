# latex-knots

`knotdiag` is a small LaTeX package for inline, oriented knot diagrams
and skein calculations. It wraps TikZ's `knots` and `hobby` libraries
with named diagrams, crossing changes, consistent crossing gaps, and
direction arrows.

```latex
\usepackage{knotdiag}

\[
  \nablaknot{figureeight}
  \qquad
  \kd[change=2]{figureeight}
  \qquad
  \skeinrel
\]
```

Global and per-diagram options include `scale`, `line width`, `gap`,
`arrows`, `flip`, and `change`.

## Examples

- `examples/conway-figure-eight.tex` gives the full skein calculation
  \(\nabla(4_1)=1-z^2\).
- `examples/gallery.tex` shows named diagrams, crossing changes, a local
  skein triple, and custom coloured strands.

Compile from the repository root with:

```sh
TEXINPUTS=.: pdflatex examples/conway-figure-eight.tex
TEXINPUTS=.: pdflatex examples/gallery.tex
```

Requires a recent TeX distribution with TikZ, `spath3`, `hobby`,
`amsmath`, and `expl3`.