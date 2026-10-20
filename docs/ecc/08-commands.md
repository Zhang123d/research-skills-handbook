# ECC · 第八章　迁移命令入口

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](07-operations.md)

使用已经迁移成技能的命令工作流，仍归属于 ECC。

本章收录 **37** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

这些 `source-command-*` 名称是迁移后的技能入口。以 `ecc:source-command-build-fix` 为例，应在聊天框指定技能与项目，不直接照搬其他宿主的斜杠命令。更新、发布等操作需依据本次实际授权，安装不代表已经启用自动执行。

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:source-command-auto-update` | 更新 ECC 源码并重新安装受管理的目标 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-build-fix` | 识别构建系统并逐步修复构建或类型错误 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-cpp-review` | 审查 C++ 内存安全、并发和现代用法 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-ecc-guide` | 从当前 ECC 源码查找功能和使用入口 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-epic-claim` | 认领 epic 工作项并同步协调状态 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-decompose` | 将 epic 分解为子任务 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-publish` | 将经验证的 epic 状态发布回项目管理系统 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-review` | 记录 epic 评审请求和处理状态 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-sync` | 同步 GitHub epic 内容、标签和本地快照 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-unblock` | 检查依赖完成情况并解除相应阻塞 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-epic-validate` | 检查 epic 的依赖、就绪状态和协调约束 | 工作项编号、依赖与希望更新的状态 |
| `$ecc:source-command-fastapi-review` | 审查 FastAPI 架构、异步逻辑和安全性 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-feature-dev` | 先理解代码库再推进新功能 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-go-build` | 逐步修复 Go 构建、vet 与 lint 问题 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-go-review` | 审查 Go 代码、并发和错误处理 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-gradle-build` | 排查 Android/KMP 的 Gradle 构建错误 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-hookify` | 根据明确规则生成行为约束 hook | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-hookify-configure` | 交互启用或停用已有 hookify 规则 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-hookify-help` | 解释 hookify 的配置与用法 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-hookify-list` | 列出已有 hookify 规则 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-instinct-export` | 导出已学习的项目或全局行为模式 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-instinct-import` | 从指定文件或 URL 导入行为模式 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-instinct-status` | 查看学习到的行为模式及置信度 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-jira` | 读取并按授权更新 Jira 工作项 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-learn` | 从当前工作中提取可复用模式候选 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-plan-canvas` | 在画布中打开计划与 HTML 材料 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-projects` | 列出已知项目与会话信息 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-promote` | 将项目范围的行为模式提升为全局候选 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-prune` | 清理不再需要的待处理行为模式 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-refactor-clean` | 识别无用代码并验证安全清理 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-review-pr` | 对指定 Pull Request 进行代码评审 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-setup-pm` | 配置项目使用的包管理器 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-skill-host-compat` | 检查 ECC 技能的宿主兼容性 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-test-coverage` | 检查测试覆盖缺口并补充必要验证 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-token-card` | 生成用量统计卡片 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-update-codemaps` | 根据代码库更新结构图与模块索引 | 对应项目、报错或待处理工作项 |
| `$ecc:source-command-update-docs` | 根据实际代码变更更新文档 | 对应项目、报错或待处理工作项 |

[返回 ECC 总目录](README.md)
