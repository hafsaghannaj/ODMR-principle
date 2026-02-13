# Changelog

All notable changes to this project will be documented in this file.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [0.1.0] — 2026-02-13

### Added
- Python figure generation pipeline (`scripts/generate_figures.py`)
  - Fig 3: Zeeman splitting ODMR spectra (Lorentzian dip model, B = 0/3/5 mT)
  - Fig 6: Temperature shift of zero-field splitting D(T)
- Output formats: PNG (300 DPI), SVG, and PDF for each figure
- TikZ source files for figures 1, 2, 4, 5 (`diagrams/source/tikz/`)
- TikZ-to-image conversion script (`scripts/tikz2png.py`)
- Docker containerization for reproducible builds
- GitHub Actions CI workflow (`.github/workflows/reproducibility.yml`)
- Physical parameter documentation (`PARAMETERS.md`)
- Theory and experimental setup docs (`docs/theory.md`, `docs/experimental.md`)
- Dual licensing: MIT for code, CC-BY-4.0 for figures
- Machine-readable citation metadata (`CITATION.cff`)
