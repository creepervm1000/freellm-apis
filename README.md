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

### Google Gemini (Google AI Studio)

| Detail | Info |
|--------|------|
| **Models** | Gemini 2.0 Flash, Gemini 1.5 Pro, Gemini 1.5 Flash, and more |
| **API Endpoint** | `https://generativelanguage.googleapis.com/v1beta` |
| **Sign Up** | [aistudio.google.com](https://aistudio.google.com) |
| **Auth** | Google account, API key from AI Studio dashboard |
| **Rate Limits** | ~10 RPM, ~250K tokens/min, ~1M tokens/day |
| **Credit Card** | Not required |
| **Notes** | Massive context windows (up to 2M tokens on some models). Per-project quotas. |

Google AI Studio provides free access to the Gemini model family with remarkably generous token quotas. The standout feature is context window size — some Gemini models support up to 2 million tokens, which is useful for processing large documents or long conversation histories. The free tier uses per-project quotas, so you can create multiple projects to effectively multiply your limits. The API uses Google's own format (not OpenAI-compatible), but there are open-source wrappers that add OpenAI compatibility. Also includes free access to their web UI for quick testing.

---

### Groq

| Detail | Info |
|--------|------|
| **Models** | Llama 3.3 70B, Llama 3.1 8B, Llama 4 Scout, Qwen3 32B, Mixtral, and more |
| **API Endpoint** | `https://api.groq.com/openai/v1` (OpenAI-compatible) |
| **Sign Up** | [console.groq.com](https://console.groq.com) |
| **Auth** | API key from dashboard |
| **Rate Limits** | 30 req/min, 6,000 tokens/min, 14,400 req/day |
| **Credit Card** | Not required |
| **Notes** | Ultra-low-latency inference on LPU chips. All models free. One of the most generous free tiers. |

Groq offers the fastest inference of any provider on this list thanks to their custom LPU (Language Processing Unit) chips. The free tier gives access to every model on their platform with no restrictions on which models you can use. At 30 requests per minute and 14,400 requests per day, the rate limits are generous enough for serious development work. The API is fully OpenAI-compatible — just swap the base URL and API key in any OpenAI SDK or compatible tool. This is one of the best free tiers available for real-time applications where latency matters.

---

### Cerebras

| Detail | Info |
|--------|------|
| **Models** | Llama 3.1 70B, Llama 3.1 8B, and more from their model catalog |
| **API Endpoint** | `https://api.cerebras.ai/v1` (OpenAI-compatible) |
| **Sign Up** | [cloud.cerebras.ai](https://cloud.cerebras.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | 5 req/min, ~30K tokens/min, 1M tokens/day |
| **Credit Card** | Not required |
| **Notes** | World's fastest inference (CS-3 wafer-scale chip). Free tier limited to 8K context. |

Cerebras runs on their CS-3 wafer-scale engine — a single chip the size of an entire wafer — which makes it the fastest inference hardware available. The free tier offers a generous 1 million tokens per day, but the request rate is low (5 per minute) and the context window is capped at 8,192 tokens on the free tier (compared to 128K on paid). Best suited for batch processing tasks where you need throughput over the course of a day rather than high requests-per-minute. The API is OpenAI-compatible.

---

### Mistral AI (La Plateforme)

| Detail | Info |
|--------|------|
| **Models** | Mistral Large, Mistral Medium, Codestral, Mistral Small, Mistral Nemo, and more |
| **API Endpoint** | `https://api.mistral.ai/v1` (OpenAI-compatible) |
| **Sign Up** | [console.mistral.ai](https://console.mistral.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | Rate-limited (shared quota pools across models) |
| **Credit Card** | Not required |
| **Notes** | Free access to Mistral Large (flagship) and Codestral. Labeled "experiment" tier — not for production. |

Mistral's free "experiment" tier is remarkable because it includes access to Mistral Large, their flagship closed-source model, as well as Codestral, their specialized code generation model. Very few providers offer their best proprietary models for free. The API is OpenAI-compatible and the key is ready within minutes of signing up. The main limitation is the "experiment" label — this tier is explicitly not meant for production use, and the shared quota pools mean heavy use of one model affects your limits on others. Still, for development and prototyping, getting Mistral Large for free is hard to beat.

---

### SambaNova

| Detail | Info |
|--------|------|
| **Models** | Llama 3.1 405B, DeepSeek-R1, and more |
| **API Endpoint** | `https://api.sambanova.ai/v1` (OpenAI-compatible) |
| **Sign Up** | [sambanova.ai](https://sambanova.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | Varies by model (some as low as 20 req/day) |
| **Credit Card** | Not required |
| **Notes** | Free access to Llama 3.1 405B — the largest open-weight model on any free API. |

SambaNova's standout feature is offering free access to Llama 3.1 405B, the largest open-weight model available through any free provider. If you need to test prompts against a massive model without paying, this is the place. The trade-off is that rate limits on larger models can be very low (as few as 20 requests per day on some models), so this is best suited for experimentation and evaluation rather than sustained use. The API is OpenAI-compatible.

---

### Cohere

| Detail | Info |
|--------|------|
| **Models** | Command R+, Command R, Command R7B, Aya Expanse, Embed 4, Rerank 3.5 |
| **API Endpoint** | `https://api.cohere.ai/v1` |
| **Sign Up** | [dashboard.cohere.com](https://dashboard.cohere.com) |
| **Auth** | Trial API key from dashboard |
| **Rate Limits** | 20 req/min, 1,000 API calls/month |
| **Credit Card** | Not required |
| **Notes** | Best free tier for embeddings and reranking. Monthly call cap is the main limitation. |

Cohere's free trial tier is unique because it includes access to specialized models that most other free providers don't offer — specifically Embed 4 (embedding model) and Rerank 3.5 (reranking model). If you're building search, RAG, or any system that needs embeddings or reranking, Cohere is the best free option for those specific tasks. The chat models (Command R+, Command R) are solid for general use as well. The main limitation is the 1,000 calls per month cap, which is low compared to other providers. This is a trial key for prototyping and research, not a high-volume production endpoint.

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

### Hugging Face Inference API

| Detail | Info |
|--------|------|
| **Models** | Thousands of open-source models (free tier limited to models under ~10B parameters) |
| **API Endpoint** | `https://api-inference.huggingface.co/models/{model_id}` |
| **Sign Up** | [huggingface.co](https://huggingface.co) |
| **Auth** | HF API token from account settings |
| **Rate Limits** | ~100-200 req/hour |
| **Credit Card** | Not required for free tier |
| **Notes** | Largest model catalog. Free tier limited to smaller models. PRO tier ($9/mo) unlocks much more. |

Hugging Face offers access to the largest catalog of open-source models through their Inference API. The free tier is limited to models under approximately 10 billion parameters and has relatively low hourly rate limits, but the sheer variety of available models is unmatched. If you need a specific model for a specific task — a fine-tuned classification model, a small instruction-tuned model, a sentence transformer — Hugging Face probably has it. The free tier is best for light prototyping and experimentation with niche models. For heavier use, the PRO tier at $9/month is one of the cheapest paid options available anywhere.

---

### Cloudflare Workers AI

| Detail | Info |
|--------|------|
| **Models** | Llama, Mistral, Qwen, Phi, and more (broad open-source catalog) |
| **API Endpoint** | `https://api.cloudflare.com/client/v4/accounts/{account_id}/ai/run/@cf/{model}` |
| **Sign Up** | [dash.cloudflare.com](https://dash.cloudflare.com) |
| **Auth** | Cloudflare API token |
| **Rate Limits** | 10,000 Neurons/day (Cloudflare's compute unit) |
| **Credit Card** | Not required for Workers Free plan |
| **Notes** | Runs on Cloudflare's edge network. Neuron-based billing (not token-based). Also does image generation, classification. |

Cloudflare Workers AI runs models on Cloudflare's global edge network, which means low latency from anywhere in the world. The billing uses "Neurons" (a normalized compute unit) rather than raw tokens, so costs vary by model size — smaller models get you more requests per Neuron. The free plan gives 10,000 Neurons per day. Beyond LLMs, Workers AI also offers image generation, translation, classification, and other AI tasks, making it a versatile free AI platform. Requires a Cloudflare account. The API format is not OpenAI-compatible — it uses Cloudflare's own REST format.

---

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

## Quick Comparison

| Provider | API Format | All Models Free | Best For |
|----------|-----------|----------------|----------|
| Google Gemini | Google API | Yes | Long context (up to 2M tokens) |
| Groq | OpenAI-compatible | Yes | Speed + generous limits |
| Cerebras | OpenAI-compatible | Yes | Fastest raw inference |
| Mistral AI | OpenAI-compatible | Yes | Flagship models for free |
| SambaNova | OpenAI-compatible | Partial | Llama 3.1 405B access |
| Cohere | Proprietary | Yes | Embeddings + reranking |
| OpenRouter | OpenAI-compatible | Partial (free labeled) | General-purpose, most reliable |
| NVIDIA NIM | OpenAI-compatible | Yes | Embeddings, NVIDIA-optimized models |
| Hugging Face | HF API | Partial (<=10B params) | Largest model catalog |
| Cloudflare Workers AI | CF REST | Yes | Edge inference, versatile AI tasks |
| OpenAI Codex | CLI | N/A | Code generation tasks |
| Kilocode Gateway | OpenAI-compatible | Rotating | Rotating model access |

## Contributing

Found a provider that's actually free and useful? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Fake providers, dead links, and paid-only services masquerading as free will be rejected.

## Disclaimer

Free tiers can change at any time. Providers may introduce rate limits, remove models, or shut down free access without notice. This list is maintained on a best-effort basis. Always check the provider's current terms before relying on them for production use.

## License

[MIT](LICENSE) © creepervm1000