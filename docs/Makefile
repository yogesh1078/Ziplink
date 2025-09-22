# Makefile for LaTeX document compilation

# Document name (without .tex extension)
DOC = system-design

# LaTeX compiler
LATEX = pdflatex

# Output directory
OUTDIR = build

# Source files
TEXFILE = $(DOC).tex

# Create output directory if it doesn't exist
$(OUTDIR):
	mkdir -p $(OUTDIR)

# Build the PDF
$(OUTDIR)/$(DOC).pdf: $(TEXFILE) | $(OUTDIR)
	$(LATEX) -interaction=nonstopmode -output-directory=$(OUTDIR) $(TEXFILE)
	$(LATEX) -interaction=nonstopmode -output-directory=$(OUTDIR) $(TEXFILE)  # Run twice for cross-references

# Default target
all: $(OUTDIR)/$(DOC).pdf

# Clean build files
clean:
	rm -rf $(OUTDIR)

# Clean and rebuild
rebuild: clean all

# Install LaTeX dependencies (for Ubuntu/Debian)
install-deps:
	sudo apt-get update
	sudo apt-get install -y texlive-latex-base texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra

# View the PDF (if available)
view: $(OUTDIR)/$(DOC).pdf
	xdg-open $(OUTDIR)/$(DOC).pdf 2>/dev/null || open $(OUTDIR)/$(DOC).pdf 2>/dev/null || echo "Please open $(OUTDIR)/$(DOC).pdf manually"

.PHONY: all clean rebuild install-deps view

# Help target
help:
	@echo "Available targets:"
	@echo "  all         - Build the PDF document (default)"
	@echo "  clean       - Remove build files"
	@echo "  rebuild     - Clean and rebuild"
	@echo "  install-deps- Install LaTeX dependencies"
	@echo "  view        - Open the PDF in default viewer"
	@echo "  help        - Show this help message"