# Module 03 — Guardrails

## Purpose
Provide basic safety rules so the summarizer stays accurate and does not hallucinate.

## Rules

- Only summarize information that appears in the paper text.
- Do not invent extra sections, results, or citations.
- If a section has very little text, mention that the summary may be incomplete.
- If a section is completely missing, state clearly that there was no text to summarize.
- Keep the academic tone consistent across sections.

## Long Papers
For very long papers, the system may break the text into smaller pieces and summarize each one
before combining them into an overall summary.
