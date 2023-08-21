# Makefile for LaTeX to PDF conversion with multiple compilations and cleaning

# Get a list of all .tex files in the current directory (excluding extension)
TEX_FILES = $(basename $(wildcard *.tex))

# LaTeX compiler command
LATEX_COMPILER = platex

# Command to convert DVI to PDF
DVI_TO_PDF_CONVERTER = dvipdfmx

# Flags for the LaTeX compiler
LATEX_FLAGS = -kanji=utf

# Number of times to compile for generating dependent files (e.g., .toc)
NUM_COMPILE = 2

# Makefile rules
all: $(addsuffix .pdf, $(TEX_FILES))
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb *.dvi *.fls *.fdb_latexmk
	@echo "Compilation and cleaning completed."
	

%.pdf: %.tex
	$(LATEX_COMPILER) $(LATEX_FLAGS) $<
	for i in $(shell seq 2 $(NUM_COMPILE)); do \
		$(LATEX_COMPILER) $(LATEX_FLAGS) $<; \
	done
	$(DVI_TO_PDF_CONVERTER) $(basename $<).dvi

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb *.dvi *.fls *.fdb_latexmk *.pdf

.PHONY: all clean
