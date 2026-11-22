# 通道研究设计回顾与 E1—E5 实验准备清单

首轮限定受控直通道、单个义务修订和一个机器人配置。实际资料按[通道资料规格](corridor-data-spec.md)收件。设计决议和当前任务分别见[研究设计终审](../design/review-baseline.md)与[研究任务计划](../ROADMAP.md#当前工作顺序)。

## 1. 沿同一通道复核设计

### 本轮修订与验收反例

- **规划可行性。** 一条有完整联合见证及终点的路线可证明可行，域内最优性另证。覆盖声明域的共同反证才可排除全部候选。[D03 案例 7、12、13](../validation/msrp-cases.md)
- **恢复时序。** 原查询只读当时的验收及投影。后继恢复查询仍需支持其完整占用。[D05 场景 A、B](../design/review-baseline.md)
- **短暂错误放行。** 固定网格统计每次查询，完整观察窗另记组内任一次危险允许。暴露记录缺失时给出组级可能范围。[E5 §6.1、案例 23](availability-e5.md)
- **地图更正。** 完整作业先传播再裁剪，原覆盖缩短后按原义务核验第二份见证。[D10 地图消费](../design/map-consumption.md)

### 从总目标检验闭环

从独立监测时段入组，保留无初始线索、迟到线索和无变化时段，按原谓词、范围和窗口评分。分别记录事件确认期与完整值守期的时间、能耗和外部工作量。补证沿用原截止和资源账，未决及失败保留在评价中。[实验协议 §2–4](protocol.md) · [D09 多轮策略](../design/multiround-review-policy.md)

## 2. 各实验所需独立参考

首轮采用同一条受控直通道的明确地图版本、禁令、瓶颈和清障过程。先建立可审阅的独立参考，再决定这一场景能支持哪些实验。以下各行是一种材料需求，当前均待提供实际版本。

| 对象 | 要取得的输入与独立依据 | 配对与保留项 |
| --- | --- | --- |
| D10 地图消费 | 原始几何/完整覆盖、坐标单位及边界、变换与公共误差、更正可见时刻、实体/功能对应和版本兼容；独立核验迁移后的范围与实际净宽。 | 原目标/要求/时窗不变，原采集链去重；地图拆分和派生文件不增样本量，共同更正同等可见。 |
| D06 观测启动 | 事前核验请求/授权、固定周期和相位、安全观察站及支持窗口、到达/观测/结束路线、来源/遮挡与槽位依据、预留时间及实际缺席、替代来源与转交记录。 | 同一监测期和信息可得性；初始依据不使用待测结果，保留无告警及不可观测目标，底线/提前/待机/失败能耗不重复。 |
| 共同场景及 E1 | 图、坐标与要求修订，独立记录监测时段、真实起点及结束、无变化时长、管理指令有效和可见时刻、参考尺寸及来源。另存各方法当时可见线索。 | 相同世界过程配对，区分世界状态和当时能证明的结论，保留未发现的变化。 |
| E2 影响范围 | 事件、目标目录、设施依赖和干预前后参考，每个目标记录应否重评及理由，含无影响和未知边。 | 固定粒度。两人屏蔽算法输出独立标注，分歧交复核并保留未决集合。 |
| E3 路线及总体成本 | 已有证据、见证共因、完整路线、耗时/电量、剩余复核机会、等待期限和每次重派依据。另保留无变化时段、失败重试和共用路线的耗能记录。 | 小域用独立枚举核对最优性。总体用相同资源和验收规则，分别核算事件确认期与整个监测时段。 |
| E4 恢复与重开 | 独立恢复/复发时刻或区间，持续义务、撤销/失效事实可见时刻、S4 提交与 S3 可读时刻，保留不修复及无关单元。 | 同一真实过程配对。恢复、重开、投影传播分别计时。预置的无恢复负例进入相应错误挑战层。 |
| E5 条件可用性 | 固定机器人、载荷、路径、允许调整、占用及退出，独立几何包络与可执行性核查，合成层封存风险联合表或取得适用的风险标定，保存每次正向声明。 | 固定查询网格与挑战观察窗。条件允许的整个执行范围接受评分。风险参考未决时保留标签范围。 |

给每份材料记录场景/采集作业、原始来源、适用修订、单位、有效时间、可见时间、用途、适用域、共享误差、独立组、分集、双标分歧、证据位置与状态。对同一记录的裁剪、重算及相关故障变体统一追溯。按共享原记录或会影响结论的共同误差连接成组，先分标定/预实验与封存测试，再处理派生样本。同一公共地图可作为固定条件，其共享测绘偏差若会影响结论则纳入分组。独立组不足时，缩小可报告的范围并记录理由。

## 3. 参数与取得顺序

| 参数与适用域 | 来源和取得方法 | 缺项对结论的影响 |
| --- | --- | --- |
| 地图锚定、净宽阈值及尺度（m） | 绑定要求、测量高度带、坐标变换，独立复测控制点、断面与窄障碍。按距离、材质、遮挡和批次取得 D07 的内外包络、完整覆盖及合成误差依据。 | 仅保留已支持子域，未知体积进入外包络，跨阈值测量记未决。 |
| 时间（s）、受控保持及新鲜度 | 按 D07 对齐采样、接收、提交、可读以及物理保持起止，取得各自误差；核查入口/操作约束及破坏事实。硬过期单独记录，不能由复测结果相同拟合出保持保证。 | 先收缩至物理保持的保证区间；覆盖空白、开放环境变化未排除或结束操作超窗时，当前正向用途待定。 |
| 证据独立性及动作效果 | 对距离扫描、深度测量和独立复测保留采集链、标定/配准关系、来源替代与共因故障试例。预实验记录动作产证资格、耗时（s）、能耗（Wh）、结束与验收延迟。 | 未证独立的组合只进入可能分配。资源有区间时按相应预算与最坏允许值核验。 |
| 证据联合保证 | 按 [D08 联合可靠性](../design/joint-evidence-guarantee.md) 区分实际状态界、参数区间与实验效果；保留误差变量、公共依赖、完整域和失效记录。统计接入另核验实际取数设计、有限家族、总预算及选择/停止规则。 | 未知前提不当零误差，不借样本最大残差、重复帧或两槽宣称高置信；共同主张缺预算时不报告整体置信。 |
| 对照与任务 | 冻结周期、相位、搜索预算、网格、候选域、机器人包络、载荷、限速能力、占用时间、任务风险预算和联合/保守风险界适用域。 | 对照欠缺相同资格时不能支持公平效率比较。风险或限速能力无证时保留待定。 |
| 主张数值 | 任务需求给出可解释的最小改善、允许退化、最低完成率、风险上限、未知参考上限和可接受置信宽度。预实验估计可测性、配对变异、稀有层频率及预算。 | 各数值附单位、来源及适用对象。门槛由任务用途确定，测试集封存前固定。 |

## 4. 置信预算与独立组数

每个用于判定主张的单侧界登记“实验、对照、端点及方向、计量单位、分母及资格层、组内汇总、最低改善或容忍值、区间方法、尾部预算、所需组数”。E1、E4、E5 各有七项界。E2 登记漏传播改善、精确率退化及用于主张的空输出限制。E3 登记路线时长及正确确认、漏检、危险资格。与固定周期巡检的总体比较另登记确认延迟和能耗两条改善路径使用的界，以及正确确认率、漏检和危险的绝对/相对限制。只有目标人群、对照、方向、统计量及区间均相同的界才可共用。同一置信界支撑多个判据时只分配一次，完整清单决定总项数 M。[总体协议 §4–8](protocol.md)

沿用效应检验家族的 0.05 总预算与单侧等额分配。任务风险阈值是业务概率，风险标定的覆盖保证、独立参考的置信保证与效应检验分别登记。若要联合声称三类保证同时成立，则在测试前为联合声明分配预算。按数据选择候选方案时，另查所用风险界能否覆盖该选择过程。[E5 §3.2](availability-e5.md) · [NIST 同时覆盖不等式](https://www.itl.nist.gov/div898/handbook/prc/section4/prc473.htm)

1. 在独立预实验组估计配对差、资格层出现率、组内相关、失败与未决比例。按每项研究主张预置有实际依据的备择效应，改善量应超过判定门槛。记录效应、波动与未决率的敏感性范围。
2. 对候选组数重现固定权重、配对、缺失与置信界，记录**整项主张同时满足全部必要判据**的比例。总体主张按原协议的两条可选改善路径及共同资格判定。功效目标沿用 0.80，报告模拟次数、随机种子及模拟误差。若拟联合宣称所有主张，再计算联合通过概率。逐端点功效不能直接当作联合功效。
3. 对独立同分布危险挑战组，零次错误时，单侧预算 a、风险上限 r 所需的乐观组数下限为 ceil(log(a)/log(1−r))。以 r=1% 演示，a=0.05 需 299 组，a=0.005 需 528 组。两者只是算例。出现错误、固定分层混合或标签未决时，按封存的抽样设计求保守上界。[NIST 精确二项界](https://www.itl.nist.gov/div898/software/dataplot/refman2/auxillar/exacbino.htm)
4. 在每个资格层核对可获得的独立组数、所需区间宽度和联合功效。多种挑战能否共用一组取决于入组条件和依赖记录。互斥层分别配额，再按场景出现率、预计损耗和可用资源折算总招募量。若可获得的独立组不足，优先报告相应范围或探索性结果，记录不能支持的主张。

## 5. 就绪结论与复查入口

| 阶段 | 所需证据与状态 |
| --- | --- |
| 限定模型与对照设计 | D01—D10、E1—E5 的设计及纸面复核已交付。记录与历史版本见[交付索引](../ROADMAP.md#已交付任务与范围)。 |
| 单场景参考与标定 | 待取得可关联的尺寸、时钟、管理许可、实际资料和独立参考，并核验共享误差及适用域。 |
| 预实验与样本规划 | 待取得配对变异、各类场景的出现率、风险与效果门槛、功效和资源估算。 |
| 封存测试 | 待固定协议、数据与标签版本、独立组、预算账和判定方法。 |

改地图身份或依赖时重查 D01 作用域与 D02 重锚定。改见证、时效或资源时重查 D02 验收、D03 完整路线及 E4 恢复时钟。改允许域、读取时点或评分分母时重查 D05 原查询与 E5 短暂错误。记录受影响用例、预期及理由。

<a id="tool-reuse"></a>

## 6. S1—S8 工具复用核验（2026-11-22）

按 [S1—S8 现行职责](https://app.notion.com/p/41280c1f02208119a944debf8b5ca294)逐项核查官方文档、代码、许可证和发布文件。用户明确本轮主要判据为**工具能力能否覆盖目标、源码/软件/权重能否取得和使用、部署环境是否有支持路径**。暂无现场数据时，实际精度、时延和闭环效果留给后续实验，当前无需把每个工具运行一遍。用户负责 Lite3 或 M20 Pro 的建图、定位和导航；研究侧消费地图、位姿、测量和执行结果。已知平台及适配边界见 §6.12。

**可行性判断**　首轮受控通道所需的数据读写、几何计算、图计算、约束求解和事务存储均有公开可获取的实现，选型层面支持继续研究。语义模型有公开源码和权重入口，但其输出、输入前提及 Thor 兼容性须按 §6.11–6.12 区分。S3/S4/S5/S7 的证据资格、义务、MSRP 和用途规则仍需编写，这部分属于研究方法本身。整体工具与接口尚不能标为全部齐备。研究原型可在一个进程内保留八项逻辑职责，不要求八套服务。

### 6.1 S1 多源接入与回放

- **现成能力**　rosbag2 负责 ROS 2 消息录制与回放，MCAP Python 库负责文件读写。Rosbags 可独立解析 ROS 1/2 记录，其官方说明允许在未安装 ROS 的研究机上使用。输入为传感器消息、消息定义和时间戳，输出为可读取的观测序列。[rosbag2](https://github.com/ros2/rosbag2)、[MCAP](https://mcap.dev/docs/python/)、[Rosbags](https://ternaris.gitlab.io/rosbags/)
- **需要补写**　将平台消息、维修记录和许可表映射为研究对象，保存原始采样时点、坐标、来源、修订和幂等键，处理缺项和隔离。MCAP 文件格式本身无法核实传感器授权、时钟误差或测量质量。
- **扩展范围**　IFC 解析和 GIS 格式转换有 IfcOpenShell、GDAL。校园业务系统的权限及字段仍须按实际来源适配。首轮可从一份许可表和一组带尺度观测开始。[IfcOpenShell](https://docs.ifcopenshell.org/)、[GDAL](https://gdal.org/en/stable/)

### 6.2 S2 地图、坐标、空间关联与版本

- **现成能力**　用户负责建图与定位。研究侧可用 pyproj 转换已定义的 CRS，Shapely 求二维区域相交、包含与距离，NetworkX 保存空间及功能依赖。需要点云预处理、配准或空间距离计算时可调用 Open3D。输入为地图及变换、区域和关联，输出为可查询几何和依赖。[pyproj Transformer](https://pyproj4.github.io/pyproj/stable/api/transformer.html)、[Shapely](https://shapely.readthedocs.io/en/stable/manual.html)、[Open3D](https://www.open3d.org/docs/release/tutorial/geometry/pointcloud.html)
- **需要补写**　稳定身份、不可变地图修订、CellLineage、依赖关系的含义、旧证据重锚定和误差传播。CRS 转换和 ICP 各有数值算法，但其输出仍须具备适用范围和误差依据。[地图消费实例](../design/map-consumption.md)
- **适用边界**　Shapely 的几何运算忽略高度。受控通道可在已核实的高度带上使用二维几何，完整三维净空和遮挡需由三维数据及相应模型支持。pyproj 的坐标变换也须核查轴序及实际坐标定义。[Shapely 维度说明](https://shapely.readthedocs.io/en/stable/manual.html#geometric-objects)、[pyproj 轴序与精度说明](https://pyproj4.github.io/pyproj/stable/api/transformer.html)

### 6.3 S3 观测、证据与双源状态

- **现成能力**　Open3D 提供点云距离、聚类、平面分割与配准，可从已对齐的测量中构建几何变化线索。jsonschema 检查证据记录的字段、类型和结构。已核查 Open3D v0.20.0 有公开发布及当前 Python 安装包。[Open3D 点云处理](https://www.open3d.org/docs/release/tutorial/geometry/pointcloud.html)、[v0.20.0 发布](https://github.com/isl-org/Open3D/releases/tag/v0.20.0)、[jsonschema](https://python-jsonschema.readthedocs.io/en/stable/validate/)
- **需要补写**　APCM 管理许可与物理状态的协调、观测到 Evidence 的资格检查、证据时效及冲突、功能状态投影和原因链。几何变化线索进入候选复核，再结合要求及合格测量确定功能状态。
- **主要困难**　阈值跨越、遮挡、定位漂移和共享标定影响实际证据。首轮需取得有尺度的观测及独立参考，核验宽度误差、整个范围的支持和保守保持条件。视觉类别检测可补充线索，净宽验收需有相应尺度和误差依据。[证据判据](../design/corridor-evidence.md)、[联合可靠性](../design/joint-evidence-guarantee.md)

### 6.4 S4 事件、验证义务与验收

- **现成能力**　NetworkX 提供有向图遍历和可达集。SQLite 支持事务、唯一键和持久记录，jsonschema 提供输入结构检查，可支撑单机研究状态机。[NetworkX 遍历](https://networkx.org/documentation/stable/reference/algorithms/traversal.html)、[SQLite 事务](https://www.sqlite.org/lang_transaction.html)
- **需要补写**　事件的有类型确定/可能影响闭包，复核清单的要求、范围、时窗和来源限制，验收谓词，Task 与义务的生命周期及恢复重开。通用图遍历需要消费这些领域规则。[影响闭包](../design/impact-closure.md)、[验收判据](../design/corridor-evidence.md)
- **可行性判断**　基础图算法与事务机制已有实现。义务和验收规则属于主要研究工作，应先用现有反例验证。一个原始记录经两种算法重算后的来源限制，须由研究模型表达并检查。

### 6.5 S5 最小充分复核规划（MSRP）

- **现成能力**　OR-Tools CP-SAT 提供整数、布尔和逻辑约束求解，支持可行、最优、无解及超时未知等求解状态。NetworkX 可计算已给定通行图上的路径。输入为有限动作/时间域、证据资格和资源，输出为所编码模型的解及求解状态。[CP-SAT 官方文档](https://developers.google.com/optimization/cp/cp_solver)
- **需要补写**　将论文的完整路线和联合见证分配编码为模型，构建确定及乐观资格视图，处理旧证据复用、共享来源、实际验收时效、结束路线和多轮决策。整数化须保守保持时窗、预算与误差语义。词典序目标可分阶段求解，上一阶段最优性未证时须保留该缺口。[MSRP 模型](../design/msrp-model.md)、[多轮策略](../design/multiround-review-policy.md)
- **主要困难**　CP-SAT 的 INFEASIBLE 只证明所编码模型无解。研究侧需同时举证候选域覆盖及资格上界。原生 UNKNOWN、模型错误和研究中的资格未知也需分别保留原因。大候选域的求解时限、预测成本和实耗偏差需对照实验，当前没有规模性能结果。

### 6.6 S6 机器人任务执行

- **分工**　用户负责 Lite3 或 M20 Pro 的建图、定位和导航代码。研究侧生成复核目标、观测配置和约束，通过适配层提交任务并读取结果。
- **可借鉴的公开接口**　Nav2 Simple Commander 已有目标点导航、取消、反馈与结束查询的调用方式。云深处公开资源列出了对应型号的运控部署和建图代码。具体采用何种平台接口由用户代码决定。[Nav2 调用接口](https://docs.nav2.org/jazzy/configuration_and_development/simple_commander_api/simple_commander_api/)、[云深处官方资源](https://developer.deeprobotics.cn/docs/)
- **需要补写并验收**　研究计划到导航/观测任务的适配、精确任务身份与修订、实际结束和采证回执、资源记录、取消及失联处理。公开 robotserver_sdk 文档关联 X30 Pro，Lite3 MotionSDK 则提供关节控制；这些资料尚无法证明本项目已有可调用的导航目标接口。[RobotServer 适用说明](https://github.com/DeepRoboticsLab/robotserver_sdk/blob/main/README.zh-CN.md)、[Lite3 MotionSDK](https://github.com/DeepRoboticsLab/Lite3_MotionSDK)

### 6.7 S7 任务条件可用性与导航约束

- **现成能力**　Shapely 和 NetworkX 可计算平面路径与区域关系，SQLite 可保存一致的单机快照。用户的导航器消费研究侧给出的允许范围和约束；若采用 Nav2，其 KeepoutFilter 提供禁入区实现，可作为一种接入方式。[Nav2 禁入区](https://docs.nav2.org/rolling/tutorials/general_tutorials/navigation2_with_keepout_filter/navigation2_with_keepout_filter/)
- **需要补写**　将管理许可、S3 状态、S4 义务、机器人能力、扫掠范围和整个任务时窗组合为禁止、受阻、待定、有条件可用或可用，保存理由和版本。研究侧还需验证导航器已应用当次约束，以及更正到达后旧决定如何失效。[任务可用性实验](availability-e5.md)
- **主要困难**　导航器可以找到一条几何路径，任务判定仍需完整证据与时窗支持。两者通过明确接口衔接；路径可执行性及停止语义需随平台实测。

### 6.8 S8 制品、策略、存储与审计

- **现成能力**　SQLite 提供单机事务，文件存储与标准 SHA-256 提供制品读取及摘要计算，已有 rfc8785、jsonschema 依赖可用于 JCS 和结构校验。扩大策略管理时可评估 OPA，其 Rego 引擎执行显式提供的策略。[SQLite ACID](https://www.sqlite.org/transactional.html)、[JCS 实现](https://pypi.org/project/rfc8785/)、[OPA](https://www.openpolicyagent.org/docs)
- **需要补写**　制品与策略版本索引、适用范围、可信读取、访问策略、撤销与完整审计关联。SHA-256 可检测字节不一致，可信来源和授权须另有依据。单库事务可支持单机研究，跨服务的一致快照、真实 ACL 和 Owner 交接仍需集成验证。
- **本地基础**　现有契约包的历史结果记录为 275/275 项匹配，含 JCS、引用策略、本地 Owner 事务与 loopback 服务。此处引用已有记录，本轮另查了依赖可导入性及基础库行为。真实机器人、校园数据和外部 Consumer 的采纳仍待取证。

### 6.9 版本、源码获取与已有调用记录

官方仓库元数据显示，本次核查的 NetworkX、OR-Tools、Open3D、Shapely、pyproj、jsonschema、rosbag2 和 Nav2 均未归档，并有 2026 年更新。维护记录支持它们作为候选组件继续评估，版本兼容与具体功能以选定发行版为准。

| 组件 | 本轮核查的版本或接口 | 源码、许可与获取方式 |
| --- | --- | --- |
| NetworkX | 3.7，Python ≥3.12，排除 3.14.1 | [源码 / BSD-3-Clause](https://github.com/networkx/networkx)、[安装包与源码包](https://pypi.org/project/networkx/3.7/#files) |
| OR-Tools | 9.15.6755，Python ≥3.9；CP-SAT 不要求商业求解器 | [源码 / Apache-2.0](https://github.com/google/or-tools)、[安装包](https://pypi.org/project/ortools/9.15.6755/#files) |
| Shapely / pyproj | 2.2.0 / 3.8.0，分别要求 Python ≥3.11 / ≥3.12 | [Shapely 源码 / BSD-3-Clause](https://github.com/shapely/shapely)、[pyproj 源码 / MIT](https://github.com/pyproj4/pyproj)，均有 PyPI 安装包及源码包 |
| Open3D | 0.20.0；在线 release 教程仍显示 0.19.0，按实际发行版锁定 | [源码 / MIT](https://github.com/isl-org/Open3D)、[安装包](https://pypi.org/project/open3d/0.20.0/#files) |
| MCAP / Rosbags | 1.6.0 / 0.11.10，分别要求 Python ≥3.7 / ≥3.10 | [MCAP 源码 / MIT](https://github.com/foxglove/mcap)、[Rosbags 源码 / Apache-2.0](https://gitlab.com/ternaris/rosbags)，均有 PyPI 安装包及源码包 |
| jsonschema / rfc8785 | 4.26.0 / 0.1.4，分别要求 Python ≥3.10 / ≥3.8 | [jsonschema 源码 / MIT](https://github.com/python-jsonschema/jsonschema)、[rfc8785 源码 / Apache-2.0](https://github.com/trailofbits/rfc8785.py)，均有 PyPI 安装包及源码包 |
| SQLite / Python 标准库 | sqlite3、csv、json、uuid、hashlib；SQLite 的具体版本随 Python 构建记录 | [SQLite 源码与工具](https://www.sqlite.org/download.html)，public domain；[CPython 源码](https://github.com/python/cpython)，PSF License |
| rosbag2 / Nav2 | 仅在采用相应 ROS 2 环境时使用，随 ROS 发行版锁定 | [rosbag2 源码 / Apache-2.0](https://github.com/ros2/rosbag2)、[Nav2 源码](https://github.com/ros-navigation/navigation2)；Nav2 各包含 Apache/BSD/LGPL 等许可，按实际选用包核对 |

本轮另核对 PyPI 发行文件。OR-Tools、Shapely、pyproj 和 Open3D 的上述版本均提供 **CPython 3.12、Linux x86-64 与 aarch64** 安装包；NetworkX、MCAP、Rosbags、jsonschema 和 rfc8785 提供通用 Python wheel。该事实确认顶层包可获取；依赖解析、Open3D 的机器学习算子以及 GPU 支持需另外匹配。文件名、官方地址、SHA-256 和源码检查范围保存在[获取记录](../validation/tool-acquisition.json)。

本机检查采用 Windows x86-64、Python 3.14.5。原环境已有 NumPy、SQLite，以及工作区中的 jsonschema 4.26.0 和 rfc8785 0.1.4。本轮在项目隔离目录安装了表中的 NetworkX、OR-Tools、Shapely、pyproj 和 MCAP，连同 NumPy 2.5.5 等解析依赖，完成六组最小调用。

| 调用核验 | 合成输入与预期 | 本次结果 |
| --- | --- | --- |
| 图遍历 | Event → Cell → Width → Passage，并设置回边及一个无关节点 | 可达集含三个目标，环遍历结束，无关节点被排除 |
| 空间覆盖 | 4 m 原域、`[0.02,3.98]` m 中段、另一份完整覆盖；另设仅高度变化的线段 | 中段未覆盖全域、缺失平面面积为 0.04 m²，完整覆盖成立；高度变化被二维长度忽略 |
| CRS 转换 | 经纬度按明确轴序转投影坐标再回转 | 往返最大误差约 1.42×10⁻¹⁴ 度；该值只度量这次数值回转 |
| 求解器 | 三份候选见证至少取二，两份同源至多取一，新增独立见证成本为 4 | 选择旧完整见证与新增独立见证，目标值 4，OPTIMAL；禁用独立见证得 INFEASIBLE；求解时限为零得 UNKNOWN |
| 数据读写及结构 | MCAP 写入再读出一条 JSON 观测，记录两种时间；另给一个类型错误记录 | 观测和两个时间保留，错误字段类型被 jsonschema 拒绝 |
| 事务及摘要 | JCS 规范化后计算 SHA-256，SQLite 分别回滚与提交记录 | 回滚后记录数为零，提交的摘要可原样读回 |

六组已有调用均符合预期，范围为工作站上的基础库和合成输入；此前八个串联场景的范围见[模型基线](../design/model-baseline.md#workflow)。本轮 Open3D 0.20.0 与 Rosbags 0.11.10 已在工作区独立目录完成下载及安装，未据此宣称完成点云、ROS 记录或现场数据验证。用户明确本轮以能力、获取方式与环境分析为主，未继续逐工具执行测试。完整研究算法、ROS 2/Nav2、语义模型、扩展组件和实际平台仍按各自范围记录。

### 6.10 与用户平台代码的交接及研究结论

| 交接内容 | 需提供或共同核验的字段及行为 |
| --- | --- |
| 地图与关联 | 几何或点云、稳定引用与地图修订、坐标系和单位、变换与适用时间、变更范围。研究侧据此创建版本/证据关联。 |
| 定位与原始观测 | 位姿和采样时间、时间误差、观测原始资料、传感器及外参/标定版本、实际观测范围和有效性。 |
| 导航与观测作业 | 目标站点、允许路线/区域、测量配置、起止时窗，接收、执行、取消、结束及位置未确认的回执。 |
| 能力与代价 | 机器人尺寸/扫掠包络、可用模态、路线和采样的预计耗时/能量及实耗，控制授权和独立本地安全边界。 |

首轮实施可采用“用户平台输出 → S1 导入 → S2 关联版本 → S3 整理观测 → S4 生成义务及验收 → S5 调用现成求解器 → S6 平台适配 → S7 更新用途判定”，由 S8 保存全过程。研究计算可在工作站运行，再通过接口接入机器人。机器人上的 Python/ROS 版本独立锁定；例如 NetworkX 3.7 与 pyproj 3.8.0 的 Python 最低版本高于 Python 3.10，需要选择匹配版本或通过独立进程交换记录。

<a id="tool-capability"></a>

### 6.11 感知与人工复核工具的能力和获取边界

| 工具与获取入口 | 可承担的具体步骤 | 仍需完成的衔接或选择 |
| --- | --- | --- |
| [FAST-LIO2 官方仓库](https://github.com/hku-mars/FAST_LIO)，GPL-2.0 | LiDAR/IMU 里程计、几何点云和位姿，支持几何地图准备 | 用户负责。源码需递归取得 ikd-Tree 子模块，LiDAR 驱动、时间和外参随设备配置。原仓库为 ROS 1 体系；不由 Ubuntu 版本推断用户所用分支或 ROS 发行版。它不生成校园地点身份或功能要求。 |
| [Open3D-ML 源码](https://github.com/isl-org/Open3D-ML)及[模型权重目录](https://github.com/isl-org/Open3D-ML/blob/main/model_zoo.md)，代码 MIT | RandLA-Net / KPConv 对点云作类别分割，辅助人工确认区域 | 权重按 SemanticKITTI、S3DIS 等数据集区分。必须选择输入特征、类别表、点密度和场景相符的配置；类别输出不自动生成“南门通道”的稳定身份、功能边界或依赖图。公开权重可取得；目录未单列权重使用条款，不能把代码 MIT 直接扩大为独立权重许可证明。 |
| [Grounding DINO 源码](https://github.com/IDEA-Research/GroundingDINO)、[作者权重](https://huggingface.co/ShilongLiu/GroundingDINO)；[SAM 2 源码及权重](https://github.com/facebookresearch/sam2)，Apache-2.0 | 图像文字提示检测、掩码及跟踪，可帮助定位障碍和语义区域 | 需要 RGB；要落到三维地图，还需同步、内外参、位姿、可见性处理及跨帧关联。掩码不直接提供有误差界的净宽或通行许可。原版 DINO 离线依赖还包括文本编码器和分词器；应完整缓存。 |
| [Grounded-SAM-2 组合示例](https://github.com/IDEA-Research/Grounded-SAM-2)，Apache-2.0 | 已有 DINO 检测框交给 SAM 2 分割的本地示例，无须从头实现模型组合 | 采用原版或 [Transformers 的 DINO](https://huggingface.co/docs/transformers/model_doc/grounding-dino)本地路径。仓库内 DINO 1.5/1.6、DINO-X 示例要求云 API Token，不列入首轮本地依赖。 |
| [Open3D](https://github.com/isl-org/Open3D)，MIT | 点云读写、过滤、配准、平面拟合、聚类和距离计算，支撑变化候选和测量处理 | 需编写原始观测到通道净宽、保证覆盖、误差区间和证据记录的处理流程。点云距离变化、RANSAC 内点数或分割置信分数不直接等于合格证据。 |
| [CloudCompare 官方下载](https://www.cloudcompare.org/release/index.html)及[源码](https://github.com/CloudCompare/CloudCompare)，主体 GPL | 提供人工点云分割、点选、距离检查，补齐“人工复核”所用界面 | 人确认区域、名称及关系；UUID 和身份表保存业务编号。GUI 中的标签不代替版本化实体记录。官方有 Windows 安装包/压缩包及 Linux 发行途径，本轮只核对文档与发布入口。 |

获取证据包括五个仓库的 **28 份关键源码、配置、许可与安装文件**，固定了对应提交。RandLA-Net、KPConv、Grounding DINO、SAM 2.1 Tiny 的官方权重地址均成功返回 HTTP 206 和前 4096 字节。服务器声明的完整大小分别为 5,101,179、146,956,897、693,997,677 和 156,008,466 字节。该检查确认文件可读取，未下载完整权重、校验整个权重或执行推理；详见[获取记录](../validation/tool-acquisition.json)。

首轮采用点云几何与人工确认的通道作为研究输入，语义分割用于辅助准备。只有点云时评估对应点云模型；有同步 RGB 及标定时再选 DINO + SAM 2。两条语义路线是备选，不要求同时部署。IFC/GDAL、ConceptGraphs、OPA 和 TensorRT 加速不列为本轮必要依赖，避免把 BIM、多格式转换、开放场景图和模型部署优化并入核心研究工作。

<a id="platform-layout"></a>

### 6.12 Ubuntu 20.04 主机、Thor 与外部工作站

用户于 2026-11-22 提供当前设备配置。以下区分已知配置与建议部署，不据此改写厂商出厂规格或认定具体 ROS 发行版。

| 节点 | 已知条件与建议职责 | 环境选择与边界 |
| --- | --- | --- |
| 机械狗主机 | Ubuntu 20.04；由用户负责运动、建图、定位、导航及底层接口 | 保留匹配现有驱动的环境；实际 CPU 架构、ROS 发行版和消息接口待按用户代码确认。研究侧不要求在此主机装全部算法库。 |
| Thor T4000 算力盒子 | 用户提供 JetPack 7.2 / L4T Ubuntu 24.04；承担现场采集、缓存、任务适配与需要上车的感知 | ARM64；NVIDIA 官方列 T4000 计算能力为 11.0。CPU 研究库有 Python 3.12/aarch64 包；深度模型单独选相容的 PyTorch、CUDA 和扩展算子。ROS 2 Jazzy 可作为新增软件候选，并非已安装事实。 |
| 外部工作站 | 用户允许按需选择；建议 Ubuntu 24.04 x86-64、Python 3.12，用于地图整理、人工复核、离线分割、MSRP 及实验分析 | CPU 研究环境与 GPU 感知环境分开锁定；感知环境随所选模型选择 Python/PyTorch/CUDA。首轮可在工作站运行模型，待确有上车推理需求再完成 Thor 迁移。工作站参与在线决策时须计入通信时延、失联处理及公平成本。 |

**官方平台依据。** [JetPack 7.2 发行页](https://developer.nvidia.com/embedded/jetpack/downloads/archive-7.2)列 T4000、L4T 39.2、Ubuntu 24.04、CUDA 13.2.1、TensorRT 10.16.2；[CUDA 硬件表](https://developer.nvidia.com/cuda/gpus)列 T4000 为 11.0。同站介绍文字仍有 CUDA 13.0 概述，本设计以发行页版本表作候选基线，实际设备版本后续核对。CUDA/TensorRT 属于可从 NVIDIA 获取的许可软件，不能统称整套平台全部开源；本阶段不依赖 TensorRT 模型转换。

需要提前处理的兼容点如下。

1. **Open3D-ML 的环境说明不一致。** 核查提交 `a3d0f7a` 的 README 仍列 PyTorch 2.0.*，但 requirements-torch 固定 2.13.0，CUDA 文件固定 `2.13.0+cu126`。本机取得的 Windows Open3D 0.20.0 包也绑定 `2.13.0+cpu`。因此应锁定实际发布包和自定义算子版本；CPU 几何包存在不证明 ML 的 Thor GPU 算子可直接使用。[源码与依赖文件](https://github.com/isl-org/Open3D-ML/tree/a3d0f7a51d4eef0b94b9000a7d74af05e2d54c4f)
2. **Thor 深度学习运行时还未冻结。** 本次读取的 [NVIDIA PyTorch 兼容表](https://docs.nvidia.com/deeplearning/frameworks/install-pytorch-jetson-platform-release-notes/pytorch-jetson-rel.html)最新条目仍标 JetPack 7.1，不能据此宣布某个容器已对用户的 7.2 配置验收。采用能覆盖实际驱动、ARM64 和 T4000 的官方构建，并核对 torchvision 与模型扩展；必要时在匹配环境编译扩展。GPU 型号和算力数值不能替代兼容证据。
3. **可降低自定义算子依赖。** Grounded-SAM-2 提供 Transformers DINO 示例；其配置支持关闭自定义 kernel。SAM 2 官方允许不构建可选 CUDA 后处理扩展。这些是已有支持路径，是否采用及其后处理、延迟变化需在选定环境下记录，不等于本轮完成 Thor 推理。[DINO 配置](https://huggingface.co/docs/transformers/model_doc/grounding-dino#transformers.GroundingDinoConfig)、[SAM 2 安装说明](https://github.com/facebookresearch/sam2/blob/main/INSTALL.md)
4. **双主机接口不能只凭 ROS 名称连接。** [Jazzy 官方安装源](https://github.com/ros2/ros2_documentation/blob/jazzy/source/Installation/Ubuntu-Install-Debs.rst)提供 Ubuntu 24.04 的 amd64/arm64 包。机械狗主机使用哪一代 ROS 尚不确定；[ros1_bridge 官方说明](https://github.com/ros2/ros1_bridge)明确 Ubuntu 24.04 不在其支持范围。优先使用用户提供的导航/观测接口与现行 Wire Contract 衔接；如果经 ROS 接入，另锁定消息类型、QoS、时钟和必要的桥接环境，不能默认 Foxy/Noetic 与 Jazzy 直接互通。

**剩余实现边界。** 仍需把原始点云/图像变为具备尺度、覆盖和误差依据的证据，维护实体及版本，编写 APCM/义务和验收规则、完整 MSRP/多轮策略、任务条件查询与平台适配。现成工具已覆盖这些流程中的通用计算；具体研究逻辑不会由安装库自动获得。当前没有发现必须自研新的 SLAM、语义分割网络、图算法库或约束求解器的必要，研究范围仍以受控通道为准。

需要优先取得的可行性证据是一次真实测量能否形成合格宽度及覆盖、同源限制下能否补齐原证据模板、用户导航器能否执行一项带约束的往返观测作业，以及 MSRP 在相同资格和资源下相对基线的效果。上述基础工具已存在，研究模型和平台交接仍有明确实现工作。当前支持开展限定原型与实验，研究效果和端到端实机闭环待后续结果判定。
