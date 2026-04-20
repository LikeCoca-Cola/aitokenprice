---
name: compare
description: "Compare prices of specific AI models side by side. Use when user wants to compare costs between models."
argument-hint: "<model1> <model2> [model3...]"
allowed-tools:
  - mcp__aiprice__compare_prices
  - mcp__aiprice__get_model_detail
  - mcp__aiprice__get_prices
---

# Compare AI Model Prices

Compare the prices of the specified AI models using the AIPrice API.

## Steps

1. Parse the model names from `$ARGUMENTS`
2. If the user provided display names (like "DeepSeek V3"), first use `get_prices` to find the correct slugs
3. Use `compare_prices` with the comma-separated slugs
4. Present results in a clear comparison table
5. Highlight the cheapest option and any free models

If no models are specified, ask the user which models they'd like to compare, and suggest popular ones.

$ARGUMENTS
