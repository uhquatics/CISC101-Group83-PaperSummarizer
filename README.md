# CISC101-Group83-PaperSummarizer

This repository contains our CISC101 Paper Summarizer project from PS3.  
It includes the main system prompt and a set of internal modules that work together to summarize a research paper.

## Repository components 

- `system_prompt.md`  
  - The main instructions for the Research Paper Summarizer (inputs, outputs, boundaries, and overall behavior).

- `modules/`  
  - `01_intake_and_setup.md` – receives the paper text + metadata and normalizes sections.  
  - `02_section_loop.md` – loops over each section and generates section summaries.  
  - `03_guardrails.md` – handles missing/short sections and hallucination checks.  
  - `04_rendering_and_refinement.md` – assembles the final output and formats it.  
  - `05_citation_extractor.md` – finds and tracks citations used in the paper.  
  - `06_key_contributions_summarizer.md` – extracts the main contributions of the paper.
