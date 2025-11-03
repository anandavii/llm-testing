# LLM Evaluation: Failure-Mode Testing Across Seven AI Risk Dimensions  

This project contains a structured set of LLM evaluation tests designed to assess **robustness, safety, and ethical behavior** across seven core failure modes using **Promptfoo**.

## Overview  

* Evaluates an LLM’s performance on key AI-safety themes:  
  **Security**, **Hallucination**, **Bias & Fairness**, **Performance Consistency**, **Context-Window Limits**, **Human-Values Alignment**, and **Regulatory Compliance**  
* Each test simulates realistic risk scenarios — from prompt injections to factual pressure and long-context confusion  
* Uses the **Groq Llama 3.3 70B Versatile** model as the main provider  
* Provides reproducible YAML configurations for automated LLM benchmarking  

## Structure  

* `configs/` — YAML files defining seven thematic test suites  
  * `security.yaml` – validates safe refusals under injection attempts  
  * `hallucination.yaml` – detects fabricated or uncertain factual responses  
  * `bias_fairness.yaml` – ensures equal and neutral treatment across demographics  
  * `consistency.yaml` – checks reasoning stability and latency consistency  
  * `context_limit.yaml` – evaluates recall under long-context input and hidden instructions  
  * `values_alignment.yaml` – measures ethical and human-values alignment  
  * `compliance.yaml` – verifies adherence to GDPR, copyright, and policy norms  
* `prompts/` — shared text context used by long-input tests  
  * `context_window_limits.txt` – long passage on space exploration with an embedded hidden instruction  

## Run the Test
`promptfoo eval -c <config-file.yaml> --no-cache`

# View interactive results dashboard
promptfoo view