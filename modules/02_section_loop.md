> Branch v2 note: this version adds summary_level logic and detailed bullet lists.
# Module 02 — Section Loop

## Overview
This module summarizes each normalized section of the paper in order.

## Behavior
FOR each section in [Introduction, Model Architecture, Results, Conclusion]:

   IF section is missing:
        output a short note that this section was not provided.
        CONTINUE

   Generate a concise summary of the section
   (aim for 2–3 sentences and keep the length under 150 words).

   Use terminology from the original paper (e.g., encoder–decoder, self-attention).
   Maintain academic tone.
   Avoid adding information that is not present in the text.

END LOOP
