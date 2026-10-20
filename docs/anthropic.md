# 第三篇 · Anthropic Skills：文档、设计与开发

[返回全书目录](../README.md) · [使用方法](getting-started.md)

本篇收录自行安装在用户技能目录的 **19 个 Anthropic 技能**，不是 Codex 自带的文档运行时。根据文件类型或任务选择一项即可，不必把同类流程全部串联执行。

## 本篇目录

- [第一章　办公文件与协作文档（6）](#chapter-1)
- [第二章　视觉设计与网页材料（7）](#chapter-2)
- [第三章　开发、学习与技能维护（6）](#chapter-3)

<a id="chapter-1"></a>

## 第一章　办公文件与协作文档

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$anthropic-doc-coauthoring` | 协作组织文档、技术规格与决策材料 | 读者、文档目标、已有材料和大纲 |
| `$anthropic-docx` | 创建、读取和修改 Word 文档与模板 | Word 文件或模板、修改位置与版式要求 |
| `$anthropic-internal-comms` | 起草状态报告、公告和内部沟通材料 | 受众、事实要点、语气和沟通类型 |
| `$anthropic-pdf` | 提取、合并、拆分、创建和处理 PDF | PDF 文件、页码与提取/修改目标 |
| `$anthropic-pptx` | 创建、读取和修改 PowerPoint 演示文件 | 演示主题/源 PPTX、听众与模板要求 |
| `$anthropic-xlsx` | 创建、修改与分析电子表格和公式 | 表格文件、目标列/公式与输出要求 |

<a id="chapter-2"></a>

## 第二章　视觉设计与网页材料

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$anthropic-algorithmic-art` | 用 p5.js 和可控随机性制作生成艺术 | 画面主题、交互方式、尺寸与随机种子要求 |
| `$anthropic-brand-guidelines` | 应用 Anthropic 品牌配色与字体约定 | 待设计制品、品牌适用范围与格式 |
| `$anthropic-canvas-design` | 制作静态海报与 PNG/PDF 视觉设计 | 海报主题、文字素材、尺寸与导出格式 |
| `$anthropic-frontend-design` | 设计具有明确视觉方向的前端界面 | 界面需求、参考风格、组件和技术栈 |
| `$anthropic-slack-gif-creator` | 生成适合 Slack 使用的动画 GIF | 动画内容、尺寸、时长与大小限制 |
| `$anthropic-theme-factory` | 为文档、幻灯片和网页应用视觉主题 | 目标制品、主题选择或品牌参考 |
| `$anthropic-web-artifacts-builder` | 构建带状态与组件的交互网页材料 | 网页功能、页面流程与交互需求 |

<a id="chapter-3"></a>

## 第三章　开发、学习与技能维护

| 调用名称 | 用途 | 使用时提供 |
| --- | --- | --- |
| `$anthropic-academy-guide` | 根据 Claude 使用问题匹配官方学习课程 | Claude 使用问题、已有基础与学习目标 |
| `$anthropic-claude-api` | 查阅 Claude API、SDK、工具调用和模型参数 | 代码片段、SDK/模型标识与接口问题 |
| `$anthropic-discernment-nudge` | 提醒核对建议或草稿中的事实与行动依据 | 待采用的建议/草稿与需要核查的依据 |
| `$anthropic-mcp-builder` | 构建连接外部服务的 MCP 服务器 | 外部 API 文档、权限范围和服务语言 |
| `$anthropic-skill-creator` | 创建、改进技能并设计效果评估 | 目标工作流、示例任务和评估标准 |
| `$anthropic-webapp-testing` | 用 Playwright 检查本地网页交互与日志 | 网页地址/项目、操作路径与预期结果 |

## 使用示例

```text
请使用 $anthropic-pptx，把我提供的阅读笔记整理成 10 分钟中文汇报。
请保留证据来源，加入讲者备注，输出可打开的 PPTX；缺少工具时先说明。
```

来源：[Anthropic Skills](https://github.com/anthropics/skills)。文件处理、API、MCP 和网页测试等路线的依赖不同，按当前任务核对。
