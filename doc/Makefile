# originally forked based on https://github.com/pinga-lab/paper-tle-euler-tutorial
# Thanks to @leouieda of swung.rocks
MANUSCRIPT=overview
BIB=biblio.bib
# LATEXHEADER=-H header.tex
PANDOCARGS=-V fontsize=11pt --bibliography $(BIB) --csl=ieee.csl --filter pandoc-citeproc --standalone

all: pdf

pdf: $(MANUSCRIPT).pdf

$(MANUSCRIPT).pdf: $(MANUSCRIPT).md $(BIB) #header.tex
	pandoc $(LATEXHEADER) $(PANDOCARGS) $< -o $(MANUSCRIPT).tex
	# this is executed multiple times so the references are updated
	pdflatex $(MANUSCRIPT).tex
	pdflatex $(MANUSCRIPT).tex
	pdflatex $(MANUSCRIPT).tex

doc: $(MANUSCRIPT).doc

$(MANUSCRIPT).doc: $(MANUSCRIPT).md $(BIB)
	pandoc $(PANDOCARGS) $< -o $@

odt: $(MANUSCRIPT).odt

$(MANUSCRIPT).odt: $(MANUSCRIPT).md $(BIB)
	pandoc $(PANDOCARGS) $< -o $@

wordcount:
	@echo "Word count:"
	@wc -w $(MANUSCRIPT).md

clean:
	rm -f $(MANUSCRIPT).tex $(MANUSCRIPT).pdf *.aux *.bbl *.log *.out *.blg *.fff *.lof *.toc
