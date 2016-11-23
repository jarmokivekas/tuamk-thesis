# originally forked based on https://github.com/pinga-lab/paper-tle-euler-tutorial
# Thanks to @leouieda of swung.rocks
MANUSCRIPT=overview
BIB=biblio.bib
PREAMBLE=preamble.tex
POSTAMBLE=postamble.tex
PANDOCARGS=-V fontsize=11pt --bibliography $(BIB) --csl=ieee.csl --filter pandoc-citeproc

all: pdf

pdf: $(MANUSCRIPT).pdf
tex: $(MANUSCRIPT).tex

$(MANUSCRIPT).tex: $(MANUSCRIPT).md $(BIB) $(PREAMBLE)
	pandoc  $(PANDOCARGS) $< -o $(MANUSCRIPT).tex
	cat $(PREAMBLE) $(MANUSCRIPT).tex $(POSTAMBLE) > $(MANUSCRIPT)-tmp.tex
	mv $(MANUSCRIPT)-tmp.tex $(MANUSCRIPT).tex

$(MANUSCRIPT).pdf: $(MANUSCRIPT).tex
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
