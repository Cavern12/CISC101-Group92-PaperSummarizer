# Module 05 — Citation Extractor

## Purpose
Extract all in-text citations and create a reference awareness list.

## Behavior
- Scan the paper for citations of the form:
  - (Author, Year)
  - Author et al. (Year)
  - [Numbered citations]

- Build a list of all detected citation markers.
- Note if citations appear but are not summarized in the main text.
- Output:
   - "Detected citations:"
   - list of all markers found.

## Warning Rules
If a citation is referenced but no context is provided:
   - output:
     "Warning: Citation mentioned without surrounding explanatory text."
