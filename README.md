# AI Crawler `robots.txt` & `llms.txt` Presets (2026 Edition)

Production-ready `robots.txt` policies and an `llms.txt` starter template maintained by **[AI SEO COMPANY](https://www.ai-seo-company.pl/)** (`AI SIGNALS COMPANY P.S.A.`, Warsaw).

Most websites accidentally block **AI search & citation crawlers** (`OAI-SearchBot`, `PerplexityBot`, `Claude-SearchBot`) when trying to block **LLM foundation-model training scrapers** (`GPTBot`, `ClaudeBot`, `Google-Extended`). OpenAI, Anthropic, Perplexity, and Google operate separate user-agents for live search citations vs. model training.

Test your live domain (including HTTP `200/403` WAF headers, Cloudflare Verified Bots, and SSR payload visibility without JS) with our free live scanner:

- **English:** [AI Crawler & `robots.txt` Live Checker](https://www.ai-seo-company.pl/en/tools/ai-crawler-robots-txt-checker) · [`llms.txt` Generator](https://www.ai-seo-company.pl/en/tools/llms-txt-generator)
- **Polski:** [Tester robotów AI i generator `robots.txt`](https://www.ai-seo-company.pl/narzedzia/tester-robotow-ai-robots-txt) · [Generator `llms.txt`](https://www.ai-seo-company.pl/narzedzia/generator-llms-txt)
- **Deutsch:** [KI-Crawler & `robots.txt` Live-Prüfer](https://www.ai-seo-company.pl/de/tools/ki-crawler-robots-txt-pruefen) · [`llms.txt` Generator](https://www.ai-seo-company.pl/de/tools/llms-txt-generator)

---

## Included Presets

| File | Goal | AI Search & Citations | LLM Training Scrapers | Classic Google & Bing |
| :--- | :--- | :--- | :--- | :--- |
| `presets/recommended-geo.robots.txt` | **Recommended for B2B & E-commerce (GEO + SEO)** | **Allowed** (`OAI-SearchBot`, `ChatGPT-User`, `PerplexityBot`, `Claude-SearchBot`) | **Blocked** (`GPTBot`, `ClaudeBot`, `Google-Extended`, `Applebot-Extended`, `Meta-ExternalAgent`) | **Allowed** (`Googlebot`, `Bingbot`, `Applebot`) |
| `presets/open-geo.robots.txt` | Maximum brand exposure across all search & LLM datasets | **Allowed** | **Allowed** | **Allowed** |
| `presets/strict-block-ai.robots.txt` | Paywalled publishers blocking all generative AI | **Blocked** | **Blocked** | **Allowed** |
| `presets/cms-wordpress-woocommerce.robots.txt` | WordPress & WooCommerce crawl-budget + GEO policy | **Allowed** | **Blocked** | **Allowed** |
| `presets/cms-shopify.robots.txt` | Shopify (`/collections/*+*` & cart protection) + GEO policy | **Allowed** | **Blocked** | **Allowed** |
| `presets/cms-nextjs-vercel.robots.txt` | Next.js App Router / Vercel (`/_next/static/` open, `/api/` blocked) | **Allowed** | **Blocked** | **Allowed** |
| `presets/cms-webflow.robots.txt` | Webflow internal search protection + GEO policy | **Allowed** | **Blocked** | **Allowed** |
| `presets/cms-prestashop.robots.txt` | PrestaShop faceted controller protection + GEO policy | **Allowed** | **Blocked** | **Allowed** |
| `templates/llms.txt` | Structured Markdown index of canonical URLs & entity facts for LLMs | Used by AI assistants & agents | - | - |
| `packages/llms-txt-check` | Zero-dependency Node.js CLI validator for `/llms.txt` & `/robots.txt` | Validates 15 AI & search bots | - | - |

---

## 2026 AI User-Agent Reference Matrix

| User-Agent | Operator | Role | Recommended Action for B2B Brands |
| :--- | :--- | :--- | :--- |
| `OAI-SearchBot` | OpenAI | ChatGPT Search index & live source citations | `Allow: /` |
| `ChatGPT-User` | OpenAI | Live page fetch during user prompts in ChatGPT | `Allow: /` |
| `PerplexityBot` | Perplexity AI | Perplexity answer engine index & citations | `Allow: /` |
| `Perplexity-User` | Perplexity AI | User-triggered live fetch in Perplexity | `Allow: /` |
| `Claude-SearchBot` | Anthropic | Claude web search & cited answers | `Allow: /` |
| `Googlebot` | Google | Google Search & Google AI Overviews / AI Mode | `Allow: /` |
| `Bingbot` | Microsoft | Bing Search & Copilot / ChatGPT Search grounding | `Allow: /` |
| `Applebot` | Apple | Siri & Spotlight Search | `Allow: /` |
| `GPTBot` | OpenAI | Foundation model training corpus | `Disallow: /` (optional) |
| `ClaudeBot` | Anthropic | Claude model training corpus | `Disallow: /` (optional) |
| `Google-Extended` | Google | Gemini training opt-out token (does not affect Google Search or AI Overviews) | `Disallow: /` (optional) |
| `Applebot-Extended` | Apple | Apple Intelligence model training opt-out | `Disallow: /` (optional) |
| `Meta-ExternalAgent` | Meta | Llama AI training & scraping | `Disallow: /` (optional) |

---

## Why `robots.txt` Alone Is Not Enough for GEO

1. **WAF / CDN Bot Fight Mode (`HTTP 403`):** Even with `Allow: /` in `robots.txt`, Cloudflare Bot Fight Mode or firewall rules can block `OAI-SearchBot` or `PerplexityBot` at the HTTP edge.
2. **Client-Side JavaScript (`CSR`):** Most AI answer-engine fetchers do not execute heavy client-side JS bundles. If your content renders inside an empty `<div id="root"></div>`, AI crawlers index an empty shell. Compare SSR vs CSR performance with our [Core Web Vitals & SSR Comparison Tool](https://www.ai-seo-company.pl/en/tools/core-web-vitals-competitor-comparison).
3. **Entity Consistency (`JSON-LD` + `/llms.txt`):** Pair clean crawler access with `Organization` / `Person` `sameAs` links (validate yours in our [Entity Graph JSON-LD Validator](https://www.ai-seo-company.pl/en/tools/entity-graph-json-ld-validator)) and a concise `/llms.txt` index at the root of your domain.
4. **2026 Empirical Benchmark (CC BY 4.0):** See real AI crawler blocking rates and the top 49 technical SEO issues across 149+ commercial domains in our [2026 Technical SEO & AI Bot Benchmark Report](https://www.ai-seo-company.pl/en/seo-errors-benchmark-report) ([Polish version](https://www.ai-seo-company.pl/raport-bledow-seo-w-polsce)).

## License

MIT License - Copyright (c) 2026 AI SIGNALS COMPANY Prosta Spółka Akcyjna ([https://www.ai-seo-company.pl/](https://www.ai-seo-company.pl/)).
