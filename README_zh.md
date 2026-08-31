# 免费 LLM API

一份精选的**真正有用**的免费大语言模型 API 提供商列表。没有虚假条目，没有死链接，没有"免费但需要信用卡"的陷阱。这里列出的每个提供商都经过验证，确实提供免费的 API 访问。

[English](README.md) | [贡献指南](CONTRIBUTING_zh.md) | [行为准则](CODE_OF_CONDUCT_zh.md)

---

## 为什么需要这个列表？

大多数"免费 LLM API"列表都充斥着已经失效的提供商、需要付费才能使用的服务，或者提供的模型太弱以至于完全没有实际用处。本列表只收录满足以下所有条件的提供商：

- **真正免费** —— 不需要信用卡，不需要付费计划即可访问免费层级
- **提供 API 访问** —— 可以进行编程式请求，而不仅仅是在网页界面聊天
- **目前可用** —— 定期检查，如果提供商下线则会被移除
- **模型实用** —— 免费模型可以处理实际任务，而不仅仅是说"你好世界"

---

## 提供商

### Google Gemini (Google AI Studio)

| 项目 | 信息 |
|------|------|
| **模型** | Gemini 2.5 Pro、Gemini 2.5 Flash、Gemini 3.5 Flash、Gemini 3.6 Flash、Gemma 4 等 |
| **API 端点** | `https://generativelanguage.googleapis.com/v1beta` |
| **注册** | [aistudio.google.com](https://aistudio.google.com) |
| **认证** | Google 账号，从 AI Studio 仪表盘获取 API 密钥 |
| **速率限制** | 根据模型约 5-15 RPM，约 100 万 tokens/天 |
| **需要信用卡** | 否 |
| **备注** | 超大上下文窗口（部分模型高达 100 万 tokens）。按项目配额。免费层级的提示词可能会被 Google 用于改进模型。 |

Google AI Studio 免费提供 Gemini 模型系列的访问，且 token 配额非常慷慨。其突出特点是上下文窗口大小 —— Gemini 模型支持高达 100 万 tokens，非常适合处理大型文档或长对话历史。免费层级使用按项目配额，因此你可以创建多个项目来有效倍增你的限额。API 使用 Google 自己的格式（不兼容 OpenAI），但有开源封装器可以添加 OpenAI 兼容性。同时也提供免费的网页 UI 用于快速测试。

---

### Groq

| 项目 | 信息 |
|------|------|
| **模型** | GPT-oss-120B、GPT-oss-20B、Qwen3.6-27B、Groq Compound 等 |
| **API 端点** | `https://api.groq.com/openai/v1`（兼容 OpenAI）|
| **注册** | [console.groq.com](https://console.groq.com) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 30 请求/分钟，6,000 tokens/分钟，每个模型最多 1,000 请求/天 |
| **需要信用卡** | 否 |
| **备注** | 基于 LPU 芯片的超低延迟推理。所有模型免费。最慷慨的免费层级之一。 |

Groq 凭借其定制的 LPU（语言处理单元）芯片提供了本列表中任何提供商中最快的推理速度。免费层级可以访问其平台上的每个模型，不限制你可以使用哪些模型。以每分钟 30 个请求的速率，该限制足够慷慨，可满足严肃的开发工作。API 完全兼容 OpenAI —— 只需在任何 OpenAI SDK 或兼容工具中更换基础 URL 和 API 密钥即可。这是对延迟敏感的实时应用的最佳免费层级。

---

### DeepSeek

| 项目 | 信息 |
|------|------|
| **模型** | DeepSeek V4 Pro、DeepSeek V4 Flash |
| **API 端点** | `https://api.deepseek.com/v1`（兼容 OpenAI）|
| **注册** | [platform.deepseek.com](https://platform.deepseek.com) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 注册赠送 500 万免费 tokens，有效期 30 天 |
| **需要信用卡** | 否 |
| **备注** | 所有提供商中注册赠送最多的 tokens。强大的推理模型。积分可用于所有模型。 |

DeepSeek 为每个新账户在注册时赠送 500 万免费 tokens —— 不需要信用卡 —— 有效期 30 天。这是本列表中任何提供商最慷慨的注册赠金。DeepSeek 的模型，特别是 V4 Pro 和 V4 Flash，是强大的通用和推理模型，性价比极高（前 500 万 tokens 完全免费）。API 完全兼容 OpenAI。主要缺点是这是一次性赠金，不是永久免费层级 —— 500 万 tokens 用完或 30 天过期后，你需要付费。但对于开始使用、评估模型或运行大量请求，没有什么比 500 万免费 tokens 更好的了。

---

### Mistral AI (La Plateforme)

| 项目 | 信息 |
|------|------|
| **模型** | Mistral Large 3、Mistral Medium 3.5、Mistral Small 4、Codestral、Ministral 3 等 |
| **API 端点** | `https://api.mistral.ai/v1`（兼容 OpenAI）|
| **注册** | [console.mistral.ai](https://console.mistral.ai) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 约 1 RPS，约 500K tokens/分钟（共享配额池）|
| **需要信用卡** | 否 |
| **备注** | 免费使用 Mistral Large（旗舰模型）和 Codestral。每月约 10 美元 API 积分。免费模式的提示词可能被用于训练 Mistral 模型。 |

Mistral 的免费层级非常出色，因为它包含了对 Mistral Large（其旗舰闭源模型）和 Codestral（其专用代码生成模型）的访问。很少有提供商免费提供其最佳专有模型。API 兼容 OpenAI，注册后几分钟内即可获取密钥。免费模式每月提供约 10 美元的 API 积分。共享配额池意味着一个模型的大量使用会影响你在其他模型上的限制。不过对于开发和原型设计来说，免费获得 Mistral Large 是很难被超越的。

---

### SiliconFlow

| 项目 | 信息 |
|------|------|
| **模型** | 100+ 模型，包括 Qwen、DeepSeek、Llama、GLM 等 |
| **API 端点** | `https://api.siliconflow.cn/v1`（兼容 OpenAI）|
| **注册** | [siliconflow.com](https://www.siliconflow.com) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 每个免费模型有固定的速率限制（因模型而异）|
| **需要信用卡** | 免费模型不需要 |
| **备注** | 永久免费模型，不会过期。需要身份验证。新账户还获得初始积分。 |

SiliconFlow 是一个中国/国际 AI 推理平台，拥有超过 100 个模型的目录。其核心特色是一组**永久免费模型**，不会过期 —— 这些模型在其定价页面上明确标记为 0 美元。免费模型包括流行的开源模型如 Qwen 和 DeepSeek 变体。除了永久免费模型外，新账户还会获得初始积分。主要缺点是需要身份验证才能注册。API 完全兼容 OpenAI。这是少数几个免费层级真正永久而非限时试用的平台之一。

---

### 智谱 AI (Zhipu AI)

| 项目 | 信息 |
|------|------|
| **模型** | GLM-4.7-Flash、GLM-4.6V-Flash（多模态）|
| **API 端点** | `https://open.bigmodel.cn/api/paas/v4`（兼容 OpenAI）|
| **注册** | [open.bigmodel.cn](https://open.bigmodel.cn) |
| **认证** | 从用户中心获取 API 密钥 |
| **速率限制** | 每个免费模型 1 个并发请求 |
| **需要信用卡** | 否 |
| **备注** | 永久免费层级。GLM-4.7-Flash 支持 200K 上下文。中英文。并发限制低。 |

智谱 AI 提供对其 GLM 模型系列的永久免费访问。GLM-4.7-Flash 支持高达 200K 上下文 tokens，是可用的最大免费上下文窗口之一。模型在中英文方面都表现出色，如果你需要中文语言支持，这是一个绝佳选择。主要限制是免费模型只有 1 个并发请求，意味着你不能并行化请求。API 兼容 OpenAI。还提供免费的多模态模型（GLM-4.6V-Flash），可以同时处理图像和文本。

---

### SambaNova

| 项目 | 信息 |
|------|------|
| **模型** | Llama 3.1 405B、DeepSeek-R1 等 |
| **API 端点** | `https://api.sambanova.ai/v1`（兼容 OpenAI）|
| **注册** | [sambanova.ai](https://sambanova.ai) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 因模型而异（部分模型低至每天 20 个请求）|
| **需要信用卡** | 否 |
| **备注** | 免费使用 Llama 3.1 405B —— 任何免费 API 中最大的开源权重模型。 |

SambaNova 的突出特点是免费提供对 Llama 3.1 405B 的访问，这是任何免费提供商中最大的开源权重模型。如果你需要在不付费的情况下针对超大规模模型测试提示词，这里是最好的选择。代价是较大模型上的速率限制可能非常低（某些模型上每天只有 20 个请求），因此最适合实验和评估，而非持续使用。API 兼容 OpenAI。

---

### Cohere

| 项目 | 信息 |
|------|------|
| **模型** | Command A+、Command A、Command R+、Embed 4、Rerank 3.5、Aya Expanse |
| **API 端点** | `https://api.cohere.com/v2` |
| **注册** | [dashboard.cohere.com](https://dashboard.cohere.com) |
| **认证** | 从仪表盘获取试用 API 密钥 |
| **速率限制** | 20 请求/分钟，每月 1,000 次 API 调用 |
| **需要信用卡** | 否 |
| **备注** | 最佳的免费嵌入和重排序层级。仅限非商业使用。每月调用次数上限是主要限制。 |

Cohere 的免费试用层级是独一无二的，因为它包含了对大多数其他免费提供商不提供的专用模型的访问 —— 特别是 Embed 4（嵌入模型）和 Rerank 3.5（重排序模型）。如果你正在构建搜索、RAG 或任何需要嵌入或重排序的系统，Cohere 是这些特定任务的最佳免费选择。聊天模型（Command A+、Command R+）在通用场景下也很出色，现在还包括多模态功能。主要限制是每月 1,000 次调用的上限，与其他提供商相比较低。这是用于原型设计和研究的试用密钥，而非高容量生产端点。

---

### OpenRouter 免费

| 项目 | 信息 |
|------|------|
| **模型** | Llama 3.3 70B、Gemma、Mistral、Qwen 等数十个模型（免费模型有明确标注）|
| **API 端点** | `https://openrouter.ai/api/v1`（兼容 OpenAI）|
| **注册** | [openrouter.ai](https://openrouter.ai) |
| **认证** | 从仪表盘获取 API 密钥 |
| **速率限制** | 有速率限制，因模型而异 |
| **需要信用卡** | 免费层级不需要 |
| **备注** | 最可靠的免费 LLM API。模型选择丰富，兼容 OpenAI，文档完善。 |

OpenRouter 是免费 LLM API 访问的黄金标准。他们聚合了数十个模型（包括开源和专有），并提供其中一部分的免费访问。免费模型在模型列表中有明确标注。其 API 完全兼容 OpenAI，这意味着任何为 OpenAI API 构建的工具、库或框架只需更改基础 URL 即可与 OpenRouter 配合使用。他们还提供用于测试的聊天界面。免费层级足够慷慨，可用于真实的开发工作，文档也非常出色。如果你只使用本列表中的一个提供商，那就是它。

---

### NVIDIA NIM

| 项目 | 信息 |
|------|------|
| **模型** | Llama、Mistral、CodeLlama、NV-EmbedQA、GPT-oss-120B 等 |
| **API 端点** | `https://integrate.api.nvidia.com/v1`（兼容 OpenAI）|
| **注册** | [build.nvidia.com](https://build.nvidia.com) |
| **认证** | 从 NVIDIA 开发者仪表盘获取 API 密钥 |
| **速率限制** | 免费层级慷慨，速率限制因模型而异 |
| **需要信用卡** | 否 |
| **备注** | NVIDIA 的托管推理 API。最适合在 NVIDIA GPU 上优化的模型。还提供嵌入模型。 |

NVIDIA NIM 提供对 NVIDIA 基础设施上运行的一系列开源模型的免费 API 访问。由于这些模型运行在 NVIDIA 自己的 GPU 上（它们就是为这些硬件设计的），性能和可靠性都非常出色。API 兼容 OpenAI，集成非常简单。除了聊天/补全模型外，NIM 还提供对嵌入模型和其他专用模型的免费访问。开发者仪表盘提供使用追踪和 API 密钥管理。如果你需要嵌入功能，或者想在优化的 NVIDIA 硬件上对模型进行基准测试，这尤其有用。

---

### Hugging Face 推理 API

| 项目 | 信息 |
|------|------|
| **模型** | 数千个开源模型（免费层级路由到多个推理提供商）|
| **API 端点** | `https://router.huggingface.co/v1`（兼容 OpenAI）|
| **注册** | [huggingface.co](https://huggingface.co) |
| **认证** | HF API 令牌（从账户设置获取）|
| **速率限制** | 免费用户每月约 0.10 美元的推理提供商积分 |
| **需要信用卡** | 不需要 |
| **备注** | 最大的模型目录。路由到 Fireworks、Together、Nebius 等。PRO 层级（9 美元/月）解锁更多。 |

Hugging Face 通过其推理 API 提供对最大规模开源模型目录的访问。免费层级提供少量月度积分，将请求路由到各个推理提供商（Fireworks、Together、Nebius 等）。可用模型的种类是无与伦比的 —— 如果你需要特定的微调模型、句子转换器或小众分类模型，Hugging Face 大概都有。免费层级最适合轻量级原型设计和实验。

---

### Cloudflare Workers AI

| 项目 | 信息 |
|------|------|
| **模型** | 75+ 模型，包括 Llama、Mistral、Qwen、DeepSeek R1、GPT-oss-120B 等 |
| **API 端点** | `https://api.cloudflare.com/client/v4/accounts/{account_id}/ai/run/@cf/{model}` |
| **注册** | [dash.cloudflare.com](https://dash.cloudflare.com) |
| **认证** | Cloudflare API 令牌 |
| **速率限制** | 每天 10,000 Neurons |
| **需要信用卡** | Workers 免费计划不需要 |
| **备注** | 运行在 Cloudflare 的边缘网络上。免费层级 75+ 模型。基于 Neuron 计费。还支持图像生成、分类。 |

Cloudflare Workers AI 在 Cloudflare 的全球边缘网络上运行模型，这意味着从世界任何地方都能获得低延迟。计费使用"Neurons"（标准化计算单位）而非原始 token，因此成本因模型大小而异。免费计划每天提供 10,000 个 Neurons，现在免费层级提供 75+ 模型，包括 DeepSeek R1 Distill 和 GPT-oss-120B 等强大模型。除了 LLM 之外，Workers AI 还提供图像生成、翻译、分类和其他 AI 任务。

---

### LLM7.io

| 项目 | 信息 |
|------|------|
| **模型** | GPT-oss-20B、Mistral Nemo、MiniMax M2.7 等 |
| **API 端点** | `https://api.llm7.io/v1`（兼容 OpenAI）|
| **注册** | 匿名访问无需注册 |
| **认证** | 无需密钥（匿名）或从 token.llm7.io 获取免费令牌以提高限制 |
| **速率限制** | 10 RPM，60 请求/小时（匿名）；使用免费令牌更高 |
| **需要信用卡** | 否 |
| **备注** | 本列表中唯一不需要任何注册的提供商。直接调用 API 即可。 |

LLM7.io 在本列表中是独一无二的，因为它**不需要账户也不需要 API 密钥**即可匿名访问。你可以字面意义上立即开始发请求，零摩擦。匿名层级在 GPT-oss-20B 和 Mistral Nemo 等模型上支持 128K 上下文。如果你想要更高的速率限制，可以从他们的网站获取免费令牌，但即使匿名层级也是可用的。这使得 LLM7.io 是上手最快的提供商 —— 没有注册表单，没有邮箱验证，没有仪表盘。只需将你的代码指向端点即可。

---

### OpenAI Codex 免费计划

| 项目 | 信息 |
|------|------|
| **模型** | Codex（代码生成代理）|
| **API 端点** | 基于 CLI（非传统 REST API）|
| **注册** | [github.com/openai/codex](https://github.com/openai/codex) |
| **认证** | GitHub 账号（免费层级使用 GitHub 的计算资源）|
| **速率限制** | 有限的计算配额，定期重置 |
| **需要信用卡** | 否 |
| **备注** | CLI 工具，非 REST API。专为代码生成任务设计。在终端中运行。 |

OpenAI 的 Codex CLI 通过基于终端的代理提供免费的代码生成功能。你通过命令行而非传统的 API 调用来与之交互。它在底层使用 OpenAI 的模型，但接口是基于代理的，而非请求-响应模式。适用于直接从终端进行自动化编码工作流、代码重构和代码审查任务。

---

### Kilocode Gateway 免费模型

| 项目 | 信息 |
|------|------|
| **模型** | Nemotron-3-Ultra-550B、Step-3.7-Flash、Laguna S 2.1、Tencent Hy3 等（免费模型池）|
| **API 端点** | `https://api.kilo.ai/api/gateway`（兼容 OpenAI）|
| **注册** | [kilo.ai](https://app.kilo.ai) |
| **认证** | 免费模型不需要 API 密钥 |
| **速率限制** | 200 请求/小时 |
| **需要信用卡** | 否 |
| **备注** | 自动路由器（`kilo-auto/free`）自动选择最佳模型。无需密钥。200 请求/小时非常慷慨。 |

Kilocode Gateway 充当聚合器，通过兼容 OpenAI 的 API 提供对多个模型的访问。其突出特点是 `kilo-auto/free` 自动路由器，会动态将你的请求路由到免费池中最佳可用模型 —— 完全不需要 API 密钥。以每小时 200 个请求的速度，速率限制非常慷慨。免费模型池包括强大的模型如 Nemotron-3-Ultra-550B（100 万上下文）和 Laguna S 2.1 代码生成模型。请查看其仪表盘获取当前可用免费模型列表，因为模型选择会随时间变化。

---

## 快速对比

| 提供商 | API 格式 | 所有模型免费 | 最适合 |
|--------|-----------|------------|--------|
| Google Gemini | Google API | 是 | 超长上下文（高达 100 万 tokens）|
| Groq | 兼容 OpenAI | 是 | 速度 + 慷慨的限制 |
| DeepSeek | 兼容 OpenAI | 试用积分 | 强大推理模型，最佳注册赠金（500 万 tokens）|
| Mistral AI | 兼容 OpenAI | 是 | 免费获得旗舰模型 |
| SiliconFlow | 兼容 OpenAI | 部分（标注免费）| 永久免费模型，中国/国际 |
| 智谱 AI | 兼容 OpenAI | 部分（免费模型）| GLM 模型，中英文，200K 上下文 |
| SambaNova | 兼容 OpenAI | 部分 | Llama 3.1 405B 访问 |
| Cohere | 专有格式 | 是 | 嵌入 + 重排序 |
| OpenRouter | 兼容 OpenAI | 部分（标注免费）| 通用场景，最可靠 |
| NVIDIA NIM | 兼容 OpenAI | 是 | 嵌入模型，NVIDIA 优化模型 |
| Hugging Face | 兼容 OpenAI | 部分（按积分计费）| 最大的模型目录 |
| Cloudflare Workers AI | CF REST | 是 | 边缘推理，75+ 免费模型 |
| LLM7.io | 兼容 OpenAI | 是 | 零摩擦匿名访问 |
| OpenAI Codex | CLI | 不适用 | 代码生成任务 |
| Kilocode Gateway | 兼容 OpenAI | 免费标注 | 自动路由，200 请求/小时，无需密钥 |

## 贡献

发现了真正免费且有用的提供商？请查看[贡献指南](CONTRIBUTING_zh.md)。虚假提供商、死链接和伪装成免费的付费服务将被拒绝。

## 免责声明

免费层级可能随时更改。提供商可能会在不另行通知的情况下引入速率限制、移除模型或关闭免费访问。本列表基于尽力而为的原则维护。在生产环境中依赖这些服务之前，请务必查看提供商的当前条款。

## 许可证

[MIT](LICENSE) © creepervm1000