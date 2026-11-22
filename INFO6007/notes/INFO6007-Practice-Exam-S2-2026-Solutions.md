---
title: INFO6007 Practice Exam（S2 2026）整卷逐题解析
categories:
  - Course Notes
  - INFO6007
tags:
  - INFO6007
  - Exam-Review
  - Project-Management
description: >-
  INFO6007 Semester 2 2026 Practice Exam 整卷逐题解析：4 道情景大题共 12 个小问——Waterfall vs Agile 选型、范围蔓延与变更控制、PERT 三点估算、
  需求收集技术、按成熟度调整领导风格、上线前风险识别与应对、WBS 的作用、EMV 判断是否批准测试、make-or-buy 分析、SPI/CPI 计算与解读、
  Tuckman 模型与团队变动、服务级别管理的可衡量目标。课程没有发布官方答案（Model Answer Sheet 只是空白答题纸），全部为自拟答案框架。
mathjax: true
abbrlink: info6007-practice-exam-s2-2026-solutions
date: 2026-11-03 22:00:00
---

# INFO6007 Practice Exam（S2 2026）整卷逐题解析

> - **课程**：INFO6007 — Project Management in IT
> - **材料**：`Exam Prep/INFO6007 Practice Exam - S2 2026.pdf`（18 页）；同目录的 `Model Answer Sheet-[print double-sided] INFO6007.pdf` 我打开看过，**是空白答题纸**（每页只写「Question will be revealed by the tutor on screen」和 (a)(b)(c) 答题框），**不是参考答案**。
> - **⚠️ 答案来源**：**全部为自拟、非官方**的答案框架。计算题结果是确定的；论述题按课程讲义的概念组织，与各周笔记里「📝 考试相关」提示的方向一致。
> - **形式**：答题 2 小时 + 阅读 10 分钟；**限制性开卷**——可带一张 A4 双面手写/打印笔记、双语词典、非编程计算器；**4 道题 × 15 分 = 60 分**，每题一个情景 + (a)(b)(c) 三个小问。

## 答题方法（适用于每个小问）

INFO6007 的论述题几乎都是同一个结构：**定义/解释概念 → 结合情景分析 → 给出推荐并说明理由（必要时写假设）**。题干里的每个动词都是一个得分点：

| 动词 | 要写什么 |
|:---|:---|
| Explain / Discuss | 概念是什么 + 为什么在这个情景里重要 |
| Compare | 逐个维度并列对比（最好用表格） |
| Recommend / Propose | 明确选一个 + 具体做法 + 理由 |
| Evaluate / Critically assess | 先判断对错，再说依据和例外 |
| Calculate | 写公式 → 代数 → 结果带单位 → 解读 |
| State assumptions | 单独列出，题目要求时漏写会扣分 |

---

## Question 1（15 分）大学移动应用

> **Original question (English)** · Question 1 [15 points] A university is developing a mobile application that will allow students to manage enrolments, receive announcements, and access digital student ID cards. The university plans to release an initial version before the start of the next semester but expects additional features to be introduced throughout the following year.

情景：大学开发一款管理选课、接收公告、电子学生证的 App，下学期开学前先发布初版，之后一年内持续加功能。

### 1(a)（5 分）Waterfall 还是 Agile？

> **Original question (English)** · 1 (a) The project sponsor is deciding whether to use a Waterfall or Agile project management methodology. Compare the two methodologies in terms of their approach to planning, stakeholder involvement, and managing changing requirements. Recommend the methodology that is most appropriate for this project and justify your recommendation. (5 points)

**对比**：

| 维度 | Waterfall | Agile |
|:---|:---|:---|
| 规划 | 前期一次性详细规划，阶段顺序推进，范围先固定 | 滚动式/迭代规划，每个 sprint 规划下一批待办，范围随反馈调整 |
| 干系人参与 | 主要在需求阶段和验收阶段 | 全程持续参与：sprint review、Product Owner 排优先级 |
| 需求变更 | 走正式变更控制，后期变更代价高 | 欢迎变更，通过 backlog 重新排序吸收 |

**推荐 Agile（或以 Agile 为主的 Hybrid）**，理由结合情景：

1. 有**明确的初版截止**（开学前）+ **之后一年持续加功能** → 适合先交付 MVP（选课、公告、电子学生证），再按迭代增量发布；
2. 用户是学生、院系等**多类干系人**，需求会随使用反馈变化，Agile 的持续参与能及早发现问题；
3. 移动应用可以频繁发版，技术上支持增量交付。

可以补一句：电子学生证涉及身份与隐私，**安全和合规要求**可以在早期用 Waterfall 式的方式固定下来（Hybrid）。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week02-PM-Methodologies-Summary|W02 项目管理方法论]]、[[26-S2-Course/INFO6007/INFO6007-Week03-Tutorial-Methodology-Stakeholder|W03 Tutorial 方法论选型]]

**English answer (Unofficial, self-drafted) — model answer**

- **Planning:** Waterfall plans the whole project in detail up front and moves through fixed sequential phases; Agile plans iteratively, refining the backlog sprint by sprint.
- **Stakeholder involvement:** Waterfall involves stakeholders mainly at requirements and acceptance; Agile involves them continuously (Product Owner prioritisation, sprint reviews).
- **Changing requirements:** Waterfall handles change through formal change control, and late changes are costly; Agile expects change and absorbs it by re-prioritising the backlog.
- **Recommendation: Agile (or an Agile-led hybrid).** The app has a fixed first-release date before semester starts, followed by a year of new features, so the team can ship an MVP (enrolment, announcements, digital ID) and add features in increments.
- Students and departments will give feedback once they use the app, and mobile releases can be frequent, so continuous involvement reduces the risk of building the wrong features. Security and privacy requirements for the digital ID can be fixed early (the hybrid element).

### 1(b)（5 分）范围蔓延

> **Original question (English)** · 1 (b) During development of the university mobile application, several departments request additional features, including event registration and campus navigation. Developers begin implementing these features without formally assessing their impact or obtaining approval. The original release deadline and budget remain unchanged. Explain why this situation represents scope creep and discuss two potential consequences for the project. Recommend a practical measure the project manager should take to control scope while allowing useful changes to be considered. (5 points)

**为什么是 scope creep**：范围蔓延 = **未经控制地**增加范围。这里各院系提出新功能（活动报名、校园导航），开发者**没有评估影响、没有获得批准**就开始做，而**截止日期和预算不变**——三重约束中只有范围在增长，没有对应调整时间和成本。

**两个后果**（任选两个并结合情景）：

1. **进度延误**：初版可能赶不上开学，核心功能（选课、学生证）反而受影响；
2. **成本超支 / 团队过载**：预算不变而工作量上升，靠加班硬扛；
3. **质量下降**：测试时间被压缩，缺陷增多；
4. **干系人不满与基线失效**：范围基线和计划失去意义，无法衡量进度。

**措施：建立正式的整体变更控制流程**——所有变更请求提交到 change log，PM 评估对范围、进度、成本、质量和风险的影响，由**变更控制委员会（CCB）/ 赞助人**审批；获批的变更更新基线，有价值但不紧急的需求放进**后续版本的 backlog**（与 1(a) 的迭代发布衔接）。这样既控制范围，又不拒绝有用的变更。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week03-Scope-Schedule-Management-Summary|W03 范围管理]]、[[26-S2-Course/INFO6007/INFO6007-Week10-Integration-Management-Summary|W10 整体变更控制]]、[[26-S2-Course/INFO6007/INFO6007-Week04-Tutorial-Scope-WBS-Critical-Path|W04 Tutorial 范围蔓延]]

**English answer (Unofficial, self-drafted) — model answer**

- **Why scope creep:** scope creep is the uncontrolled growth of scope. New features (event registration, campus navigation) are being built without impact assessment or approval, while the deadline and budget stay the same, so only scope grows in the triple constraint.
- **Consequence 1 – schedule delay:** effort moves to unplanned features, so the initial release may miss the start of semester and core features (enrolment, digital ID) may be delayed.
- **Consequence 2 – cost overrun / lower quality:** with a fixed budget, extra work leads to overtime and compressed testing, so more defects reach students, and the scope baseline no longer measures progress.
- **Measure – formal integrated change control:** every request goes into a change log; the PM assesses its impact on scope, time, cost, quality and risk; the sponsor or a change control board approves or rejects it; approved changes update the baseline.
- Useful but non-urgent requests (e.g. campus navigation) go into the backlog for a later release, so good ideas are kept without endangering the first release.

### 1(c)（5 分）PERT 三点估算

> **Original question (English)** · 1 (c) The team provides the following duration estimates for integrating the digital student ID feature: Optimistic duration: 4 days; Most likely duration: 7 days; Pessimistic duration: 16 days. Calculate the expected activity duration using the PERT three-point estimation method, showing your working. Explain why this method is useful when activity durations are uncertain. Identify one limitation of using the calculated estimate to commit to a delivery date, relating your explanation to the figures provided. (5 points)

$O = 4$，$M = 7$，$P = 16$ 天：

$$
t_E = \frac{O + 4M + P}{6} = \frac{4 + 28 + 16}{6} = \frac{48}{6} = 8\ \text{天}
$$

（可选）标准差 $\sigma = \frac{P - O}{6} = \frac{12}{6} = 2$ 天。

**为什么有用**：不确定时单点估计容易过于乐观；三点估算把**乐观、最可能、悲观**情况都考虑进去，按 Beta 分布加权，得到更现实的期望值，还能给出波动范围（σ），用来设缓冲。

**局限（结合数字）**：8 天是**期望值（平均）**，不是保证。这里分布**明显右偏**——悲观值 16 天离最可能值 7 天很远，说明集成存在较大的下行风险。按 8 天承诺交付，大约只有一半左右的把握；更稳妥的做法是用 $t_E + \sigma = 10$ 天或 $t_E + 2\sigma = 12$ 天，或加入应急缓冲。另外三个输入本身也是主观估计，团队缺乏经验时可能都偏乐观。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week03-Scope-Schedule-Management-Summary|W03 三点估算 / PERT]]、[[26-S2-Course/INFO6007/INFO6007-Week06-Resource-Management-Summary|W06 活动资源与工期估算]]

**English answer (Unofficial, self-drafted) — model answer**

- **Calculation:** t_E = (O + 4M + P) / 6 = (4 + 4×7 + 16) / 6 = 48 / 6 = **8 days** (standard deviation σ = (P − O)/6 = 12/6 = 2 days).
- **Why useful:** a single-point estimate is often optimistic; PERT combines the best, most likely and worst cases (beta-weighted) into a more realistic expected value, and σ shows how uncertain the estimate is, which helps set buffers.
- **Limitation:** 8 days is an expected (average) value, not a guarantee. The distribution is right-skewed – the pessimistic 16 days is far above the most likely 7 days – so committing to 8 days gives only about a 50% chance of finishing on time. A safer commitment is t_E + σ = 10 days or t_E + 2σ = 12 days, or adding a contingency buffer. The three inputs are also subjective estimates.

---

## Question 2（15 分）市政建筑许可在线申请系统

> **Original question (English)** · Question 2 [15 points] A local council is developing an online permit application system that allows residents to apply for building permits, upload supporting documents, and track application progress.

### 2(a)（4 分）需求收集为什么重要 + 两个技术

> **Original question (English)** · 2 (a) During planning, several stakeholders provide different expectations for the new system. Explain why effective requirements gathering is important in IT projects. Recommend two techniques that the project manager could use to collect accurate requirements from stakeholders. (4 points)

**重要性**：需求是范围、WBS、估算和验收的基础。干系人期望不同（居民、审批员、IT、财务），如果不及早澄清和协调，会导致**错误的系统、返工、范围蔓延、上线后采用率低**。修复需求阶段遗漏的缺陷，越到后期成本越高。

**两个技术**（推荐并说明为什么适合本情景）：

1. **访谈 / 焦点小组**：分别访谈审批员和前台员工，了解现有流程痛点；用焦点小组让不同干系人当面协调分歧；
2. **工作坊（JAD）+ 原型**：把各方放在一起梳理端到端流程（申请 → 上传文件 → 审批 → 跟踪进度），用线框图/原型让居民代表试用，尽早暴露误解。

（其他可答：问卷调查（覆盖大量居民）、观察现有流程、文档分析（现行法规和表格）。）

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week03-Scope-Schedule-Management-Summary|W03 收集需求]]、[[26-S2-Course/INFO6007/INFO6007-Week03-Tutorial-Methodology-Stakeholder|W03 Tutorial 干系人分析]]

**English answer (Unofficial, self-drafted) — model answer**

- **Importance:** requirements are the basis of scope, the WBS, estimates and acceptance criteria. Residents, permit assessors, IT and finance expect different things; if these are not clarified and reconciled early, the project risks building the wrong system, rework, scope creep and low adoption, and fixing a missed requirement costs more the later it is found.
- **Technique 1 – interviews / focus groups:** interview assessors and front-desk staff about pain points in the current permit process, and use a focus group to resolve conflicting expectations face to face.
- **Technique 2 – workshops with prototypes:** bring stakeholders together to walk through the end-to-end flow (apply → upload documents → assessment → track progress), and let resident representatives try wireframes or a prototype so misunderstandings surface early.

### 2(b)（5 分）对所有人都用指令式领导是否合适

> **Original question (English)** · 2 (b) During development of the council permit application system, the experienced software developers want greater autonomy in deciding how to complete their tasks. However, newly assigned council staff are unfamiliar with project work and need clear guidance. The project manager currently uses the same directive approach with everyone. Evaluate the suitability of this approach. Recommend how the project manager should adapt their leadership approach for each group, explaining how your recommendations could improve team performance. (5 points)

**评价**：不合适。一刀切的指令式风格**压制了资深开发者**（他们有能力自主决策，被微观管理会降低积极性和效率，甚至流失），**对新员工也不够**（他们需要的不只是命令，还有解释和辅导）。领导风格应**按成员的能力和成熟度调整**（情境领导）。

**推荐**：

| 群体 | 风格 | 具体做法 | 对绩效的作用 |
|:---|:---|:---|:---|
| 资深开发者 | **授权 / 参与式（delegating / participative）** | 给出目标和约束，让他们决定实现方式；请他们参与技术决策、担任导师 | 提高内在激励（自主、精通），决策更快，留住骨干 |
| 新调来的市政员工 | **指令式 + 辅导（directing → coaching）** | 明确任务、标准、截止时间，配导师，定期检查并解释原因 | 减少错误和返工，随能力提升逐步放手 |

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week06-Resource-Management-Summary|W06 领导风格与激励]]、[[26-S2-Course/INFO6007/INFO6007-Week09-Leadership-Governance-Alignment-Summary|W09 领导力]]

**English answer (Unofficial, self-drafted) — model answer**

- **Evaluation:** a single directive style is not suitable. It micromanages the experienced developers, which lowers their motivation and productivity and risks losing them, and it gives new staff instructions without the explanation and coaching they need. Leadership should match each person's competence and maturity (situational leadership).
- **Experienced developers – delegating / participative:** set goals and constraints, let them decide how to implement, involve them in technical decisions and ask them to mentor others. This builds intrinsic motivation (autonomy, mastery), speeds up decisions and retains key people.
- **New council staff – directing moving to coaching:** give clear tasks, standards and deadlines, pair them with a mentor, check in regularly and explain the reasons behind decisions. This reduces errors and rework, and the PM can step back as their skills grow.
- **Effect on performance:** each group gets the support it needs, so the team delivers faster with fewer defects and higher morale.

### 2(c)（6 分）上线前的两项风险

> **Original question (English)** · 2 (c) The council plans to launch the permit application system before its busiest application period. However, integration testing with the existing payment system is incomplete, and only half of the council staff have attended training. Identify two distinct project risks arising from this situation and explain the potential impact of each. For each risk, recommend an appropriate risk response strategy and describe one specific action the project manager should take to implement it. (6 points)

| | 风险 1：支付系统集成失败 | 风险 2：员工培训不足 |
|:---|:---|:---|
| 原因 | 与现有支付系统的集成测试未完成 | 只有一半员工参加了培训 |
| 影响 | 繁忙期居民无法缴费 → 申请卡住、收入受损、投诉与声誉损失、可能需要手工处理 | 员工不会处理申请或回答居民问题 → 审批变慢、错误增多、积压、对新系统的抵触 |
| 应对策略 | **Mitigate（减轻）**（若无法按时完成，可 **Avoid**：推迟上线到测试通过） | **Mitigate（减轻）** |
| 具体行动 | 在上线前完成端到端集成测试并设定**上线准入标准（go/no-go）**；准备回退方案（保留旧缴费渠道）；指定风险责任人 | 上线前安排补训（多场次/录播）、制作快速参考指南和知识库，上线首周安排**超级用户/现场支持** |

（也可以把「繁忙期上线」本身作为风险：用 **Avoid**——在繁忙期之前留出缓冲，或推迟到繁忙期之后上线。）

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week07-Risk-Management-Summary|W07 风险识别与应对策略]]

**English answer (Unofficial, self-drafted) — model answer**

- **Risk 1 – payment integration failure:** integration testing with the existing payment system is incomplete. **Impact:** during the busiest period residents may be unable to pay, so applications stall, revenue is lost, complaints rise and staff may have to process payments manually.
- **Response: mitigate** (or **avoid** by postponing launch until testing passes). **Action:** complete end-to-end integration testing before launch with a formal go/no-go criterion, assign a risk owner, and keep the old payment channel as a fallback.
- **Risk 2 – insufficient staff training:** only half of the staff are trained. **Impact:** staff cannot process applications or answer residents' questions, so approvals slow down, errors and backlogs grow, and staff resist the new system.
- **Response: mitigate.** **Action:** run additional training sessions (several time slots or recorded) before launch, provide quick-reference guides and a knowledge base, and place super-users / floor support on site during the first week.

---

## Question 3（15 分）员工在线培训平台

> **Original question (English)** · Question 3 [15 points] A software company is developing an online employee training platform that allows staff to complete courses, undertake assessments, and track professional development.

### 3(a)（4 分）WBS 的目的

> **Original question (English)** · 3 (a) The project manager asks the team to develop a Work Breakdown Structure (WBS) before estimating costs and preparing the project schedule. Explain the purpose of a WBS and discuss how it supports effective project planning using the scenario. (4 points)

**定义**：WBS 是把项目的全部工作**按可交付成果逐层分解**成更小、可管理的工作包；遵守 **100% 规则**（包含且只包含全部工作）。

**如何支撑规划（结合情景）**：

1. **范围完整**：例如分解为 课程管理模块 / 测评模块 / 职业发展跟踪 / 用户与权限 / 测试 / 部署与培训，避免遗漏（如数据迁移、用户培训）；
2. **估算的基础**：成本和工期在工作包层面估算，再自下而上汇总，比整体估算准确；
3. **进度计划**：工作包进一步分解为活动 → 排序 → 网络图和关键路径；
4. **责任分配**：每个工作包有明确负责人（配合 RACI），也是 EVM 中衡量进度的单位。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week03-Scope-Schedule-Management-Summary|W03 创建 WBS]]、[[26-S2-Course/INFO6007/INFO6007-Week04-Tutorial-Scope-WBS-Critical-Path|W04 Tutorial WBS]]

**English answer (Unofficial, self-drafted) — model answer**

- **Purpose:** a WBS decomposes all project work, deliverable by deliverable, into smaller manageable work packages, following the 100% rule (all of the work and only the work).
- **Complete scope:** for the training platform – course management, assessment module, professional-development tracking, user accounts and permissions, testing, deployment and user training – so nothing (e.g. data migration) is missed.
- **Basis for estimates and schedule:** cost and duration are estimated per work package and rolled up bottom-up, which is more accurate than one top-down guess; work packages are broken into activities that are sequenced into the network diagram and critical path.
- **Accountability and control:** each work package gets an owner (with a RACI) and becomes the unit for tracking progress, e.g. in earned value.

### 3(b)（5 分）EMV：是否批准额外测试

> **Original question (English)** · 3 (b) The team estimates a 25% probability that an assessment-processing defect will require \$120,000 in corrective work. An additional testing programme costing \$24,000 would reduce this probability to 10%. The cost of corrective work, if required, would remain unchanged. Calculate: the expected monetary cost of the risk without additional testing; the total expected cost, including the testing programme, with additional testing. Show your working and recommend whether the additional testing programme should be approved based on your calculations. (5 points)

$$
\text{不测试：}EMV = 0.25\times\$120{,}000 = \$30{,}000
$$

$$
\text{测试：}\$24{,}000 + 0.10\times\$120{,}000 = \$24{,}000 + \$12{,}000 = \$36{,}000
$$

**建议：仅从 EMV 看不批准**——测试后总期望成本 \$36,000 > \$30,000，多花 \$6,000；测试带来的期望损失减少（\$18,000）抵不上测试本身的成本（\$24,000）。

**补充**（拿满分的关键）：EMV 是长期平均值。如果组织**风险规避**，或这个缺陷还会带来**未量化的影响**（学员成绩错误、声誉、合规），或者测试能同时发现其他缺陷，那么仍可以考虑批准——要写明这些假设。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week07-Risk-Management-Summary|W07 EMV 与定量风险分析]]

**English answer (Unofficial, self-drafted) — model answer**

- **Without testing:** EMV = 0.25 × \$120,000 = **\$30,000**.
- **With testing:** \$24,000 + 0.10 × \$120,000 = \$24,000 + \$12,000 = **\$36,000**.
- **Recommendation:** on EMV alone, **do not approve** – testing raises the total expected cost by \$6,000, because the reduction in expected loss (\$30,000 − \$12,000 = \$18,000) is smaller than the \$24,000 cost of the programme.
- **Caveat (state assumptions):** EMV is a long-run average. If the organisation is risk-averse, or the defect has unquantified impacts (wrong assessment results, reputation, compliance), or the testing would also find other defects, approving the programme could still be justified.

### 3(c)（6 分）测评编写组件 make-or-buy

> **Original question (English)** · 3 (c) The platform requires an assessment-authoring component. Developing it internally would allow close customisation, but the team has limited experience with this type of component. An existing commercial component could be available sooner, although it would involve recurring licence fees and offer less flexibility. Conduct a make-or-buy analysis using three relevant factors. For each factor, compare the implications of developing the component internally and purchasing it. Recommend one option, justifying your recommendation. State any assumptions. (6 points)

| 因素 | Make（内部开发） | Buy（商业组件） |
|:---|:---|:---|
| **时间** | 团队缺乏经验 → 学习曲线长，进度风险高 | 现成可用，上线更快 |
| **成本** | 一次性开发成本高，后期维护自担 | 前期投入低，但有**持续许可费**——要按 3–5 年 TCO 比较 |
| **控制 / 灵活性** | 可深度定制、自主演进、掌握数据 | 灵活性低，受供应商路线图约束，存在**供应商锁定** |

（也可以用「风险」「质量」「内部能力」作为因素。）

**推荐示例：Buy**。**假设**：测评编写不是平台的核心差异化能力；上线时间紧；按 5 年计算许可费总额仍低于内部开发 + 维护成本；商业组件能满足主要测评题型。同时在合同中争取 **API / 数据导出**能力和 SLA，以降低锁定风险。

（反过来，如果测评编写是公司的核心竞争力且时间充裕，就应 Make——关键是**推荐要与假设一致**。）

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week08-Procurement-Management-Summary|W08 Make-or-Buy 分析]]

**English answer (Unofficial, self-drafted) — model answer**

- **Time:** Make – limited experience means a learning curve and high schedule risk; Buy – available sooner, so the platform launches faster.
- **Cost:** Make – high one-off development cost plus ongoing maintenance carried in-house; Buy – lower upfront cost but recurring licence fees, so compare total cost of ownership over 3–5 years.
- **Control / flexibility:** Make – full customisation and control of the roadmap and data; Buy – less flexibility, dependence on the vendor's roadmap, and vendor lock-in.
- **Recommendation: Buy.** Assumptions: assessment authoring is not the platform's core differentiator; time to market matters; licence fees over 5 years cost less than building and maintaining the component; the product supports the main question types.
- Reduce the lock-in risk by negotiating API / data-export access and an SLA in the contract. (If authoring were a core competitive capability and time allowed, Make would be justified – the recommendation must follow from the stated assumptions.)

---

## Question 4（15 分）零售连锁云库存管理系统

> **Original question (English)** · Question 4 [15 points] A software company is developing a cloud-based inventory management system for a national retail chain. The system will automate stock tracking, generate purchasing recommendations, and provide real-time inventory reporting across hundreds of stores. The project has a planned duration of 10 months.

计划工期 10 个月。

### 4(a)（4 分）SPI 与 CPI

> **Original question (English)** · 4 (a) At the end of Month 4, the project manager reviews the following performance data: Planned Value (PV): \$300,000; Earned Value (EV): \$240,000; Actual Cost (AC): \$320,000. Calculate the Schedule Performance Index (SPI) and Cost Performance Index (CPI), showing your working. Interpret what each result indicates about the project's current performance. (4 points)

$$
SPI = \frac{EV}{PV} = \frac{240{,}000}{300{,}000} = 0.80,\qquad CPI = \frac{EV}{AC} = \frac{240{,}000}{320{,}000} = 0.75
$$

**解读**：

- **SPI = 0.80 < 1 → 进度落后**：只完成了计划工作价值的 80%（SV = −\$60,000）；
- **CPI = 0.75 < 1 → 成本超支**：每花 \$1 只挣到 \$0.75 的价值（CV = −\$80,000）。
- 项目**又慢又贵**，而且已经进行到 40%，需要尽快查原因并纠偏；不纠偏的话最终成本会显著超出预算（EAC = BAC / 0.75）。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week04-Cost-Management-Summary|W04 挣值管理]]、[[26-S2-Course/INFO6007/INFO6007-Week05-Tutorial-EVM-Exercises|W05 Tutorial EVM 计算]]

**English answer (Unofficial, self-drafted) — model answer**

- **SPI** = EV / PV = 240,000 / 300,000 = **0.80**. SPI < 1, so the project is **behind schedule**: only 80% of the planned work has been completed (SV = −\$60,000).
- **CPI** = EV / AC = 240,000 / 320,000 = **0.75**. CPI < 1, so the project is **over budget**: each \$1 spent earns only \$0.75 of value (CV = −\$80,000).
- **Interpretation:** the project is both late and over budget 40% of the way through. Without corrective action the final cost will be well above budget (EAC = BAC / 0.75), so the PM should find the causes and act now.

### 4(b)（5 分）Tuckman 模型与团队变动

> **Original question (English)** · 4 (b) The inventory system project team has been working effectively, completing tasks independently and meeting its targets. Two new developers then join the team. Disagreements emerge over established working practices, and delivery slows. The sponsor argues that an experienced team should not need further team-development support. Using Tuckman's model, critically assess the sponsor's view. Explain how the change in team membership could affect team development, and propose one management intervention, justifying how it could help restore effective collaboration. (5 points)

**评价赞助人的观点**：不正确。Tuckman 的 **Forming → Storming → Norming → Performing → Adjourning** 不是一次性的线性过程。团队原本处于 **Performing**，但**成员变动**会让团队**退回 Forming/Storming**：新成员不了解既有规范，老成员要重新建立信任，对工作方式的分歧（题中所述）正是 Storming 的表现。「有经验」指的是个人能力，**团队的协作关系**需要重新建立。

**影响**：分歧消耗时间和精力，交付变慢；若不处理，冲突会固化，新人被边缘化或老成员士气下降。

**干预（一个即可，要说明为什么有效）**：

- 组织一次**工作方式工作坊 / 更新团队章程**：重新确认编码规范、评审流程、RACI 和沟通规则，让新老成员共同参与制定 → 把分歧变成共识，帮团队快速进入 Norming；
- 或者 **结对编程 / 导师制**：让新人与老成员结对，快速学习既有实践，同时建立信任。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week06-Resource-Management-Summary|W06 Tuckman 团队发展]]

**English answer (Unofficial, self-drafted) — model answer**

- **Assessment:** the sponsor's view is incorrect. Tuckman's stages (forming → storming → norming → performing → adjourning) are not a one-way, one-time sequence. The team was **performing**, but a change in membership can push it back to **forming/storming**.
- **Effect of the change:** the new developers do not know the established norms, and existing members must rebuild trust with them. The disagreements about working practices are typical storming behaviour. Individual experience does not replace team cohesion, so delivery slows; if this is ignored, conflict can harden and morale fall.
- **Intervention: a working-agreement workshop to update the team charter.** New and existing members jointly agree coding standards, review process, roles (RACI) and communication rules. This turns disagreement into shared norms and moves the team quickly to norming and back to performing. (Alternative: pair programming / mentoring between new and existing developers.)

### 4(c)（6 分）服务级别管理：把「可靠且响应快」变成可衡量目标

> **Original question (English)** · 4 (c) Before the inventory system becomes operational, the retail chain and service provider agree only that it should be "reliable and responsive". Store managers are concerned that this wording will make service performance difficult to assess. Using service level management, propose two measurable service targets appropriate for the inventory system and justify their relevance to store operations. Explain how the provider and retail chain should monitor and review performance against the agreed targets. State any assumptions used to set your targets. (6 points)

| 目标 | 假设 | 与门店运营的关系 |
|:---|:---|:---|
| **可用性 ≥ 99.9%**（营业时间内，按月计） | 门店营业 8:00–22:00；计划维护安排在营业时间外且不计入 | 系统不可用 → 门店无法查库存、补货建议中断、可能缺货 |
| **95% 的库存查询在 2 秒内返回**；库存数据与 POS 同步延迟 ≤ 5 分钟 | 高峰期数百家门店同时访问 | 「实时」库存才能支撑补货和销售决策，响应慢会拖慢门店操作 |

（其他可选：P1 事件 30 分钟内响应、4 小时内恢复；每月补货建议准确率。）

**监控与评审**：

1. 服务商用监控工具**自动采集**指标，生成**月度 SLA 报告**（可用性、响应时间、事件数量与解决时间）；
2. 双方定期举行**服务评审会**（月度运营 / 季度管理层），复盘违约、事件趋势和改进行动；
3. 违约触发**服务补偿（service credits）**或改进计划；
4. 业务变化（如门店扩张、促销季）时**重新协商**目标；也要收集门店经理的满意度，避免「指标达标但用户不满」（西瓜效应）。

**知识点**：[[26-S2-Course/INFO6007/INFO6007-Week12-ITSM-Processes-2-Summary|W12 服务级别管理]]、[[26-S2-Course/INFO6007/INFO6007-Week11-ITSM-Processes-1-Summary|W11 ITSM 概念]]

**English answer (Unofficial, self-drafted) — model answer**

- **Target 1 – availability ≥ 99.9% during store trading hours, measured monthly.** Assumption: stores trade 8 am–10 pm and planned maintenance happens outside trading hours. Relevance: if the system is down, stores cannot check stock or receive purchasing recommendations, which leads to stock-outs and lost sales.
- **Target 2 – 95% of stock queries answered within 2 seconds, and inventory data synchronised with POS within 5 minutes.** Assumption: hundreds of stores query at peak times. Relevance: "real-time" inventory is needed for replenishment and sales decisions, and slow responses hold up store staff.
- **Monitoring:** the provider collects the metrics automatically with monitoring tools and issues a monthly SLA report (availability, response time, incidents and resolution times).
- **Review:** both parties hold regular service reviews (monthly operational, quarterly management) to examine breaches, trends and improvement actions. Breaches trigger service credits or an improvement plan, and targets are renegotiated when business needs change (e.g. store expansion, peak seasons).
- Also survey store-manager satisfaction, so the targets are not met on paper while users are still unhappy (the "watermelon effect").

---

## 本卷考点分布

| 小问 | 主题 | 周次 |
|:---|:---|:---|
| 1(a) | Waterfall vs Agile | W02 |
| 1(b) | 范围蔓延、变更控制 | W03、W10 |
| 1(c) | PERT 三点估算 | W03 |
| 2(a) | 需求收集 | W03 |
| 2(b) | 领导风格 | W06、W09 |
| 2(c) | 风险识别与应对 | W07 |
| 3(a) | WBS | W03 |
| 3(b) | EMV | W07 |
| 3(c) | Make-or-buy | W08 |
| 4(a) | SPI / CPI | W04 |
| 4(b) | Tuckman | W06 |
| 4(c) | 服务级别管理 | W11–W12 |

**规律**：每道大题都**跨 3 个不同主题**；每题至少有一个计算（PERT、EMV、EVM）或一个「设计可衡量目标」的小问。**计算公式必须写在 A4 笔记上**：PERT、EMV、CV/SV/CPI/SPI/EAC、可用性。更多情景练习见 [[26-S2-Course/INFO6007/INFO6007-Scenario-Question-Bank-Solutions|INFO6007 情景题库解析]]。
