MANUSCRIPT=overview
BIB=biblio.bib
# LATEXHEADER=-H header.tex
PANDOCARGS=-V fontsize=11pt --bibliography $(BIB) --csl=ieee.csl --filter pandoc-citeproc --standalone

all: pdf

pdf: $(MANUSCRIPT).pdf

$(MANUSCRIPT).pdf: $(MANUSCRIPT).md $(BIB) #header.tex
	pandoc $(LATEXHEADER) $(PANDOCARGS) $< -o $(MANUSCRIPT).tex
	# pdflatex $(MANUSCRIPT).tex
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
