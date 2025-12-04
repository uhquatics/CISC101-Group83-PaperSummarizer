# Module 3: Guardrails

## Purpose
Ensure summarization integrity and prevent hallucinations.

## Guardrail Checks
- **Missing/Empty Sections**: Flag explicitly.
- **Short Sections (<50 words)**: Warn user.
- **Hallucination Mitigation**: Summaries must only use provided text.
- **Long-Paper Chunking**: Apply PS2 context-window strategies:
  - Break paper into chunks.
  - Summarize each chunk.
  - Merge summaries into final output.

## Constraints
- No invented citations.
- No fabricated content.
