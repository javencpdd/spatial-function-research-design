# 课题研究任务计划

首轮限定一条受控直通道、净宽义务和一个 M20 Pro 配置。研究在版本化地图上组织按需复核，比较确认时间与验证成本，并共同检查漏检和危险误放行。

## 当前设计进展（2026-11-27）

| 范围 | 当前状态 |
| --- | --- |
| D01—D10 / E1—E5 | 限定模型、反例及实验设计完成；公式和实验协议继续适用。 |
| 设备基础 | 已完成 Thor、AOS、NOS、GOS 的只读登录和系统识别。M20 为 ARM64 / Ubuntu 20.04 / Foxy；Thor 为 T4000 / Ubuntu 24.04 / JetPack 7.2 系列。 |
| 相机与数据 | Thor 到 AOS 的两路 RTSP 描述请求成功，返回 H.264；不等于本轮完成持续解码、频率、同步或雷达/IMU采集。 |
| 具体部署路线 | 已形成“主机—算法—输入—产物—交接”的八步设计，见[实验步骤](experiments/m20-thor-workflow.md)。 |
| 研究程序与效果 | 统一算法实现、真实通道资料、误差和成本标定、导航任务适配、正式实验均待完成。 |

Thor 暂用无线，有线问题后续处理。本轮实验规划假设所需网络已连通，不把路由排查列为下一项任务；数据传输和时间资格仍须独立验证。设备详细记录及原件见 [Notion 平台笔记](https://app.notion.com/p/41280c1f022081068737f619a3e65c32)。

### 当前工作顺序

**现场线先完成 1—4；算法线同步完成 5—6；在真实回放汇合，再做 7—8 和对照实验。** 用户承担建图、定位、导航及现场操作，研究侧承担输入适配、义务、MSRP、验收、回放及评分。

<a id="research-delivery"></a>

## 下一阶段任务与完成条件

| 顺序 | 主机和具体任务 | 完成条件 | 状态 |
| --- | --- | --- | --- |
| 1 | GOS 用 Foxy rosbag2 采集；Thor 保存 RTSP | 短包能读回，真实话题/字段、原始时间、缺口、来源和作业编号明确。 | 下一项 |
| 2 | Thor 独立 Humble 容器验证 Lightning-LM 录包建图 | 冻结提交/配置，输出点云和轨迹；有独立尺度检查，容器适配有实测记录。 | 待输入与环境验证 |
| 3 | Thor Open3D 辅助分割，电脑 CloudCompare 人工确认 | M0/G0/T0、稳定 Cell/实体、净宽要求、观察位、独立参考与保持条件可追溯。 | 随建图推进 |
| 4 | Thor 将新点云转为变化候选和净宽证据 | 原件可复算；误差、覆盖、遮挡、时间和当前地图关联明确；不足部分保持未决。 | 待真实资料 |
| 5 | Thor 实现类型化影响、义务、验收、双源状态和用途 | 沿用 D01/D02/D07/D08 的规则，旧证据充分时直接验收，重复、冲突及失效可追溯。 | 可并行实现 |
| 6 | Thor 实现 MSRP CP-SAT 与完整成本贪心 | 同一动作域、验收器和预算；小域独立参照核对完整路线、联合见证、求解状态及多轮停止。 | 可并行实现 |
| 7 | GOS 任务适配 → NOS 导航 → AOS 运动 → 回执 | 地图坐标和任务接口核验，一次到站、采集、安全结束全过程可追溯；首轮可人工按计划执行并计成本。 | 待接口及执行验证 |
| 8 | Thor 回放验收、状态更新及用途重评 | 同一原目标上的观测—义务—计划—回执—验收—查询链完整；独立评分资料不泄露给算法。 | 待前述产物 |

逐步输入、输出和工具来源只在[实验步骤](experiments/m20-thor-workflow.md)维护；资料字段、独立参考及缺项处置见[通道资料规格](experiments/corridor-data-spec.md)。

## 预实验、正式实验与论文

预实验取得两份独立合格见证的可达条件、完整空间/时间支持、测量误差、路线成本和失败率。当前 `2-of-3` 模板不因缺设备而自动改成单源；独立人工供证须核验共因、可见时刻和成本，评分参考另存。

E2/E3 优先，E1/E4/E5支撑双源、恢复和任务用途；随后按[总体协议](experiments/protocol.md)比较“共同周期底线＋线索提前复核”和固定周期巡检。保留无初始告警、无变化、失败及未决，按独立组估计样本量并封存测试。方法/相关工作可并行撰写，效果结论等待数据。

首轮可用一个进程保存 S1—S8 的逻辑职责，SQLite 与原始制品目录支撑回放。多机服务、正式 Wire 发行及 E6 跨实现验证按其自身条件后续开展，不作为离线研究程序的前置要求。自动运动仍需验证本地安全与任务接口。正式契约状态继续以 [Notion 终审](https://app.notion.com/p/41480c1f02208179ab78d1e68a2f1bb5)为准。

## 已交付任务与范围

| 设计 | 正文与验收记录 |
| --- | --- |
| **D01—D03** 影响闭包、证据、完整路线 | [D01](design/impact-closure.md) · [D02](design/corridor-evidence.md) · [D03](design/msrp-model.md) · [验收 #1](https://github.com/javencpdd/spatial-function-research-design/issues/1) / [#2](https://github.com/javencpdd/spatial-function-research-design/issues/2) / [#3](https://github.com/javencpdd/spatial-function-research-design/issues/3) |
| **D04—D05** 实验协议与跨模块终审 | [实验协议](experiments/protocol.md) · [设计终审及三场景](design/review-baseline.md) · [验收 #4](https://github.com/javencpdd/spatial-function-research-design/issues/4) / [#5](https://github.com/javencpdd/spatial-function-research-design/issues/5) |
| **D06—D10** 安全观测、时空支持、联合保证、多轮与地图 | [D06](design/observation-bootstrap.md) · [D07](design/spatiotemporal-support.md) · [D08](design/joint-evidence-guarantee.md) · [D09](design/multiround-review-policy.md) · [D10](design/map-consumption.md) · [验收 #11](https://github.com/javencpdd/spatial-function-research-design/issues/11) |
| **E1/E4/E5** 领域实验设计 | [双源维护](experiments/dual-source-e1.md) · [恢复与重开](experiments/recovery-e4.md) · [条件可用性](experiments/availability-e5.md) · [验收 #6](https://github.com/javencpdd/spatial-function-research-design/issues/6) / [#7](https://github.com/javencpdd/spatial-function-research-design/issues/7) / [#8](https://github.com/javencpdd/spatial-function-research-design/issues/8) |
| **跨阶段复核** 输入、指标及失败边界 | [准备清单](experiments/readiness.md) · [验收 #9](https://github.com/javencpdd/spatial-function-research-design/issues/9) / [#10](https://github.com/javencpdd/spatial-function-research-design/issues/10) |
