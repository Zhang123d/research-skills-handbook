# 第四篇 · Superpowers：开发协作方法

[返回全书目录](../README.md) · [使用方法](getting-started.md)

本篇收录自行安装的 **15 个 Superpowers 技能**。它们主要规范怎样梳理需求、执行、调试和验证。按当前阶段选择，不必每次从第一章完整重跑。

## 本篇目录

- [第一章　需求与计划（2）](#chapter-1)
- [第二章　执行、隔离与调试（6）](#chapter-2)
- [第三章　评审、验证与交付（4）](#chapter-3)
- [第四章　技能使用与流程复盘（3）](#chapter-4)

<a id="chapter-1"></a>

## 第一章　需求与计划

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$superpowers-brainstorming` | 在开发前澄清需求、备选方案与设计约束 | 需求、用户场景、已有约束和可选方案 |
| `$superpowers-writing-plans` | 把需求拆成可执行、可验证的实现步骤 | 需求、项目约束和可验证交付目标 |

<a id="chapter-2"></a>

## 第二章　执行、隔离与调试

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$superpowers-dispatching-parallel-agents` | 将互不依赖的任务分配给并行 Agent | 独立任务、各自范围与汇总要求 |
| `$superpowers-executing-plans` | 按已有实现计划逐项执行并验证 | 已确定计划、当前进度与项目目录 |
| `$superpowers-subagent-driven-development` | 由独立子任务推进已有开发计划 | 计划、独立任务与边界；需子 Agent 能力 |
| `$superpowers-systematic-debugging` | 基于证据定位错误原因并验证修复 | 完整错误、启动方式、环境与最近改动 |
| `$superpowers-test-driven-development` | 按先失败测试、再实现的流程开发 | 行为需求、项目和已有测试工具 |
| `$superpowers-using-git-worktrees` | 为需要隔离的开发工作建立 Git 工作区 | 仓库、起始分支与隔离工作目标 |

<a id="chapter-3"></a>

## 第三章　评审、验证与交付

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$superpowers-finishing-a-development-branch` | 检查工作完成状态并选择分支集成方式 | 分支状态、验证证据与集成目标 |
| `$superpowers-receiving-code-review` | 核对代码评审意见后再落实修改 | 评审意见、相关代码和验证依据 |
| `$superpowers-requesting-code-review` | 在交付或合并前安排代码评审 | 待评审提交/修改、需求与验证记录 |
| `$superpowers-verification-before-completion` | 在宣称完成前获取实际验证证据 | 交付标准、实际修改和可运行检查 |

<a id="chapter-4"></a>

## 第四章　技能使用与流程复盘

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$superpowers-diagnosing-superpowers` | 复盘 Superpowers 会话中的流程失效 | 失败会话记录、预期与实际过程 |
| `$superpowers-using-superpowers` | 选择并读取适用的 Superpowers 技能 | 实际任务和当前宿主可用技能 |
| `$superpowers-writing-skills` | 编写、修改与验证技能说明 | 目标工作流、技能文件和验证样例 |

## 使用示例

```text
请使用 $superpowers-systematic-debugging，分析以下完整报错。
先给出基于日志的假设与最小检查，每次说明预期输出如何验证假设。
本次用于教学，不替我执行命令。
```

来源：[Superpowers](https://github.com/obra/superpowers)。工作区隔离、多 Agent、评审等能力取决于当前宿主支持；不能将同一上下文的角色扮演当作独立评审。
