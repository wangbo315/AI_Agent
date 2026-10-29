---
publish: true
created: 2026-10-21T11:00:23.651Z
modified: 2026-10-29T02:25:59.302Z
---

**NVIDIA DGX Spark** 是一款基于 **GB10 Grace Blackwell Superchip** 的紧凑型桌面 AI 超级计算机，专为本地大模型开发、微调与推理设计。

# 一、概述

### 1、核心规格（128GB 版为主，官方数据）

| 项目 | 参数 |
|------|------|
| **芯片** | NVIDIA GB10 Grace Blackwell Superchip（TSMC 3nm） |
| **CPU** | 20 核 Arm（10× Cortex-X925 + 10× Cortex-A725） |
| **GPU** | Blackwell 架构，**6144 CUDA Cores**，第5代 Tensor Cores（支持 FP4），第4代 RT Cores |
| **AI 算力** | 最高约 **1 PFLOP FP4**（含稀疏），约 1000 AI TOPS |
| **内存** | **128 GB** LPDDR5X 统一内存（CPU+GPU 共享），256-bit，带宽 **273 GB/s**（也有 64GB 版本） |
| **存储** | 1 TB 或 4 TB 自加密 NVMe M.2（Founders Edition 多为 4TB） |
| **网络** | ConnectX-7 Smart NIC（200 Gbps，支持多机互联）、1× 10 GbE RJ-45、Wi-Fi 7、蓝牙 5.4 |
| **接口** | 4× USB Type-C、1× HDMI 2.1a、支持多屏 |
| **视频** | 1× NVENC + 1× NVDEC |
| **操作系统** | NVIDIA DGX OS（基于 Ubuntu 的 Linux） |
| **电源** | 外部 240W 电源（GB10 TDP 约 140W） |
| **尺寸 / 重量** | 150 × 150 × 50.5 mm，约 1.2 kg |
| **模型支持** | 单机最高约 **200B 参数**（128GB 版，FP4 量化） |

### 配置与集群

- **单机**：64GB 或 128GB 两种统一内存配置（芯片与带宽相同）。
- **多机集群**（通过 ConnectX-7 互联）：
- 2 台可直连，内存池化（如 2×128GB = 256GB）
- 最多支持 4 台组成集群（最高 512GB）

### 其他要点

- 采用**统一内存架构**，无独立显存，数据无需在 CPU/GPU 内存间拷贝。
- 内存不可用户自行升级。
- 功耗低、体积小，适合桌面 7×24 运行本地 AI 智能体与大模型原型开发。
- 软件预装 NVIDIA AI 栈（CUDA、TensorRT-LLM、vLLM 等），可无缝对接数据中心/云端。

数据主要来自 NVIDIA 官方产品页与用户指南。具体 OEM 版本在存储、外观上可能有细微差异。如需某方面（如实际跑模型性能、与 RTX Spark 对比）的更细信息，可继续提问。
