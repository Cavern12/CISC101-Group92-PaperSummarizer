# Module 02 — Section Loop
# CHANGE LOG (v2)
- Added summary_level variable.
- Added conditional behavior for short vs detailed summaries.
- Added bullet list generation.
- Enforced ≤150-word section limit.

## Overview
This module summarizes each normalized section while enforcing evidence constraints and summary options.

## Variables
summary_level = "short" | "detailed"

## Loop Logic
FOR each section in [Introduction, Model Architecture, Results, Conclusion]:

   IF section flag == missing:
        output: "Section skipped: no usable text was provided."
        CONTINUE

   IF section flag == short:
        output warning:
          "Section very short: summary may be incomplete."

   IF summary_level == "short":
        • Generate a compact 1–2 sentence summary (≤ 60 words).
        • Do NOT include bullets.

   IF summary_level == "detailed":
        • Generate a paragraph summary (≤ 150 words).
        • THEN produce a bullet list (3–5 items) capturing:
            - main claim
            - methods
            - findings
            - terminology
            - implications

   Apply terminology consistency from PS2.
   Enforce no-hallucination and evidence mode constraints.

END LOOP
