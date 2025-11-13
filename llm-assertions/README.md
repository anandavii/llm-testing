# LLM Evaluation: Assertions, Semantic Similarity & Model-Graded Testing  

This project explores **Promptfoo’s advanced assertion types**, combining deterministic rules, semantic similarity (embeddings), and model-graded metrics to measure **accuracy, relevance, and factuality**.

## Overview  

* Expands testing beyond binary pass/fail to **graded and weighted evaluations**  
* Implements **semantic** and **LLM-based grading** using multiple providers  
* Demonstrates how to test **relevance**, **factual correctness**, and **response quality**  
* Uses **Groq Llama 3.3 70B Versatile** for generation and **Cohere/OpenAI** for evaluation  

## Structure  

* `deterministic/` — Tests with predictable, rule-based assertions  
  * `contains.yaml` – validates presence of keywords  
  * `regex.yaml` – ensures correct pattern and format  
  * `similar.yaml` – checks semantic overlap using embeddings (Groq + Cohere)  

* `llm-graded/` — Tests that use a **grading LLM** or **semantic comparison**  
  * `factuality.yaml` – evaluates factual correctness using OpenAI grader  
  * `answer_relevance.yaml` – checks contextual relevance using embeddings  
  * `llm_rubric.yaml` – applies human-like grading with structured rubric  

## Run the Test  

**To run a single test suite** (e.g., semantic similarity):  
```bash
promptfoo eval -c deterministic/similar.yaml --no-cache
```

## View interactive results dashboard
promptfoo view

# Example Execution (Demo)
After running the test, you should see evaluation results with detailed pass/fail assertions per test.
<p align="center">
  <video src="https://github.com/user-attachments/assets/795db562-1b8f-4a4b-9b0c-88313747ee80"
         width="100%"
         autoplay
         loop
         muted
         playsinline
         controls="false"
         style="pointer-events:none;">
    Sorry, your browser doesn't support embedded videos.
  </video>
</p>