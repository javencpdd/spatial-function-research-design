# 校园空间功能状态的按需复核与更新方法

研究在版本化地图上关联管理许可与现场证据，按事件影响生成验证义务，规划采证并更新状态，再判断指定机器人能否在任务时窗内使用空间。首轮采用受控直通道净宽、单个义务修订和一个机器人配置。实验比较义务驱动复核与固定周期巡检的确认时间及验证成本，并共同核查漏检和危险误放行。

D01—D10 的限定模型与 E1—E5 实验设计已经完成。近期工作是明确工具输出到研究输入的接口、实现离线算法，并准备首条真实测量链。完整算法和现场结果待验证。

| 查阅内容 | 入口 |
| --- | --- |
| 后续任务、分工与完成条件 | [课题研究任务计划](ROADMAP.md#research-delivery) |
| 工作流程、业务输入、现行方法及备选 | [研究模型基线](design/model-baseline.md#workflow) · [方法比较](design/model-baseline.md#method-options) |
| 实验、现场资料及工具 | [总体实验协议](experiments/protocol.md) · [通道资料规格](experiments/corridor-data-spec.md) · [准备清单与工具](experiments/readiness.md) |
| 可复算案例与设计决议 | [MSRP 案例](validation/msrp-cases.md) · [设计终审与全线复审](design/review-baseline.md) · [已交付设计索引](ROADMAP.md#已交付任务与范围) |
| 全局架构、对象归属与契约状态 | [Notion 研究主页](https://app.notion.com/p/41280c1f022081a68d6ae9a03edc2484) · [架构与契约任务](https://app.notion.com/p/41480c1f02208164b52beacba8d8374f) |

用户负责 Lite3 或 M20 Pro 的建图、定位和导航。研究侧消费地图、位姿、原始观测及任务回执，负责事件义务、复核规划、验收和状态判断。[工具复用及平台交接](experiments/readiness.md#tool-reuse)
