# Module 03 — Guardrails
# CHANGE LOG (v2)
- Added strict evidence mode.
- Added standardized missing/short section warnings.
- Strengthened hallucination controls.

## Evidence Mode
evidence_mode = "default" | "strict"

IF evidence_mode == "strict":
   • Only include information explicitly present in the source text.
   • No inferred results.
   • No invented equations.
   • If insufficient evidence:
         output:
         "The source text does not provide enough detail to summarize this section in strict evidence mode."

## Missing/Short Section Rules
IF section missing:
     output:
     "Section skipped: no usable text was provided."

IF section < 50 words:
     output:
     "Section very short: summary may be incomplete."

## Hallucination Safeguards
- Never fabricate content.
- Never invent subsections, citations, datasets, or methods.
- Only refer to entities explicitly present in the text.

## Chunking Strategy (PS2 Requirement)
For long papers:
1. Split text into chunks below model token limits.
2. Summarize each chunk.
3. Merge into hierarchical summaries.
