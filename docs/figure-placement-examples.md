# Figure Placement Examples

This document demonstrates the difference between various LaTeX figure placement options that address the issue described in the problem statement.

## Before (Problematic)

Using restrictive placement like `[p]` (page floats):
- Figures appear on separate pages
- Text and diagrams are far apart
- Readers must flip between pages

## After (Solution Implemented)

### Option 1: Flexible Placement `[!htbp]`
```latex
\begin{figure}[!htbp]
    % diagram content
    \caption{Description}
    \label{fig:example}
\end{figure}
```
- `!` - Override LaTeX's internal float parameters
- `h` - Try to place here first
- `t` - Try top of page
- `b` - Try bottom of page
- `p` - Allow float page as last resort

### Option 2: Prioritized Placement `[!ht]`
```latex
\begin{figure}[!ht]
    % diagram content
    \caption{Description}
    \label{fig:example}
\end{figure}
```
- Prioritizes "here" or "top" placement
- Keeps figures close to referencing text

### Option 3: Fixed Placement `[H]` (using float package)
```latex
\usepackage{float}
\begin{figure}[H]
    % diagram content
    \caption{Description}
    \label{fig:example}
\end{figure}
```
- Forces figure to appear exactly where defined
- No floating behavior
- Guaranteed proximity to text

## Implementation in system-design.tex

The system design document implements all these strategies:

1. **Includes float package**: `\usepackage{float}`
2. **Uses `[!ht]` placement**: For critical diagrams that should stay near text
3. **Uses `[!htbp]` placement**: For flexibility when exact positioning isn't critical
4. **Uses `[H]` placement**: For workflow diagrams that must appear in sequence
5. **Proper referencing**: All figures have labels and are referenced in text

This ensures optimal readability by keeping diagrams and explanatory text together.