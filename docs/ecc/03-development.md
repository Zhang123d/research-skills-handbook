# ECC · 第三章　编程、架构与代码协作

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](02-agents.md) · [下一章](04-quality.md)

阅读代码库、设计架构并按项目语言和技术栈开发。

本章收录 **45** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

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

[返回 ECC 总目录](README.md)
