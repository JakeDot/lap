# LaTeX PDF Build Repository

This repository contains a GitHub Actions workflow to automatically build LaTeX documents into PDF format and upload them as workflow artifacts.

## GitHub Actions Workflow

The workflow `.github/workflows/build-latex-pdf.yml`:
- Triggers on `push` and `pull_request` events.
- Sets up TeX Live environment with required packages (`scheme-basic`, `latexmk`, `texlive-latex-recommended`, `texlive-latex-extra`, `texlive-fonts-recommended`, `texlive-fonts-extra`).
- Automatically detects `paper.tex` or the first `.tex` file in the root directory.
- Compiles the LaTeX document using `latexmk -pdf`.
- Uploads any generated `.pdf` files as an artifact named `pdf`.
