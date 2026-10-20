# 本机其他 Skill 完整目录

[返回首页](../README.md) · [Nature Skills 详解](nature-skills.md) · [使用路线](research-workflows.md)

本页逐项列出 **405 个 Nature 以外、当前 Codex 会话列出的技能入口**。用途依据本机 `SKILL.md` 归纳；部分 ECC 简介参考同版本附带的中文说明。可调用不代表依赖已装好或功能已实测。

## 统一调用方法

表格第一列就是聊天中的调用名称。将它放到下面模板中，并补上这一行要求的材料：

```text
请使用 $<调用名称>。
材料：<文件/目录/文本/链接或工作项>。
目标：<希望该技能解决的具体问题>。
边界：<只分析、需要修改哪些文件、是否执行操作>。
输出：<报告、代码、图表或文件格式与保存位置>。
```

例如：`请使用 $ecc:python-patterns，审查这个 Python 项目的错误处理，先给出问题和修改建议。`
也可以不写 `$`，直接说“请使用 ecc:python-patterns 技能”。它们不是终端命令。不要假定 Claude 版本中的 `/命令` 能直接在 Codex 中运行。

当前技能目录与宿主约束决定可用工具。某些原始技能面向 Claude、Hermes、Cursor 或特定 CLI；调用时应先确认适配和依赖，不能从名称推断配置已完成。

## 来源与依赖提示

| 来源 | 常见依赖/注意点 |
| --- | --- |
| Anthropic | 文档处理依赖相应文件工具；Claude API、MCP 与 Playwright 功能另需环境 |
| Superpowers | 适用于工程协作；分支、代码评审、并行任务依赖宿主提供的能力 |
| ECC | 内容覆盖广；API、MCP、CLI、网络、账号和框架按单个任务核对 |
| 应用插件 | 需要相关插件及连接；实时 Excel 与本地表格文件是不同入口 |
| 系统技能 | 以 Codex 当前工具支持为准，安装技能不会自动开通外部服务 |

## Anthropic 用户全局技能（19）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$anthropic-academy-guide` | 根据 Claude 使用问题匹配官方学习课程 | Claude 使用问题、已有基础与学习目标 |
| `$anthropic-algorithmic-art` | 用 p5.js 和可控随机性制作生成艺术 | 画面主题、交互方式、尺寸与随机种子要求 |
| `$anthropic-brand-guidelines` | 应用 Anthropic 品牌配色与字体约定 | 待设计制品、品牌适用范围与格式 |
| `$anthropic-canvas-design` | 制作静态海报与 PNG/PDF 视觉设计 | 海报主题、文字素材、尺寸与导出格式 |
| `$anthropic-claude-api` | 查阅 Claude API、SDK、工具调用和模型参数 | 代码片段、SDK/模型标识与接口问题 |
| `$anthropic-discernment-nudge` | 提醒核对建议或草稿中的事实与行动依据 | 待采用的建议/草稿与需要核查的依据 |
| `$anthropic-doc-coauthoring` | 协作组织文档、技术规格与决策材料 | 读者、文档目标、已有材料和大纲 |
| `$anthropic-docx` | 创建、读取和修改 Word 文档与模板 | Word 文件或模板、修改位置与版式要求 |
| `$anthropic-frontend-design` | 设计具有明确视觉方向的前端界面 | 界面需求、参考风格、组件和技术栈 |
| `$anthropic-internal-comms` | 起草状态报告、公告和内部沟通材料 | 受众、事实要点、语气和沟通类型 |
| `$anthropic-mcp-builder` | 构建连接外部服务的 MCP 服务器 | 外部 API 文档、权限范围和服务语言 |
| `$anthropic-pdf` | 提取、合并、拆分、创建和处理 PDF | PDF 文件、页码与提取/修改目标 |
| `$anthropic-pptx` | 创建、读取和修改 PowerPoint 演示文件 | 演示主题/源 PPTX、听众与模板要求 |
| `$anthropic-skill-creator` | 创建、改进技能并设计效果评估 | 目标工作流、示例任务和评估标准 |
| `$anthropic-slack-gif-creator` | 生成适合 Slack 使用的动画 GIF | 动画内容、尺寸、时长与大小限制 |
| `$anthropic-theme-factory` | 为文档、幻灯片和网页应用视觉主题 | 目标制品、主题选择或品牌参考 |
| `$anthropic-web-artifacts-builder` | 构建带状态与组件的交互网页材料 | 网页功能、页面流程与交互需求 |
| `$anthropic-webapp-testing` | 用 Playwright 检查本地网页交互与日志 | 网页地址/项目、操作路径与预期结果 |
| `$anthropic-xlsx` | 创建、修改与分析电子表格和公式 | 表格文件、目标列/公式与输出要求 |

## Superpowers 用户全局技能（15）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$superpowers-brainstorming` | 在开发前澄清需求、备选方案与设计约束 | 需求、用户场景、已有约束和可选方案 |
| `$superpowers-diagnosing-superpowers` | 复盘 Superpowers 会话中的流程失效 | 失败会话记录、预期与实际过程 |
| `$superpowers-dispatching-parallel-agents` | 将互不依赖的任务分配给并行 Agent | 独立任务、各自范围与汇总要求 |
| `$superpowers-executing-plans` | 按已有实现计划逐项执行并验证 | 已确定计划、当前进度与项目目录 |
| `$superpowers-finishing-a-development-branch` | 检查工作完成状态并选择分支集成方式 | 分支状态、验证证据与集成目标 |
| `$superpowers-receiving-code-review` | 核对代码评审意见后再落实修改 | 评审意见、相关代码和验证依据 |
| `$superpowers-requesting-code-review` | 在交付或合并前安排代码评审 | 待评审提交/修改、需求与验证记录 |
| `$superpowers-subagent-driven-development` | 由独立子任务推进已有开发计划 | 计划、独立任务与边界；需子 Agent 能力 |
| `$superpowers-systematic-debugging` | 基于证据定位错误原因并验证修复 | 完整错误、启动方式、环境与最近改动 |
| `$superpowers-test-driven-development` | 按先失败测试、再实现的流程开发 | 行为需求、项目和已有测试工具 |
| `$superpowers-using-git-worktrees` | 为需要隔离的开发工作建立 Git 工作区 | 仓库、起始分支与隔离工作目标 |
| `$superpowers-using-superpowers` | 选择并读取适用的 Superpowers 技能 | 实际任务和当前宿主可用技能 |
| `$superpowers-verification-before-completion` | 在宣称完成前获取实际验证证据 | 交付标准、实际修改和可运行检查 |
| `$superpowers-writing-plans` | 把需求拆成可执行、可验证的实现步骤 | 需求、项目约束和可验证交付目标 |
| `$superpowers-writing-skills` | 编写、修改与验证技能说明 | 目标工作流、技能文件和验证样例 |

## Codex 系统技能（4）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$imagegen` | 通过可用生图工具生成、编辑图片或透明素材 | 画面描述/原图、修改要求与透明背景需求 |
| `$openai-docs` | 按当前官方资料处理 OpenAI/Codex 使用问题 | 具体产品/API、问题、相关版本与本地线索 |
| `$skill-creator` | 创建或更新 Codex 技能及其配套资源 | 技能目标、输入输出、示例与安装范围 |
| `$skill-installer` | 从指定仓库或技能目录安装 Codex 技能 | 仓库链接、技能路径、版本与安装范围 |

## 应用与内置运行时插件技能（19）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$computer-use:computer-use` | 通过允许的电脑控制工具操作 Windows 应用 | 目标应用、可见状态、操作目标和范围 |
| `$documents:documents` | 生成、修改并渲染核对 Word 文档 | Word/内容材料、修改位置和版式要求 |
| `$google-drive:google-docs` | 通过已连接工具创建和修改 Google Docs | 已连接文档或新文档目标、内容与范围 |
| `$google-drive:google-drive` | 查找与管理已连接的 Google Drive 文件 | 文件名/链接、查找范围和管理目标 |
| `$google-drive:google-drive-comments` | 定位、回复与处理 Google Drive 文档评论 | 文档链接、具体位置与评论内容 |
| `$google-drive:google-sheets` | 按精确范围处理已连接的 Google Sheets | 在线表格、工作表/单元格范围和目标 |
| `$google-drive:google-slides` | 根据模板或参考稿组织 Google Slides | 在线模板/源稿、汇报目标与内容 |
| `$pdf:pdf` | 读取、生成、渲染与核对 PDF 版面及表单 | PDF/源材料、页码与版面或表单需求 |
| `$plugin-management:plugin-management` | 发现插件、检查连接与管理插件权限 | 所需服务、插件名称或连接问题 |
| `$presentations:Presentations` | 创建、读取和修改演示文稿文件 | 源稿/内容、听众、时长与模板 |
| `$sites:sites` | 使用 Sites 创建、修改和发布网站 | 网站目标、内容、页面与发布要求 |
| `$sites:sites-remix` | 根据指定来源网站创建新的 Sites 副本 | 源 Sites 链接与希望调整的内容 |
| `$spreadsheets:Spreadsheets` | 处理本地表格、公式、格式与图表 | 本地表格、字段、公式与图表目标 |
| `$spreadsheets:excel-live-control` | 操作已有连接的实时 Excel 工作簿 | 已连接的实时 Excel 会话及操作范围 |
| `$template-creator:template-creator` | 从参考文件建立可复用的个人制品模板技能 | 参考制品、保留样式与后续填充字段 |
| `$visualize:visualize` | 在对话中制作交互可视化与解释工具 | 需要解释的关系、参数与交互目标 |
| `$work-pets:create-pet` | 创建和验证 ChatGPT Work 动画宠物 | 角色描述/参考图与宠物名称 |
| `$work-pets:pets` | 查看、选择与管理已有 Work 动画宠物 | 已有 Work 宠物与查看/选择等目标 |
| `$work-pets:update-pet` | 修改已有 Work 动画宠物及图像资源 | 现有 Work 宠物与具体修改内容 |

## ECC 2.2.3 常规技能（311）

以下按主题分组，分组仅为本手册导航。原始技能有重叠用途，不代表必须按分组顺序使用。

### 科研、检索与机器学习（16）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:benchmark` | 使用此技能测量性能基线，检测PR前后的回归，并比较堆栈替代方案 | 基准任务、运行环境、指标与比较版本 |
| `$ecc:benchmark-methodology` | 设计有证据支撑的对比评分与基准方法 | 比较对象、统一预算、指标和证据来源 |
| `$ecc:benchmark-optimization-loop` | 用基准测量、定位与回归检查持续优化性能 | 可重复基准、瓶颈线索与优化目标 |
| `$ecc:deep-research` | 使用firecrawl和exa MCPs进行多源深度研究 | 研究问题、资料范围与报告格式 |
| `$ecc:market-research` | 进行市场研究、竞争分析、投资者尽职调查和行业情报，附带来源归属和决策导向的摘要 | 研究问题、资料范围与报告格式 |
| `$ecc:ml-adoption-playbook` | 规划机器学习方案从需求到落地的过程 | 业务问题、数据、成本约束与验收指标 |
| `$ecc:mle-workflow` | 组织生产机器学习开发和评估流程 | 数据、模型、训练/评估流程和部署要求 |
| `$ecc:prediction-market-oracle-research` | 研究预测市场的事件与预言机证据 | 研究问题、资料范围与报告格式 |
| `$ecc:pytorch-patterns` | PyTorch深度学习模式与最佳实践，用于构建稳健、高效且可复现的训练流程、模型架构和数据加载 | 项目目录、技术栈与待改功能 |
| `$ecc:recsys-pipeline-architect` | 设计可组合的推荐系统数据与模型流水线 | 推荐场景、数据、候选召回和评估约束 |
| `$ecc:research-ops` | 以证据为先的ECC当前状态研究工作流程 | 研究问题、资料范围与报告格式 |
| `$ecc:scientific-db-pubmed-database` | 通过 PubMed/NCBI 检索生物医学文献 | 生物医学主题、MeSH/关键词与日期范围 |
| `$ecc:scientific-db-uspto-database` | 查询 USPTO 官方专利与商标记录 | 专利/商标号、主体或检索问题 |
| `$ecc:scientific-pkg-gget` | 使用 gget 查询基因、序列与生信数据库 | 基因/序列标识、物种和查询目标 |
| `$ecc:scientific-thinking-literature-review` | 规划系统文献检索、筛选、综合与证据记录 | 问题、纳排标准、检索范围和输出格式 |
| `$ecc:scientific-thinking-scholar-evaluation` | 检查论文、研究计划及方法的证据和论证质量 | 论文/计划、评价范围和证据材料 |

### Agent、技能、上下文与流程（60）

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
| `$ecc:verification-loop` | Claude Code 会话的全面验证系统 | 代码目录、运行方式与验证目标 |

### 编程、架构与代码协作（45）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:api-connector-builder` | 通过匹配目标仓库现有的集成模式，构建一个新的API连接器或提供者 | 项目目录、技术栈与待改功能 |
| `$ecc:backend-patterns` | 后端架构模式、API设计、数据库优化以及适用于Node.js、Express和Next.js API路由的服务器端最佳实践 | 项目目录、技术栈与待改功能 |
| `$ecc:bun-runtime` | Bun 作为运行时、包管理器、打包器和测试运行器 | 现有材料、预期目标与交付范围 |
| `$ecc:code-tour` | 创建 CodeTour `.tour` 文件——针对特定角色的、带有真实文件和行锚点的逐步演练 | 项目目录、技术栈与待改功能 |
| `$ecc:codebase-onboarding` | 分析一个陌生的代码库，并生成一个结构化的入门指南，包括架构图、关键入口点、规范和一个起始的CLAUDE.md文件 | 项目目录、技术栈与待改功能 |
| `$ecc:coding-standards` | 适用于TypeScript、JavaScript、React和Node.js开发的通用编码标准、最佳实践和模式 | 项目目录、技术栈与待改功能 |
| `$ecc:compose-multiplatform-patterns` | KMP项目中的Compose Multiplatform和Jetpack Compose模式——状态管理、导航、主题化、性能优化和平台特定UI | 项目目录、技术栈与待改功能 |
| `$ecc:content-hash-cache-pattern` | 使用SHA-256内容哈希缓存昂贵的文件处理结果——路径无关、自动失效、服务层分离 | 项目目录、技术栈与待改功能 |
| `$ecc:contract-first` | 先明确接口契约，再协调前后端开发 | 现有材料、预期目标与交付范围 |
| `$ecc:cpp-coding-standards` | 基于C++核心指南（isocpp.github.io）的C++编码标准 | 项目目录、技术栈与待改功能 |
| `$ecc:dashboard-builder` | 为 Grafana、SigNoz 等平台构建能够回答实际运维人员问题的监控仪表板 | 项目目录、技术栈与待改功能 |
| `$ecc:database-migrations` | 数据库迁移最佳实践，涵盖模式变更、数据迁移、回滚以及零停机部署，适用于PostgreSQL、MySQL及常用ORM（Prisma、Drizzle、Django、TypeORM、golang-mi… | 项目目录、技术栈与待改功能 |
| `$ecc:django-patterns` | Django架构模式，使用DRF设计REST API，ORM最佳实践，缓存，信号，中间件，以及生产级Django应用程序 | 项目目录、技术栈与待改功能 |
| `$ecc:dotnet-patterns` | 惯用的C#和.NET模式、约定、依赖注入、async/await以及构建健壮、可维护的.NET应用程序的最佳实践 | 项目目录、技术栈与待改功能 |
| `$ecc:error-handling` | 设计错误分类、恢复、重试和用户可见错误 | 现有材料、预期目标与交付范围 |
| `$ecc:fastapi-patterns` | 开发与审查 FastAPI 接口、异步逻辑和依赖注入 | 项目目录、技术栈与待改功能 |
| `$ecc:git-workflow` | Git工作流模式，包括分支策略、提交约定、合并与变基、冲突解决以及适用于各种规模团队的协作开发最佳实践 | 现有材料、预期目标与交付范围 |
| `$ecc:github-ops` | GitHub 仓库操作、自动化与管理 | 现有材料、预期目标与交付范围 |
| `$ecc:golang-patterns` | 用于构建健壮、高效且可维护的Go应用程序的惯用Go模式、最佳实践和约定 | 项目目录、技术栈与待改功能 |
| `$ecc:healthcare-cdss-patterns` | 临床决策支持系统（CDSS）开发模式 | 项目目录、技术栈与待改功能 |
| `$ecc:healthcare-emr-patterns` | 医疗应用中EMR/EHR的开发模式 | 项目目录、技术栈与待改功能 |
| `$ecc:hexagonal-architecture` | 设计、实现并重构端口与适配器系统，具有清晰的领域边界、依赖反转以及跨 TypeScript、Java、Kotlin 和 Go 服务的可测试用例编排 | 现有材料、预期目标与交付范围 |
| `$ecc:i18n-sync` | 同步不同语言的界面与文档翻译 | 现有材料、预期目标与交付范围 |
| `$ecc:inherit-legacy-style` | 修改旧项目时保持已有代码与视觉风格 | 现有材料、预期目标与交付范围 |
| `$ecc:java-coding-standards` | Spring Boot服务的Java编码标准：命名、不可变性、Optional用法、流、异常、泛型和项目布局 | 项目目录、技术栈与待改功能 |
| `$ecc:jpa-patterns` | Spring Boot中的JPA/Hibernate模式，用于实体设计、关系处理、查询优化、事务管理、审计、索引、分页和连接池 | 项目目录、技术栈与待改功能 |
| `$ecc:kotlin-exposed-patterns` | JetBrains Exposed ORM 模式，包括 DSL 查询、DAO 模式、事务、HikariCP 连接池、Flyway 迁移和仓库模式 | 项目目录、技术栈与待改功能 |
| `$ecc:kotlin-ktor-patterns` | Ktor 服务器模式，包括路由 DSL、插件、身份验证、Koin DI、kotlinx.serialization、WebSockets 和 testApplication 测试 | 项目目录、技术栈与待改功能 |
| `$ecc:kotlin-patterns` | 惯用的Kotlin模式、最佳实践和约定，用于构建健壮、高效且可维护的Kotlin应用程序，包括协程、空安全和DSL构建器 | 项目目录、技术栈与待改功能 |
| `$ecc:laravel-patterns` | Laravel架构模式、路由/控制器、Eloquent ORM、服务层、队列、事件、缓存以及用于生产应用的API资源 | 项目目录、技术栈与待改功能 |
| `$ecc:mybatis-patterns` | 组织 MyBatis 数据访问、映射和查询逻辑 | 项目目录、技术栈与待改功能 |
| `$ecc:mysql-patterns` | 设计与优化 MySQL/MariaDB 查询和结构 | 项目目录、技术栈与待改功能 |
| `$ecc:nestjs-patterns` | NestJS 架构模式，涵盖模块、控制器、提供者、DTO 验证、守卫、拦截器、配置以及生产级 TypeScript 后端 | 项目目录、技术栈与待改功能 |
| `$ecc:perl-patterns` | 现代 Perl 5.36+ 的惯用法、最佳实践和约定，用于构建稳健、可维护的 Perl 应用程序 | 项目目录、技术栈与待改功能 |
| `$ecc:plankton-code-quality` | 使用Plankton进行编写时代码质量强制执行——通过钩子在每次文件编辑时自动格式化、代码检查和Claude驱动的修复 | 项目目录、技术栈与待改功能 |
| `$ecc:postgres-patterns` | 用于查询优化、模式设计、索引和安全性的PostgreSQL数据库模式 | 项目目录、技术栈与待改功能 |
| `$ecc:prisma-patterns` | 设计 Prisma 模型、查询和迁移 | 项目目录、技术栈与待改功能 |
| `$ecc:python-patterns` | Pythonic 惯用法、PEP 8 标准、类型提示以及构建稳健、高效且可维护的 Python 应用程序的最佳实践 | 项目目录、技术栈与待改功能 |
| `$ecc:quarkus-patterns` | 开发与组织 Quarkus 应用架构 | 项目目录、技术栈与待改功能 |
| `$ecc:rails-patterns` | 组织 Ruby on Rails 应用与开发模式 | 项目目录、技术栈与待改功能 |
| `$ecc:redis-patterns` | 设计 Redis 数据结构、缓存和访问模式 | 项目目录、技术栈与待改功能 |
| `$ecc:rust-patterns` | 地道的Rust模式、所有权、错误处理、特质、并发，以及构建安全、高性能应用程序的最佳实践 | 项目目录、技术栈与待改功能 |
| `$ecc:springboot-patterns` | Spring Boot架构模式、REST API设计、分层服务、数据访问、缓存、异步处理和日志记录 | 项目目录、技术栈与待改功能 |
| `$ecc:team-builder` | 用于组合和派遣并行团队的交互式代理选择器 | 项目目录、技术栈与待改功能 |
| `$ecc:tinystruct-patterns` | 开发 tinystruct Java 项目及启动脚本 | 项目目录、技术栈与待改功能 |

### 测试、安全与质量（41）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:ai-regression-testing` | AI辅助开发的回归测试策略 | 代码目录、运行方式与验证目标 |
| `$ecc:automation-audit-ops` | 面向ECC的以证据为先的自动化清单与重叠审计工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:change-impact` | 分析代码修改影响的模块、契约与验证范围 | 现有材料、预期目标与交付范围 |
| `$ecc:click-path-audit` | 追踪每个面向用户的按钮/触点的完整状态变化序列，以发现功能单独工作但相互抵消、产生错误最终状态或使UI处于不一致状态的错误 | 现有材料、预期目标与交付范围 |
| `$ecc:conventional-commit-review` | 检查暂存修改与 Conventional Commits 提交信息 | 现有材料、预期目标与交付范围 |
| `$ecc:cpp-testing` | 仅用于编写/更新/修复C++测试、配置GoogleTest/CTest、诊断失败或不稳定的测试，或添加覆盖率/消毒器时使用 | 代码目录、运行方式与验证目标 |
| `$ecc:csharp-testing` | 使用 xUnit、FluentAssertions、模拟、集成测试和测试组织最佳实践的 C# 和 .NET 测试模式 | 代码目录、运行方式与验证目标 |
| `$ecc:defi-amm-security` | Solidity AMM 合约、流动性池和交换流程的安全检查清单 | 现有材料、预期目标与交付范围 |
| `$ecc:delivery-gate` | 用交付检查约束尚未验证的完成声明 | 现有材料、预期目标与交付范围 |
| `$ecc:django-security` | Django 安全最佳实践、认证、授权、CSRF 防护、SQL 注入预防、XSS 预防和安全部署配置 | 现有材料、预期目标与交付范围 |
| `$ecc:django-tdd` | Django 测试策略，包括 pytest-django、TDD 方法、factory_boy、模拟、覆盖率以及测试 Django REST Framework API | 代码目录、运行方式与验证目标 |
| `$ecc:django-verification` | Django项目的验证循环：迁移、代码检查、带覆盖率的测试、安全扫描，以及在发布或PR前的部署就绪检查 | 代码目录、运行方式与验证目标 |
| `$ecc:e2e-testing` | Playwright E2E 测试模式、页面对象模型、配置、CI/CD 集成、工件管理和不稳定测试策略 | 代码目录、运行方式与验证目标 |
| `$ecc:fsharp-testing` | 编写和组织 F# 测试 | 代码目录、运行方式与验证目标 |
| `$ecc:golang-testing` | Go测试模式包括表格驱动测试、子测试、基准测试、模糊测试和测试覆盖率 | 代码目录、运行方式与验证目标 |
| `$ecc:kotlin-testing` | 使用Kotest、MockK、协程测试、基于属性的测试和Kover覆盖率的Kotlin测试模式 | 代码目录、运行方式与验证目标 |
| `$ecc:laravel-security` | Laravel 安全最佳实践，涵盖认证/授权、验证、CSRF、批量赋值、文件上传、密钥管理、速率限制和安全部署 | 现有材料、预期目标与交付范围 |
| `$ecc:laravel-tdd` | 使用 PHPUnit 和 Pest、工厂、数据库测试、模拟以及覆盖率目标进行 Laravel 的测试驱动开发 | 代码目录、运行方式与验证目标 |
| `$ecc:laravel-verification` | Verification loop for Laravel projects: env checks, linting, static analysis, tests with coverage… | 代码目录、运行方式与验证目标 |
| `$ecc:module-regression` | 根据模块边界设计回归检查 | 代码目录、运行方式与验证目标 |
| `$ecc:perl-security` | 全面的Perl安全指南，涵盖污染模式、输入验证、安全进程执行、DBI参数化查询、Web安全（XSS/SQLi/CSRF）以及perlcritic安全策略 | 现有材料、预期目标与交付范围 |
| `$ecc:perl-testing` | 使用Test2::V0、Test::More、prove runner、模拟、Devel::Cover覆盖率和TDD方法的Perl测试模式 | 代码目录、运行方式与验证目标 |
| `$ecc:prediction-market-risk-review` | 检查预测市场方案的风险与证据限制 | 现有材料、预期目标与交付范围 |
| `$ecc:production-audit` | 根据本地证据检查产品实现与可发布程度 | 现有材料、预期目标与交付范围 |
| `$ecc:python-testing` | 使用pytest的Python测试策略，包括TDD方法、夹具、模拟、参数化和覆盖率要求 | 代码目录、运行方式与验证目标 |
| `$ecc:quarkus-security` | 检查 Quarkus 身份认证、授权与安全配置 | 现有材料、预期目标与交付范围 |
| `$ecc:quarkus-tdd` | 使用测试驱动流程开发 Quarkus 功能 | 代码目录、运行方式与验证目标 |
| `$ecc:quarkus-verification` | 执行 Quarkus 构建、测试与交付验证 | 代码目录、运行方式与验证目标 |
| `$ecc:repo-scan` | 用于从固定且可审查的提交安装外部 repo-scan 技能的引导指针 | 现有材料、预期目标与交付范围 |
| `$ecc:rust-testing` | Rust测试模式，包括单元测试、集成测试、异步测试、基于属性的测试、模拟和覆盖率 | 代码目录、运行方式与验证目标 |
| `$ecc:safety-guard` | 使用此技能可防止在生产系统上工作或自主运行代理时进行破坏性操作 | 现有材料、预期目标与交付范围 |
| `$ecc:security-bounty-hunter` | 在仓库中寻找可利用、值得赏金的安全问题 | 现有材料、预期目标与交付范围 |
| `$ecc:security-review` | 在添加身份验证、处理用户输入、处理机密信息、创建API端点或实现支付/敏感功能时使用此技能 | 现有材料、预期目标与交付范围 |
| `$ecc:security-scan` | 使用AgentShield扫描您的Claude代码配置（.claude/目录），以发现安全漏洞、配置错误和注入风险 | 现有材料、预期目标与交付范围 |
| `$ecc:springboot-security` | Java Spring Boot 服务中认证/授权、验证、CSRF、密钥、标头、速率限制和依赖安全性的 Spring Security 最佳实践 | 现有材料、预期目标与交付范围 |
| `$ecc:springboot-tdd` | 使用JUnit 5、Mockito、MockMvc、Testcontainers和JaCoCo进行Spring Boot的测试驱动开发 | 代码目录、运行方式与验证目标 |
| `$ecc:springboot-verification` | Spring Boot项目验证循环：构建、静态分析、测试覆盖、安全扫描，以及发布或PR前的差异审查 | 代码目录、运行方式与验证目标 |
| `$ecc:swift-protocol-di-testing` | 基于协议的依赖注入，用于可测试的Swift代码——使用聚焦协议和Swift Testing模拟文件系统、网络和外部API | 代码目录、运行方式与验证目标 |
| `$ecc:tdd-workflow` | 在编写新功能、修复错误或重构代码时使用此技能 | 代码目录、运行方式与验证目标 |
| `$ecc:test-collaboration` | 维护需求、风险与可执行测试的对应关系 | 代码目录、运行方式与验证目标 |
| `$ecc:workspace-surface-audit` | 审计活跃仓库、MCP服务器、插件、连接器、环境表面和工具设置，然后推荐最高价值的ECC原生技能、钩子、代理和操作员工作流 | 现有材料、预期目标与交付范围 |

### 前端、视觉与多媒体（41）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:accessibility` | 使用 WCAG 2.2 Level AA 标准设计、实施和审计包容性数字产品 | 现有材料、预期目标与交付范围 |
| `$ecc:angular-developer` | 按项目约定开发 Angular 应用和组件 | 项目目录、技术栈与待改功能 |
| `$ecc:api-design` | REST API设计模式，包括资源命名、状态码、分页、过滤、错误响应、版本控制和生产API的速率限制 | 现有材料、预期目标与交付范围 |
| `$ecc:article-writing` | 根据提供的示例或品牌指导，以独特的语气撰写文章、指南、博客帖子、教程、新闻简报等长篇内容 | 现有材料、预期目标与交付范围 |
| `$ecc:blender-motion-state-inspection` | 检查 Blender 动画、帧状态与运动结果 | 现有材料、预期目标与交付范围 |
| `$ecc:brand-discovery` | 梳理品牌定位、受众和视觉方向 | 现有材料、预期目标与交付范围 |
| `$ecc:brand-voice` | 从真实的帖子、文章、发布说明、文档或网站文案中构建基于源材料的写作风格档案，然后在内容、外展和社交工作流中重复使用该档案 | 现有材料、预期目标与交付范围 |
| `$ecc:counterparty-channel-discipline` | 区分沟通渠道权限并约束外部内容影响 | 现有材料、预期目标与交付范围 |
| `$ecc:dart-flutter-patterns` | 生产就绪的 Dart 和 Flutter 模式，涵盖空安全、不可变状态、异步组合、Widget 架构、流行的状态管理框架（BLoC、Riverpod、Provider）、GoRouter 导航、… | 项目目录、技术栈与待改功能 |
| `$ecc:design-system` | 使用此技能生成或审计设计系统，检查视觉一致性，并审查涉及样式的PR | 现有材料、预期目标与交付范围 |
| `$ecc:fal-ai-media` | 通过 fal.ai MCP 实现统一的媒体生成——图像、视频和音频 | 现有材料、预期目标与交付范围 |
| `$ecc:flutter-dart-code-review` | 库无关的Flutter/Dart代码审查清单，涵盖Widget最佳实践、状态管理模式（BLoC、Riverpod、Provider、GetX、MobX、Signals）、Dart惯用法、性能、可… | 项目目录、技术栈与待改功能 |
| `$ecc:frontend-a11y` | 改善网页语义、键盘操作和无障碍体验 | 现有材料、预期目标与交付范围 |
| `$ecc:frontend-design-direction` | 明确前端视觉方向和设计约束 | 现有材料、预期目标与交付范围 |
| `$ecc:frontend-patterns` | React、Next.js、状态管理、性能优化和UI最佳实践的前端开发模式 | 项目目录、技术栈与待改功能 |
| `$ecc:frontend-slides` | 从零开始或通过转换PowerPoint文件创建令人惊艳、动画丰富的HTML演示文稿 | 现有材料、预期目标与交付范围 |
| `$ecc:ios-icon-gen` | 为 iOS 应用生成图标资源 | 现有材料、预期目标与交付范围 |
| `$ecc:liquid-glass-design` | iOS 26 液态玻璃设计系统 — 适用于 SwiftUI、UIKit 和 WidgetKit 的动态玻璃材质，具有模糊、反射和交互式变形效果 | 现有材料、预期目标与交付范围 |
| `$ecc:manim-video` | 构建可复用的Manim解释器，用于技术概念、图表、系统图和产品演示，并在需要时移交给更广泛的ECC视频栈 | 现有材料、预期目标与交付范围 |
| `$ecc:motion-advanced` | 实现复杂交互动效及高级运动设计 | 现有材料、预期目标与交付范围 |
| `$ecc:motion-foundations` | 定义动效节奏、弹簧、缓动和基础规范 | 现有材料、预期目标与交付范围 |
| `$ecc:motion-patterns` | 实现可复用的界面动效模式 | 项目目录、技术栈与待改功能 |
| `$ecc:nextjs-turbopack` | Next.js 16+ 和 Turbopack — 增量打包、文件系统缓存、开发速度，以及何时使用 Turbopack 与 webpack | 现有材料、预期目标与交付范围 |
| `$ecc:nuxt4-patterns` | Nuxt 4 应用模式，涵盖水合安全、性能优化、路由规则、懒加载，以及使用 useFetch 和 useAsyncData 进行 SSR 安全的数据获取 | 项目目录、技术栈与待改功能 |
| `$ecc:plan-canvas` | 在画布中查看和维护计划或 HTML 材料 | 现有材料、预期目标与交付范围 |
| `$ecc:react-native-patterns` | 开发 React Native/Expo 移动应用 | 项目目录、技术栈与待改功能 |
| `$ecc:react-patterns` | 组织 React 组件、状态和应用结构 | 项目目录、技术栈与待改功能 |
| `$ecc:react-performance` | 分析并改善 React/Next.js 性能 | 现有材料、预期目标与交付范围 |
| `$ecc:react-testing` | 为 React 组件与交互编写测试 | 代码目录、运行方式与验证目标 |
| `$ecc:remotion-video-creation` | Remotion 最佳实践 - 在 React 中创建视频 | 现有材料、预期目标与交付范围 |
| `$ecc:swiftui-patterns` | SwiftUI 架构模式，使用 @Observable 进行状态管理，视图组合，导航，性能优化，以及现代 iOS/macOS UI 最佳实践 | 项目目录、技术栈与待改功能 |
| `$ecc:taste` | 规划指定音乐视频风格与视听剪辑方向 | 现有材料、预期目标与交付范围 |
| `$ecc:taste-application` | 应用提炼出的风格包生成和剪辑视频 | 现有材料、预期目标与交付范围 |
| `$ecc:taste-distillation` | 从参考视频提炼配色、节奏和风格包 | 现有材料、预期目标与交付范围 |
| `$ecc:tasteforge-video` | 组织多模态素材、视频风格和编辑导出流程 | 现有材料、预期目标与交付范围 |
| `$ecc:ui-demo` | 使用 Playwright 录制精美的 UI 演示视频 | 现有材料、预期目标与交付范围 |
| `$ecc:ui-to-vue` | 将界面截图或设计稿转成 Vue 3 组件 | 现有材料、预期目标与交付范围 |
| `$ecc:video-editing` | AI辅助的视频编辑工作流程，用于剪辑、构建和增强实拍素材 | 现有材料、预期目标与交付范围 |
| `$ecc:videodb` | 视频与音频的查看、理解与行动 | 现有材料、预期目标与交付范围 |
| `$ecc:vite-patterns` | 配置 Vite 构建、插件、开发代理与优化 | 项目目录、技术栈与待改功能 |
| `$ecc:vue-patterns` | 开发 Vue 3、Pinia 和 Vue Router 应用 | 项目目录、技术栈与待改功能 |

### 环境、部署与网络（23）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:cisco-ios-patterns` | 审查 Cisco IOS/IOS-XE 配置与网络约定 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:data-throughput-accelerator` | 定位并改善数据处理、传输与吞吐瓶颈 | 现有材料、预期目标与交付范围 |
| `$ecc:deployment-patterns` | 部署工作流、CI/CD流水线模式、Docker容器化、健康检查、回滚策略以及Web应用程序的生产就绪检查清单 | 项目目录、技术栈与待改功能 |
| `$ecc:docker-patterns` | 用于本地开发的Docker和Docker Compose模式，包括容器安全、网络、卷策略和多服务编排 | 项目目录、技术栈与待改功能 |
| `$ecc:flox-environments` | 建立可复现、跨平台的 Flox 开发环境 | 现有材料、预期目标与交付范围 |
| `$ecc:homelab-network-readiness` | 检查家庭实验室网络部署的前置条件 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:homelab-network-setup` | 配置家庭或个人实验室网络 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:homelab-pihole-dns` | 配置 Pi-hole DNS、广告过滤和诊断 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:homelab-vlan-segmentation` | 通过 VLAN 划分家庭实验室网络 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:homelab-wireguard-vpn` | 配置家庭实验室 WireGuard VPN | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:ito-baskets` | 只读查询与分析 Itô 计算资源组合 | 现有材料、预期目标与交付范围 |
| `$ecc:ito-compute` | 查询 Itô GPU 资源与可用性 | 现有材料、预期目标与交付范围 |
| `$ecc:ito-inference` | 检查 Itô 推理服务与可用模型 | 现有材料、预期目标与交付范围 |
| `$ecc:ito-training` | 检查 Itô 训练资源与服务能力 | 现有材料、预期目标与交付范围 |
| `$ecc:kubernetes-patterns` | 设计 Kubernetes 工作负载和部署配置 | 项目目录、技术栈与待改功能 |
| `$ecc:latency-critical-systems` | 定位低延迟系统瓶颈并验证延迟改进 | 现有材料、预期目标与交付范围 |
| `$ecc:netmiko-ssh-automation` | 使用 Netmiko 编排网络设备 SSH 操作 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:network-bgp-diagnostics` | 以诊断为主检查 BGP 邻居、路由及异常 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:network-config-validation` | 在部署前检查网络配置与预期一致性 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:network-interface-health` | 诊断网络接口错误、丢包和链路状态 | 拓扑/配置/诊断输出与操作范围 |
| `$ecc:terminal-opener` | 按明确参数在可见终端中启动程序 | 现有材料、预期目标与交付范围 |
| `$ecc:terminal-ops` | 基于证据优先的仓库执行工作流，适用于ECC | 现有材料、预期目标与交付范围 |
| `$ecc:uncloud` | 使用 Uncloud CLI 管理服务、入口与集群 | 现有材料、预期目标与交付范围 |

### 文档、业务与其他工作流（85）

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$ecc:ai-first-engineering` | 团队中人工智能代理生成大部分实施输出的工程运营模型 | 现有材料、预期目标与交付范围 |
| `$ecc:android-clean-architecture` | 适用于Android和Kotlin多平台项目的Clean Architecture模式——模块结构、依赖规则、用例、仓库以及数据层模式 | 现有材料、预期目标与交付范围 |
| `$ecc:architecture-decision-records` | 在Claude Code会话期间，将做出的架构决策捕获为结构化的架构决策记录（ADR） | 现有材料、预期目标与交付范围 |
| `$ecc:bengali-nlp` | 孟加拉语文本处理和 NLP 工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:blueprint` | 将单行目标转化为多会话、多代理工程项目的分步构建计划 | 现有材料、预期目标与交付范围 |
| `$ecc:brownfield-retrospective` | 根据已有工程证据复盘开发过程与改进项 | 现有材料、预期目标与交付范围 |
| `$ecc:browser-qa` | Automate visual testing and UI interaction verification using browser automation after deployment | 现有材料、预期目标与交付范围 |
| `$ecc:canary-watch` | 使用此技能在部署、合并或依赖升级后监控已部署的URL是否存在回归问题 | 现有材料、预期目标与交付范围 |
| `$ecc:carrier-relationship-management` | 用于管理承运商组合、协商运费、跟踪承运商绩效、分配货运以及维护战略承运商关系的编码专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:ck` | Claude Code 的每个项目持久化记忆 | 现有材料、预期目标与交付范围 |
| `$ecc:claude-devfleet` | 通过Claude DevFleet协调多智能体编码任务——规划项目、在隔离的工作树中并行调度智能体、监控进度并读取结构化报告 | 现有材料、预期目标与交付范围 |
| `$ecc:clickhouse-io` | ClickHouse数据库模式、查询优化、分析以及高性能分析工作负载的数据工程最佳实践 | 现有材料、预期目标与交付范围 |
| `$ecc:competitive-platform-analysis` | 按统一范围和证据比较竞品平台 | 现有材料、预期目标与交付范围 |
| `$ecc:competitive-report-structure` | 组织有评分依据的竞品分析报告 | 现有材料、预期目标与交付范围 |
| `$ecc:configure-ecc` | 在 Claude Code、Codex 或 Kimi 内引导 ECC 安装、更新或重新配置，同时严格遵守各家工具真实的插件、范围和 Hook 能力 | 现有材料、预期目标与交付范围 |
| `$ecc:connections-optimizer` | 重新组织用户的X和LinkedIn网络，采用审查优先的修剪策略，提供添加/关注建议，并以用户真实口吻起草针对不同渠道的温和外联 | 现有材料、预期目标与交付范围 |
| `$ecc:content-engine` | 为X、LinkedIn、TikTok、YouTube、新闻通讯和跨平台重新利用的多平台活动创建平台原生内容系统 | 现有材料、预期目标与交付范围 |
| `$ecc:crosspost` | 跨X、LinkedIn、Threads和Bluesky的多平台内容分发 | 现有材料、预期目标与交付范围 |
| `$ecc:customer-billing-ops` | 使用 Stripe 等连接计费工具操作客户计费工作流，例如订阅、退款、流失分类、计费门户恢复和计划分析 | 现有材料、预期目标与交付范围 |
| `$ecc:customs-trade-compliance` | 海关文件、关税分类、关税优化、受限方筛查以及多司法管辖区法规合规的编码化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:dev-team` | 通过不同工程角色协作推进开发任务 | 现有材料、预期目标与交付范围 |
| `$ecc:django-celery` | 设计 Django 与 Celery 异步任务和重试流程 | 现有材料、预期目标与交付范围 |
| `$ecc:dmux-workflows` | 使用dmux（AI代理的tmux窗格管理器）进行多代理编排 | 现有材料、预期目标与交付范围 |
| `$ecc:docs-governance` | 为不同类型文档选择维护、审查与发布流程 | 现有材料、预期目标与交付范围 |
| `$ecc:documentation-lookup` | 通过 Context7 MCP 使用最新的库和框架文档，而非训练数据 | 现有材料、预期目标与交付范围 |
| `$ecc:dynamic-workflow-mode` | 根据当前任务设计合适的 Agent 执行流程 | 现有材料、预期目标与交付范围 |
| `$ecc:email-ops` | 以证据为先的邮箱分类、草稿、发送验证及已发送邮件安全跟进工作流，适用于ECC | 现有材料、预期目标与交付范围 |
| `$ecc:energy-procurement` | 电力与燃气采购、电价优化、需量电费管理、可再生能源购电协议评估及多设施能源成本管理的编码化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:esign-field-placement` | 根据文档坐标放置电子签名及表单字段 | 现有材料、预期目标与交付范围 |
| `$ecc:exa-search` | 通过Exa MCP进行神经搜索，适用于网络、代码和公司研究 | 现有材料、预期目标与交付范围 |
| `$ecc:finance-billing-ops` | 面向ECC的以证据为先的收入、定价、退款、团队计费和计费模型真相工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:foundation-models-on-device` | 苹果FoundationModels框架用于设备上的LLM——文本生成、使用@Generable进行引导生成、工具调用，以及在iOS 26+中的快照流 | 现有材料、预期目标与交付范围 |
| `$ecc:generating-python-installer` | 为 Python 应用生成面向分发的安装程序 | 现有材料、预期目标与交付范围 |
| `$ecc:google-workspace-ops` | 将 Google 云端硬盘、文档、表格和幻灯片作为一个工作流界面来操作，用于处理计划、追踪器、演示文稿和共享文档 | 现有材料、预期目标与交付范围 |
| `$ecc:growth-log` | 记录能力提升、工程经验和成长证据 | 现有材料、预期目标与交付范围 |
| `$ecc:healthcare-phi-compliance` | 医疗应用中受保护健康信息（PHI）和个人身份信息（PII）的合规模式 | 现有材料、预期目标与交付范围 |
| `$ecc:hermes-imports` | 将本地 Hermes 操作员工作流转换为经过清理的 ECC 技能和发布包工件 | 现有材料、预期目标与交付范围 |
| `$ecc:hipaa-compliance` | 针对医疗隐私和安全工作的HIPAA特定入口点 | 现有材料、预期目标与交付范围 |
| `$ecc:intent-driven-development` | 将模糊意图转为可验证的需求与交付标准 | 现有材料、预期目标与交付范围 |
| `$ecc:inventory-demand-planning` | 为多地点零售商提供需求预测、安全库存优化、补货规划及促销提升估算的编码化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:investor-materials` | 创建和更新宣传文稿、一页简介、投资者备忘录、加速器申请、财务模型和融资材料 | 现有材料、预期目标与交付范围 |
| `$ecc:investor-outreach` | 草拟冷邮件、热情介绍简介、跟进邮件、更新邮件和投资者沟通以筹集资金 | 现有材料、预期目标与交付范围 |
| `$ecc:iterative-retrieval` | 逐步优化上下文检索以解决子代理上下文问题的模式 | 现有材料、预期目标与交付范围 |
| `$ecc:jira-integration` | 在检索Jira工单、分析需求、更新工单状态、添加评论或转换问题时使用此技能 | 现有材料、预期目标与交付范围 |
| `$ecc:knowledge-ops` | 知识库管理、摄取、同步和跨多个存储层（本地文件、MCP内存、向量存储、Git仓库）的检索 | 现有材料、预期目标与交付范围 |
| `$ecc:kotlin-coroutines-flows` | Kotlin协程与Flow在Android和KMP中的模式——结构化并发、Flow操作符、StateFlow、错误处理和测试 | 现有材料、预期目标与交付范围 |
| `$ecc:laravel-plugin-discovery` | 通过LaraPlugins.io MCP发现和评估Laravel包 | 现有材料、预期目标与交付范围 |
| `$ecc:lead-intelligence` | AI原生的潜在客户情报与外联管道 | 现有材料、预期目标与交付范围 |
| `$ecc:living-docs-governance` | 持续维护长期项目文档与事实一致性 | 现有材料、预期目标与交付范围 |
| `$ecc:logistics-exception-management` | 针对货运异常、货物延误、损坏、丢失和承运商纠纷的编码化专业知识，由拥有15年以上运营经验的物流专业人士提供 | 现有材料、预期目标与交付范围 |
| `$ecc:mailtrap-email-integration` | 集成 Mailtrap 邮件服务与发送工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:make-interfaces-feel-better` | 改善界面反馈、间距、动效与交互细节 | 现有材料、预期目标与交付范围 |
| `$ecc:marketing-campaign` | 组织营销活动计划、内容与结果衡量 | 现有材料、预期目标与交付范围 |
| `$ecc:master-agreement-generator` | 根据材料整理主协议的待审阅草稿 | 现有材料、预期目标与交付范围 |
| `$ecc:messages-ops` | 面向ECC的以证据为先的实时消息工作流 | 现有材料、预期目标与交付范围 |
| `$ecc:nanoclaw-repl` | 操作并扩展NanoClaw v2，这是ECC基于claude -p构建的零依赖会话感知REPL | 现有材料、预期目标与交付范围 |
| `$ecc:nasiko-control-plane` | 管理实验性 Nasiko Agent 控制平面 | 现有材料、预期目标与交付范围 |
| `$ecc:nodejs-keccak256` | 防止 JavaScript 和 TypeScript 中的以太坊哈希错误 | 现有材料、预期目标与交付范围 |
| `$ecc:nutrient-document-processing` | 使用Nutrient DWS API处理、转换、OCR识别、提取、编辑、签名和填写文档 | 现有材料、预期目标与交付范围 |
| `$ecc:openclaw-persona-forge` | 为 OpenClaw Agent 构建角色设定和行为约束 | 现有材料、预期目标与交付范围 |
| `$ecc:opensource-pipeline` | 开源流水线：fork、清理并打包私有项目以安全公开发布 | 现有材料、预期目标与交付范围 |
| `$ecc:osint-investigation` | 根据公开线索进行可追溯的信息调查 | 现有材料、预期目标与交付范围 |
| `$ecc:parallel-execution-optimizer` | 当用户希望通过并行工作、并发 agents、批量工具调用、隔离 worktree 或多条独立验证通道来大幅加速任务、同时不损失正确性时使用 | 现有材料、预期目标与交付范围 |
| `$ecc:product-capability` | 将PRD意图、路线图需求或产品讨论转化为可实施的方案计划，在开始多服务工作之前暴露约束、不变性、接口和未解决的决策 | 现有材料、预期目标与交付范围 |
| `$ecc:product-lens` | 使用此技能在构建前验证“为什么”，运行产品诊断，并在请求成为实施合同之前对产品方向进行压力测试 | 现有材料、预期目标与交付范围 |
| `$ecc:production-scheduling` | 为离散和批量制造中的生产调度、作业排序、产线平衡、换模优化和瓶颈解决提供编码化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:project-flow-ops` | 通过分类问题和拉取请求、关联活跃工作、保持GitHub对外可见而Linear作为内部执行层，来协调GitHub和Linear之间的执行流程 | 现有材料、预期目标与交付范围 |
| `$ecc:quality-nonconformance` | 为受监管制造业中的质量控制、不合格调查、根本原因分析、纠正措施和供应商质量管理提供编码化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:ralphinho-rfc-pipeline` | 基于RFC驱动的多智能体DAG执行模式，包含质量门、合并队列和工作单元编排 | 现有材料、预期目标与交付范围 |
| `$ecc:recursive-decision-ledger` | 记录重复决策、验证证据与选择理由 | 现有材料、预期目标与交付范围 |
| `$ecc:regex-vs-llm-structured-text` | 选择在解析结构化文本时使用正则表达式还是大型语言模型的决策框架——从正则表达式开始，仅在低置信度的边缘情况下添加大型语言模型 | 现有材料、预期目标与交付范围 |
| `$ecc:returns-reverse-logistics` | 用于退货授权、接收与检验、处置决策、退款处理、欺诈检测以及保修索赔管理的标准化专业知识 | 现有材料、预期目标与交付范围 |
| `$ecc:rules-distill` | 扫描技能以提取跨领域原则并将其提炼为规则——追加、修订或创建新的规则文件 | 现有材料、预期目标与交付范围 |
| `$ecc:search-first` | 研究优先于编码的工作流程 | 现有材料、预期目标与交付范围 |
| `$ecc:seo` | 审计、规划并实施SEO改进，涵盖技术SEO、页面优化、结构化数据、核心网页指标和内容策略 | 现有材料、预期目标与交付范围 |
| `$ecc:social-graph-ranker` | 加权社交图谱排名，用于在X和LinkedIn上发现温暖介绍、桥梁评分和网络差距分析 | 现有材料、预期目标与交付范围 |
| `$ecc:social-publisher` | 通过支持的平台工具排期和发布社交内容 | 现有材料、预期目标与交付范围 |
| `$ecc:story-lifecycle` | 维护 epic、用户故事和迭代的文件化流程 | 现有材料、预期目标与交付范围 |
| `$ecc:strategic-compact` | 建议在逻辑间隔处手动压缩上下文，以在任务阶段中保留上下文，而非任意的自动压缩 | 现有材料、预期目标与交付范围 |
| `$ecc:swift-actor-persistence` | 在 Swift 中使用 actor 实现线程安全的数据持久化——基于内存缓存与文件支持的存储，通过设计消除数据竞争 | 现有材料、预期目标与交付范围 |
| `$ecc:swift-concurrency-6-2` | Swift 6.2 可接近的并发性 — 默认单线程，@concurrent 用于显式后台卸载，隔离一致性用于主 actor 类型 | 现有材料、预期目标与交付范围 |
| `$ecc:unified-notifications-ops` | 将通知作为统一的 ECC 原生工作流进行操作，涵盖 GitHub、Linear、桌面提醒、钩子以及连接的通信界面 | 现有材料、预期目标与交付范围 |
| `$ecc:visa-doc-translate` | 将签证申请文件（图片）翻译成英文，并创建包含原文和译文的双语PDF | 现有材料、预期目标与交付范围 |
| `$ecc:windows-desktop-e2e` | 测试 Windows 原生桌面应用的完整交互流程 | 现有材料、预期目标与交付范围 |
| `$ecc:x-api` | X/Twitter API集成，用于发布推文、线程、读取时间线、搜索和分析 | 现有材料、预期目标与交付范围 |

## ECC 迁移命令技能（37）

这些是迁移成技能入口的 `source-command-*`。名称描述的是原工作流，不是本次安装新执行的操作。例如 auto-update 不代表已设自动更新；publish 不代表可未经授权发布。

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

## 磁盘存在但当前未列为 Codex 可调用技能

以下不计入 427。若要使用，先检查宿主、插件启用状态和对应依赖；本次没有为它们创建新的全局入口。

| 名称 | 用途 | 当前状态与使用方式 |
| --- | --- | --- |
| `artifact-template-analytics-dashboard` | 获客、参与度与留存分析仪表盘表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-annual-impact-report` | 年度成果与影响报告演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-brand-guidelines` | 品牌视觉规范演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-business-review` | 业务表现与 KPI 复盘演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-calder-architecture` | 建筑项目与设计展示演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-creative-campaign-brief` | 创意活动目标与策略简报演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-design-report` | 设计说明与建议报告文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-experiment-analysis` | 实验假设、结果与分析报告文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-financial-budget` | 预算、实际与情景预测表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-growth-strategy` | 增长机会与策略演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-investment-committee-memo` | 投资委员会讨论备忘录文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-legal-memorandum` | 法律议题分析备忘录模板 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-market-trends-report` | 市场与行业趋势报告演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-minimal-letterhead` | 带简约信头的信件文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-next-generation-os` | 操作系统概念展示演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-operating-calendar` | 年度与月度运营日历表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-photography-portfolio` | 摄影作品集演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-product-pitch` | 产品提案演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-product-strategy` | 产品战略演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-project-kickoff` | 项目启动与分工演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-project-tracker` | 任务、负责人、状态与时间跟踪表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-sales-pipeline` | 销售机会与阶段跟踪表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-state-of-art` | 艺术与创意方向展示演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-strategy-memorandum` | 战略选择与行动备忘录文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-system-design` | 系统架构、需求与组件设计文档 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-three-statement-forecast` | 财务三表联动预测表格 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `artifact-template-weekly-business-review` | 每周业务指标与行动复盘演示稿 | 模板缓存；先确认模板插件已启用，再按模板名和目标文件调用 |
| `review-agent` | 辅助代码审查的系统技能；本次未列入可调用目录 | 系统目录存在，但本次可调用目录未暴露；不手工强行启用 |
| `scientific-figure-making` | 按特定 matplotlib 风格制作可出版图件 | 位于 Claude Code 技能目录；在其宿主中按任务调用，不能假定 Codex 已加载 |

## 副本与共享支持包

- `nature-shared` 是 Nature 技能的内部共享资料，不单独调用；详见 Nature 手册。
- ECC 另有 **751** 个 `SKILL.md` 位于翻译文档、Pi、Kiro、Cursor、其他 Agent 示例等路径。它们是同一插件包附带的副本或其他宿主材料，本次不作为新增可用能力计数。
- 全部 1,208 个文件的相对位置和内容摘要哈希见 [磁盘核对表](../data/disk-skill-files.json)。按路径保留记录，不把名称相同的不同文件强行合并。

这 751 个文件按 frontmatter 名称归并后有 267 个名称，其中 264 个名称已出现在当前技能的源名称中。另有 3 个名称仅在这些其他宿主/示例路径出现，补充如下；名称匹配不是内容完全相同的证明。

| 额外名称 | 用途 | 使用方式 |
| --- | --- | --- |
| `ecc-conventions` | ECC 开发约定与 Conventional Commits 示例 | 作为其原宿主中的项目规则参考；不是当前 Codex 新入口 |
| `ecc-council` | Pi 宿主的四视角决策讨论流程 | 按 Pi 的安装与调用规则使用；当前 Codex 对应可用入口为 `ecc:council` |
| `project-guidelines-example` | 项目架构、开发、测试与部署指南模板 | 作为编写项目指南的示例，不当作独立执行能力 |

## 怎样回查原始说明

[结构化清单](../data/skills-inventory.json) 为每个入口记录了相对安装位置。将 `~` 替换为自己的用户主目录，即可找到对应 `SKILL.md`。不要把另一位使用者的绝对目录直接复制到自己电脑。

外部来源：[Nature Skills](https://github.com/Yuan1z0825/nature-skills)、[ECC](https://github.com/affaan-m/ECC)、[Superpowers](https://github.com/obra/superpowers)、[Anthropic Skills](https://github.com/anthropics/skills)。应用附带插件以安装版本的本地说明为准。

本目录只整理说明，不执行条目中的更新、发布、发消息、删除、资源申请或部署操作。
