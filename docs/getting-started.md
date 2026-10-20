# 前言 · 怎样使用这本手册

[返回全书目录](../README.md)

## 1. 先选技能集，再选具体任务

| 要做的事 | 从哪一篇开始 |
| --- | --- |
| 查文献、读论文、记录实验、绘图和学术写作 | [Nature Skills](nature-skills.md) |
| 阅读代码、开发、排错、测试、工程与 Agent 工作流 | [ECC](ecc/README.md) |
| 通用 Word/PDF/PPT/表格、视觉设计及网页材料 | [Anthropic Skills](anthropic.md) |
| 梳理需求、写计划、调试、代码评审和验证交付 | [Superpowers](superpowers.md) |
| 在 Claude Code 中按已有 matplotlib 风格制图 | [独立科研绘图技能](independent-skills.md) |

Skill 通常由任务说明、参考资料、模板与可选脚本组成。调用它就是让 AI 按相应流程处理任务。它不是一个自动启动的桌面程序，也不会自动开通外部账号或 API。

## 2. 在聊天框中调用

```text
请使用 $nature-paper-xray，讲解我上传的这篇论文。
我是计算机专业新手。请解释研究问题、方法动机、关键公式的具体算例，
以及实验支持到什么程度。输出中文 Markdown，并标明原文位置。
```

也可以直接写“请使用 nature-paper-xray 技能”。`$技能名` 是聊天中的写法，**不是终端命令**。插件技能可能带命名空间，例如 `$ecc:python-patterns`；以当前宿主的技能选择器为准。

## 3. 提供四件事

```text
请使用 $<技能名>。
材料：<文件、目录、文本或链接>。
目标：<要解决的具体问题>。
边界：<只分析，还是修改/执行；限制在哪些范围>。
输出：<Markdown、代码、图表等，以及保存位置>。
```

例如：`请使用 $ecc:codebase-onboarding，解释这个项目各目录和启动流程，只做教学分析，不运行实验。`

## 4. 名称、依赖与宿主

- 文件夹 `nature-proposal-writer` 的实际调用名是 `researchwrite`。
- ECC 的 `source-command-*` 是迁移后的技能入口，不能假定原宿主 `/命令` 可以直接在 Codex 执行。
- 有些技能需要 Python/R、CLI、MCP、浏览器或第三方服务；本手册列出入口，不表示依赖已逐项配置并实测。
- 独立的 `scientific-figure-making` 位于 Claude Code 目录；不要假定 Codex 已自动加载它。

先给出一个明确的小任务，让 AI 核对所需工具，再按需补齐依赖。遇到未验证的信息应保留为未验证，不应补造实验结果、引用或配置。
