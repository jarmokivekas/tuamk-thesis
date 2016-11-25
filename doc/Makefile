# originally forked based on https://github.com/pinga-lab/paper-tle-euler-tutorial
# Thanks to @leouieda of swung.rocks
MANUSCRIPT=overview
BIB=biblio.bib
PREAMBLE=preamble.tex
POSTAMBLE=postamble.tex
# PANDOCARGS=-V --bibliography $(BIB) --csl=ieee.csl --filter pandoc-citeproc
PANDOCARGS=
BUILDDIR=build

MDFILES=overview.md abstract.md
TEXTARGETS=$(patsubst %.md,%.tex,$(MDFILES))
TEXFILES=$(wildcard *.tex)

all: pdf

pdf: thesis.pdf


%.tex: %.md
	pandoc  $(PANDOCARGS) $< -o $@

thesis.pdf: $(TEXTARGETS) $(TEXFILES)
	# this is executed multiple times so the references are updated
	pdflatex thesis
	bibtex thesis
	pdflatex thesis
	pdflatex thesis


wordcount:
	@echo "Word count:"
	@wc -w $(MANUSCRIPT).md

test:
	# $(MDFILES)
	# $(TEXTARGETS)
	# $(TEXFILES)

clean:
	rm -f $(TEXTARGETS) thesis.pdf *.aux *.bbl *.log *.out *.blg *.fff *.lof *.toc
