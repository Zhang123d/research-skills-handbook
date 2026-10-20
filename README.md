# 科研 Skill 中文使用手册

面向刚开始读论文、复现实验和写作的同学，说明如何选择 Skill、准备输入材料，以及检查交付结果。以本机实际安装的技能为基础，重点讲解完整 Nature Skills 技能集，并汇总其他技能。

**核验日期：2026-10-20。** 这是一份安装与使用说明快照，运行依赖和外部服务没有逐项实测。第三方 Skill 的功能以本机对应版本的 `SKILL.md` 为准。

## 阅读入口

| 文档 | 内容 |
| --- | --- |
| [Nature Skills 详细说明](docs/nature-skills.md) | 22 个功能技能逐项说明：用途、材料、输出、调用示例、依赖与边界；另有 1 个共享支持包 |
| [本机其他 Skill 完整目录](docs/local-skills-catalog.md) | 405 个其他可调用技能，按来源逐项列出用途和用法；另列当前未暴露的目录与缓存 |
| [科研复现使用路线与常见问题](docs/research-workflows.md) | 从读懂论文、检查代码、记录实验，到汇报和写作的可复制示例 |
| [脱敏清单 JSON](data/skills-inventory.json) | 扫描范围、统计、调用名称、用途摘要和相对于用户目录的安装位置 |
| [磁盘文件核对表 JSON](data/disk-skill-files.json) | 1,208 个技能说明文件的相对位置、状态和 SHA-256；便于区分副本 |

## Skill 是什么，怎么使用

Skill 是给 AI 的任务说明与配套资源。通常由 `SKILL.md`、参考资料、模板和可选脚本组成。安装 Skill 后，AI 可以按这套流程工作；它不会自动变成一个桌面软件，也不会自动获得数据库账号、付费 API 或电脑操作权限。

在 Codex 聊天框输入即可，例如：

```text
请使用 $nature-paper-xray，讲解我上传的这篇论文。
我是计算机专业新手，请解释研究问题、方法动机、关键公式的具体算例、
以及实验究竟支持了哪些结论。输出中文 Markdown，并标明原文位置。
```

也可以直接写“请使用 nature-paper-xray 技能”。`$技能名` 用于聊天输入，**不是在 PowerShell、Python 控制台或 PyCharm 终端执行的命令**。如果输入 `$` 后出现技能选择器，以选择器展示的名称为准。插件技能可能使用 `ecc:python-patterns` 这样的带命名空间名称。

调用时提供四件事：**材料、目标、边界、输出位置或格式**。例如“读取这个 PDF；讲清楚方法；不要替我运行实验；输出中文 Markdown”。只想问一个公式时，直接限定到该公式，不必每次让技能处理全文。

## 先按任务选技能

| 现在想做什么 | 优先选择 | 需要准备 |
| --- | --- | --- |
| 查某方向有哪些论文 | `nature-academic-search` | 主题、关键词、时间范围、筛选条件 |
| 获取论文正文与补充材料 | `nature-downloader` | DOI/标题/链接，是否需要补充材料；必要时使用已有机构授权 |
| 真正读懂一篇论文的方法和公式 | `nature-paper-xray` | 正文，最好包括附录 |
| 做一张结构化精读卡 | `nature-paper-card` | 论文或已有阅读材料 |
| 中英对照阅读并追溯原文 | `nature-reader` | PDF、全文或指定片段 |
| 得到保留版面关系的中文 PDF | `nature-paper-trans` | 英文 PDF、页码；需要内置生图能力 |
| 认识 GitHub 复现代码的结构 | `ecc:codebase-onboarding` | 代码目录和 README |
| 排查实验报错 | `superpowers-systematic-debugging` | 完整报错、启动方式、环境信息 |
| 整理实验过程和失败原因 | `nature-experiment-log` | 日志、配置、记录和图片 |
| 检查样本数、随机种子、置信区间的表述 | `nature-statistics` | 实验设计、结果表、统计说明 |
| 绘制论文结果图 | `nature-figure` | 实际数据、字段解释，指定 Python 或 R |
| 做组会汇报 | `nature-paper2ppt` | 论文、汇报时长、听众背景 |
| 写论文初稿 | `nature-writing` | 已完成的方法、实验结果、证据材料 |
| 修改已有段落的语言 | `nature-polishing` | 原段落、术语和目标风格 |
| 写开题报告、研究计划 | `researchwrite` | 研究问题、文献基础、计划与约束 |
| 核查参考文献真假和字段 | `nature-ref-verifier` | `.bib` 或参考文献列表 |

## 本机扫描结果

扫描目录为 `~/.codex/skills`、`~/.agents/skills`、`~/.codex/plugins/cache`、`~/.claude/skills`。`~` 表示当前用户的主目录，文档不公开真实用户名及绝对路径。另检查的用户级 Cursor、Gemini、OpenCode、Copilot 常见技能目录当时不存在。

| 分类 | 当前目录中可调用 | 补充说明 |
| --- | ---: | --- |
| Nature Skills | 22 | 另有 `nature-shared` 内部支持包 1 个 |
| Anthropic 用户全局技能 | 19 | 与办公、设计、开发有关 |
| Superpowers 用户全局技能 | 15 | 需求梳理、计划、调试、验证等 |
| ECC 2.2.3 常规技能 | 311 | 研究、工程、Agent、业务等 |
| ECC 2.2.3 迁移命令技能 | 37 | `source-command-*`，不要假定原宿主斜杠命令在 Codex 中可直接执行 |
| Codex 内置系统技能 | 4 | 创建/安装技能、OpenAI 文档、生图 |
| 应用插件技能 | 19 | 文档、表格、演示、云盘、网站、电脑操作等 |
| **合计** | **427** | 其中 Nature 以外 **405** 个 |

另外发现 ECC 翻译、其他宿主示例等 751 个文件，OpenAI Templates 缓存 27 个文件，当前未列出的 `review-agent` 1 个，以及 Claude Code 专用 `scientific-figure-making` 1 个。加上上述 427 项和 `nature-shared`，共 1,208 个 `SKILL.md`。文件数包含不同路径的副本，**不能解释为安装了 1,208 种独立可用能力**。

“当前可调用”仅指本次 Codex 会话列出了该技能入口，不代表 Python 包、MCP、浏览器登录、CLI、API 或账号权限全部可用。缓存中存在文件也不等于当前已启用。没有扫描整块硬盘、其他 Windows 账号或远程机器；此前仅收集链接而未安装的候选 Skill 不计入可调用数量。

## 版本和来源

Nature Skills 安装版本为 [`c8599197e7d2a22c2a091bbf8c14efcb3625cfa0`](https://github.com/Yuan1z0825/nature-skills/tree/c8599197e7d2a22c2a091bbf8c14efcb3625cfa0)。已安装 23 个目录，并对其中 808 个文件完成与该 Git 提交的内容核对。这里只汇总说明与使用示例，不复制完整技能源代码，也不声称完成所有技能的运行测试。

其他来源包括 [ECC](https://github.com/affaan-m/everything-claude-code)、[Superpowers](https://github.com/obra/superpowers)、[Anthropic Skills](https://github.com/anthropics/skills) 和 Codex 应用附带插件。名称中包含 Nature 或 Anthropic 不代表本手册获得相关机构的背书；Nature 技能是第三方科研辅助工作流。

技能安装和外部服务配置分开管理。遇到依赖缺失时按当前任务补齐，不需要为了阅读一篇论文一次性安装清单中所有工具。技能升级后，重新核对名称、输入输出和依赖；这份快照不会自动更新，也没有设置定时推送或自动更新任务。

