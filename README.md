# Mathematical Writing Notes

This repository contains the LaTeX source for a short article on mathematical writing.  
Running `latexmk` in the repository root directory generates the final PDF.

## Features

- Self-contained LaTeX project  
- Automatically builds the PDF using GitHub Actions  
- The compiled PDF is saved as an artifact  
- Automatic spell checking on every push

## Build

To compile locally:

```bash
latexmk -pdf main.tex
