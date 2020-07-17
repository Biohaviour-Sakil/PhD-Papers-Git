TEX=pdflatex
BIB=bibtex
TARGET=Cloud_Anomaly_Detection
SOURCES=*.tex
BIBSOURCE=references.bib

all: $(TARGET).pdf

view: $(TARGET).pdf
	open $(TARGET).pdf

clean:
	rm -rf *.aux *.log *.bbl *.blg *.toc *.out *.lot *.lof *.pdf

$(TARGET).pdf: $(TARGET).tex $(SOURCES) $(TARGET).bbl
	$(TEX) $(TARGET)
	$(TEX) $(TARGET)

$(TARGET).bbl: $(SOURCES) $(BIBSOURCE)
	$(TEX) $(TARGET)
	$(BIB) $(TARGET)
	
