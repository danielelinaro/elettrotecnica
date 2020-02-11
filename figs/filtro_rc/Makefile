
TEX := latex
DVIPS := dvips
PS2EPS := ps2eps
EPS2PDF := epstopdf
RM := rm -f
MV := mv
SED := sed
EXTENSION := .eps

all: filter clean

filter:
	$(RM) tmp.*
	$(SED) 's/SCHEMATIC/RC_filter/' template.tex > tmp.tex
	$(TEX) tmp.tex
	$(DVIPS) tmp.dvi
	$(PS2EPS) tmp.ps
	$(EPS2PDF) tmp$(EXTENSION)
	$(MV) tmp.pdf RC_filter.pdf

clean:
	rm -f tmp.*
	rm -f *.aux
	rm -f *.log

