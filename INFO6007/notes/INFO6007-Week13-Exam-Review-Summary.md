---
title: INFO6007 Week 13 期末复习课讲课总结
categories:
  - Course Notes
  - INFO6007
tags:
  - INFO6007
  - Exam-Review
  - Project-Management
description: >-
  INFO6007 Week 13 期末复习课讲课总结：期末题型（4 道情景题 × 15 分）与 What / Why / How 答题法，
  按 W1–W12 整理复习课强调的考点——项目定义与三重约束、项目成功维度、Waterfall / Agile / DevOps、WBS 与网络图、
  PDM 依赖类型、PERT、关键路径与进度压缩、成本估算与 EVM、QA vs QC 与质量工具、领导风格、动机、RACI、
  资源平衡、Tuckman 与冲突处理、风险类型与应对、make-or-buy、RFP vs RFQ、合同类型、外包模式、治理机制、
  整合管理、ITSM 与 ITIL 4（四维度、SVS、服务价值链、关键实践），最后给出 4 道仿真情景题及中英文参考答案。
mathjax: true
abbrlink: info6007-week13-exam-review
date: 2026-11-22 10:45:00
---

# INFO6007 Week 13 期末复习课讲课总结

> - **课程**：INFO6007 — Project Management in IT，Semester 2 2026
> - **来源**：`Lecture - INFO6007 Week 13 - Semester review and Final exam prep.pdf` + Echo360 转写稿
>
> 复习课把 W1–W12 每周挑重点过了一遍，最后用 Practice Exam Q1 演示答题方法。**复习课讲到的不等于考试范围**：讲课和 tutorial 里的任何内容都可能考，复习时仍要回到各周讲义。各章节末尾链接到对应周的详细笔记。
>
> ⚠️ 第十四章的 4 道仿真题和参考答案是笔者按本课题型自拟的，不是官方题目。

---

## 一、期末题型与答题方法

**题型**：4 道情景题，每题 15 分，共 60 分；每题一个简短的**假设情景**（不考真实公司案例）加 3 个左右的小问（幻灯片写 3–4 个，讲课时说每题都是 3 个）。答题 2 小时 + 10 分钟阅读，**每题大约 30 分钟**。阅读材料和客座讲座不直接考，但可以拿来当例子充实答案。

**评分看三件事（What / Why / How）**：

| 层次 | 要写什么 | 示例（PERT 小问） |
|:---|:---|:---|
| **What** | 说清楚概念是什么，体现理解 | 写出 PERT 公式并算出结果 |
| **Why** | 为什么在这个情景里用它、它好在哪 / 差在哪 | PERT 考虑了乐观到悲观的整个区间，不只靠一个估计值 |
| **How** | 把概念落到题目情景里：具体做什么 | 8 天是期望值不是承诺值；估计区间 4–16 天，排期要留应急储备 |

**答题习惯**：

1. 先快速通读整卷，再逐题**划出关键词**（例如 Waterfall、Agile、planning、stakeholder involvement、recommend）——题干里的每个动词都是一个得分点；
2. Recommend 类题目**没有唯一答案**：选 Waterfall、Agile 或 Hybrid 都可以，关键是理由要贴合情景；
3. 计算题：公式 → 代数 → 结果（带单位）→ 一句解读，缺一不可。

详细的题型拆解见 [[26-S2-Course/INFO6007/INFO6007-Practice-Exam-S2-2026-Solutions|Practice Exam 逐题解析]]，更多练习见 [[26-S2-Course/INFO6007/INFO6007-Scenario-Question-Bank-Solutions|情景题库解析]]。

---

## 二、W1 项目基础

**项目** = 为创造独特产品、服务或成果而进行的**临时性**工作（PMBOK 第 6 版）。四个特征：

| 特征 | 含义 |
|:---|:---|
| Temporary | 有明确起止点，不是持续运营 |
| Unique outcome | 产出新的产品、服务或成果 |
| Specific objectives | 为满足特定目标或解决特定问题 |
| Constraints | 受范围、时间、成本、资源约束 |

项目「有始有终」，这是它和服务管理、治理（持续、偏战略）的根本区别。

**三重约束**（必须会推导连锁影响）：

| 变化 | 通常的后果 |
|:---|:---|
| 范围增加 | 时间和/或成本增加 |
| 时间缩短 | 成本上升、范围缩小，或必须提高交付效率 |
| 预算削减 | 范围缩小、时间延长，或质量/风险受影响 |

**项目成功不只看「按时、按预算、按范围」**：复习课专门问过「三项都达标是否就算成功？」——答案是否定的。成功维度还包括质量、干系人满意度、业务价值、团队表现、可持续性、用户采用、战略一致性、长期运营影响、风险管理与灵活性。

**项目 → 项目集 → 项目组合**：战略层级逐级升高。类比：一门课是一个项目，一个学位（degree program）是项目集，学院所有学位合起来是项目组合。

**十大知识领域**：范围、进度、成本、质量、资源、沟通、风险、采购、干系人，以及把它们串起来的**整合管理**。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week01-Introduction-Summary|W01 Introduction]]、[[26-S2-Course/INFO6007/INFO6007-Week02-Tutorial-Triple-Constraint|W02 Tutorial 三重约束]]

---

## 三、W2 项目管理方法论

- **生命周期 vs 过程组**：PMBOK 里启动、规划、执行、监控、收尾叫「过程组」；本课允许直接当作生命周期阶段来用，答题时这样写不扣分。
- **Waterfall**：线性、顺序，每个阶段完成后才进入下一阶段（需求 → 设计 → 实现 → 测试 → 部署 → 维护）。适合需求稳定、安全关键的行业（军工、医疗）。
- **Agile / Scrum**：迭代增量交付；从产品待办（backlog）选一批功能，在 1–4 周的 sprint 里开发、发布、收集反馈，再进入下一个 sprint。
- **DevOps**：把开发和运维打通，交付流程里包含部署，持续集成、持续部署。

| | 流程形态 |
|:---|:---|
| Waterfall | Design → Code → Test → Deploy（一条直线） |
| Agile | Design → (Code → Test) × n → Deploy（循环） |
| DevOps | 开发与运维连成持续循环，部署是循环的一部分 |

**需求收集技术**：访谈（一对一）、问卷（快速收集大范围意见）、工作坊（协作讨论）、观察（看用户怎么用现有系统）、文档分析（查现有流程和系统文档）。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week02-PM-Methodologies-Summary|W02 项目管理方法论]]、[[26-S2-Course/INFO6007/INFO6007-Week03-Tutorial-Methodology-Stakeholder|W03 Tutorial 方法论选型]]

---

## 四、W3 范围与进度管理

**范围管理计划的组成**：范围说明书（做什么、不做什么）、范围管理方法、需求收集方式、WBS、范围确认流程、范围控制流程、角色职责、假设与约束。复习课提示：范围管理六个过程的名字**不需要背**，但要理解每一步在做什么（例如用什么技术收集需求、怎么确认范围）。

**WBS**：对可交付成果的层级分解；配套 **WBS 词典**（每个工作包的描述、负责人、验收标准等）。

**三种网络图**：

| 图 | 表示方式 | 要点 |
|:---|:---|:---|
| **AON**（Activity on Node） | 活动在节点上，箭头表示依赖 | 业界最常用，好画好懂，MS Project / Primavera 都支持 |
| **AOA**（Activity on Arrow） | 活动在箭头上，节点是事件 | 较复杂，**唯一常需要虚活动（dummy，工期 0）** 的图 |
| **PDM**（Precedence Diagramming） | AON 的一种 | 显式标注四种依赖类型，支持 lead / lag |

**PDM 四种依赖**（考法：给出情景，判断依赖类型）：

| 类型 | 含义 | 例子 |
|:---|:---|:---|
| **FS** 完成-开始 | A 完成后 B 才能开始（最常见） | 单元测试完成后才能开始集成测试 |
| **SS** 开始-开始 | A 开始后 B 才能开始 | 开始编写代码后即可开始编写测试用例 |
| **FF** 完成-完成 | A 完成后 B 才能完成 | 测试完成后文档才能定稿 |
| **SF** 开始-完成 | A 开始后 B 才能完成（罕见） | 新系统上线后旧系统才能停止 |

**PERT 三点估算**：

$$
t_E = \frac{O + 4M + P}{6}
$$

$O$ 乐观、$M$ 最可能、$P$ 悲观。好处：考虑不确定性而非单点估计；局限：算出的是**期望值**，不保证完成，排期仍需应急储备和依赖分析。

**关键路径法（CPM）**：关键路径是**最长的**依赖活动序列，决定项目**最短可能工期**；关键路径上任何延误都会**推迟整个项目**；非关键活动有浮动时间（slack）。

**进度压缩**：

| 方法 | 做法 | 代价 |
|:---|:---|:---|
| **Fast tracking（快速跟进）** | 把原本顺序进行的活动并行做 | **风险增加**（返工），通常不直接加钱 |
| **Crashing（赶工）** | 给**关键路径**上的活动加资源 | **成本增加**，也可能增加风险 |

只压缩关键路径上的活动才能缩短工期；压缩非关键活动是浪费。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week03-Scope-Schedule-Management-Summary|W03 范围与进度管理]]、[[26-S2-Course/INFO6007/INFO6007-Week04-Tutorial-Scope-WBS-Critical-Path|W04 Tutorial 范围蔓延、WBS 与关键路径]]

---

## 五、W4 成本管理与挣值

**四个过程**：规划成本管理 → 估算成本 → 制定预算（把总估算分配到工作项，形成成本基线）→ 控制成本。

**估算技术**：

| 技术 | 特点 |
|:---|:---|
| Analogous（类比） | 基于相似项目的历史数据；**快但不准** |
| Parametric（参数） | 统计/数量模型（如每功能点单价 × 数量） |
| Bottom-up（自下而上） | 逐个工作包估算再汇总；**最详细、最准确**，但费时 |
| Three-point（PERT） | 同进度估算，考虑不确定性 |
| Expert judgement | 依靠领域专家或顾问 |

**EVM（挣值管理）**：把范围、进度、成本整合起来客观衡量绩效，回答「现在怎样、往哪走、能否按预算按时完工」，能**提前预警**超支。

| 量 | 含义 |
|:---|:---|
| **PV** | 到某日**计划**完成工作的预算成本 |
| **EV** | 到某日**实际完成**工作的预算成本（「挣得」的价值） |
| **AC** | 实际完成这些工作的**真实花费** |

$$
CV = EV - AC,\quad SV = EV - PV,\quad CPI = \frac{EV}{AC},\quad SPI = \frac{EV}{PV},\quad EAC = \frac{BAC}{CPI}
$$

| 指标 | > 0 或 > 1 | < 0 或 < 1 |
|:---|:---|:---|
| CV / CPI | 低于预算（成本有效） | 超支 |
| SV / SPI | 进度超前 | 进度落后 |

记忆：**都拿 EV 去比**——比 AC 看钱，比 PV 看时间。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week04-Cost-Management-Summary|W04 成本管理]]、[[26-S2-Course/INFO6007/INFO6007-Week05-Tutorial-EVM-Exercises|W05 Tutorial EVM 计算]]

---

## 六、W5 质量管理

**三个过程**：规划质量管理 → 管理质量 → 控制质量。

**QA vs QC（复习课课堂提问）**：

| | Quality Assurance（管理质量） | Quality Control（控制质量） |
|:---|:---|:---|
| 时机 | **事前**：预先建立保障措施 | **事后**：检查产出 |
| 焦点 | 过程是否被遵守，**预防**缺陷 | 交付物是否达标，**发现并纠正**缺陷 |
| 活动 | 过程审计、QA 评审、持续过程改进、风险与缺陷预防 | 测试与检查、缺陷记录、对照质量指标测量、验收决定（接受/有条件接受/拒绝） |

**Verification vs Validation**：Verification 问「我们把东西做对了吗」（符合规格）；Validation 问「我们做的是对的东西吗」（满足用户需要）。

**角色**：项目经理对质量负最终责任（制定 QMP、平衡成本/时间/质量、批准纠正和预防措施）；QA 团队定义流程和指标、做审计；测试团队执行测试、记录缺陷；开发团队遵守编码规范、做同行评审和单元测试。

**质量工具**（考法：给情景选工具并说明用途）：

| 工具 | 用途 |
|:---|:---|
| Cost-benefit analysis | 比较质量活动的成本和收益（ROI），如是否引入自动化测试 |
| Cause-and-effect（鱼骨图 / Ishikawa） | 找问题的**根本原因** |
| Control chart | 随时间看过程表现，超出上下控制限即异常 |
| Checksheet | 实时收集并计数数据（如每周投诉、工单分类） |
| Flowchart | 画出流程步骤，找缺口、冗余和风险点 |
| Scatter diagram | 两个变量的相关性 |
| Histogram | 频数分布 |
| **Pareto chart** | 柱状图 + 累计折线，**80/20 法则**：约 80% 的问题来自约 20% 的原因，先解决这些原因 |

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week05-Quality-Management-Summary|W05 质量管理]]

---

## 七、W6 资源管理

**领导风格**：

| 风格 | 优点 | 缺点 |
|:---|:---|:---|
| Autocratic（专断/指令式） | 决策快，适合危机（如系统宕机） | 士气低，压抑创造力 |
| Democratic（民主/参与式） | 促进创新和投入 | 决策慢，可能引发冲突 |
| Laissez-faire（放任） | 适合高技能、自驱的团队 | 团队经验不足时会混乱 |

最好的做法是**视人视情况组合使用**（见 W9 的 adaptive leadership）。

**内在 vs 外在动机**：内在动机来自工作本身（享受、掌握技能、成就感）；外在动机来自外部（薪水、认可、晋升、避免惩罚）。

**RACI 矩阵**：

| 字母 | 角色 | 沟通方式 |
|:---|:---|:---|
| **R** Responsible | 实际干活的人 | — |
| **A** Accountable | 最终负责、批准的人（每项任务只有一个） | — |
| **C** Consulted | 做之前要征求意见的人 | 双向 |
| **I** Informed | 需要被告知进展或决定的人 | 单向 |

**其他工具**：资源分解结构（RBS，按资源类别分解）、资源直方图（各时段需要多少人）。资源估算技术与成本估算类似：专家判断、类比、自下而上（最准但费时）、PERT。

**资源负荷 vs 资源平衡**：

$$
\text{Resource Load} = \frac{\sum \text{Allocated Hours}}{\text{Available Hours}}
$$

负荷 > 100% 即过度分配；**资源平衡**的手段：推迟任务、拆分任务、重新分配任务、调整工时。

**Tuckman 团队发展模型**：Forming（组建）→ Storming（震荡）→ Norming（规范）→ Performing（执行，最顺畅）→ Adjourning（解散/收尾）。

**冲突处理五种模式**：

| 模式 | 坚持度 | 合作度 | 适用 |
|:---|:---:|:---:|:---|
| Competing（竞争） | 高 | 低 | 关键问题、时间紧需快速决定 |
| Collaborating（协作） | 高 | 高 | 复杂问题，需要各方意见，追求双赢 |
| Compromising（妥协） | 中 | 中 | 时间有限、需要临时方案 |
| Avoiding（回避） | 低 | 低 | 小问题，或情绪激动时先冷却 |
| Accommodating（迁就） | 低 | 高 | 维护关系，或问题对对方更重要 |

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week06-Resource-Management-Summary|W06 资源管理]]

---

## 八、W7 风险管理

**正面风险 vs 负面风险**：风险不一定是坏事。机会（正面）要利用，威胁（负面）要化解，都需要结构化管理。

**风险类别**：市场风险、财务风险（资金、预算、超支、通胀、利率）、技术风险（技术过时、补丁、安全）、人员风险（人员流失、干系人参与）、结构/流程风险（流程和治理不健全）。

**风险效用（风险偏好）**：

| 类型 | 典型组织 |
|:---|:---|
| Risk-seeking（风险寻求） | 初创公司 |
| Risk-neutral（风险中性） | 多数大公司，取平衡 |
| Risk-averse（风险规避） | 大学、医院、军事组织 |

**风险识别**：头脑风暴、德尔菲法（匿名多轮专家意见）、访谈、SWOT 分析。

**概率与影响评估**（定性分析）：分别评定**可能性**（发生的概率）和**影响**（一旦发生对成本、时间、范围、质量的后果）。高概率不一定高影响，两者要分开评。

**应对策略**：

| 威胁（负面） | 做法 | 机会（正面） | 做法 |
|:---|:---|:---|:---|
| **Avoid** 规避 | 消除威胁，如把高风险功能移出范围 | **Exploit** 开拓 | 确保机会发生，如派最强的人保证提前完成 |
| **Mitigate** 减轻 | 降低概率或影响，如加测试 | **Enhance** 提高 | 提高概率或影响，如培训提升生产率 |
| **Transfer** 转移 | 交给第三方，如保险、带 SLA 的外包 | **Share** 分享 | 与第三方合作共享收益 |
| **Accept** 接受 | 不主动处理，发生了再应对 | **Accept** 接受 | 机会来了就用，不主动追求 |
| **Escalate** 上报 | 超出项目范围时上报项目集/组合层 | **Escalate** 上报 | 超出项目权限时上报 |

**风险登记册**：记录所有已识别风险、特征、负责人和应对措施的中心文档；是**活文档**，贯穿整个生命周期更新；保证可见、可追踪、有人负责。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week07-Risk-Management-Summary|W07 风险管理]]

---

## 九、W8 采购管理

**Make-or-Buy 分析**：决定自己做还是外购。考虑因素：成本、时间、质量、专业能力、控制与保密、战略重要性。

**采购文档**：

| 文档 | 作用 |
|:---|:---|
| **SOW**（工作说明书） | 采购的「做什么、怎么做」：范围、可交付成果、时间表、标准；减少误解和范围蔓延，争议时作法律依据 |
| **RFP**（建议邀请书） | **需求还不清楚**、希望供应商**提出解决方案**时用；包含背景、范围（引用 SOW）、需求、提交指南、评估标准、时间表、预算（可选）、条款 |
| **RFQ**（报价邀请书） | **需求明确、标准化**，只要**价格**、交货和付款条件时用 |

**合同类型与买方风险**：固定总价（买方风险最低，卖方承担超支）< 工料合同 T&M（中）< 成本补偿（买方风险最高）。要会根据情景选合同：范围清楚用固定总价，范围不清用 T&M 或成本补偿。

**供应商评估**：

| 方法 | 用途 |
|:---|:---|
| Weighted scoring（加权评分） | 给每个标准定权重、给供应商打分，加权求和后比较 |
| Checklist（检查清单） | 检查供应商是否满足某些必要标准 |
| Vendor scorecard（供应商记分卡） | 合同授予**之后**持续监控已合作供应商的 KPI（准时率、缺陷率等，常用红黄绿灯） |

**外包模式**：Onshore（同国）、Nearshore（邻近国家/时区）、Offshore（远方国家，省成本）、Hybrid（内部 + 外部混合）、Multisource（多种模式组合）、Insourcing（与外包相反，交给公司内部其他团队）。考法：给情景选模式或组合。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week08-Procurement-Management-Summary|W08 采购管理]]

---

## 十、W9 领导力、治理与一致性

**Leader vs Manager**：Leader 关注人、愿景和激励，面向未来（「我们去哪、为什么」）；Manager 关注流程、任务和控制，面向当下（「怎么高效正确地做完」）。

**领导风格**（在 W6 基础上补充）：Transformational（变革型，推动创新）、Transactional（交易型，靠奖惩和结构）、Autocratic、Laissez-faire，以及最推荐的 **Adaptive / Agile leadership**：根据项目需要、团队状态和业务优先级灵活切换风格，平衡控制与授权。

**项目领导者的关键技能**：沟通、适应力、战略思维、风险管理与批判性思维、决策与解决问题、干系人管理与谈判、人员管理、**情商**。

**沟通管理三个过程**：规划沟通管理 → 管理沟通 → 监督沟通。

**常见治理机制**：

| 机制 | 作用 |
|:---|:---|
| Steering Committee（指导委员会） | 战略指导，批准重大变更，监控绩效 |
| PMO（项目管理办公室） | 统一流程、监控 KPI、支持项目经理、确保方法论合规 |
| Project Sponsor（发起人） | 推动项目、批准预算、解决上报问题、确保与战略一致 |
| Stage-gate reviews（阶段关口评审） | 在关键里程碑正式审批进度、交付物和资源 |
| Dashboards（绩效报告） | 预算、进度、范围、风险、质量的可视化 |
| Escalation procedures（上报流程） | 规定风险和问题怎么上报、评估、解决 |
| Decision-making frameworks | 谁能在什么情况下做什么决定 |
| Audits and reviews | 独立检查合规、质量与一致性 |

**一致性框架**：SAM（Henderson & Venkatraman，业务战略与 IT 战略对齐）、Balanced Scorecard（把项目连到战略目标）、COBIT（ISACA 的 IT 治理框架）、ITIL（IT 服务管理最佳实践）、TOGAF（企业架构）。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week09-Leadership-Governance-Alignment-Summary|W09 领导力、治理与一致性]]

---

## 十一、W10 整合管理

**知识领域 × 生命周期阶段**：规划阶段几乎涉及所有知识领域；启动阶段侧重沟通、干系人、整合；执行阶段侧重质量、资源、沟通等；**监控阶段涉及全部领域**；收尾阶段侧重沟通、干系人、整合和采购。**整合、干系人、沟通贯穿所有阶段**。

**IT 项目的特点**：复杂度高、技术变化快、交付物无形（别人看不到投入的工作量）、干系人多、不确定性和风险高、依赖需求的准确性。

**整合工具**：PMIS（MS Project、Jira、Asana、Trello）、实时仪表盘、**变更控制委员会（CCB）**（批准或拒绝变更）、文档与知识库（Wiki、Confluence、SharePoint，沉淀经验教训）。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week10-Integration-Management-Summary|W10 整合管理]]

---

## 十二、W11 ITSM 与 ITIL 4 基础

**ITSM**：组织用来设计、交付、管理和改进 IT 服务的一套政策、流程和实践，以满足业务和客户需要。关键理念：面向服务、结构化流程（事件、问题、变更、服务级别管理）、创造业务价值、采用 ITIL / COBIT 等框架。

**产品 vs 服务**：

| | Product | Service |
|:---|:---|:---|
| 性质 | 有形或明确的软硬件 | 无形，基于体验 |
| 所有权 | 客户拥有或获得许可 | 客户使用，提供方拥有 |
| 交付 | 一次性或按版本 | 持续 |
| 价值焦点 | 特性和功能 | 结果和体验 |
| 例子 | 买断 Adobe Photoshop | 订阅 Adobe Creative Cloud |

**项目管理 vs 服务管理**：PM 交付一次性的独特成果（创造或改变某样东西）；ITSM 保证已上线服务持续可靠运行（管理事件、变更、SLA）。项目交付的成果最终交给服务管理去运营。

**服务关系模型**：B2B、B2C、B2G；C2C、C2B、G2B、G2C、G2G；新兴的 B2E、D2C、B2M、M2M、N2C、N2B。考法：给情景判断属于哪种模型并说明理由。

**服务管理四个维度**：

1. **Organisations and People**：文化、结构、能力、沟通；
2. **Information and Technology**：管理和交付服务所需的信息、知识和技术；
3. **Partners and Suppliers**：共同创造和交付服务的第三方；
4. **Value Streams and Processes**：价值如何通过协调的流程被创造和交付。

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week11-ITSM-Processes-1-Summary|W11 IT 服务管理与流程（一）]]

---

## 十三、W12 ITIL 4 服务价值系统与关键实践

**SVS（服务价值系统）的组件**：Guiding Principles（普遍适用的建议）、Governance（方向与控制）、**Service Value Chain（SVS 的运营核心，把需求转化为价值）**、Practices（34 个管理实践，分一般、服务、技术三类）、Continual Improvement。复习课强调：**要理解这些组件之间的关系**。

**服务价值链六项活动**：

| 活动 | 做什么 |
|:---|:---|
| **Plan** | 对齐愿景、战略和改进计划 |
| **Improve** | 识别并实施服务、实践、流程的改进 |
| **Engage** | 与干系人互动，理解需求、期望和反馈 |
| **Design & Transition** | 构建、修改新服务或变更后的服务并转入运行 |
| **Obtain / Build** | 获取或构建服务所需的组件 |
| **Deliver & Support** | 运营服务并提供持续支持 |

**关键实践**：34 个实践不用全背；复习课点名的重点是**事件管理、问题管理、变更管理、服务请求管理、服务台、服务级别管理、知识管理、服务连续性管理**。考法是**用某个实践去处理给定情景**（例如用事件管理恢复服务、用服务台改善服务交付）。

| 实践 | 一句话 |
|:---|:---|
| Incident Management | **尽快恢复**正常服务，减少对业务的影响 |
| Problem Management | 找**根本原因**，防止事件重复发生（已知错误、变通方案） |
| Change Enablement | 评估、授权、安排变更，平衡变更速度与风险；standard / normal / emergency |
| Service Request Management | 处理用户发起的、预先定义的标准请求（如重置密码、申请软件） |
| Service Desk | 用户的单一联系点，接收事件和请求 |
| Service Level Management | 设定**可衡量**的服务目标（SLA），持续监控与评审 |
| Knowledge Management | 沉淀并共享知识（如知识库文章），让问题更快解决 |
| Service Continuity Management | 保证灾难或重大中断时服务仍能维持在可接受水平 |

→ 详见 [[26-S2-Course/INFO6007/INFO6007-Week12-ITSM-Processes-2-Summary|W12 IT 服务管理与流程（二）]]

---

## 十四、仿真情景题（自拟，附参考答案）

以下 4 道题按期末格式自拟：每题一个情景 + 3 个小问，共 15 分。题干为英文，先给中文解析，再给可直接照写的英文答案。为避免和 Practice Exam、情景题库重复，选了它们没有覆盖的角度。

### 仿真题 1（15 分）医院预约系统：关键路径、赶工与快速跟进

> **Question 1 [15 points]** A regional hospital is replacing its outpatient appointment system. The project manager has prepared the following activity list (durations in weeks).
>
> | Activity | Description | Duration | Predecessor |
> |:---:|:---|:---:|:---:|
> | A | Requirements analysis | 3 | – |
> | B | Core system build | 5 | A |
> | C | Data migration scripts | 4 | A |
> | D | Integration testing | 6 | B |
> | E | Data validation | 2 | C |
> | F | Staff training and go-live | 3 | D, E |
>
> (a) Identify all paths through the network, determine the critical path and the project duration, and calculate the slack of activities C and E. (5 points)
>
> (b) The hospital executive asks for go-live in 15 weeks. The following crashing options are available: B can be shortened by 1 week for \$4,000; C by up to 2 weeks at \$1,000 per week; D by up to 2 weeks at \$3,000 per week; F by 1 week for \$6,000. Recommend the cheapest way to meet the 15-week target and explain why crashing activity C would not help, despite being the cheapest option. (5 points)
>
> (c) Instead of crashing, a team member suggests starting staff training (F) at the same time as integration testing (D). Explain what this technique is, how the dependency between D and F changes, and discuss one risk of this approach in the hospital context. (5 points)

#### 1(a) 中文解析

两条路径：

| 路径 | 工期 |
|:---|:---|
| A → B → D → F | 3 + 5 + 6 + 3 = **17 周** |
| A → C → E → F | 3 + 4 + 2 + 3 = 12 周 |

关键路径是最长的那条：**A–B–D–F，工期 17 周**。C 和 E 在非关键路径上，浮动时间 = 17 − 12 = **5 周**（两者共享这 5 周）。

**English answer (unofficial)**

- Path A–B–D–F = 3 + 5 + 6 + 3 = 17 weeks; path A–C–E–F = 3 + 4 + 2 + 3 = 12 weeks.
- The critical path is the longest path, **A–B–D–F**, so the project duration is **17 weeks**. Any delay to A, B, D or F delays go-live.
- C and E lie on the non-critical path, so their slack is 17 − 12 = **5 weeks** (shared along that path): C or E could slip by up to 5 weeks in total without delaying the project.

#### 1(b) 中文解析

要从 17 周压到 15 周，必须在**关键路径**上缩短 2 周。关键路径上的赶工选项：B 1 周 \$4,000；D 每周 \$3,000，最多 2 周；F 1 周 \$6,000。最便宜：**D 压缩 2 周，共 \$6,000**（比 D 1 周 + B 1 周的 \$7,000 便宜）。压缩后 A–B–D–F = 15 周，另一条路径仍是 12 周，关键路径不变。

C 虽然每周只要 \$1,000，但它在**非关键路径**上，已有 5 周浮动时间；压缩 C 只增加浮动，不会改变 17 周的工期——花钱没有效果。

**English answer (unofficial)**

- To finish in 15 weeks, the **critical path** must be shortened by 2 weeks, because project duration is set by the longest path.
- Options on the critical path: B (1 week, \$4,000), D (\$3,000 per week, up to 2 weeks), F (1 week, \$6,000). **Crashing D by 2 weeks costs \$6,000**, which is cheaper than D + B (\$7,000) or any option using F.
- After crashing, A–B–D–F = 15 weeks and A–C–E–F = 12 weeks, so the critical path stays the same and the target is met.
- Crashing C is cheap but useless: C is on the non-critical path with 5 weeks of slack, so shortening it only increases slack and leaves the 17-week duration unchanged. Crashing adds cost, so it should only be applied to critical activities, starting with the cheapest per week.

#### 1(c) 中文解析

这是**快速跟进（fast tracking）**：把原本顺序进行的活动并行做。D 和 F 的依赖从 **FS（D 完成后 F 才开始）变成 SS（D 开始后 F 即可开始）**。快速跟进一般不直接增加成本，但**增加风险**：

- **风险**：集成测试期间系统还会改（修缺陷、改界面），员工培训用的是未定版本，测试发现问题后培训材料要**返工**，员工可能学到错误流程；在医院场景里，前台员工按错误流程操作预约，会直接影响病人就诊。
- **应对**：先培训不受测试影响的部分（业务流程、角色分工），界面操作部分放到测试稳定后；或用「培训测试版 + 上线前短时复训」。

**English answer (unofficial)**

- This is **fast tracking**: performing activities in parallel that were originally planned in sequence, to shorten the schedule without adding resources.
- The dependency changes from **finish-to-start** (F starts only after D finishes) to **start-to-start** (F can start once D starts), so up to 3 weeks of F overlap with D.
- **Risk:** integration testing may still find defects that change screens and workflows. Staff would then be trained on an unstable version, the training materials would need rework, and reception staff could learn incorrect booking procedures. In a hospital, booking errors directly affect patient care.
- **Mitigation:** train first on content that testing will not change (business process, roles), schedule screen-level training after the main test cycles pass, and run a short refresher before go-live.

---

### 仿真题 2（15 分）市立图书馆预订系统：EVM 与质量工具

> **Question 2 [15 points]** A city council is building an online booking system for its libraries. The total budget (BAC) is \$400,000 over 10 months. At the end of month 5, the project reports: Planned Value: \$200,000; Earned Value: \$160,000; Actual Cost: \$180,000. User acceptance testing has also produced 120 defect reports: login and authentication 52, payment 34, search 18, display formatting 16.
>
> (a) Calculate CV, SV, CPI and SPI. Interpret what these figures indicate about the project's cost and schedule performance. (5 points)
>
> (b) Calculate the Estimate at Completion (EAC) using the CPI method and the Variance at Completion (VAC). Explain one limitation of relying on this forecast. (4 points)
>
> (c) Explain how a Pareto chart could help the project team respond to the defect reports, and distinguish between one quality assurance and one quality control action the project manager should take. (6 points)

#### 2(a) 中文解析

$$
CV = EV - AC = 160{,}000 - 180{,}000 = -20{,}000
$$

$$
SV = EV - PV = 160{,}000 - 200{,}000 = -40{,}000
$$

$$
CPI = \frac{EV}{AC} = \frac{160{,}000}{180{,}000} \approx 0.89,\qquad SPI = \frac{EV}{PV} = \frac{160{,}000}{200{,}000} = 0.80
$$

解读：CV 为负、CPI < 1 → **超支**，每花 \$1 只挣回约 \$0.89 的工作；SV 为负、SPI < 1 → **进度落后**，只完成了计划工作的 80%（计划完成 50%，实际只完成 40%）。项目同时超支和延误，需要纠偏。

**English answer (unofficial)**

- CV = EV − AC = 160,000 − 180,000 = **−\$20,000**
- SV = EV − PV = 160,000 − 200,000 = **−\$40,000**
- CPI = EV / AC = 160,000 / 180,000 ≈ **0.89**
- SPI = EV / PV = 160,000 / 200,000 = **0.80**
- **Cost:** negative CV and CPI < 1 mean the project is over budget; it earns about \$0.89 of work for every \$1 spent.
- **Schedule:** negative SV and SPI < 1 mean it is behind schedule; only 80% of the planned work is done (40% of the total work completed against 50% planned).
- The project is both over budget and behind schedule, so the project manager should investigate the causes and take corrective action now, while half the work remains.

#### 2(b) 中文解析

$$
EAC = \frac{BAC}{CPI} = \frac{400{,}000}{160{,}000 / 180{,}000} = 450{,}000
$$

$$
VAC = BAC - EAC = 400{,}000 - 450{,}000 = -50{,}000
$$

照当前效率，项目最终约花 **\$450,000**，超支 **\$50,000**。

**局限**：这个公式假设**未来的成本效率和过去一样**。如果超支原因是一次性的（例如前期采购了许可证），EAC 会高估；如果后面还有更难的工作（支付集成缺陷多），EAC 会低估。它也只预测成本，不反映进度落后带来的额外成本。所以 EAC 要在项目过程中定期重算，并结合原因分析。

**English answer (unofficial)**

- EAC = BAC / CPI = 400,000 / 0.889 = **\$450,000** (equivalently 400,000 × 180,000 / 160,000).
- VAC = BAC − EAC = 400,000 − 450,000 = **−\$50,000**, so the project is forecast to finish \$50,000 over budget if nothing changes.
- **Limitation:** the CPI method assumes future work will be performed at the same cost efficiency as past work. If the overrun came from a one-off cost, the EAC overstates the final cost; if the remaining work is harder (for example, fixing payment defects), it understates it. The forecast should be recalculated regularly and combined with an analysis of the causes.

#### 2(c) 中文解析

**Pareto 图**：把缺陷类别按数量从高到低排成柱状图，再画累计百分比折线。这里登录 52 + 支付 34 = 86，占 120 的 **71.7%**——两个类别贡献了七成多的缺陷，符合 80/20 法则。团队应**优先集中资源解决登录和支付缺陷**，而不是平均用力。

**QA vs QC 各一项行动**：

- **QC（事后，检查产出）**：对登录和支付模块做针对性回归测试，记录缺陷并在修复后复测，按验收标准决定是否接受；
- **QA（事前，预防缺陷）**：对认证和支付代码引入强制同行评审和编码规范检查，或用鱼骨图分析根本原因（例如需求不清、第三方支付接口文档不足），改进开发流程，防止同类缺陷再出现。

**English answer (unofficial)**

- A **Pareto chart** ranks defect categories from most to least frequent as bars, with a cumulative percentage line. Login (52) and payment (34) account for 86 of 120 defects, or **71.7%**, so a small number of causes produce most of the problems (the 80/20 rule).
- The team should therefore focus testing and fixing effort on the login and payment modules first, rather than spreading effort evenly across all four categories.
- **Quality control action (after the fact):** run targeted regression tests on login and payment, log each defect, retest fixes, and make acceptance decisions against the agreed criteria.
- **Quality assurance action (preventive):** introduce mandatory peer review and coding standards for authentication and payment code, and use a cause-and-effect diagram to find the root causes (for example, unclear requirements or poor payment-gateway documentation), so similar defects do not recur.

---

### 仿真题 3（15 分）医疗网络排班系统：采购与风险

> **Question 3 [15 points]** A regional health network wants a new staff rostering system for 12 hospitals. The internal IT team has no rostering expertise, and the business requirements are still being clarified. Management is considering an offshore vendor to reduce cost. The system will store staff personal and payroll data.
>
> (a) Using make-or-buy analysis, recommend whether the health network should build the system internally or buy it from a vendor. Justify your recommendation with two relevant factors. (4 points)
>
> (b) Explain the difference between a Request for Proposal (RFP) and a Request for Quotation (RFQ). Recommend which document should be issued and suggest a suitable contract type, explaining how it allocates risk between buyer and seller. (5 points)
>
> (c) Identify two risks of using an offshore vendor for this project. For each, recommend an appropriate risk response strategy and a specific action. (6 points)

#### 3(a) 中文解析

推荐 **Buy（外购）**。理由选两个和情景相关的因素：

1. **专业能力**：内部团队没有排班领域经验，自建需要学习时间，质量和进度风险都高；成熟供应商已有排班规则引擎和医院行业经验。
2. **时间与成本**：12 家医院同时上线，外购可以基于现成产品配置，比从零开发快；总拥有成本通常也更低。

需要补一句**控制与保密**：员工个人和薪资数据敏感，外购时必须在合同里约束数据处理方式（衔接 3(c)）。

**English answer (unofficial)**

- **Recommendation: buy** the rostering system from a specialist vendor.
- **Expertise:** the internal IT team has no rostering expertise. Building in-house would require learning complex award and shift rules, raising quality and schedule risk, while a vendor brings an existing rules engine and health-sector experience.
- **Time and cost:** configuring an existing product for 12 hospitals is faster than building from scratch, and the development and maintenance cost is shared across the vendor's customers.
- **Condition:** because the system stores staff personal and payroll data, control and confidentiality must be protected through contract terms on data handling and security.

#### 3(b) 中文解析

| | RFP | RFQ |
|:---|:---|:---|
| 什么时候用 | 需求**不清楚**，希望供应商提出解决方案 | 需求**明确、标准化** |
| 要供应商给什么 | 方案、方法、经验、价格 | 主要是**价格**、交付和付款条件 |

本题需求仍在澄清、需要供应商提出方案 → **发 RFP**，并附 SOW 说明已知范围和评估标准（可用加权评分比较供应商）。

**合同类型**：需求不清楚时直接签固定总价，供应商会把不确定性加进报价，或后期频繁提变更。合理的做法是**分阶段**：需求澄清和方案设计阶段用 **T&M（工料合同）**，买方承担中等风险、按实际工时付费；需求和 SOW 确定后，实施阶段改用**固定总价（FFP）**，超支风险转给卖方，买方风险最低。

**English answer (unofficial)**

- An **RFP** is used when requirements are not fully defined and the buyer wants vendors to propose a solution, approach and price. An **RFQ** is used when requirements are clear and standardised, and the buyer mainly wants price, delivery and payment terms.
- Requirements are still being clarified and the network needs vendor expertise, so it should **issue an RFP**, referencing a Statement of Work with the known scope and the evaluation criteria (for example, weighted scoring).
- **Contract type:** a phased approach. Use **time and materials** for the discovery and design phase, where the buyer pays for actual effort and carries a moderate share of the risk while scope is uncertain. Once requirements and the SOW are agreed, use a **firm fixed-price** contract for implementation, which transfers cost-overrun risk to the seller and gives the buyer the lowest risk.

#### 3(c) 中文解析

| 风险 | 类别 | 应对策略 | 具体行动 |
|:---|:---|:---|:---|
| 员工个人与薪资数据跨境处理，可能违反隐私法规或发生数据泄露 | 技术 / 合规 | **Avoid** 或 **Transfer** | 合同要求数据存放在澳大利亚境内（规避跨境）；合同约定安全标准、审计权和违约赔偿（转移财务后果） |
| 时差和沟通障碍导致需求误解、反馈慢、交付延误 | 人员 / 流程 | **Mitigate** | 约定每天重叠的工作时段，每两周演示可运行版本，指定双方联络人；用记分卡跟踪交付准时率 |

每项风险都应写进**风险登记册**，指定负责人并定期复核。

**English answer (unofficial)**

- **Risk 1, data privacy and compliance:** staff personal and payroll data processed offshore could breach privacy obligations or be exposed in a security incident. **Response: avoid / transfer.** Require in the contract that data is hosted in Australia (avoiding cross-border transfer), and specify security standards, audit rights and penalty clauses, so financial consequences are transferred to the vendor.
- **Risk 2, communication and time zones:** working across time zones may cause misunderstood requirements, slow feedback and late delivery. **Response: mitigate.** Agree daily overlapping working hours, hold fortnightly demos of working software, appoint a single point of contact on each side, and monitor on-time delivery with a vendor scorecard.
- Both risks should be recorded in the **risk register** with an owner, and reviewed regularly throughout the project.

---

### 仿真题 4（15 分）学生门户宕机：ITSM 实践与 SLA

> **Question 4 [15 points]** On the first day of enrolment, a university's student portal crashed three times. Each time the service desk restarted the application server and service returned within 20 minutes. Investigation later showed that a memory leak had been introduced by an urgent update that was deployed the night before without testing. On another day that month, an unplanned network outage made the portal unavailable for 1.5 hours.
>
> (a) Using ITIL 4, distinguish between incident management and problem management, and explain how each practice should respond in this scenario. (5 points)
>
> (b) Explain the purpose of change enablement. Discuss how the way the update was deployed contributed to the outages, and recommend one improvement to the change process. (4 points)
>
> (c) The SLA defines agreed service hours as 7:00 am to 11:00 pm every day (30-day month), with an availability target of 99.5%. Calculate the portal's availability for the month, state whether the target was met, and calculate the maximum downtime the SLA allows. Recommend one action that service level management should take. (6 points)

#### 4(a) 中文解析

| | Incident Management | Problem Management |
|:---|:---|:---|
| 目标 | **尽快恢复**正常服务，减少影响 | 找到并消除**根本原因**，防止再次发生 |
| 本题怎么做 | 服务台记录三次宕机工单，按影响（选课首日、全体学生）定为高优先级，重启服务器恢复服务，通知用户 | 三次同类事件触发问题记录；分析日志找到内存泄漏，确认来自前一晚的更新；记录为**已知错误**，在修复前把「重启服务器」作为**变通方案**写进知识库；最终通过回滚或补丁修复 |

重启服务器只是事件管理层面的恢复；不做问题管理，宕机会反复出现。

**English answer (unofficial)**

- **Incident management** aims to restore normal service as quickly as possible and minimise business impact. Here, the service desk should log each crash, prioritise it as high impact (enrolment day, all students affected), restore service by restarting the server, and communicate status to users.
- **Problem management** aims to find and remove the root cause so incidents do not recur. Three similar incidents should trigger a problem record; analysis traces the memory leak to the previous night's update; it is recorded as a **known error**, with the restart documented as a **workaround** in the knowledge base until a permanent fix (rollback or patch) is deployed.
- Restarting only treats the symptom. Without problem management, the portal would keep crashing during the busiest period.

#### 4(b) 中文解析

**变更实施（Change Enablement）** 的目的：通过评估风险、授权和安排变更，**在变更速度和服务稳定性之间取得平衡**，最大化成功变更的数量。

本题的更新是「紧急」但**没有测试**，直接在选课首日前一晚上线——既没评估对高峰期的影响，也没有回滚计划，导致了内存泄漏和三次宕机。

**改进**：区分三类变更——**standard**（预授权、低风险）、**normal**（需评估和授权）、**emergency**（加速授权，但仍需最低限度的测试和回滚计划）；并设置**变更冻结期**：选课等关键时段前不部署非必要变更。

**English answer (unofficial)**

- **Change enablement** maximises the number of successful changes by assessing risk, authorising changes and scheduling them, balancing speed of change against service stability.
- The update was treated as urgent but was deployed **without testing, risk assessment or a rollback plan**, the night before the portal's busiest day. This introduced the memory leak that caused the three outages.
- **Improvement:** classify changes as standard (pre-authorised, low risk), normal (assessed and authorised) or emergency (expedited approval, but still with minimum testing and a rollback plan). Also introduce a **change freeze** before peak periods such as enrolment, so non-essential changes are not deployed then.

#### 4(c) 中文解析

约定服务时间：每天 16 小时 × 30 天 = **480 小时**。宕机：3 × 20 分钟 = 1 小时，加 1.5 小时 = **2.5 小时**。

$$
\text{Availability} = \frac{480 - 2.5}{480} \times 100\% = \frac{477.5}{480} \times 100\% \approx 99.48\%
$$

99.48% < 99.5%，**未达标**。SLA 允许的最大宕机：

$$
480 \times (1 - 0.995) = 2.4 \text{ 小时} = 144 \text{ 分钟}
$$

实际 150 分钟，超出 6 分钟。

**SLM 应采取的行动**：在服务评审会上向干系人报告这次违约及原因（未测试的变更 + 网络故障），与问题管理、变更管理一起制定改进计划；同时检查 SLA 指标是否足够——选课期间可以单独设更严格的可用性目标和更快的响应时间。

**English answer (unofficial)**

- Agreed service time = 16 hours × 30 days = **480 hours**. Downtime = 3 × 20 minutes + 1.5 hours = **2.5 hours**.
- Availability = (480 − 2.5) / 480 × 100% = 477.5 / 480 × 100% ≈ **99.48%**, which is **below the 99.5% target**, so the SLA was breached.
- Maximum allowed downtime = 480 × (1 − 0.995) = **2.4 hours (144 minutes)**; actual downtime was 150 minutes, 6 minutes over.
- **SLM action:** report the breach and its causes (the untested change and the network outage) at the service review with stakeholders, agree an improvement plan with problem and change management, and review whether the SLA needs a stricter availability target and faster response times during peak periods such as enrolment.

---

## 十五、复习清单

| 周 | 必会 | 典型考法 |
|:---|:---|:---|
| W1 | 项目四特征、三重约束、成功维度、项目/项目集/组合 | 三项达标是否算成功 |
| W2 | Waterfall / Agile / DevOps、需求收集五技术 | 方法论选型 + 理由 |
| W3 | WBS、AON / AOA / PDM、四种依赖、PERT、关键路径、赶工 vs 快速跟进 | 算关键路径、压缩工期 |
| W4 | 估算技术、PV / EV / AC、CV / SV / CPI / SPI / EAC | EVM 计算与解读 |
| W5 | QA vs QC、验证 vs 确认、质量工具（鱼骨图、控制图、Pareto 等） | 给情景选工具 |
| W6 | 领导风格、内外动机、RACI、资源平衡、Tuckman、冲突五模式 | 团队冲突怎么处理 |
| W7 | 风险类别、风险偏好、概率×影响、威胁与机会的应对、风险登记册 | 识别风险 + 应对 + 行动 |
| W8 | make-or-buy、SOW / RFP / RFQ、合同类型与风险、供应商评估、外包模式 | 选采购文档和合同 |
| W9 | Leader vs Manager、adaptive leadership、治理机制、一致性框架 | 治理机制怎么用 |
| W10 | 知识领域 × 阶段、IT 项目特点、CCB 等整合工具 | 变更怎么走流程 |
| W11 | ITSM、产品 vs 服务、PM vs ITSM、服务关系模型、四维度 | 判断模型 + 四维度分析 |
| W12 | SVS 组件、SVC 六活动、八个关键实践、可用性计算 | 用实践处理情景、SLA 计算 |
