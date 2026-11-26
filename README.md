# 校园空间功能状态的按需复核与更新方法

研究在版本化地图上关联管理许可与现场证据，按事件影响生成验证义务，规划采证并更新状态，再判断指定机器人能否在任务时窗内使用空间。首轮采用受控直通道净宽、单个义务修订和一个机器人配置。实验比较义务驱动复核与固定周期巡检的确认时间及验证成本，并共同核查漏检和危险误放行。

D01—D10 限定模型及 E1—E5 实验设计已完成。2026-11-27 已完成 Thor 与 M20 Pro 三台主机的只读系统识别，现进入首条真实测量链和离线算法准备。传感器完整采集、Thor 建图适配、研究算法和实验效果仍待验证。

当前路线：GOS 录包 → Thor 离线建图 → 电脑人工复核与编号 → Thor 变化检测、义务生成及 MSRP → GOS 任务适配 → NOS/AOS 执行 → Thor 验收与状态更新。先完成受控通道回放，导航接口就绪后再接自动作业。

| 查阅内容 | 入口 |
| --- | --- |
| 在哪台主机运行什么、产物交给谁 | [M20 与 Thor 实验步骤](experiments/m20-thor-workflow.md) |
| 当前状态、下一项任务与完成条件 | [课题研究任务计划](ROADMAP.md#research-delivery) |
| 工作流程、业务输入、现行方法及备选 | [研究模型基线](design/model-baseline.md#workflow) · [方法比较](design/model-baseline.md#method-options) |
| 实验、现场资料及工具 | [总体实验协议](experiments/protocol.md) · [通道资料规格](experiments/corridor-data-spec.md) · [准备清单与工具](experiments/readiness.md) |
| 可复算案例与设计决议 | [MSRP 案例](validation/msrp-cases.md) · [设计终审与全线复审](design/review-baseline.md) · [已交付设计索引](ROADMAP.md#已交付任务与范围) |
| 全局架构、对象归属与契约状态 | [Notion 研究主页](https://app.notion.com/p/41280c1f022081a68d6ae9a03edc2484) · [架构与契约任务](https://app.notion.com/p/41480c1f02208164b52beacba8d8374f) |

首轮使用 M20 Pro 与 Thor T4000。用户负责建图、定位、导航和现场操作，研究侧负责输入适配、变化与证据处理、事件义务、MSRP、验收和评分。库和厂家算法可复用，领域规则及任务适配仍需实现。[工具与平台边界](experiments/readiness.md#tool-reuse)
