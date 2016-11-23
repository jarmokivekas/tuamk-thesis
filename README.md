

This repository contains material related to Jarmo Kivekäs' thesis work at Turku University of Applied Sciences.


# Compiling documentation

Much of the work is documented in either markdown (.md) files or Jupyter notebooks (.ipynb). In order to use these in a user friendly manner, some software is needed.

Use the Makefile in the `/doc` directory:

    cd doc
    make all

## Pandoc

The actual thesis document is converted from markdown to pdf via LaTeX using `pandoc`

The required apt-get packages are `pandoc` and `pandoc-citeproc`. The latter is needed for properly handling citations in the markdown documents.

Rough pdf preview:

    pandoc -s -S --bibliography biblio.bib --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.pdf

For creating a standalone tex file with all the appropriate pre-document mess

    pandoc -s -S  --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.tex --standalone


# Meta

use the command

    \rule{\textwidth}{\textheight}

to make a text body sized box

tool versions

    pandoc 1.16.0.2
    Compiled with texmath 0.8.4.1, highlighting-kate 0.6.1


    pdfTeX 3.14159265-2.6-1.40.16 (TeX Live 2015/Debian)
    kpathsea version 6.2.1
