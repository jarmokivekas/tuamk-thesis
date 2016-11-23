

This repository contains material related to Jarmo Kivekäs' thesis work at Turku University of Applied Sciences.


# Compiling documentation

Much of the work is documented in either markdown (.md) files or Jupyter notebooks (.ipynb). In order to use these in a user friendly manner, some software is needed.

## Pandoc

The actual thesis document is converted from markdown to pdf via LaTeX using `pandoc`

The required apt-get packages are `pandoc` and `pandoc-citeproc`. The latter is needed for properly handling citations in the markdown documents.

Rough pdf preview:

    pandoc -s -S --bibliography biblio.bib --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.pdf

For creating a standalone tex file with all the appropriate pre-document mess

    pandoc -s -S  --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.tex --standalone
