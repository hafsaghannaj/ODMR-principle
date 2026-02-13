# Release: vX.Y.Z

**Date:** YYYY-MM-DD

## Summary

Brief description of this release (1–2 sentences).

## Changes

### Figures

- [ ] New figures added: (list filenames)
- [ ] Existing figures modified: (list filenames and describe changes)
- [ ] No figure changes

### Theory / Documentation

- [ ] Theory content updated: (describe)
- [ ] Experimental documentation updated: (describe)
- [ ] No documentation changes

### Scripts / Infrastructure

- [ ] `generate_figures.py` modified: (describe)
- [ ] `tikz2png.py` modified: (describe)
- [ ] Dependencies updated: (list changes to `requirements.txt`)
- [ ] No script changes

## Reproducibility Check

- [ ] `python generate_figures.py` completes without errors
- [ ] `python tikz2png.py` completes without errors (if TeX available)
- [ ] Output figures match expected results
- [ ] All random seeds are fixed; output is deterministic

## Versioning

This project uses semantic versioning:

- **Major** (X): Incompatible changes to figure content or repository structure
- **Minor** (Y): New figures, new documentation sections, or significant enhancements
- **Patch** (Z): Corrections, style adjustments, dependency updates

## Checklist

- [ ] `CITATION.cff` version field updated
- [ ] README reflects any new or changed figures
- [ ] All output formats (PNG, SVG, PDF) regenerated
- [ ] No uncommitted changes in working tree
