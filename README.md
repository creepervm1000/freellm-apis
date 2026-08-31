# Free LLM APIs

A curated list of **actually useful** free LLM API providers. No fake entries, no dead links, no "free but requires a credit card" traps. Every provider listed here has been verified to offer free API access to real models.

[中文版](README_zh.md) | [Contributing](CONTRIBUTING.md) | [Code of Conduct](CODE_OF_CONDUCT.md)

---

## Why This List?

Most "free LLM API" lists are bloated with providers that are dead, require payment methods, or offer models so limited they're useless for real work. This list only includes providers that meet all of the following criteria:

- **Actually free** — no credit card, no paid plan required to access the free tier
- **API access** — you can make programmatic requests, not just chat in a web UI
- **Currently working** — providers are checked regularly and removed if they go offline
- **Useful models** — the free models can actually handle real tasks, not just "hello world"

---

## Providers

### OpenAI Codex Free Plan

| Detail | Info |
|--------|------|
| **Models** | Codex (code generation agent) |
| **API Endpoint** | CLI-based (not a REST API in the traditional sense) |
| **Sign Up** | [github.com/openai/codex](https://github.com/openai/codex) |
| **Auth** | GitHub account (free tier uses GitHub's compute) |
| **Rate Limits** | Limited compute quota, resets periodically |
| **Credit Card** | Not required |
| **Notes** | CLI tool, not a REST API. Designed for code generation tasks. Runs in your terminal. |

OpenAI's Codex CLI provides free code generation capabilities through a terminal-based agent. You interact with it through the command line rather than traditional API calls. It uses OpenAI's models under the hood but the interface is agent-based, not request-response. Useful for automated coding workflows, refactoring, and code review tasks directly from your terminal.

---

### Kilocode Gateway Free Models

| Detail | Info |
|--------|------|
| **Models** | Various (rotates frequently, check their dashboard for current offerings) |
| **API Endpoint** | OpenAI-compatible API |
| **Sign Up** | [kilocode.ai](https://kilocode.ai) or their Discord |
| **Auth** | API key provided after sign up |
| **Rate Limits** | Varies by model, generally generous for free tier |
| **Credit Card** | Not required |
| **Notes** | Gateway/aggregator — routes to multiple model providers. Free models rotate. |

Kilocode Gateway acts as an aggregator that provides access to multiple models through an OpenAI-compatible API format. Their free tier offers a rotating selection of models, which can include both open-source and proprietary models depending on availability. The API format means you can drop it into any tool that supports the OpenAI API spec by changing the base URL and API key. Check their dashboard or Discord for the current list of available free models, as the selection changes over time.

---

### OpenRouter Free

| Detail | Info |
|--------|------|
| **Models** | Llama 3.3 70B, Gemma 2 9B, Mistral 7B, Qwen 2.5, and more (rotates) |
| **API Endpoint** | `https://openrouter.ai/api/v1` (OpenAI-compatible) |
| **Sign Up** | [openrouter.ai](https://openrouter.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | Rate-limited, varies by model. Some models have token-per-minute caps. |
| **Credit Card** | Not required for free tier |
| **Notes** | The most reliable free LLM API. Large model selection, OpenAI-compatible, well-documented. |

OpenRouter is the gold standard for free LLM API access. They aggregate dozens of models (both open-source and proprietary) and offer a subset of them for free. The free models are clearly labeled in their model list. Their API is fully OpenAI-compatible, meaning any tool, library, or framework built for OpenAI's API will work with OpenRouter by simply changing the base URL. They also provide a chat playground for testing. The free tier is generous enough for real development work, and the documentation is excellent. If you only use one provider from this list, make it this one.

---

### NVIDIA NIM

| Detail | Info |
|--------|------|
| **Models** | Llama 3.1, Mistral, CodeLlama, NV-EmbedQA, and more |
| **API Endpoint** | `https://integrate.api.nvidia.com/v1` (OpenAI-compatible) |
| **Sign Up** | [build.nvidia.com](https://build.nvidia.com) |
| **Auth** | API key from NVIDIA developer dashboard |
| **Rate Limits** | Generous free tier, rate limits vary by model |
| **Credit Card** | Not required |
| **Notes** | NVIDIA's hosted inference API. Best for models optimized for NVIDIA GPUs. Also offers embedding models. |

NVIDIA NIM provides free API access to a range of open-source models hosted on NVIDIA's infrastructure. Since these models run on NVIDIA's own GPUs (the hardware they were designed for), performance and reliability are excellent. The API is OpenAI-compatible, making integration straightforward. Beyond chat/completion models, NIM also offers free access to embedding models and other specialized models. The developer dashboard provides usage tracking and API key management. Particularly useful if you need embeddings or want to benchmark models on optimized NVIDIA hardware.

---

## Quick Comparison

| Provider | API Compatible | Requires CC | Best For |
|----------|---------------|------------|----------|
| OpenAI Codex | CLI (not REST) | No | Code generation tasks |
| Kilocode Gateway | OpenAI-compatible | No | Rotating model access |
| OpenRouter | OpenAI-compatible | No | General-purpose, most reliable |
| NVIDIA NIM | OpenAI-compatible | No | Embeddings, NVIDIA-optimized models |

## Contributing

Found a provider that's actually free and useful? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Fake providers, dead links, and paid-only services masquerading as free will be rejected.

## Disclaimer

Free tiers can change at any time. Providers may introduce rate limits, remove models, or shut down free access without notice. This list is maintained on a best-effort basis. Always check the provider's current terms before relying on them for production use.

## License

[MIT](LICENSE) © creepervm1000
