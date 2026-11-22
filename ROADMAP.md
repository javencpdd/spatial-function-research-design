# 课题研究任务计划

首轮研究范围为受控直通道净宽、一个验证义务修订和一个机器人配置。初始研究设计以提交 `7a8bc69` 为基线。项目笔记的架构与契约入口见 [Notion 研究主页](https://app.notion.com/p/41280c1f022081a68d6ae9a03edc2484)。

## 当前设计进展（2026-11-22）

D01—D10 已完成限定设计与纸面复核。E1—E5 已有实验方案，现场观测、误差界、独立参考、算法效果和样本规模待取得。[研究设计终审](design/review-baseline.md) · [实验准备清单](experiments/readiness.md)

### 当前工作顺序

落实工具输出与研究输入的约定后，**离线算法（4–5）和地图及现场资料（3）并行**，在真实数据回放（6）汇合。近期交付为输入清单与合成样例、统一离线算法、首条真实测量链。

<a id="research-delivery"></a>

## 从现有设计到论文结果的待办流程

| 阶段 | 交付与完成条件 |
| --- | --- |
| **1 · 主方法已确定** | A 联合约束规划为现行主线，B 贪心为快速备选及 E3 主要对照。C 任务与运动联合规划、D 概率主动复核按数据和实际需求评估。四条路线的来源、用途、边界和工作量见[方法比较](design/model-baseline.md#method-options)。 |
| **2 · 研究输入接口** | 在现有资料规格补齐采集清单、字段与单位映射、缺项处理及合成贯通例。地图/实体、管理记录、观测、证据、候选作业和回执均可追溯到原件、时间、来源和修订。预计产证与实际覆盖分别记录。[流程](design/model-baseline.md#workflow) · [资料规格](experiments/corridor-data-spec.md) |
| **3 · 地图与首批资料** | 整理一条通道的几何图、位姿和原始观测。人工校验关键分割、边界、编号和关系。取得能够对应同一地图修订及采集作业的独立尺寸/时钟、管理许可、物理保持和安全站位资料。[资料规格](experiments/corridor-data-spec.md) |
| **4 · 事件、义务、验收与状态** | 实现双轴状态和差异候选、类型化影响闭包、义务生成、证据验收、失效重评及五态用途查询。用案例核对通过、失败、未知、过期、冲突、同源和局部支持。旧证据充分时可直接验收。[模型基线](design/model-baseline.md) |
| **5 · MSRP 与多轮策略** | 实现 A/B 的完整路线、联合见证、时窗、预算和多轮反馈。用同一主实现回放二十类规划边界及 D09 四条过程，以独立小域参照核对成本、可行性、最优性范围、重派和停止。收到回执后用阶段 4 的验收规则。[案例](validation/msrp-cases.md) · [多轮策略](design/multiround-review-policy.md) |
| **6 · 真实数据回放与预实验** | 从原件复算净宽区间、保证覆盖及缺口，核验测量/配准误差、物理保持、来源独立性、路线时间和能耗。按当时可见顺序回放义务到用途判断，确认能否取得两份独立合格见证。根据独立参考和预实验估计正式实验规模。[准备清单](experiments/readiness.md) |
| **7 · 机器人作业与闭环** | 先验证一次到获准观测位、采集及到允许终点的作业，再接入义务、规划和验收。任务身份、地图版本、原始数据、结束回执及实耗一致可追溯。核对采集缺失、执行失败、取消、失联和输入失效。[平台交接](experiments/readiness.md#tool-reuse) · [MSRP §8](design/msrp-model.md) |
| **8 · 正式实验** | 预先锁定主要对照、参数、预算、停止与统计方案。E2/E3 优先，E1/E4/E5 验证双源、恢复和任务用途，整个流程对比固定周期巡检。使用同等硬约束和输入条件、独立评分，保留未决和失败。分别计事件内及完整监测期的代价，注明计量来源。[实验协议](experiments/protocol.md) |
| **9 · 论文与复现** | 每项主张对应公式、算法和可追溯结果。整理版本、参数、数据来源、运行入口及典型失败。正式实验完成前可并行撰写方法与相关工作。现场原件按其权限管理。 |

用户承担建图、定位、导航和现场操作。研究侧承担输入规范、数据处理、义务、规划、验收、回放和评分。初始地图可人工校验并作为各方法共用输入。运行中的人工干预单独记时和记结果，独立评分资料保留在评分侧。工作站优先承担离线研究，Thor 分工及环境依据集中维护在[平台资料](experiments/readiness.md#platform-layout)。

首轮原型可在一个进程内保留八项逻辑职责，以一个通道及一套机器人配置完成必要接入。按开题报告的学期安排，在明确接口和完成小规模预实验后估算工期。正式契约发布、E6 跨实现验证及生产部署按[架构终审条件](https://app.notion.com/p/41480c1f02208179ab78d1e68a2f1bb5)取证。

## 已交付任务与范围

| 设计 | 正文与验收记录 |
| --- | --- |
| **D01—D03** 影响闭包、证据、完整路线 | [D01](design/impact-closure.md) · [D02](design/corridor-evidence.md) · [D03](design/msrp-model.md) · [验收 #1](https://github.com/javencpdd/spatial-function-research-design/issues/1) / [#2](https://github.com/javencpdd/spatial-function-research-design/issues/2) / [#3](https://github.com/javencpdd/spatial-function-research-design/issues/3) |
| **D04—D05** 实验协议与跨模块终审 | [实验协议](experiments/protocol.md) · [设计终审及三场景](design/review-baseline.md) · [验收 #4](https://github.com/javencpdd/spatial-function-research-design/issues/4) / [#5](https://github.com/javencpdd/spatial-function-research-design/issues/5) |
| **D06—D10** 安全观测、时空支持、联合保证、多轮与地图 | [D06](design/observation-bootstrap.md) · [D07](design/spatiotemporal-support.md) · [D08](design/joint-evidence-guarantee.md) · [D09](design/multiround-review-policy.md) · [D10](design/map-consumption.md) · [验收 #11](https://github.com/javencpdd/spatial-function-research-design/issues/11) |
| **E1/E4/E5** 领域实验设计 | [双源维护](experiments/dual-source-e1.md) · [恢复与重开](experiments/recovery-e4.md) · [条件可用性](experiments/availability-e5.md) · [验收 #6](https://github.com/javencpdd/spatial-function-research-design/issues/6) / [#7](https://github.com/javencpdd/spatial-function-research-design/issues/7) / [#8](https://github.com/javencpdd/spatial-function-research-design/issues/8) |
| **跨阶段复核** 输入、指标及失败边界 | [准备清单](experiments/readiness.md) · [验收 #9](https://github.com/javencpdd/spatial-function-research-design/issues/9) / [#10](https://github.com/javencpdd/spatial-function-research-design/issues/10) |

研究设计、实验方案及可公开样例按已确认的发布约定维护。历史任务计划和逐轮交付可查阅[整理前版本](https://github.com/javencpdd/spatial-function-research-design/blob/d10416453e63aa492dacdf3d44f05eca204865fc/ROADMAP.md)及对应任务。
