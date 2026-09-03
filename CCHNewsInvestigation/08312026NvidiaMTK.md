
# 08/31/2026 [英伟达向联发科投资35亿美元](https://www.mediatek.com/zh-tw/press-room/nvidia-and-mediatek-deepen-long-standing-partnership-to-build-ai-edge-to-cloud-computing-platforms)  
## 新闻回顾  
NVIDIA 想把自己的 GPU、NVLink 互连、软件生态和机柜级 AI 工厂架构，借助联发科的定制芯片、SoC、先进封装与量产能力，扩展到更多“从云到边缘”的 AI 硬件市场。  
联发科将接入 NVIDIA 的 NVLink Fusion 平台，为超大规模云厂商、云服务商和前沿模型公司开发定制化的 XPU/AI 加速器，并将其接入 NVIDIA 的 NVLink 机柜级 AI 系统。  
双方会继续合作开发后续数代的 RTX Spark 和 DGX Spark 芯片与电脑平台，目标是把 NVIDIA GPU 整合进联发科设计的 SoC。  
在车用方面，联发科的 Dimensity Auto 平台会整合 NVIDIA 技术，为智能座舱提供 AI 能力和 RTX 图形能力，并可与 NVIDIA DRIVE AGX 协同工作。  
NVIDIA 将投资 35 亿美元认购联发科发行的海外可转换公司债（ECB）。  

## 技术分解 
### 什么是海外可转换公司债？  
可转换公司债：投资者先是债权人，获得利息和到期还本的权利；但若公司股价上涨到有利水平，也可按事先约定的转换价格，把债券换成公司股票。  

### 什么是NVLink Fusion 平台？  
NVLink Fusion = 让定制 AI 芯片接入 NVIDIA NVLink 高速互连、机柜和软件生态的“接口标准 + 系统方案”。   
例如，云厂商自研一颗训练/推理 ASIC，或联发科为客户设计定制 XPU。过去，它们需要自己解决芯片之间的高速互连、机柜拓扑、CPU-GPU/XPU 协作、HBM 整合、网络扩展及系统验证。  
NVLink Fusion 试图把其中的关键“scale-up”层交给 NVIDIA 的成熟体系处理。  

### 什么是XPU？它跟CPU/GPU有什么区别？  
XPU 不是像 CPU、GPU 那样定义严格的一种固定芯片类型。它通常是一个泛称：X 代表变量，指任何可承担特定计算任务的处理单元或加速器——可以是 CPU、GPU、NPU、TPU、FPGA，或为某个客户/模型专门定制的 AI ASIC。  

### 为什么英伟达不自己做XPU？  
英伟达不是不能自己做 XPU；更准确地说，它已经在做大量高度专用的 AI 计算芯片，只是通常把它们命名为 GPU、Grace CPU、DPU、网络交换芯片等。  
NVLink Fusion 中所说的“custom XPU”，特指由云厂商或 AI 公司按自身工作负载定义的定制 ASIC；  
英伟达选择不包办所有客户的定制计算核心，而是试图占据更高价值、更难替代的互连、机柜架构、软件和生态层。  

### 这样看的话，联发科是不是帮英伟达把低价值的事情做了？  
NVIDIA 没有把低价值工作“外包”给联发科；它是在把高复杂度、强客户定制、难以规模复制的工程风险交给联发科，同时把最容易形成标准、锁定生态并获得平台溢价的 NVLink、软件与机柜接口留在自己手里。  
这也是这则合作最值得继续追踪的地方：联发科最终会成为拥有客户与产品定义权的定制硅平台，还是 NVIDIA NVLink 生态中一位高技术含量、但议价权受限的实现伙伴？  

### RTX Spark 和 DGX Spark是什么？它跟英伟达的RTX 5090等个人消费显卡有什么区别？  
DGX Spark 是 NVIDIA 面向 AI 开发者的桌面级 AI 系统；  
RTX Spark 是面向 Windows 笔记本和小型桌面机的 AI PC 平台。它们的重点是把大容量统一内存、Arm CPU 与 Blackwell RTX GPU 封装成一台适合本地运行大模型/Agent 的完整电脑；  
而 RTX 5090 是一张装进传统 PC 的高性能消费级独立显卡，重点仍是游戏、图形创作和通用 GPU 加速。  
| 维度 | DGX Spark | RTX Spark | GeForce RTX 5090 |
|---|---|---|---|
| 产品形态 | NVIDIA 定义的完整桌面 AI 系统 | OEM 可做成笔记本或小型桌面机的平台 | 单张 PCIe 消费级独立显卡 |
| 核心芯片 | GB10 Grace Blackwell Superchip | Grace CPU + Blackwell RTX GPU 的 Spark Superchip | GB202 Blackwell GPU |
| CPU | 内置 20 核 Arm Grace CPU | 内置 20 核 Arm Grace CPU | 没有 CPU，依赖主机的 x86/Arm CPU |
| GPU | Blackwell GPU | 6,144 CUDA cores 的 Blackwell RTX GPU | 21,760 CUDA cores 的 Blackwell GPU |
| 内存结构 | 最高 128 GB 共享统一内存 | 最高 128 GB 共享统一内存 | 32 GB 独立 GDDR7 显存 |
| CPU–GPU 连接 | NVLink-C2C | NVLink-C2C | PCIe 5.0 x16 |
| 内存带宽 | 273 GB/s 系统统一内存带宽 | 约 300 GB/s 级别，实际因产品而异 | 1,792 GB/s GDDR7 显存带宽 |
| 功耗重点 | 整机级、约 140 W SoC | 笔记本/小型桌面功耗范围 | 575 W 级 GPU 功耗 |
| 主要定位 | 本地 LLM、AI 开发、原型和 Agent | 个人 AI、创作、轻薄 PC 与本地 Agent | 游戏、渲染、传统 GPU 计算和本地 AI |
| 操作系统 | DGX OS / Linux AI 软件栈 | Windows on Arm 方向 | Windows/Linux，通常为 x86 PC |  

总结：DGX Spark 与 RTX Spark 试图把“能装下大模型”带到桌面和笔记本；RTX 5090 则是在传统 PC 上把“能跑得快、能渲染、能打游戏”的单卡能力推到极致。

### 什么是Dimensity Auto 平台？什么是NVIDIA DRIVE AGX？
Dimensity Auto（天玑汽车） = 车里的“高性能智能座舱 + 连接中枢”，是联发科面向软件定义汽车的车载计算平台/产品组合   
NVIDIA DRIVE AGX = 更偏向 ADAS / 自动驾驶 / 车辆集中计算的“大脑”  
两者(只能座舱和自动驾驶)可以协作，而不是简单互相替代。联发科的新闻表述是：Dimensity Auto 可整合 NVIDIA 的 AI 与 RTX 图形能力，并与 NVIDIA DRIVE AGX 一同构成可扩展的车载计算架构。  
NVIDIA 与联发科在汽车领域的合作，实际上是在尝试把双方各自最强的部分拼起来  
NVIDIA：高性能 GPU / AI、CUDA、DRIVE 软件与自动驾驶平台  
联发科：低功耗 SoC、移动生态、通信连接、成本控制与大规模出货能力  

## 新闻分析  
对联发科意味着什么？  
1. 用较低的现金成本拿到大额资金  
2. 获得 NVIDIA 的长期“战略背书”  
3. 代价：潜在稀释与更强的生态依赖  
联发科不是免费拿钱。  
若未来转换成股票：会增加流通股数，原有股东会被稀释。  
若没有转换：联发科仍须支付利息，并在到期时偿还本金，除非选择再融资或提前处理。  
战略层面：联发科借 NVLink Fusion 切入数据中心客户，会获得机会，但也会更紧密地绑定 NVIDIA 的互连、系统与软件生态。  

对NVidia意味着什么？  
1. 以“债权 + 上行期权”绑定合作伙伴  
2. 推动 NVLink Fusion 成为定制芯片的“共同底座”  
3. 把合作伙伴的成功与自己的回报对齐  

|  |  | 值得追问的问题 |
|---|---|---|
| 算力 | NVLink Fusion、定制 XPU、HBM、机柜级 AI 基础设施 | 联发科首批产品的性能、能效、软件兼容性和量产时间是什么？ |
| 资本 | 39 亿美元海外可转债；NVIDIA 认购 35 亿美元 | 转换价、票息、期限、资金用途、潜在稀释和实际控制权影响是什么？ |
| 幻觉 | “定制 ASIC 可以无缝接入 NVIDIA 生态”的宏大叙事 | 有多少真实客户、订单和部署规模？客户是否能真正降低 TCO，还是只是获得新的供应商组合？ |

[返回目录](https://github.com/gpuwangge/NewsDeepDive/blob/main/README.md)
