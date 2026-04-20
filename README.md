# 🦐 AIPrice Plugin for Claude Code / CodeBuddy

> Query real-time AI model prices from Chinese providers directly in your coding session.

Powered by [aiprice.cn](https://aiprice.cn) — the real-time AI model pricing tracker for Chinese AI providers.

## ✨ Features

- 🔍 **Query prices** for 100+ AI models from 10+ Chinese providers
- ⚡ **Compare models** side by side with a single command
- 💰 **Find cheapest** models for any category
- 🤖 **Auto-trigger** — just ask about AI model pricing in natural language
- 🔌 **MCP integration** — connects automatically, no API key needed

## 📦 Install

### Claude Code

```bash
claude plugin install github:LikeCoca-Cola/aitokenprice
```

### CodeBuddy (小龙虾)

In your IDE, open CodeBuddy and run:

```
/plugin install github:LikeCoca-Cola/aitokenprice
```

Or manually add to your MCP config (`.claude/settings.json` or IDE settings):

```json
{
  "mcpServers": {
    "aiprice": {
      "type": "url",
      "url": "https://aiprice.cn/api/mcp"
    }
  }
}
```

## 🚀 Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/aiprice:prices [provider]` | Query model prices, optionally filter by provider |
| `/aiprice:compare <model1> <model2>` | Compare models side by side |
| `/aiprice:cheapest [category]` | Find cheapest models for a category |

### Natural Language (auto-triggered)

Just ask in your normal conversation:

- "DeepSeek V3 多少钱？"
- "帮我对比一下 Qwen3 和 GLM-4 的价格"
- "最便宜的 coding 模型是哪个？"
- "What's the cheapest flagship model from Chinese providers?"
- "Compare deepseek-chat vs qwen3-max pricing"

### MCP Tools (for advanced users)

The plugin exposes 4 MCP tools that AI can call directly:

| Tool | Description |
|------|-------------|
| `get_prices` | Query model prices with filters (provider, category, currency) |
| `get_providers` | List all tracked AI providers |
| `get_model_detail` | Get detailed specs and pricing for a model |
| `compare_prices` | Compare multiple models in a table |

## 🏢 Supported Providers

| Provider | Slug |
|----------|------|
| DeepSeek | `deepseek` |
| Qwen (通义千问) | `qwen` |
| Zhipu AI (智谱) | `zhipu` |
| Moonshot (月之暗面) | `moonshot` |
| Baidu ERNIE (文心一言) | `ernie` |
| Tencent Hunyuan (混元) | `hunyuan` |
| ByteDance Doubao (豆包) | `doubao` |
| Baichuan (百川) | `baichuan` |
| MiniMax | `minimax` |
| StepFun (阶跃星辰) | `step` |
| Yi (零一万物) | `yi` |

## 📊 Data

- Prices are updated daily from official provider pricing pages
- Supports both USD and CNY
- Includes input, output, and blended (3:1) pricing per million tokens
- Tracks 100+ models across 10+ providers

## 📄 License

MIT

## 🔗 Links

- Website: [aiprice.cn](https://aiprice.cn)
- API Docs: [aiprice.cn/api-docs](https://aiprice.cn/zh/api-docs)
- MCP Endpoint: `https://aiprice.cn/api/mcp`
