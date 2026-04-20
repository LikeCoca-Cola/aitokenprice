---
name: prices
description: "Query and compare AI model prices from Chinese providers. Use when: user asks about AI model pricing, cost comparison, cheapest/most expensive models, or mentions providers like DeepSeek, Qwen, Zhipu, Moonshot, Doubao, Hunyuan, etc."
argument-hint: "[provider or model name]"
allowed-tools:
  - mcp__aiprice__get_prices
  - mcp__aiprice__get_providers
  - mcp__aiprice__get_model_detail
  - mcp__aiprice__compare_prices
---

# AI Model Price Query

You have access to real-time AI model pricing data from Chinese providers via the AIPrice MCP tools.

## Available Tools

1. **get_prices** — Query model prices with optional filters
   - `provider`: Filter by provider slug (deepseek, qwen, zhipu, moonshot, ernie, hunyuan, doubao, baichuan, minimax, step, yi)
   - `category`: Filter by category (flagship, reasoning, coding, lite, multimodal, vision, long-context, embedding, image, audio)
   - `currency`: usd or cny (default: usd)
   - `limit`: Max results (default: 50)

2. **get_providers** — List all tracked Chinese AI providers

3. **get_model_detail** — Get detailed info for a specific model
   - `slug`: Model slug (e.g. deepseek-chat, qwen3-max, glm-4-plus)

4. **compare_prices** — Compare multiple models side by side
   - `models`: Comma-separated slugs (e.g. "deepseek-chat,qwen3-max,glm-4-plus")

## Instructions

When the user asks about AI model prices:

1. **Identify intent**: Are they looking for a specific model, comparing models, or browsing?
2. **Choose the right tool**:
   - General browsing → `get_prices` with relevant filters
   - Specific model → `get_model_detail`
   - Comparison → `compare_prices`
   - Provider info → `get_providers`
3. **Present results clearly**: Use tables for comparisons, highlight free models, note the currency
4. **Add context**: Mention if a model is open-source, supports tool use, vision, etc.

$ARGUMENTS
