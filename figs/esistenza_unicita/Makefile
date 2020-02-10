
TEX := latex
DVIPS := dvips
PS2EPS := ps2eps
EPS2PDF := epstopdf
RM := rm -f
MV := mv
SED := sed
EXTENSION := .eps

all: ckt1 ckt2 clean

ckt1:
	$(RM) tmp.*
	$(SED) 's/SCHEMATIC/ckt_1/' template.tex > tmp.tex
	$(TEX) tmp.tex
	$(DVIPS) tmp.dvi
	$(PS2EPS) tmp.ps
	$(EPS2PDF) tmp$(EXTENSION)
	$(MV) tmp.pdf ckt_1.pdf

ckt2:
	$(RM) tmp.*
	$(SED) 's/SCHEMATIC/ckt_2/' template.tex > tmp.tex
	$(TEX) tmp.tex
	$(DVIPS) tmp.dvi
	$(PS2EPS) tmp.ps
	$(EPS2PDF) tmp$(EXTENSION)
	$(MV) tmp.pdf ckt_2.pdf

graph:
	$(RM) tmp.*
	$(SED) 's/SCHEMATIC/graph/' template.tex > tmp.tex
	$(TEX) tmp.tex
	$(DVIPS) tmp.dvi
	$(PS2EPS) tmp.ps
	$(EPS2PDF) tmp$(EXTENSION)
	$(MV) tmp.pdf graph.pdf

clean:
	rm -f tmp.*
	rm -f *.aux
	rm -f *.log

