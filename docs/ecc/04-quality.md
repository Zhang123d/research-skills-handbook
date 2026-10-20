# ECC · 第四章　测试、安全与质量

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](03-development.md) · [下一章](05-visual.md)

以明确需求和证据检查正确性、安全性与交付质量。

本章收录 **43** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

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
| `$ecc:verification-loop` | Claude Code 会话的全面验证系统 | 代码目录、运行方式与验证目标 |
| `$ecc:windows-desktop-e2e` | 测试 Windows 原生桌面应用的完整交互流程 | 现有材料、预期目标与交付范围 |
| `$ecc:workspace-surface-audit` | 审计活跃仓库、MCP服务器、插件、连接器、环境表面和工具设置，然后推荐最高价值的ECC原生技能、钩子、代理和操作员工作流 | 现有材料、预期目标与交付范围 |

[返回 ECC 总目录](README.md)
