# 附录 · 自行安装的技能集总目录

[返回全书目录](../README.md)

本页按**技能集**汇总，具体条目进入各篇查看。管理范围不包含 Codex 系统技能、应用自带技能和插件缓存。

| 篇目 | 用途概览 | 功能入口数 | 逐项说明 |
| --- | --- | ---: | --- |
| 第一篇 Nature Skills | 文献、阅读、实验记录、图表、写作与投稿 | 22 | [本篇目录](nature-skills.md) |
| 第二篇 ECC | 工程开发、研究、Agent、测试和其他工作流 | 348 | [本篇目录](ecc/README.md) |
| 第三篇 Anthropic Skills | 文件处理、视觉设计、开发与学习 | 19 | [本篇目录](anthropic.md) |
| 第四篇 Superpowers | 需求、计划、执行、调试、评审与验证 | 15 | [本篇目录](superpowers.md) |
| 第五篇 独立技能 | matplotlib 科研绘图 | 1 | [scientific-figure-making](independent-skills.md) |
| **合计** |  | **405** | 404 个当前 Codex 入口，另有 1 个 Claude Code 技能 |

Nature 还有 `nature-shared` 共享支持包 1 个，不单独调用，因此管理记录共 **406** 条。ECC 的常规技能与迁移命令入口合并计为同一个技能集，不重复计入随包翻译或其他宿主示例。

## 管理位置

- Nature：`~/.codex/skills/nature-*`，包括调用名为 `researchwrite` 的目录。
- Anthropic / Superpowers：`~/.agents/skills` 下对应前缀目录。
- ECC：2.2.3 插件的 `skills` 和 `.codex-plugin/migrated-command-skills` 目录。
- 独立科研绘图技能：`~/.claude/skills/scientific-figure-making`。

`~` 表示用户主目录。完整相对位置和用途摘要见 [结构化管理清单](../data/skills-inventory.json)，本范围内 `SKILL.md` 的 SHA-256 见 [文件核对表](../data/disk-skill-files.json)。这些数量是已核验安装的快照，不保证依赖全部可用；没有扫描其他账号或远端机器。
