<p align="center">
  <img src="./assets/asklear-mark.svg" width="72" alt="Asklear">
</p>

<h1 align="center">Asklear MCP</h1>

<p align="center">
  <strong>面向 AI Agent 的商业数据与网页研究能力。</strong>
</p>

<p align="center">
  让 Codex、Claude Code、WorkBuddy 及企业自建 Agent<br>
  获取商业数据、实时内容和深度网页证据。
</p>

<p align="center">
  <a href="https://dashboard.asklear.cn">Dashboard</a>
  ·
  <a href="https://dashboard.asklear.cn/agent-setup">连接 Asklear</a>
  ·
  <a href="https://docs.asklear.cn">使用手册</a>
  ·
  <a href="./README.md">English</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCP-Hosted-5B6EF5?style=flat-square" alt="Hosted MCP">
  <img src="https://img.shields.io/badge/Auth-OAuth-16212A?style=flat-square" alt="OAuth">
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-16212A?style=flat-square" alt="Streamable HTTP">
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Asklear/asklear-mcp-server?style=flat-square" alt="Apache-2.0 license"></a>
</p>

## Asklear 是什么

Asklear · 澈问通过托管的 [Model Context Protocol](https://modelcontextprotocol.io) 服务，为 AI Agent 提供商业研究所需的数据和网页能力。

Agent 可以通过 Asklear 获取市场、品牌、商品、内容和消费者反馈等外部证据，并结合用户已有的内部资料，完成市场分析、品类研究、竞品比较、用户研究和趋势判断。

Asklear 统一管理数据能力、账户权限、查询契约、用量与计费。

## 能做什么

| 能力 | 适合解决的问题 | 当前覆盖示例 |
| --- | --- | --- |
| 结构化历史数据 | 市场规模、增长趋势、品牌份额、商品与价格带分析 | 京东、天猫、拼多多、抖音电商 |
| 实时平台接口 | 用户反馈、内容表现、热点与话题研究 | 小红书、抖音、微博、哔哩哔哩、微信公众号、视频号 |
| 云端网页采集 | 批量读取公开网页，获得干净、结构化的正文 | 新闻、品牌官网、行业网站及其他公开页面 |

实际可用能力、字段范围和账户权益，以认证后的 MCP `tools/list` 和运行时响应为准。

## 连接 Asklear

把下面这句话发送给支持 MCP 的 Agent：

```text
请读取 https://dashboard.asklear.cn/agent-setup?format=markdown，帮我连接 Asklear。
```

Agent 会读取最新的官方连接指引，并根据当前客户端完成 MCP 配置、OAuth 授权和连接验证。

用户只需要在 Asklear 官方页面完成必要的信任、注册或登录、内测准入和授权，不需要复制或保存 API Key。

> `https://dashboard.asklear.cn/agent-setup` 是连接 Asklear 的唯一入口。具体步骤以该入口返回的最新指引为准。

## 提出第一个问题

连接后，可以直接把商业问题交给 Agent：

```text
请使用 Asklear 分析京东宠物零食品类最近 12 个完整月：

1. 市场规模和月度趋势如何？
2. 主要品牌是谁，份额如何变化？
3. 哪些商品、价格带或店铺推动了增长？
4. 有哪些值得关注的机会和风险？

请说明实际查询时间范围、指标口径、证据和限制。
```

Agent 会根据问题选择所需的数据能力，执行足以回答问题的查询，并解释实际返回的数据范围。

## 从问题到结论

Asklear 的价值不只是执行一次查询，而是让 Agent 组合不同来源的证据。

例如，研究一个消费品牌的增长机会时，Agent 可以：

1. 使用电商历史数据判断市场规模、增速和品牌份额；
2. 下钻到商品、店铺和价格带，定位增长来源；
3. 获取内容平台的最新内容和互动数据；
4. 分析消费者关注点、使用场景和负面反馈；
5. 结合企业内部销售、渠道或用户数据；
6. 输出带有口径、证据和限制的研究结论。

```text
商业问题
   ↓
结构化市场数据 + 实时内容与消费者反馈 + 公开网页与企业内部资料
   ↓
Agent 分析、验证与交付
```

## 如何选择能力

- 问市场、品类、品牌、商品、销量或销售额 → 使用结构化历史数据。
- 问最新内容、用户反馈、热点、话题或互动表现 → 使用实时平台接口。
- 需要批量读取公开网页 → 使用云端网页采集。

完整能力目录、查询规则、研究方法和错误恢复，请阅读：

- [Asklear Agent 使用手册](https://docs.asklear.cn)
- [能力与数据](https://docs.asklear.cn/capabilities)
- [查询指南](https://docs.asklear.cn/querying)
- [研究方法](https://docs.asklear.cn/cookbook)
- [错误与恢复](https://docs.asklear.cn/errors)

## Dashboard

访问 [Asklear Dashboard](https://dashboard.asklear.cn) 管理账户、连接、数据权益和用量。

## 仓库说明

这是 Asklear MCP 的公开 GitHub 入口，提供产品与能力介绍、官方连接入口、使用手册入口，以及安全和许可信息。

本仓库不包含生产服务端源码、商业数据、客户凭据或私有基础设施。服务能力、数据契约、账户权益和计费以 Asklear 线上服务及认证后的运行时响应为准。

## 安全

请按照 [SECURITY.md](./SECURITY.md) 私密报告安全问题，不要通过公开 Issue 披露漏洞或凭据。

## 许可

本仓库采用 [Apache License 2.0](./LICENSE) 许可。该许可证不授予 Asklear 商标使用权，也不代表 Asklear 对第三方项目的认可或背书。
