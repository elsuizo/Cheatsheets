SHELL := /bin/bash

LATEX=latex
#pdf latex options
#PDFLATEX=pdflatex
PDFLATEX=xelatex
DVI=dvips
PS=ps2pdf
FILE_NAME=algebra
PDFLATEX_OPTS=-interaction=nonstopmode -halt-on-error -shell-escape

TEX_FILE=$(FILE_NAME).tex
DVI_FILE=$(FILE_NAME).dvi
PS_FILE=$(FILE_NAME).ps

.PHONY: all pdf clean

all : pdf

pdf: $(TEX_FILE)
	$(LATEX) $(PDFLATEX_OPTS) $(TEX_FILE)
	$(DVI) $(DVI_FILE)
	$(PS) $(PS_FILE)

pd: $(TEX_FILE)
	$(PDFLATEX) $(PDFLATEX_OPTS) $(TEX_FILE)
clean:
	rm -fv *.{aux,log,nav,out,snm,toc,vrb}
