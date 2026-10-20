# ECC · 第七章　文档、业务与其他工作流

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](06-environment.md) · [下一章](08-commands.md)

选择文档维护、知识管理及特定业务领域的辅助流程。

本章收录 **84** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

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
| `$ecc:x-api` | X/Twitter API集成，用于发布推文、线程、读取时间线、搜索和分析 | 现有材料、预期目标与交付范围 |

[返回 ECC 总目录](README.md)
