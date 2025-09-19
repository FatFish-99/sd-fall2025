# ==========================
# Makefile for CV.tex
# ==========================

# Main LaTeX file
TEXFILE = resume.tex
PDF = $(TEXFILE:.tex=.pdf)

# Commands
LATEX = pdflatex
VIEWER = open    # MacOS
# VIEWER = xdg-open  # Linux
# VIEWER = start     # Windows (Git Bash)

# ==========================
# Targets
# ==========================

# Default: compile the PDF
all: $(PDF)

# Compile LaTeX into PDF (run twice for references, etc.)
$(PDF): $(TEXFILE)
	$(LATEX) $(TEXFILE)
	$(LATEX) $(TEXFILE)

# Open the compiled PDF
view: $(PDF)
	$(VIEWER) $(PDF)

# Clean up temporary files
clean:
	rm -f *.aux *.log *.out *.toc *.synctex.gz *.xml *.xmpi *.bcf

# Clean everything, including the PDF
distclean: clean
	rm -f $(PDF)

.PHONY: all clean distclean view
