<p align="center">
  <img src="./assets/asklear-mark.svg" width="72" alt="Asklear">
</p>

<h1 align="center">Asklear MCP</h1>

<p align="center">
  <strong>Commercial data and web research for AI agents.</strong>
</p>

<p align="center">
  Give Codex, Claude Code, WorkBuddy, and enterprise agents<br>
  access to commercial data, current content, and in-depth web evidence.
</p>

<p align="center">
  <a href="https://dashboard.asklearai.com">Dashboard</a>
  ·
  <a href="https://dashboard.asklearai.com/agent-setup">Connect Asklear</a>
  ·
  <a href="https://docs.asklearai.com">Agent Docs</a>
  ·
  <a href="./README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCP-Hosted-5B6EF5?style=flat-square" alt="Hosted MCP">
  <img src="https://img.shields.io/badge/Auth-OAuth-16212A?style=flat-square" alt="OAuth">
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-16212A?style=flat-square" alt="Streamable HTTP">
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Asklear/asklear-mcp-server?style=flat-square" alt="Apache-2.0 license"></a>
</p>

## What is Asklear?

Asklear provides the commercial data and web capabilities AI agents need for research through a hosted [Model Context Protocol](https://modelcontextprotocol.io) service.

Agents can use Asklear to gather external evidence about markets, brands, products, content, and consumer response, combine it with a user's internal material, and conduct market analysis, category research, competitive comparisons, user research, and trend analysis.

Asklear manages data capabilities, account access, query contracts, usage, and billing.

## What can it do?

| Capability | Best for | Current coverage examples |
| --- | --- | --- |
| Structured historical data | Market size, growth trends, brand share, product, and price-band analysis | JD, Tmall, Pinduoduo, and Douyin E-commerce |
| Real-time platform interfaces | Consumer response, content performance, trend, and topic research | Xiaohongshu, Douyin, Weibo, Bilibili, WeChat Official Accounts, and WeChat Channels |
| Cloud web collection | Reading public webpages in batches as clean, structured content | News, brand sites, industry sites, and other public pages |

Authenticated MCP `tools/list` results and runtime responses are authoritative for current capabilities, fields, and account access.

## Connect Asklear

Send this instruction to an MCP-capable agent:

```text
Read https://dashboard.asklearai.com/agent-setup?format=markdown and help me connect Asklear.
```

The agent reads the latest official setup instructions and completes MCP configuration, OAuth authorization, and connection verification for the current client.

You only step in on Asklear's official pages when trust, registration or sign-in, beta access, or authorization is required. You never need to copy or store an API key.

> `https://dashboard.asklearai.com/agent-setup` is the single entry point for connecting Asklear. Follow the latest instructions returned by that entry.

## Ask your first question

After connecting, give the agent a business question directly:

```text
Use Asklear to analyze the JD pet-snack category over the latest 12 complete months.

1. How large is the market, and what is the monthly trend?
2. Which brands lead, and how are their shares changing?
3. Which products, price bands, or shops are driving growth?
4. What opportunities or risks deserve attention?

Report the resolved time range, metric definitions, evidence, and limitations.
```

The agent selects the relevant capabilities, runs the queries needed to answer the question, and explains the exact scope returned.

## From question to conclusion

Asklear is not limited to running a single query. It lets an agent combine evidence from different sources.

To investigate a consumer brand's growth opportunities, an agent can:

1. Measure market size, growth, and brand share with historical commerce data;
2. Drill into products, shops, and price bands to locate the sources of growth;
3. Retrieve current content and engagement data from content platforms;
4. Analyze consumer concerns, use cases, and negative feedback;
5. Combine those findings with internal sales, channel, or customer data;
6. Deliver conclusions with definitions, evidence, and limitations.

```text
Business question
   ↓
Structured market data + current consumer content + public web and internal material
   ↓
Agent analysis, validation, and delivery
```

## Choose the right capability

- Markets, categories, brands, products, sales, or revenue → use structured historical data.
- Current content, consumer response, trends, topics, or engagement → use real-time platform interfaces.
- Multiple public webpages → use cloud web collection.

For the full capability catalog, query rules, research methods, and error recovery, read:

- [Asklear Agent Docs](https://docs.asklearai.com)
- [Capabilities & Data](https://docs.asklearai.com/capabilities)
- [Query Guide](https://docs.asklearai.com/querying)
- [Cookbook](https://docs.asklearai.com/cookbook)
- [Errors & Recovery](https://docs.asklearai.com/errors)

## Dashboard

Visit the [Asklear Dashboard](https://dashboard.asklearai.com) to manage your account, connections, data access, and usage.

## Repository scope

This is the public GitHub entry point for Asklear MCP. It provides the product and capability overview, the official connection entry, Agent Docs links, and public security and license information.

This repository does not contain the production server implementation, commercial data, customer credentials, or private infrastructure. The hosted service and authenticated runtime responses are authoritative for capabilities, data contracts, account access, and billing.

## Security

Report security issues privately as described in [SECURITY.md](./SECURITY.md). Do not disclose vulnerabilities or credentials in a public issue.

## License

Licensed under the [Apache License 2.0](./LICENSE). The license does not grant rights to use Asklear trademarks or imply endorsement of third-party projects.
