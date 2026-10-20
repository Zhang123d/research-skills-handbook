# ECC · 第二章　Agent、技能、上下文与流程

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](01-research.md) · [下一章](03-development.md)

组织 Agent 的能力、上下文、工具、运行边界与工作流程。

本章收录 **59** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:agent-architecture-audit` | 审查 Agent 的架构、工具、状态与运行边界 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-eval` | 编码代理（Claude Code、Aider、Codex等）在自定义任务上的直接比较，包含通过率、成本、时间和一致性指标 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-harness-construction` | 设计和优化AI代理的动作空间、工具定义和观察格式，以提高完成率 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-introspection-debugging` | 针对AI代理故障的结构化自调试工作流程，包括捕获、诊断、受限恢复和内省报告 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-payment-x402` | 将 x402 支付执行添加到 AI 代理中，具备每任务预算、支出控制和非托管钱包 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-runtime-gateway-smoke-test` | 最小验证本地 Agent API、网关和路由是否连通 | 代码目录、运行方式与验证目标 |
| `$ecc:agent-security-hardening` | 加固 Agent 的权限、工具执行和不可信输入边界 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-self-evaluation` | 完成工作后检查结果、证据及遗留问题 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agent-sort` | 通过将技能、命令、规则、钩子和额外内容并行进行仓库感知审查，为特定仓库构建基于证据的 ECC 安装计划，将其分为 DAILY 和 LIBRARY 两类 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agentic-engineering` | 作为代理工程师，采用评估优先执行、分解和成本感知模型路由进行操作 | 宿主、配置或工作流；先核对工具 |
| `$ecc:agentic-os` | 组织持久化多 Agent 工作环境与任务状态 | 宿主、配置或工作流；先核对工具 |
| `$ecc:autonomous-agent-harness` | 将 Claude Code 转变为具有持久记忆、定时操作、计算机使用和任务队列的完全自主代理系统 | 宿主、配置或工作流；先核对工具 |
| `$ecc:autonomous-loops` | 自主Claude代码循环的模式与架构——从简单的顺序管道到基于RFC的多智能体有向无环图系统 | 宿主、配置或工作流；先核对工具 |
| `$ecc:codehealth-mcp` | 借助 Code Health MCP 检查代码结构与可维护性 | 项目目录、技术栈与待改功能 |
| `$ecc:config-gc` | 清理已失效或多余的 Agent 配置 | 现有材料、预期目标与交付范围 |
| `$ecc:context-and-decisions` | 管理项目稳定背景、领域约束和已作决定 | 宿主、配置或工作流；先核对工具 |
| `$ecc:context-budget` | 审核Claude Code上下文窗口在代理、技能、MCP服务器和规则中的消耗情况 | 宿主、配置或工作流；先核对工具 |
| `$ecc:continuous-agent-loop` | 具有质量门、评估和恢复控制的连续自主代理循环模式 | 宿主、配置或工作流；先核对工具 |
| `$ecc:continuous-learning` | 自动从Claude Code会话中提取可重复使用的模式，并将其保存为学习到的技能以供将来使用 | 现有材料、预期目标与交付范围 |
| `$ecc:continuous-learning-v2` | 基于本能的学习系统，通过钩子观察会话，创建带置信度评分的原子本能，并将其进化为技能/命令/代理 | 现有材料、预期目标与交付范围 |
| `$ecc:cost-aware-llm-pipeline` | LLM API 使用成本优化模式 —— 基于任务复杂度的模型路由、预算跟踪、重试逻辑和提示缓存 | 现有材料、预期目标与交付范围 |
| `$ecc:cost-tracking` | 记录并分析 Agent 会话用量和费用 | 现有材料、预期目标与交付范围 |
| `$ecc:council` | 召集四方会议处理模糊决策、权衡取舍及继续/停止决策 | 现有材料、预期目标与交付范围 |
| `$ecc:council-multi-model` | 在多视角评审中加入可选外部模型 | 现有材料、预期目标与交付范围 |
| `$ecc:data-scraper-agent` | 构建一个全自动化的AI驱动数据收集代理，适用于任何公共来源——招聘网站、价格信息、新闻、GitHub、体育赛事等任何内容 | 宿主、配置或工作流；先核对工具 |
| `$ecc:deepseek-harness-setup` | 安装、配置和维护 DeepSeek Harness | 宿主、配置或工作流；先核对工具 |
| `$ecc:ecc-guide` | 在回答之前先读取仓库的实时状态，引导用户了解 ECC 当前的 agents、skills、命令、hooks、规则、安装配置档案以及项目接入流程 | 现有材料、预期目标与交付范围 |
| `$ecc:ecc-recipes` | 把实际任务匹配到 ECC 技能与工作流组合 | 现有材料、预期目标与交付范围 |
| `$ecc:ecc-tools-cost-audit` | 证据优先的ECC工具燃烧和计费审计工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:enterprise-agent-ops` | 通过可观测性、安全边界和生命周期管理来操作长期运行的代理工作负载 | 宿主、配置或工作流；先核对工具 |
| `$ecc:eval-harness` | 克劳德代码会话的正式评估框架，实施评估驱动开发（EDD）原则 | 宿主、配置或工作流；先核对工具 |
| `$ecc:evm-token-decimals` | 防止跨EVM链的静默小数不匹配错误 | 现有材料、预期目标与交付范围 |
| `$ecc:gan-style-harness` | 受GAN启发的生成器-评估器代理框架，用于自主构建高质量应用 | 宿主、配置或工作流；先核对工具 |
| `$ecc:gateguard` | 强制事实的门控，阻止编辑/写入/Bash（包括MultiEdit），并要求在允许操作之前进行具体调查（导入器、数据模式、用户指令） | 现有材料、预期目标与交付范围 |
| `$ecc:healthcare-eval-harness` | 用于医疗应用部署的患者安全评估工具 | 宿主、配置或工作流；先核对工具 |
| `$ecc:hookify-rules` | 当用户要求创建hookify规则、编写hook规则、配置hookify、添加hookify规则或需要关于hookify规则语法和模式的指导时，应使用此技能 | 现有材料、预期目标与交付范围 |
| `$ecc:llm-trading-agent-security` | 具有钱包或交易权限的自主交易代理的安全模式 | 宿主、配置或工作流；先核对工具 |
| `$ecc:loop-design-check` | 审查自主执行循环的目标、停止条件与验证 | 宿主、配置或工作流；先核对工具 |
| `$ecc:mcp-dependency-review` | 静态检查 MCP 配置、依赖与风险边界 | 宿主、配置或工作流；先核对工具 |
| `$ecc:mcp-server-patterns` | 使用Node/TypeScript SDK构建MCP服务器——工具、资源、提示、Zod验证、stdio与可流式HTTP对比 | 项目目录、技术栈与待改功能 |
| `$ecc:operator-approval-loop` | 在 Agent 执行中管理人工确认与交接 | 宿主、配置或工作流；先核对工具 |
| `$ecc:orch-add-feature` | 编排向现有项目添加功能的工程步骤 | 现有材料、预期目标与交付范围 |
| `$ecc:orch-build-mvp` | 编排最小可用产品的构建与验证 | 项目目录、技术栈与待改功能 |
| `$ecc:orch-change-feature` | 编排已有功能的修改与验证 | 现有材料、预期目标与交付范围 |
| `$ecc:orch-fix-defect` | 编排缺陷定位、修复和确认 | 现有材料、预期目标与交付范围 |
| `$ecc:orch-pipeline` | 提供工程编排技能共用的流程骨架 | 现有材料、预期目标与交付范围 |
| `$ecc:orch-refine-code` | 编排代码整理、重构与行为保持检查 | 项目目录、技术栈与待改功能 |
| `$ecc:plan-orchestrate` | 读取已有计划并编排执行和进度 | 现有材料、预期目标与交付范围 |
| `$ecc:prompt-caching-strategy` | 规划 LLM 提示缓存与成本优化 | 现有材料、预期目标与交付范围 |
| `$ecc:prompt-optimizer` | 分析原始提示，识别意图和差距，匹配ECC组件（技能/命令/代理/钩子），并输出一个可直接粘贴的优化提示 | 现有材料、预期目标与交付范围 |
| `$ecc:santa-method` | 具有收敛循环的多智能体对抗验证 | 现有材料、预期目标与交付范围 |
| `$ecc:skill-comply` | 可视化技能、规则和代理定义是否被实际遵循——自动生成3种提示严格级别的场景，运行代理，分类行为序列，并报告完整工具调用时间线的合规率 | 宿主、配置或工作流；先核对工具 |
| `$ecc:skill-host-compat` | 检查技能在 Codex/Cursor 等宿主中的兼容性 | 宿主、配置或工作流；先核对工具 |
| `$ecc:skill-scout` | 创建技能前先搜索已有本地和公开技能 | 宿主、配置或工作流；先核对工具 |
| `$ecc:skill-stocktake` | 用于审计Claude技能和命令的质量 | 宿主、配置或工作流；先核对工具 |
| `$ecc:team-agent-orchestration` | 管理多 Agent 工作项、范围隔离和合并验证 | 宿主、配置或工作流；先核对工具 |
| `$ecc:token-budget-advisor` | 在回答前，为用户提供关于消耗多少响应深度的知情选择 | 现有材料、预期目标与交付范围 |
| `$ecc:token-card` | 从本地用量记录生成可分享的统计卡片 | 现有材料、预期目标与交付范围 |
| `$ecc:unified-memory` | 在不同 Agent 宿主间保存可检查的上下文与交接 | 宿主、配置或工作流；先核对工具 |

[返回 ECC 总目录](README.md)
