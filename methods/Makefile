#  Makefile for LaTeX documents
#
TARGET = rnaseq.pdf
TOUCH=touch
PS = dvips
PDFLATEX = xelatex
LATEX = $(PDFLATEX)
BIBTEX = bibtex
PS2PDF= ps2pdf
DELETE =  *.aux *.log *.ps *.dvi *.bbl *.blg *~ $(TARGET) *.brf *.idx *.ilg *.ind *.lof *.lot *.out *.toc Body/*.aux
DVIPSFLAGS= -Pcmz -Pamz -Ppdf -G0 -tletter
TOUCH=touch
MAKE=make
MAKEIDX=makeindex

.SUFFIXES: .pdf .tex

all:
	$(LATEX) rnaseq.tex
	$(BIBTEX) rnaseq
	$(LATEX) rnaseq.tex
	$(LATEX) rnaseq.tex
clean:
	rm -f $(DELETE)
