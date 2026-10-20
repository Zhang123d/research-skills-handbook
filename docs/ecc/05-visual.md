# ECC · 第五章　前端、视觉与多媒体

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](04-quality.md) · [下一章](06-environment.md)

处理网页界面、视觉规范、动效、图像与视频工作流。

本章收录 **41** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

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

[返回 ECC 总目录](README.md)
