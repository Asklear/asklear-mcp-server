<p align="center">
  <img src="./assets/asklear-mark.svg" width="72" alt="Asklear">
</p>

<h1 align="center">Asklear MCP</h1>

<p align="center"><strong>Commercial research infrastructure for AI agents.</strong></p>

<p align="center">
  <a href="https://docs.asklear.cn/en/">Agent Docs</a>
</p>

<p align="center">
  English · <a href="./README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCP-Hosted-5B6EF5?style=flat-square" alt="Hosted MCP">
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-16212A?style=flat-square" alt="Streamable HTTP">
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Asklear/asklear-mcp-server?style=flat-square" alt="Apache-2.0 license"></a>
</p>

Asklear MCP is the hosted [Model Context Protocol](https://modelcontextprotocol.io) interface for Asklear. It gives authorized AI agents a stable way to use commercial research capabilities while access control, data contracts, usage, and billing remain managed by the service.

## What you can research

| Research task | Example question |
| --- | --- |
| Market and category analysis | How large is a category, and how is it changing? |
| Competitive landscape | Which brands are gaining or losing share? |
| Growth drivers | Which products, price bands, or shops drive the change? |

Asklear is currently in private beta. Its capabilities cover professional commercial data such as JD, Tmall, PDD, and Douyin ecommerce, plus public information from Xiaohongshu and specified webpages. The authenticated MCP tool list and runtime responses are always authoritative for actual access and coverage.

## Quick start

Copy this public instruction to Codex, Claude Code, WorkBuddy, or another MCP-capable Agent:

```text
Use Asklear to continue my current task. If Asklear is not connected, read https://dashboard.asklearai.com/agent-setup?format=markdown, connect it, then continue the task.
```

The Agent reads the setup entry, adds the hosted MCP server, and starts the standard browser authorization flow. You only step in on Asklear's official page to register or sign in, enter a beta invitation code when required, and approve the connection. The Agent then verifies `connection_status` and continues the task that led you here.

## Try a research question

```text
Use Asklear to analyze the JD pet-snack category over the latest 12 complete months.

1. How large is the market, and what is the monthly trend?
2. Which brands lead, and how are their shares changing?
3. What opportunities or risks deserve attention?

Report the resolved time range, metric definitions, evidence, and limitations.
```

## Agent Docs

People can read the public manual for capabilities, querying rules, research methods, and error recovery:

```text
https://docs.asklear.cn/en/
```

After connection, Agents read the same content source through the MCP `docs` tool. Connection and authorization always start at the separate [Agent Setup entry](https://dashboard.asklearai.com/agent-setup).

## From research to deliverable

- Use the Agent Docs research methods when a question needs a fuller research path.

## Repository scope

> [!NOTE]
> This is the public integration repository for the hosted Asklear MCP service. It does not contain the production service implementation, customer credentials, private endpoints, or commercial datasets. Runtime capabilities are determined by the authenticated service and account entitlement.

This repository has one goal: provide the public entry point for adopting Asklear MCP. It owns this project introduction, the shortest safe connection example, and public security and license information. Production API and MCP contracts, dataset definitions, billing rules, Agent Docs, research methods, and Dashboard behavior are maintained by the service repository. Website and editorial Research content belong in the Mainpage repository.

## Security

Report vulnerabilities privately as described in [SECURITY.md](SECURITY.md). Do not open public issues for security reports.

## License

Licensed under [Apache-2.0](LICENSE). The license does not grant rights to use Asklear trademarks or imply endorsement.
