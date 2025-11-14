# LLM Evaluation: Scalable Test Structuring with Inline, Modular & CSV-Driven Suites

This project demonstrates how to structure Promptfoo test suites **at scale**, using a combination of inline tests, modular YAML imports, reusable prompt templates, and metadata-rich CSV-driven evaluations.

## Overview

* Shows how real AI-QA teams organize large LLM evaluation repositories  
* Uses **three complementary structuring patterns**:
  - **Inline tests** — fast, single-file checks  
  - **Externalized YAML suites** — clean modularization for maintainability  
  - **Bulk CSV tests** — scalable evaluations with multiple assertions and metadata  
* Exercises **deterministic**, **JavaScript**, and **LLM-rubric** assertions  
* Uses **Groq Llama 3.3 70B Versatile** as the single provider for all tests  
* Demonstrates how prompt templates can be reused across many test suites

## Structure

* `prompts/` — reusable prompt templates  
  * `support_query-ext-files.txt` – support-assistant prompt for modular YAML suites  
  * `support_query-bulk-csv.txt` – precise assistant prompt for CSV-driven suites  

* `structure/` — three different test-structuring strategies  
  * `inline.yaml` – small, inline tests (simple translation checks)  
  * `ext-files.yaml` – externalized modular YAML test suites  
    * `tests/test01.yaml` – translation check  
    * `tests/test02.yaml` – math reasoning  
    * `tests/test03.yaml` – capital-city fact check  
  * `bulk-csv.yaml` – scalable multi-assertion testing using a CSV file  
    * `tests/test04_bulk.csv` – 10 advanced multi-assertion test cases  
      covering ML concepts, formatting, translation, writing, email etiquette,  
      branding constraints, code review, and security refusal

## Running the Test Suites

### 1. Inline tests
```bash
promptfoo eval -c structure/inline.yaml --no-cache
```

## View interactive results dashboard
promptfoo view

# Example Execution (Demo)
After running the test, you should see evaluation results with detailed pass/fail assertions per test.![exampleRun](/output/output.gif)