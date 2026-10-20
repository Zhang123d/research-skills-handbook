# 我安装的 Skill 使用手册

按技能集编排的中文使用手册。**只管理自行安装的技能集与独立技能**，方便像翻书一样，先选一篇，再进入章节查看具体用途和调用方法。

更新日期：2026-10-20。技能说明依据本机安装版本整理，外部工具与运行依赖没有逐项实测。

## 全书目录

### 前言 · 先学会调用

- [Skill 是什么、怎么调用、准备哪些材料](docs/getting-started.md)

### 第一篇 · Nature Skills：科研工作流

22 个功能技能，另有 1 个共享支持包。[进入本篇目录与逐项说明](docs/nature-skills.md)

- [第一章　检索、下载与引用](docs/nature-skills.md#一检索下载与引用)
- [第二章　阅读、翻译与研究理解](docs/nature-skills.md#二阅读翻译与研究理解)
- [第三章　实验记录、统计与绘图](docs/nature-skills.md#三实验记录统计与绘图)
- [第四章　汇报、幻灯片与材料转换](docs/nature-skills.md#四汇报幻灯片与材料转换)
- [第五章　写作、开题与投稿](docs/nature-skills.md#五写作开题与投稿)
- [附：共享支持包与容易选错的组合](docs/nature-skills.md#六共享支持包)

### 第二篇 · ECC：工程开发与 Agent 工作流

348 个入口，统一收在 ECC 这一篇中，包含 311 个常规技能和 37 个迁移命令技能。[进入 ECC 总目录](docs/ecc/README.md)

- [第一章　科研、检索与机器学习](docs/ecc/01-research.md)
- [第二章　Agent、技能、上下文与流程](docs/ecc/02-agents.md)
- [第三章　编程、架构与代码协作](docs/ecc/03-development.md)
- [第四章　测试、安全与质量](docs/ecc/04-quality.md)
- [第五章　前端、视觉与多媒体](docs/ecc/05-visual.md)
- [第六章　环境、部署与网络](docs/ecc/06-environment.md)
- [第七章　文档、业务与其他工作流](docs/ecc/07-operations.md)
- [第八章　迁移命令入口](docs/ecc/08-commands.md)

### 第三篇 · Anthropic Skills：文档、设计与开发

19 个自行安装的技能。[进入本篇目录](docs/anthropic.md)

- [第一章　办公文件与协作文档](docs/anthropic.md#chapter-1)
- [第二章　视觉设计与网页材料](docs/anthropic.md#chapter-2)
- [第三章　开发、学习与技能维护](docs/anthropic.md#chapter-3)

### 第四篇 · Superpowers：开发协作方法

15 个自行安装的技能。[进入本篇目录](docs/superpowers.md)

- [第一章　需求与计划](docs/superpowers.md#chapter-1)
- [第二章　执行、隔离与调试](docs/superpowers.md#chapter-2)
- [第三章　评审、验证与交付](docs/superpowers.md#chapter-3)
- [第四章　技能使用与流程复盘](docs/superpowers.md#chapter-4)

### 第五篇 · 独立技能

- [scientific-figure-making：matplotlib 科研绘图](docs/independent-skills.md)

### 附录 · 科研实践与管理清单

- [从读论文到复现、统计、绘图与汇报](docs/research-workflows.md)
- [安装范围与数量汇总](docs/local-skills-catalog.md)
- [结构化技能管理清单](data/skills-inventory.json)
- [管理范围内的说明文件核对表](data/disk-skill-files.json)

## 管理范围

| 技能集 | 功能技能/入口 | 说明 |
| --- | ---: | --- |
| Nature Skills | 22 | 另有共享支持包 1 个 |
| ECC 2.2.3 | 348 | 311 个常规技能 + 37 个迁移命令技能 |
| Anthropic Skills | 19 | 用户全局安装 |
| Superpowers | 15 | 用户全局安装 |
| 独立科研绘图技能 | 1 | 位于 Claude Code 技能目录 |
| **合计** | **405** | 404 个当前 Codex 入口 + 1 个其他宿主技能 |

连同 Nature 共享支持包，共管理 **406 条安装记录**。ECC 按技能集汇总，翻译副本、其他宿主示例与缓存不重复计数。Codex 系统技能和应用自带技能不纳入本手册。此轮只重排文档与管理清单，没有安装或卸载技能。
