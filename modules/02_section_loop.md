<!-- Change Log (2025-12-04)
- Added `summary_level` variable to control short vs detailed summaries.
- Implemented conditional logic for 1–2 sentence summaries (short mode).
- Implemented detailed mode: paragraph plus 3–5 key-point bullet list.
-->

# Module 2: Section Loop

## Purpose
Iterate through each section of the paper and generate summaries according to the selected summary level.

## Workflow
1. For each section:
   - Identify the overarching idea.
   - Extract key quotes and citations.
   - Use the `summary_level` variable to control summary detail:
     - If `summary_level = "short"`: generate a compact 1–2 sentence summary.
     - If `summary_level = "detailed"`: generate a short paragraph **plus** a bullet list of 3–5 key points.
   - Ensure the summary aligns with the user-specified word limit.
2. Apply guardrails to check for missing, empty, or short sections.
3. Store processed summaries for the rendering module.

## Constraints
- Each section summary must include:
  - Main idea.
  - Key quotes.
  - Citations.
- Detailed mode must include:
  - A short paragraph.
  - A bullet list of 3–5 key points.
- Word count must align with the user's settings.
