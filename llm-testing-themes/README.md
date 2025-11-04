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
**To run a single test suite** (e.g., security):  
`promptfoo eval -c <config-file.yaml> --no-cache`

**Or to run all test suites** located in the `configs/` directory:
`for f in configs/*.yaml; do
  echo "Running $f"
  promptfoo eval -c "$f" --no-cache
done`

## View interactive results dashboard
promptfoo view

# Example Execution (Demo)
After running the test, you should see evaluation results with detailed pass/fail assertions per test.
<p align="center"> <video src="https://github.com/user-attachments/assets/1cf51381-bd7c-4fd3-a693-fce521c31c9e" width="100%" autoplay loop muted playsinline> Sorry, your browser doesn't support embedded videos. </video> </p>