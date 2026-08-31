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
| **Models** | Gemini 2.5 Pro, Gemini 2.5 Flash, Gemini 3.5 Flash, Gemini 3.6 Flash, Gemma 4, and more |
| **API Endpoint** | `https://generativelanguage.googleapis.com/v1beta` |
| **Sign Up** | [aistudio.google.com](https://aistudio.google.com) |
| **Auth** | Google account, API key from AI Studio dashboard |
| **Rate Limits** | ~5-15 RPM depending on model, ~1M tokens/day |
| **Credit Card** | Not required |
| **Notes** | Massive context windows (up to 1M tokens). Per-project quotas. Free-tier prompts may be used by Google for model improvement. |

Google AI Studio provides free access to the Gemini model family with remarkably generous token quotas. The standout feature is context window size — Gemini models support up to 1 million tokens, which is useful for processing large documents or long conversation histories. The free tier uses per-project quotas, so you can create multiple projects to effectively multiply your limits. The API uses Google's own format (not OpenAI-compatible), but there are open-source wrappers that add OpenAI compatibility. Also includes free access to their web UI for quick testing.

---

### Groq

| Detail | Info |
|--------|------|
| **Models** | GPT-oss-120B, GPT-oss-20B, Qwen3.6-27B, Groq Compound, and more |
| **API Endpoint** | `https://api.groq.com/openai/v1` (OpenAI-compatible) |
| **Sign Up** | [console.groq.com](https://console.groq.com) |
| **Auth** | API key from dashboard |
| **Rate Limits** | 30 req/min, 6,000 tokens/min, up to 1,000 req/day per model |
| **Credit Card** | Not required |
| **Notes** | Ultra-low-latency inference on LPU chips. All models free. One of the most generous free tiers. |

Groq offers the fastest inference of any provider on this list thanks to their custom LPU (Language Processing Unit) chips. The free tier gives access to every model on their platform with no restrictions on which models you can use. At 30 requests per minute, the rate limits are generous enough for serious development work. The API is fully OpenAI-compatible — just swap the base URL and API key in any OpenAI SDK or compatible tool. This is one of the best free tiers available for real-time applications where latency matters.

---

### OVHcloud AI Endpoints

| Detail | Info |
|--------|------|
| **Models** | 20+ open-weight models including Llama, Qwen, DeepSeek, Mistral, and more |
| **API Endpoint** | `https://europe-west1.inference.ai.ovh.net/v1` (OpenAI-compatible) |
| **Sign Up** | None required for anonymous tier |
| **Auth** | No key needed (anonymous) or OVHcloud account for higher limits |
| **Rate Limits** | 2 RPM per IP per model (anonymous) |
| **Credit Card** | Not required |
| **Notes** | Fully anonymous — no signup, no API key. 20+ models. Hosted in EU (GDPR). OpenAI-compatible. |

OVHcloud AI Endpoints offers a completely anonymous free tier — no account, no API key, no signup form, no email verification. Just send a request to their endpoint and it works. They host 20+ open-weight models (Llama, Qwen, DeepSeek, Mistral, etc.) on EU infrastructure, making them one of the best options for GDPR-conscious developers who need data to stay in Europe. The rate limit is 2 requests per minute per IP per model, which is low but workable for light use. The API is fully OpenAI-compatible. If you need higher limits, creating a free OVHcloud account raises the rate limits significantly. Alongside LLM7.io, this is one of only two providers on this list that requires literally zero friction to start using.

---

### Mistral AI (La Plateforme)

| Detail | Info |
|--------|------|
| **Models** | Mistral Large 3, Mistral Medium 3.5, Mistral Small 4, Codestral, Ministral 3, and more |
| **API Endpoint** | `https://api.mistral.ai/v1` (OpenAI-compatible) |
| **Sign Up** | [console.mistral.ai](https://console.mistral.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | ~1 RPS, ~500K tokens/min (shared quota pools) |
| **Credit Card** | Not required |
| **Notes** | Free access to Mistral Large (flagship) and Codestral. ~$10/month in API credits. Free-mode prompts may be used to train Mistral models. |

Mistral's free tier is remarkable because it includes access to Mistral Large, their flagship closed-source model, as well as Codestral, their specialized code generation model. Very few providers offer their best proprietary models for free. The API is OpenAI-compatible and the key is ready within minutes of signing up. The free mode gives approximately $10/month in API credits. The shared quota pools mean heavy use of one model affects your limits on others. Still, for development and prototyping, getting Mistral Large for free is hard to beat.

---

### SiliconFlow

| Detail | Info |
|--------|------|
| **Models** | 100+ models including Qwen, DeepSeek, Llama, GLM, and more |
| **API Endpoint** | `https://api.siliconflow.cn/v1` (OpenAI-compatible) |
| **Sign Up** | [siliconflow.com](https://www.siliconflow.com) |
| **Auth** | API key from dashboard |
| **Rate Limits** | Fixed rate limits per free model (varies) |
| **Credit Card** | Not required for free models |
| **Notes** | Permanently free models with fixed limits. Identity verification required. New accounts also get starter credits. |

SiliconFlow is a Chinese/international AI inference platform with a catalog of over 100 models. The key feature is a set of **permanently free models** that don't expire — these are clearly marked as $0 on their pricing page. The free models include popular open-source models like Qwen and DeepSeek variants. Beyond the permanent free models, new accounts receive starter credits. The main drawback is that identity verification is required to sign up. The API is fully OpenAI-compatible, making it easy to integrate into existing tools and workflows. This is one of the few platforms where the free tier is truly permanent and not a limited-time trial.

---

### Zhipu AI (Z AI)

| Detail | Info |
|--------|------|
| **Models** | GLM-4.7-Flash, GLM-4.6V-Flash (multimodal) |
| **API Endpoint** | `https://open.bigmodel.cn/api/paas/v4` (OpenAI-compatible) |
| **Sign Up** | [open.bigmodel.cn](https://open.bigmodel.cn) |
| **Auth** | API key from user center |
| **Rate Limits** | 1 concurrent request per free model |
| **Credit Card** | Not required |
| **Notes** | Permanent free tier. 200K context on GLM-4.7-Flash. Chinese and English. Low concurrency limit. |

Zhipu AI offers permanent free access to their GLM model family. GLM-4.7-Flash supports up to 200K context tokens, which is one of the largest free context windows available. The models handle both Chinese and English well, making this a great choice if you need Chinese language support. The main limitation is the 1 concurrent request limit on free models, which means you can't parallelize requests. The API is OpenAI-compatible. Also offers a multimodal model (GLM-4.6V-Flash) for free, capable of processing images alongside text.

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
| **Models** | Command A+, Command A, Command R+, Embed 4, Rerank 3.5, Aya Expanse |
| **API Endpoint** | `https://api.cohere.com/v2` |
| **Sign Up** | [dashboard.cohere.com](https://dashboard.cohere.com) |
| **Auth** | Trial API key from dashboard |
| **Rate Limits** | 20 req/min, 1,000 API calls/month |
| **Credit Card** | Not required |
| **Notes** | Best free tier for embeddings and reranking. Non-commercial use only. Monthly call cap is the main limitation. |

Cohere's free trial tier is unique because it includes access to specialized models that most other free providers don't offer — specifically Embed 4 (embedding model) and Rerank 3.5 (reranking model). If you're building search, RAG, or any system that needs embeddings or reranking, Cohere is the best free option for those specific tasks. The chat models (Command A+, Command R+) are solid for general use as well, and now include multimodal capabilities. The main limitation is the 1,000 calls per month cap, which is low compared to other providers. This is a trial key for prototyping and research, not a high-volume production endpoint.

---

### OpenRouter Free

| Detail | Info |
|--------|------|
| **Models** | Llama 3.3 70B, Gemma, Mistral, Qwen, and dozens more (free models labeled) |
| **API Endpoint** | `https://openrouter.ai/api/v1` (OpenAI-compatible) |
| **Sign Up** | [openrouter.ai](https://openrouter.ai) |
| **Auth** | API key from dashboard |
| **Rate Limits** | Rate-limited, varies by model |
| **Credit Card** | Not required for free tier |
| **Notes** | The most reliable free LLM API. Large model selection, OpenAI-compatible, well-documented. |

OpenRouter is the gold standard for free LLM API access. They aggregate dozens of models (both open-source and proprietary) and offer a subset of them for free. The free models are clearly labeled in their model list. Their API is fully OpenAI-compatible, meaning any tool, library, or framework built for OpenAI's API will work with OpenRouter by simply changing the base URL. They also provide a chat playground for testing. The free tier is generous enough for real development work, and the documentation is excellent. If you only use one provider from this list, make it this one.

---

### NVIDIA NIM

| Detail | Info |
|--------|------|
| **Models** | Llama, Mistral, CodeLlama, NV-EmbedQA, GPT-oss-120B, and more |
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
| **Models** | Thousands of open-source models (free tier routes to various inference providers) |
| **API Endpoint** | `https://router.huggingface.co/v1` (OpenAI-compatible) |
| **Sign Up** | [huggingface.co](https://huggingface.co) |
| **Auth** | HF API token from account settings |
| **Rate Limits** | ~$0.10/month in Inference Provider credits for free users |
| **Credit Card** | Not required |
| **Notes** | Largest model catalog. Routes to Fireworks, Together, Nebius and others. PRO tier ($9/mo) unlocks much more. |

Hugging Face offers access to the largest catalog of open-source models through their Inference API. The free tier provides a small monthly credit that routes requests to various inference providers (Fireworks, Together, Nebius, etc.). The sheer variety of available models is unmatched — if you need a specific fine-tuned model, a sentence transformer, or a niche classification model, Hugging Face probably has it. The free tier is best for light prototyping and experimentation. For heavier use, the PRO tier at $9/month is one of the cheapest paid options available anywhere.

---

### Cloudflare Workers AI

| Detail | Info |
|--------|------|
| **Models** | 75+ models including Llama, Mistral, Qwen, DeepSeek R1, GPT-oss-120B, and more |
| **API Endpoint** | `https://api.cloudflare.com/client/v4/accounts/{account_id}/ai/run/@cf/{model}` |
| **Sign Up** | [dash.cloudflare.com](https://dash.cloudflare.com) |
| **Auth** | Cloudflare API token |
| **Rate Limits** | 10,000 Neurons/day |
| **Credit Card** | Not required for Workers Free plan |
| **Notes** | Runs on Cloudflare's edge network. 75+ models on free tier. Neuron-based billing. Also does image generation, classification. |

Cloudflare Workers AI runs models on Cloudflare's global edge network, which means low latency from anywhere in the world. The billing uses "Neurons" (a normalized compute unit) rather than raw tokens, so costs vary by model size — smaller models get you more requests per Neuron. The free plan gives 10,000 Neurons per day and now offers 75+ models on the free tier, including strong models like DeepSeek R1 Distill and GPT-oss-120B. Beyond LLMs, Workers AI also offers image generation, translation, classification, and other AI tasks. Requires a Cloudflare account. The API format is not OpenAI-compatible — it uses Cloudflare's own REST format.

---

### LLM7.io

| Detail | Info |
|--------|------|
| **Models** | GPT-oss-20B, Mistral Nemo, MiniMax M2.7, and more |
| **API Endpoint** | `https://api.llm7.io/v1` (OpenAI-compatible) |
| **Sign Up** | None required for anonymous access |
| **Auth** | No key needed (anonymous) or free token from token.llm7.io for higher limits |
| **Rate Limits** | 10 RPM, 60 req/hr (anonymous); higher with free token |
| **Credit Card** | Not required |
| **Notes** | Zero sign-up needed. Just hit the API. One of two no-auth providers on this list. |

LLM7.io is unique on this list because it requires **no account and no API key** for anonymous access. You can literally start making requests immediately with zero friction. The anonymous tier has 128K context on models like GPT-oss-20B and Mistral Nemo. If you want higher rate limits, you can grab a free token from their site, but even the anonymous tier is usable. This makes LLM7.io the fastest provider to get started with — no sign-up form, no email verification, no dashboard. Just point your code at the endpoint and go.

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
| **Models** | Nemotron-3-Ultra-550B, Step-3.7-Flash, Laguna S 2.1, Tencent Hy3, and more (free pool) |
| **API Endpoint** | `https://api.kilo.ai/api/gateway` (OpenAI-compatible) |
| **Sign Up** | [kilo.ai](https://app.kilo.ai) |
| **Auth** | No API key required for free models |
| **Rate Limits** | 200 req/hr |
| **Credit Card** | Not required |
| **Notes** | Auto-router (`kilo-auto/free`) picks the best model. No key needed. 200 req/hr is very generous. |

Kilocode Gateway is an aggregator that provides access to multiple models through an OpenAI-compatible API. Their standout feature is the `kilo-auto/free` auto-router that dynamically routes your requests to the best available model in the free pool — no API key needed at all. At 200 requests per hour, the rate limit is generous. The free model pool includes powerful models like Nemotron-3-Ultra-550B (1M context) and Laguna S 2.1 for code generation. Check their dashboard for the current list of available free models, as the selection changes over time.

---

## Quick Comparison

| Provider | API Format | All Models Free | Best For |
|----------|-----------|----------------|----------|
| Google Gemini | Google API | Yes | Long context (up to 1M tokens) |
| Groq | OpenAI-compatible | Yes | Speed + generous limits |
| OVHcloud AI | OpenAI-compatible | Yes | Anonymous, no signup, EU-hosted, GDPR |
| Mistral AI | OpenAI-compatible | Yes | Flagship models for free |
| SiliconFlow | OpenAI-compatible | Partial (free labeled) | Permanently free models, Chinese/international |
| Zhipu AI | OpenAI-compatible | Partial (free models) | GLM models, Chinese/English, 200K context |
| SambaNova | OpenAI-compatible | Partial | Llama 3.1 405B access |
| Cohere | Proprietary | Yes | Embeddings + reranking |
| OpenRouter | OpenAI-compatible | Partial (free labeled) | General-purpose, most reliable |
| NVIDIA NIM | OpenAI-compatible | Yes | Embeddings, NVIDIA-optimized models |
| Hugging Face | OpenAI-compatible | Partial (credit-metered) | Largest model catalog |
| Cloudflare Workers AI | CF REST | Yes | Edge inference, 75+ free models |
| LLM7.io | OpenAI-compatible | Yes | Zero-friction anonymous access |
| OpenAI Codex | CLI | N/A | Code generation tasks |
| Kilocode Gateway | OpenAI-compatible | Free labeled | Auto-router, 200 req/hr, no key needed |

## Contributing

Found a provider that's actually free and useful? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Fake providers, dead links, and paid-only services masquerading as free will be rejected.

## Disclaimer

Free tiers can change at any time. Providers may introduce rate limits, remove models, or shut down free access without notice. This list is maintained on a best-effort basis. Always check the provider's current terms before relying on them for production use.

## License

[MIT](LICENSE) © creepervm1000