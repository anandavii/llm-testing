# Comprehensive LLM Testing & Evaluation Repository

Welcome to the all-in-one **LLM Testing & Evaluation** repository. This project demonstrates a wide range of strategies for testing Large Language Models (LLMs) using **[Promptfoo](https://www.promptfoo.dev/)**.

From simple "Hello World" tests to advanced security assertions, semantic grading, and scalable test structuring, this repository serves as a reference for building robust AI quality assurance pipelines.

## Getting Started

### Prerequisites

Ensure you have `promptfoo` installed globally or in your project:

```bash
npm install -g promptfoo
```

### Quick Run

Navigate to any sub-project and run the evaluation command:

```bash
cd llm-hello-world
promptfoo eval
promptfoo view
```

---

## Project Directory

This repository is organized into focused sub-projects, each demonstrating a specific aspect of LLM testing.

| Project | Description | Key Patterns |
| :--- | :--- | :--- |
| **[llm-hello-world](./llm-hello-world)** | A minimal starting point for LLM testing. | Basic configuration, Single prompt test |
| **[llm-assertions](./llm-assertions)** | Specific assertion types for accuracy and quality. | Deterministic (Regex, JSON), Semantic Similarity, Model-Graded Factuality |
| **[llm-testing-themes](./llm-testing-themes)** | Stress-testing across 7 core AI failure modes. | Security (Injection), Hallucination, Bias, Continuity, Context Limits |
| **[llm-structuring](./llm-structuring)** | Best practices for organizing large test suites. | Inline tests, Modular YAML imports, CSV-driven bulk testing |
| **[llm-adavanced-tests](./llm-adavanced-tests)** | Complex scenarios for reasoning and refusal. | Math reasoning, Policy compliance, Safety refusals |
| **[llm-determinism-metrics](./llm-determinism-metrics)** | Performance benchmarking and provider comparison. | Cost analysis, Latency thresholds, Cross-provider comparison (Groq vs OpenAI vs Anthropic) |

---

## Detailed Project Breakdown

### 1. [Basic: Hello World](./llm-hello-world)
*   **Goal**: The simplest possible test to verify your setup.
*   **Scenario**: Asks an LLM to explain "AI Testing" in under 200 words.
*   **Check**: Verifies the response contains specific keywords like "software testing".

### 2. [Deep Dive: Assertions](./llm-assertions)
*   **Goal**: Move beyond simple text matching to intelligent validation.
*   **Features**:
    *   **Deterministic**: `contains`, `regex`, `json` validation.
    *   **Semantic**: Uses vector embeddings to check if the *meaning* matches the expected answer (e.g., "Hello" ≈ "Hi").
    *   **Model-Graded**: Uses a stronger LLM (e.g., GPT-4) to grade the response of the tested LLM for Factuality and Answer Relevance.

### 3. [Risk Assessment: Testing Themes](./llm-testing-themes)
*   **Goal**: Robustness testing against specific AI risks.
*   **Suites**:
    *   **Security**: Attempt prompt injections and ensure the model refuses.
    *   **Hallucination**: Ask questions about fake facts to ensure the model admits ignorance.
    *   **Bias & Fairness**: Check for neutral responses across demographic variations.
    *   **Context**: Test recall abilities with long context windows.

### 4. [Scale: Structuring Tests](./llm-structuring)
*   **Goal**: Organizing tests for maintainability when you have hundreds of cases.
*   **Patterns**:
    *   **Inline**: Quick, single-file tests.
    *   **Modular**: Importing test cases from separate YAML files.
    *   **CSV-Driven**: Managing large datasets of inputs and assertions in a spreadsheet-like format for bulk processing.

### 5. [Logic: Advanced Tests](./llm-adavanced-tests)
*   **Goal**: Testing complex reasoning chains and strict policy adherence.
*   **Scenarios**:
    *   **Math**: Verifying multi-step logical deductions.
    *   **Compliance**: Ensuring specific formatting rules (e.g., "answer must start with...") are followed.
    *   **Refusal**: Verifying that the model consistently refuses harmful instructions.

### 6. [Ops: Determinism & Metrics](./llm-determinism-metrics)
*   **Goal**: Operational excellence—cost, speed, and consistency.
*   **Metrics**:
    *   **Latency**: Ensure responses meet SLA (e.g., < 2000ms).
    *   **Cost**: Track and assert on token usage/cost per request.
    *   **Provider Comparison**: Run the same prompt across simple (Groq/Llama) and smart (GPT-4/Claude) models side-by-side to compare value.

---

## Tech Stack

*   **Core Tool**: [Promptfoo](https://www.promptfoo.dev/)
*   **Providers**:
    *   Groq (Llama 3.3 70B Versatile)
    *   OpenAI (GPT-4o-mini)
    *   Anthropic (Claude Sonnet)
*   **Format**: YAML configuration, Javascript assertions

