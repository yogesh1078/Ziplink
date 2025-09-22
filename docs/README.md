# Ziplink Documentation

This directory contains the system design documentation for the Ziplink URL shortener application.

## Files

- `system-design.tex` - Main LaTeX document containing the complete system design
- `Makefile` - Build automation for compiling the LaTeX document
- `README.md` - This file

## Building the Documentation

### Prerequisites

You need LaTeX installed on your system. For Ubuntu/Debian systems, you can install the required packages using:

```bash
make install-deps
```

Or manually install:

```bash
sudo apt-get install texlive-latex-base texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra
```

### Building

To build the PDF documentation:

```bash
make all
```

Or simply:

```bash
make
```

The compiled PDF will be available at `build/system-design.pdf`.

### Other Commands

- `make clean` - Remove build files
- `make rebuild` - Clean and rebuild
- `make view` - Open the PDF in your default viewer
- `make help` - Show all available commands

## Figure Placement Strategy

This documentation implements the following LaTeX figure placement strategies as requested:

1. **Flexible Placement Options**: Uses `[!htbp]` and `[!ht]` placement specifiers instead of restrictive `[p]` options
2. **Float Package**: Includes the `float` package for `[H]` option when absolute positioning is needed
3. **Strategic Placement**: Diagrams are placed close to their referencing text to improve readability
4. **Proper References**: All figures are properly cross-referenced in the text using `\ref{}`

### Figure Placement Options Used

- `[!ht]` - Prioritizes "here" and "top" placement
- `[!htbp]` - Gives LaTeX maximum flexibility: here, top, bottom, or page
- `[H]` - Absolute positioning for critical diagrams (using float package)

This approach ensures that diagrams appear close to their related text sections, preventing readers from having to flip between pages unnecessarily.

## Document Structure

The system design document includes:

1. **Introduction** - Overview of the Ziplink application
2. **System Architecture Overview** - High-level architecture diagram
3. **Frontend Architecture** - Component hierarchy and structure
4. **Backend API Design** - RESTful API structure
5. **Database Schema** - MongoDB collections and relationships
6. **URL Shortening Algorithm** - Workflow and process diagrams
7. **Security Considerations** - Multi-layered security architecture
8. **Deployment Architecture** - Production deployment setup
9. **Performance Optimization** - Optimization strategies across all layers
10. **Conclusion** - Summary and key benefits

Each section includes relevant diagrams created with TikZ, positioned optimally near their explanatory text.