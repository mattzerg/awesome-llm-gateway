# Awesome LLM Gateway [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of LLM API gateways, proxies, routers, and the observability tooling around them.

An **LLM gateway** is a single endpoint you route every model call through instead of wiring each provider into your app one by one. A good one gives you three things a direct call can't: a **ledger** (what every call cost), a **trace** (which model and route served it), and **control** (budgets, rate limits, fallback when a provider degrades).

Maintained by the [Router One](https://router.one) team. Entries are ordered alphabetically within each section; inclusion is not endorsement, and we list our own product in its section like any other entry. Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [Managed gateways](#managed-gateways)
- [Self-hosted gateways & proxies](#self-hosted-gateways--proxies)
- [Routing frameworks & research](#routing-frameworks--research)
- [Observability & cost tracking](#observability--cost-tracking)
- [Reading](#reading)
- [Related lists](#related-lists)

## Managed gateways

Hosted services: you get an endpoint and a key, the operator runs the infrastructure.

- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/) — Gateway layer on Cloudflare's edge: caching, rate limiting, retries, and analytics in front of your existing provider keys.
- [Eden AI](https://www.edenai.co/) — Aggregated API across many AI capabilities (LLMs, vision, speech) with unified billing.
- [OpenRouter](https://openrouter.ai/) — Large public catalog of models behind one OpenAI-compatible API, with published per-model token pricing.
- [Portkey](https://portkey.ai/) — AI gateway plus guardrails, virtual keys, and observability; also ships an open-source gateway core.
- [Requesty](https://requesty.ai/) — Managed router with fallback and cost analytics over multiple providers.
- [Router One](https://router.one) — Unified LLM API gateway: OpenAI-compatible and Anthropic-compatible endpoints for 40+ supported models, smart routing with automatic same-family fallback, per-request cost traces, per-key budgets, and native Claude Code / Codex CLI support; reachable worldwide including mainland China.
- [Unify](https://unify.ai/) — Routing layer that picks models per prompt based on quality/cost/latency benchmarks.
- [Vercel AI Gateway](https://vercel.com/docs/ai-gateway) — Managed gateway tightly integrated with the Vercel platform and AI SDK ecosystem.

## Self-hosted gateways & proxies

Open-source software you deploy and operate yourself: full control, your infrastructure, your ops.

- [Apache APISIX AI Gateway](https://apisix.apache.org/) — General-purpose API gateway with AI plugins for proxying, token limiting, and content moderation.
- [Helicone AI Gateway](https://github.com/Helicone/ai-gateway) — Rust-based self-hostable gateway from the Helicone team, with routing and caching.
- [Kong AI Gateway](https://konghq.com/products/kong-ai-gateway) — AI plugins on top of Kong Gateway: multi-provider proxying, prompt guarding, analytics.
- [LiteLLM](https://github.com/BerriAI/litellm) — The most widely used open-source LLM proxy: 100+ providers behind an OpenAI-compatible API, with routing, budgets, and a managed tier.
- [One API](https://github.com/songquanpeng/one-api) — Self-hosted multi-provider key management and OpenAI-compatible distribution station, popular in the Chinese-speaking ecosystem.
- [Portkey Gateway](https://github.com/Portkey-AI/gateway) — Open-source core of Portkey: a lightweight gateway with fallback, retries, and load balancing.
- [TensorZero](https://github.com/tensorzero/tensorzero) — Open-source gateway with built-in experimentation, observability, and optimization feedback loops.

## Routing frameworks & research

- [FrugalGPT](https://arxiv.org/abs/2305.05176) — Paper on LLM cascades: route cheap first, escalate only when needed.
- [RouteLLM](https://github.com/lm-sys/RouteLLM) — Open framework from LMSYS for training and serving quality/cost model routers.

## Observability & cost tracking

Tools that answer "what did that call cost, and why did it behave that way" — often used alongside a gateway.

- [Helicone](https://github.com/Helicone/helicone) — Open-source LLM observability: request logging, sessions, prompt analytics, evals.
- [Langfuse](https://github.com/langfuse/langfuse) — Open-source LLM engineering platform: traces, evals, prompt management, metrics.
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — OpenTelemetry-based instrumentation for LLM calls, vendor-neutral.
- [Phoenix](https://github.com/Arize-ai/phoenix) — Open-source AI observability and evaluation from Arize.

## Reading

- [Router One: how gateway routing is measured](https://router.one/routing-methodology) — A worked example of EWMA latency scoring, fallback triggers, and how routing decisions get recorded per request.
- [What is an LLM API gateway?](https://router.one/llm-api-gateway) — Ledger / trace / control framing of what a gateway adds over direct calls.

## Related lists

- [awesome-llm](https://github.com/Hannibal046/Awesome-LLM) — Large language models broadly.
- [awesome-llmops](https://github.com/tensorchord/Awesome-LLMOps) — Operating LLMs in production.

## License

[CC0 1.0](LICENSE) — public domain. Do whatever you want with this list.
