# Module 3: Guardrails

## Purpose
Ensure summarization integrity, strengthen evidence requirements, and prevent hallucinations.

## Guardrail Checks

- **Strict Evidence Mode (`evidence_mode = "strict"`):**
  - Summaries may only include claims, equations, and results that appear explicitly in the provided text.
  - If the text does not contain enough information to summarize a section, output:
    - “The source text does not provide enough detail to summarize this section in strict evidence mode.”
  - Any content not directly grounded in the text must be removed.

- **Missing / Empty Sections:**
  - If a section is missing or has no usable text, output:
    - “Section skipped: no usable text was provided.”

- **Short Sections (< 50 words):**
  - Output:
    - “Section very short: summary may be incomplete.”

- **Hallucination Mitigation (general):**
  - Summaries must only use information present in the text.
  - No invented claims, equations, or citations.

- **Long-Paper Chunking (from PS2):**
  - Break paper into chunks if needed.
  - Summarize each chunk separately.
  - Merge results into the final output.

## Constraints
- All warnings must use the standardized messages above.
- Strict evidence mode overrides all other behaviors.
- No invented citations or fabricated content.
