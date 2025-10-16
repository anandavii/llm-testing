# LLM Hello World Test with Promptfoo

This repository contains a simple "Hello World" kind of test to demonstrate LLM prompt evaluation using Promptfoo.

## Overview
- Test a single prompt: asking an LLM to explain AI Testing in less than 200 words
- Checks that the response contains key phrases like `software testing` and `testing`
- Uses the OpenAI GPT-4.1 nano model as the provider

## Structure
- `prompts`: reusable placeholders for your input prompts
- `providers`: define LLMs and configurations (here, GPT-4.1 nano)
- `tests`: define test cases, input variables, and assertions

## Run the Test
```bash
promptfoo eval
promptfoo view  # optional, opens local web viewer
```
