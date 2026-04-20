---
name: cheapest
description: "Find the cheapest AI model for a specific use case. Use when user asks for budget-friendly or cheapest models."
argument-hint: "[category: flagship|reasoning|coding|lite|embedding|...]"
allowed-tools:
  - mcp__aiprice__get_prices
  - mcp__aiprice__get_model_detail
---

# Find Cheapest AI Models

Help the user find the most affordable AI model for their use case.

## Steps

1. Determine the category from `$ARGUMENTS` (default to all if not specified)
2. Use `get_prices` with the category filter, sorted by blended price (ascending)
3. Present the top 10 cheapest models
4. For each model, note key capabilities (context length, tool use, vision support)
5. Highlight any **free** models
6. Recommend the best value option considering both price and capabilities

## Categories
- `flagship` — Top-tier models (GPT-4 class)
- `reasoning` — Chain-of-thought / reasoning models
- `coding` — Code-specialized models
- `lite` — Lightweight / fast models
- `multimodal` — Multi-modal models
- `embedding` — Embedding models
- `vision` — Vision-capable models
- `long-context` — Long context window models

$ARGUMENTS
