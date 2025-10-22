# LLM Evaluation: Reasoning, Compliance, Security, and Refusal Testing

This repository contains a structured set of LLM evaluation tests designed to assess reasoning, compliance, and security behaviors using **Promptfoo**.

## Overview

* Evaluates an LLM’s **reasoning accuracy**, **policy compliance**, and **refusal consistency**
* Tests scenarios like math reasoning, logical inference, code generation, and safety refusals
* Ensures models properly follow **formatting rules**, **safety policies**, and **instruction constraints**
* Uses the **Groq Llama 3.3 70B Versatile** model as the provider

## Structure

* `prompts`: reusable prompt template that enforces rules for math, safety, and formatting
* `providers`: defines the Llama 3.3 70B model and configuration parameters (temperature, delay, timeout)
* `tests`: organized into two major groups

  * **Group A:** Reasoning and logic alignment
  * **Group B:** Security, constraint, and refusal testing

## Run the Test

```bash
promptfoo eval
promptfoo view
```

## Example Scenarios

* **Math Format Check:** Confirms “The final answer is:” prefix is applied correctly
* **Logic Reasoning:** Validates correct deduction from multi-step logic statements
* **Safety Refusal:** Detects prompt injection, Base64 obfuscation, or harmful roleplay
* **Compliance:** Ensures correct formatting and response constraints (e.g., word count)

## Example Execution

After running the test, you should see evaluation results with detailed pass/fail assertions per test.
![exampleRun](/llm-adavanced-tests/output/output.gif)
