# ECC · 第六章　环境、部署与网络

[返回全书目录](../../README.md) · [返回 ECC 总目录](README.md) · [上一章](05-visual.md) · [下一章](07-operations.md)

处理环境、部署和网络类任务；实际操作前仍需核对目标范围与依赖。

本章收录 **23** 个入口。表格给出调用名、用途与应准备的材料。

```text
请使用 $<表中的调用名称>。
材料：……；目标：……；边界：……；输出：……。
```

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

[返回 ECC 总目录](README.md)
