

This repository contains material related to Jarmo Kivekäs' thesis work at Turku University of Applied Sciences.


# Compiling documentation

Much of the work is documented in either markdown (.md) files or Jupyter notebooks (.ipynb). In order to use these in a user friendly manner, some software is needed.

## Pandoc

The actual thesis document is converted from markdown to pdf via LaTeX using `pandoc`

The required apt-get packages are `pandoc` and `pandoc-citeproc`. The latter is needed for properly handling citations in the markdown documents.



```
pandoc -s -S --bibliography biblio.bib --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.pdf
```

For creating a standalone tex file with all the appropriate pre-document mess

````
pandoc -s -S  --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.tex --standalone
```

pandoc --biblio bibliography.bib --biblatex -o overview.md.pdf overview.md
pandoc --filter pandoc-citeproc --biblio bibligrapy.bib overview.md  -o overview.md.pdf
pandoc -s -S --bibliography biblio.bib --filter pandoc-citeproc --csl ieee.csl overview.md -o overview.md.pdf
pandoc -s -S --bibliography biblio.json --filter pandoc-citeproc --csl chicago-fullnote-bibliography.csl CITATIONS -o example24b.html
pandoc -s -S --bibliography biblio.yaml --filter pandoc-citeproc --csl ieee.csl CITATIONS -t man -o example24c.1
```
