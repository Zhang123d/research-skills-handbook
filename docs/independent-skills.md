# 第五篇 · 独立技能

[返回全书目录](../README.md) · [使用方法](getting-started.md)

## scientific-figure-making：matplotlib 科研绘图

**用途：** 按该技能自带的科研图风格，用 matplotlib 绘制用于论文、幻灯片和报告的柱状图、趋势图、散点图、热力图和多面板图，并输出印刷或矢量格式。

**安装位置与宿主：** `~/.claude/skills/scientific-figure-making`。它是用户技能目录中的独立技能；当前 Codex 目录未列出该入口，不假定跨宿主自动加载。

**准备材料：** 实际数据、字段与单位、分组方式、目标图型、尺寸及 PDF/SVG/PNG 等输出要求。

**使用方式：** 在加载该技能的 Claude Code 环境中，按下列方式提出任务；也可以直接说明技能名称。

```text
请使用 scientific-figure-making，按已有科研绘图风格处理 results.csv。
请用 matplotlib 绘制分组柱状图，保留真实样本数与单位，输出 SVG、PDF 和绘图代码。
没有足够信息定义误差条时先指出，不自行补造。
```

**适用边界：** 需要 matplotlib 和相应依赖。它针对既定科研图样式，不用于交互式网页图表，也不自动替代统计设计。若在 Codex 中使用已安装的 Nature 工具集，可选择 `nature-figure` 并明确 Python 后端；两者是不同安装项。
