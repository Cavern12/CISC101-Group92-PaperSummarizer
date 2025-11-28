# Module 01 — Intake & Setup

## Purpose
Prepare all inputs, normalize sections, detect missing content, and initialize parameters for downstream modules.

## Responsibilities
- Accept the full paper text.
- Extract or detect section boundaries.
- Normalize section names to:
  - Introduction
  - Model Architecture
  - Results
  - Conclusion
- Identify missing or <50-word sections.

## Parameter Initialization
- summary_level = "short" | "detailed"
- audience = "expert" | "lay"
- evidence_mode = "default" | "strict"

## Missing/Short Section Flags
For each section:
- If section missing → flag as “missing”
- If < 50 words → flag as “short”

These flags will be used in Modules 2–4.

## Hand-Off
Pass the normalized section dictionary + flags into Module 02.
