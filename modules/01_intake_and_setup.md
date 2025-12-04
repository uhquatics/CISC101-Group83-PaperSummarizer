# Module 1: Intake & Setup

## Purpose
Normalize input data, detect missing or short sections, and prepare the paper for summarization.

## Workflow
1. Receive full paper text and metadata (sections, audience, word limit).
2. Normalize section titles (e.g., "Intro" → "Introduction").
3. Detect missing sections compared to expected academic structure.
4. Flag sections with fewer than 50 words.
5. Pass normalized data to Section Loop module.

## Constraints
- No invented sections.
- All flags must be explicit in output.
