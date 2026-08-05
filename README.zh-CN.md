<p align="center">
  <img src="./assets/asklear-mark.svg" width="72" alt="Asklear">
</p>

<h1 align="center">Asklear MCP</h1>

<p align="center"><strong>面向 AI Agent 的商业研究基础设施。</strong></p>

<p align="center">
  <a href="https://dashboard.asklear.cn/docs/agent">使用文档</a> ·
  <a href="https://github.com/Asklear/asklear-cookbook">Cookbook</a> ·
  <a href="https://dashboard.asklear.cn/beta">申请接入</a>
</p>

<p align="center">
  <a href="./README.md">English</a> · 简体中文
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MCP-Hosted-5B6EF5?style=flat-square" alt="Hosted MCP">
  <img src="https://img.shields.io/badge/Transport-Streamable_HTTP-16212A?style=flat-square" alt="Streamable HTTP">
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Asklear/asklear-mcp-server?style=flat-square" alt="Apache-2.0 license"></a>
</p>

Asklear MCP 是 Asklear 托管的 [Model Context Protocol](https://modelcontextprotocol.io) 入口。AI Agent 通过一个稳定接口使用商业研究能力，访问控制、数据契约、用量与计费由服务端统一管理。

## 可以研究什么

| 研究任务 | 示例问题 |
| --- | --- |
| 市场与类目分析 | 一个类目的规模和趋势如何？ |
| 品牌竞争格局 | 哪些品牌的份额正在上升或下降？ |
| 增长驱动分析 | 哪些商品、价格带或店铺推动了变化？ |

当前首先开放结构化的中国月度电商研究能力。根据账户权益，可用数据集可能包括京东、天猫或其他授权来源；当前实际能力始终以认证后的 MCP 工具列表为准。

## 快速开始

### 1. 获取接入

Beta 阶段采用邀请或申请制。[申请或登录](https://dashboard.asklear.cn/beta)后，Dashboard 会提供该账户准确的 MCP 地址和 API Key。

### 2. 连接 Agent

优先使用 Dashboard 生成的当前客户端配置。通用 Streamable HTTP 配置如下：

```json
{
  "mcpServers": {
    "asklear": {
      "type": "http",
      "url": "<YOUR_ASKLEAR_MCP_URL>",
      "headers": {
        "Authorization": "Bearer <YOUR_ASKLEAR_API_KEY>"
      }
    }
  }
}
```

> [!IMPORTANT]
> API Key 只用于 MCP 配置，不要写入 Prompt、项目文件、研究报告或导出结果。

### 3. 验证连接

```text
请验证 Asklear MCP 是否已经连接。如果我还没有提出数据问题，
调用 connection_status，并告诉我认证是否成功。
```

## 尝试第一个研究问题

```text
请使用 Asklear 分析京东宠物零食品类最近 12 个完整月：

1. 市场规模和月度趋势如何？
2. 主要品牌是谁，份额如何变化？
3. 有哪些值得关注的机会和风险？

请说明实际时间范围、指标口径、证据和限制。
```

## 从研究到交付物

- 阅读 [Agent Docs](https://dashboard.asklear.cn/docs/agent)，了解当前接入方式、数据集契约和错误恢复。
- 使用 [Asklear Cookbook](https://github.com/Asklear/asklear-cookbook)，将研究结果进一步生成 PPT、PDF 或 Dashboard。

## 仓库边界

> [!NOTE]
> 这是 Asklear 托管 MCP 服务的公开采用仓库，不包含生产服务实现、客户凭据、私有接入地址或商业数据。实际能力由认证后的服务及账户权益决定。

## 安全

安全漏洞请按 [SECURITY.md](SECURITY.md) 私密上报，不要创建公开 Issue。

## 许可

本仓库采用 [Apache-2.0](LICENSE) 许可。该许可证不授予 Asklear 商标使用权，也不代表官方背书。
