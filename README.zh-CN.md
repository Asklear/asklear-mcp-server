<p align="center">
  <img src="./assets/asklear-mark.svg" width="72" alt="Asklear">
</p>

<h1 align="center">Asklear MCP</h1>

<p align="center"><strong>面向 AI Agent 的商业研究基础设施。</strong></p>

<p align="center">
  <a href="https://docs.asklear.cn">Agent 使用手册</a>
</p>

<p align="center">
  <a href="./README.md">English</a> · 简体中文
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCP-Hosted-5B6EF5?style=flat-square" alt="Hosted MCP">
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-16212A?style=flat-square" alt="Streamable HTTP">
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Asklear/asklear-mcp-server?style=flat-square" alt="Apache-2.0 license"></a>
</p>

Asklear MCP 是 Asklear · 澈问托管的 [Model Context Protocol](https://modelcontextprotocol.io) 入口。AI Agent 通过一个稳定接口使用商业研究能力，访问控制、数据契约、用量与计费由服务端统一管理。

## 可以研究什么

| 研究任务 | 示例问题 |
| --- | --- |
| 市场与类目分析 | 一个类目的规模和趋势如何？ |
| 品牌竞争格局 | 哪些品牌的份额正在上升或下降？ |
| 增长驱动分析 | 哪些商品、价格带或店铺推动了变化？ |

Asklear 目前处于内测阶段，能力覆盖京东、天猫、拼多多、抖音商城等专业商业数据，以及小红书和指定公开网页信息获取。实际权限和覆盖始终以认证后的 MCP 工具列表与运行时响应为准。

## 快速开始

把下面这句公开指令复制给 Codex、Claude Code 或 WorkBuddy：

```text
请读取 https://dashboard.asklear.cn/agent-setup?format=markdown，帮我连接 Asklear。
```

Agent 会读取 Setup 入口、添加托管 MCP 服务，并发起标准浏览器授权。你只需要在 Asklear 官方页面完成注册或登录、按需输入内测码并确认连接。授权完成后，Agent 会调用 `connection_status` 验证连接。

## 尝试第一个研究问题

```text
请使用 Asklear 分析京东宠物零食品类最近 12 个完整月：

1. 市场规模和月度趋势如何？
2. 主要品牌是谁，份额如何变化？
3. 有哪些值得关注的机会和风险？

请说明实际时间范围、指标口径、证据和限制。
```

## 使用手册

人类可在下面的公开使用手册中查看能力、查询规则、研究方法和错误恢复：

```text
https://docs.asklear.cn
```

连接后的 Agent 通过 MCP `docs` 工具读取同一内容源。连接与授权统一从独立的 [Agent Setup 入口](https://dashboard.asklear.cn/agent-setup) 开始。

## 从研究到交付物

- 当问题需要更完整的研究路径时，使用 Agent Docs 中的研究方法。

## 仓库边界

> [!NOTE]
> 这是 Asklear · 澈问托管 MCP 服务的公开接入仓库，不包含生产服务实现、客户凭据、私有接入地址或商业数据。实际能力由认证后的服务及账户权益决定。

本仓库只有一个目标：作为 Asklear MCP 的公开接入入口。这里只维护项目介绍、最短且安全的连接示例，以及公开安全与许可信息。生产 API/MCP 契约、数据集定义、计费规则、Agent Docs、研究方法和 Dashboard 行为由服务仓库维护；官网与编辑型 Research 内容属于 Mainpage 仓库。

## 安全

安全漏洞请按 [SECURITY.md](SECURITY.md) 私密上报，不要创建公开 Issue。

## 许可

本仓库采用 [Apache-2.0](LICENSE) 许可。该许可证不授予 Asklear 商标使用权，也不代表官方背书。
