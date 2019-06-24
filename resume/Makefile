PROJ = cui-resume
FILES = $(wildcard *.tex)

$(PROJ).pdf: $(FILES)
	pdflatex $(PROJ).tex
	pdflatex $(PROJ).tex

show:
	evince $(PROJ).pdf

clean:
	rm -f $(PROJ).pdf *.dvi *.aux *.log *.blg *.bbl *~
