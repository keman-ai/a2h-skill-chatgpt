# A2H Market skill · ChatGPT 版

「A2H Market」闲置集市的 agent skill：**买卖两侧都管**——想卖闲置就识图建档、定价、
上架、接待买家、代笔议价；想买就搜寻、问询、砍价。人只做拍照、确认、收钱、交货。

## 🔴 这一份不用本地安装

ChatGPT 走的是 **MCP**：工具跑在服务端，你不需要在自己机器上装任何东西，也不需要
`python3`。在 ChatGPT 里连上 A2H Market 应用、点一次授权就能用。

本仓放的是这套 MCP 应用的**内容与契约**——工具清单、各场景的行为剧本、工具入参出参的
schema。**给想看清楚「这个应用到底会做什么、拿得到什么数据」的人读**，也是提交审核时的
依据。

CLI 宿主请装另外两份：
[a2h-skill-generic](https://github.com/keman-ai/a2h-skill-generic)（Claude Code / WorkBuddy 等）、
[a2h-skill-codex](https://github.com/keman-ai/a2h-skill-codex)。

## 目录里有什么

| 路径 | 是什么 |
|------|--------|
| `SKILL.md` | 场景路由与红线——agent 拿到什么请求该走哪条剧本 |
| `references/` | 各场景的详细剧本（上架、议价、留言、开箱等） |
| `agents/openai.yaml` | 应用声明：展示名、连接方式、MCP 地址 |

## 说明

- 本仓由 CI 从内部源仓构建后**整体覆盖**，请不要直接提 PR 改这里的文件——会在下次
  同步时被冲掉。有问题提 issue。
- 内容对应**正式环境**（`a2hmarket.ai`）。
