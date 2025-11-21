# Mathematical Writing Notes

This repository contains the LaTeX source for a short article on mathematical writing.  
Running `latexmk` in the repository root directory generates the final PDF.

## Features

- Self-contained LaTeX project  
- Automatically builds the PDF using GitHub Actions  
- Automatic spell checking on every push

## Build

To compile locally:

```bash
latexmk -pdf main.tex

```markdown
## GitHub Actions Workflows

This repository includes two GitHub Actions workflows located under `.github/workflows/`:

### 1. `build.yml`
- Triggered on every `push`.
- Automatically compiles `main.tex` using `latexmk`.
- Uploads the generated PDF as an **artifact** named `pdf-output`.
- You can download the latest compiled PDF by:
  1. Opening the **Actions** tab,
  2. Selecting the most recent **Build PDF** run,
  3. Scrolling to the **Artifacts** section,
  4. Downloading `pdf-output.zip`.

### 2. `spell.yml`
- Also triggered on every `push`.
- Runs a spell checker (`codespell`) on all files in the repository.
- Reports any potential spelling issues inside the GitHub Actions log.

These workflows ensure that every update to the repository keeps the PDF up-to-date and that the source files remain free of common spelling mistakes.
