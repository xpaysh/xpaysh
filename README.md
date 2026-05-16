# 🚀 {xpay✦} — Open Protocols for Agentic Commerce

<div align="center">

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=1000&color=2563EB&width=700&lines=Open+protocols+for+agentic+commerce;ACP+%E2%80%A2+UCP+%E2%80%A2+AP2+%E2%80%A2+MCP+%E2%80%A2+x402;Multi-protocol.+Rail-agnostic.;Plugins+for+every+eCommerce+platform.)](https://git.io/typing-svg)

</div>

<div align="center">

**🛒 Per-platform OSS plugins** • **🤖 Multi-protocol from day one** • **💳 Rail-agnostic** • **🔓 Apache-2.0 / GPLv2 / CC0**

[![Website](https://img.shields.io/badge/🌐_Website-xpay.sh-2563eb?style=for-the-badge)](https://www.xpay.sh)
[![Docs](https://img.shields.io/badge/📖_Docs-docs.xpay.sh-10b981?style=for-the-badge)](https://docs.xpay.sh)
[![Comparison](https://img.shields.io/badge/⚖️_ACP_vs_UCP_vs_AP2-Compared-7c3aed?style=for-the-badge)](https://docs.xpay.sh/agentic-commerce-protocols/comparison)
[![Awesome List](https://img.shields.io/badge/📚_awesome--agentic--commerce-brightgreen?style=for-the-badge)](https://github.com/xpaysh/awesome-agentic-commerce)

</div>

---

## 🎯 What we ship

Open-source, vendor-neutral infrastructure for the layer where **AI agents transact with merchants on behalf of human buyers**.

- **Per-platform plugins** — `agentic-commerce-for-<platform>` family. Each plugin speaks **[ACP](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol)** (OpenAI + Stripe + Meta), **[UCP](https://github.com/Universal-Commerce-Protocol/ucp)** (vendor-neutral, RFC 9421 signed), and **[AP2](https://github.com/google-agentic-commerce/AP2)** (Google, mandate-based) from day one. Rail-agnostic: cards, [Stripe MPP](https://mpp.dev), [x402](https://x402.org), stablecoins — your choice.
- **Real-standard discovery only** — `/llms.txt`, schema.org JSON-LD, `robots.txt` for real AI crawlers (`GPTBot`, `ClaudeBot`, `Google-Extended`, `PerplexityBot`, `CCBot`, `Amazonbot`). We don't emit invented well-known URIs.
- **Upstream contributions** — active PRs on the ACP and UCP specs themselves ([ACP #251](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol/pull/251), [UCP #443](https://github.com/Universal-Commerce-Protocol/ucp/pull/443)), tracking RFC 9421 adoption in ACP as a longer-running SEP.

---

## 🛠️ Active projects

### Agentic commerce plugin family

| Repo | Status | What it does |
|---|---|---|
| [`agentic-commerce-for-woocommerce`](https://github.com/xpaysh/agentic-commerce-for-woocommerce) | **Live** (v0.1.7+, GPLv2) | WordPress plugin. ACP + UCP + AP2 on a WC store. |
| [`agentic-commerce-for-commercetools`](https://github.com/xpaysh/agentic-commerce-for-commercetools) | **Scaffolded** | Headless / Connect Service for commercetools projects. |
| [`agentic-commerce-for-bigcommerce`](https://github.com/xpaysh/agentic-commerce-for-bigcommerce) | **Scaffolded** | BigCommerce App for stores in the App Marketplace. |
| [`agentic-commerce-plugin-template`](https://github.com/xpaysh/agentic-commerce-plugin-template) | Scaffold | Shared TypeScript template the family builds on. CI linter blocks fictitious well-known URIs. |
| [`awesome-agentic-commerce`](https://github.com/xpaysh/awesome-agentic-commerce) | Curated index | Ecosystem registry — xpay-built + vendor-built + community. |
| `agentic-commerce-for-magento` · `…-shopify-app` · `…-salesforce-commerce` | Planned | First-party plugins, staggered cadence. |
| `…-prestashop` · `…-saleor` · `…-opencart` · `…-shopware` · `…-spree` · `…-sylius` · `…-nopcommerce` · `…-drupal-commerce` · `…-ecwid` | Community | Template-based, community-contributed. |

### x402 ecosystem

| Repo | What it does |
|---|---|
| [`awesome-x402`](https://github.com/xpaysh/awesome-x402) | Curated list of x402 resources and tooling. |
| [`x402-local`](https://github.com/xpaysh/x402-local) | Local development environment for x402. |
| [Public facilitator](https://facilitator.xpay.sh) | xpay✦-operated x402 facilitator service. Free to use. |

---

## 🤖 Agent-readable storefronts in two lines

Drop the WooCommerce plugin into a store, and your catalog becomes addressable by ChatGPT, Claude, Gemini, and Perplexity — without changing your theme or payment processor:

```bash
# Install the plugin
wp plugin install agentic-commerce-for-woocommerce --activate

# Verify discovery surface (after activation)
curl -s https://your-store.example/llms.txt
curl -s https://your-store.example/robots.txt | grep -iE 'GPTBot|ClaudeBot|Google-Extended|PerplexityBot'
curl -s https://your-store.example/product/some-slug/ | grep 'application/ld+json'
```

For headless storefronts (commercetools, BigCommerce, custom), the family's [TypeScript template](https://github.com/xpaysh/agentic-commerce-plugin-template) ships as a Node service alongside your storefront.

---

## 🤝 Upstream protocol contributions

xpay✦ is contributing back to the specifications themselves — not just consuming them:

- **ACP** — [PR #251](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol/pull/251) (README changelog listing). Tracking [Issue #97](https://github.com/agentic-commerce-protocol/agentic-commerce-protocol/issues/97) (Idempotency-Key TTL) as a near-term SEP candidate. Longer-running interest: RFC 9421 adoption in ACP, citing UCP precedent.
- **UCP** — [PR #443](https://github.com/Universal-Commerce-Protocol/ucp/pull/443) (shared-type centralization, [Issue #412](https://github.com/Universal-Commerce-Protocol/ucp/issues/412)) — endorsed by `@igrigorik` (Shopify, Tech Council) and `@wry-ry` (top committer).
- **AP2** — watching.

Side-by-side technical comparison of the three protocols: **[docs.xpay.sh/agentic-commerce-protocols/comparison](https://docs.xpay.sh/agentic-commerce-protocols/comparison)**.

---

## 🛠️ Tech stack

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-21759B?style=flat-square&logo=wordpress&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)

</div>

---

## 💬 Connect

<div align="center">

📧 **[hello@xpay.sh](mailto:hello@xpay.sh)** &middot; 🐦 **[@xpaysh](https://twitter.com/xpaysh)** &middot; 💼 **[LinkedIn](https://linkedin.com/company/xpay)** &middot; 🌐 **[xpay.sh](https://www.xpay.sh)**

</div>

---

<div align="center">

*Open protocols, real standards, every platform.*

**Last updated: May 2026**

</div>
