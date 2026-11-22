---
title: INFO6007 Week 04 Tutorial 解析：范围蔓延、WBS 与关键路径
categories:
  - Course Notes
  - INFO6007
tags:
  - INFO6007
  - Project-Management
  - Scope-Creep
  - WBS
  - Critical-Path
  - GitHub
description: >-
  INFO6007 Week 04 Tutorial 完整解析。整理 Part A 范围蔓延的三大风险与两条防控策略、Part B 三层 WBS
  的构建、Part C AON 图与关键路径计算（17 周 → 19
  周），以及小组组建与 GitHub 项目看板的搭建步骤（仓库命名、协作者、Kanban 五列工作流）。
mathjax: true
abbrlink: info6007-week04-tutorial-scope-wbs-critical-path
date: 2026-09-01 21:30:00
updated: 2026-09-29 11:03:40
---

# INFO6007 Week 04 Tutorial 解析：范围蔓延、WBS 与关键路径

> - **课程**：INFO6007 — Project Management in IT，Semester 2 2026
> - **来源**：`Tutorial sheet Week 04 INFO6007.pdf` + `Tutorial Answer Sheet Week 4.pdf`
>
> ⚠️⚠️ **先说一件容易踩坑的事**：\
> **Week 4 的 tutorial 内容与 Week 4 的 lecture 完全不对应。**\
> **Lecture 讲的是成本管理与 EVM**（见 [Week 04 讲课总结](/posts/info6007-week04-cost-management.html)），\
> **而这份 tutorial 做的是范围蔓延、WBS 和关键路径——都是 Week 3「时间管理」的内容。**\
> **复习时要把两者分开看**，别指望 tutorial 里能练到 EVM 计算题。
>
> **这个一周的错位从第一次 tutorial 起就存在，且由课程文档明写**（Week 2 答案原文："Drawing from Week 1 lecture"）：\
> [Week 2](/posts/info6007-week02-tutorial-triple-constraint.html) 做 Week 1 内容 → [Week 3](/posts/info6007-week03-tutorial-methodology-stakeholder.html) 做 Week 2 内容 → **本文（Week 4）做 Week 3 内容** → [Week 5](/posts/info6007-week05-tutorial-evm-exercises.html) 做 Week 4 的 EVM。\
> **所以本文正是 [Week 03 讲课总结](/posts/info6007-week03-scope-schedule-management.html)（范围 + 进度管理）的配套练习。**

---

## 一、Tutorial 目标与结构

**目标**：通过小组活动探讨**范围与进度管理**中的实际挑战——识别范围蔓延的风险、辩论 **WBS** 的作用、用真实场景分析**进度依赖关系**。重点是**批判性讨论、协作，以及在具体情境中应用项目管理概念**。同时**敲定小组分配并开始创建项目看板**。

**五个部分**：

| 部分 | 内容 | 性质 |
|:---:|:---|:---|
| **A** | Scope Creep 与风险分析 | 讨论题 |
| **B** | Work Breakdown Structure | 构建题 |
| **C** | 进度依赖与关键路径 | **计算题（课后自己做）** |
| **D** | 敲定小组分配 | 事务 |
| **E** | 创建项目看板 | **动手，下周要检查** |

**学习成果**：

- **LO1** 理解各项目管理知识领域
- **LO2** 应用项目管理知识、工具与技术
- **LO4** 初步掌握项目管理工具与实践

---

## 二、Part A：范围蔓延与风险分析

### 场景

> 团队正在开发一套 **HR 管理系统**。**进行到一半时**，客户要求增加新功能（**移动 App、薪资分析、多语言支持**），**但预算和时间线都不变**。

> **注意题目的设计**：三个新功能**各自属于不同的技术维度**——移动端是新平台、薪资分析是新业务域、多语言是横切关注点。**任何一个都不是小改动**，而客户把它们当成「顺便加一下」。这正是范围蔓延最典型的样子。

### 三个风险（标准答案）

| # | 风险 | 机制 |
|:---:|:---|:---|
| **1** | **交付延期**（Delays in Delivery） | 额外功能**拉长开发时间**，把项目推过原定截止日 |
| **2** | **预算超支**（Budget Overruns） | 计划外功能需要**更多资源和测试**，超出原预算 |
| **3** | **质量下降**（Reduced Quality） | **增加范围却不调整资源 → 工作量上升 → 交付物仓促或测试不足** |

> **三个风险的内在逻辑很重要**：它们正好对应**项目管理铁三角的三条边**——**时间、成本、质量**。\
> **范围增加而资源不变，压力必然从这三个方向之一泄出。** 第 3 条最隐蔽，因为**质量下降在交付前往往看不见**。

### 两条防控策略（标准答案）

| 策略 | 做法 |
|:---|:---|
| **正式变更控制流程**<br>（Formal Change Control Process） | **任何新请求都要走结构化评估**，分析其对**时间、成本、资源**的影响 |
| **清晰的范围说明书与验证**<br>（Clear Scope Statement & Validation） | **早期就确立「包含什么、不包含什么」**，并在**关键里程碑**由干系人**签字确认**范围 |

> **两条策略的分工**：\
> **变更控制是「事后闸门」**——请求来了怎么处理；\
> **范围说明书是「事前围栏」**——**尤其是明确写出 exclusions（不包含什么）**，这是实践中最容易漏、也最能防争议的一条。
>
> 💡 这两条都能挂靠到 Week 4 lecture 的成本管理：**任何范围变更都要做「成本影响分析」并获批**——NSW 数字驾照项目就是这么做的。

---

## 三、Part B：Work Breakdown Structure

### 任务

沿用同一个 HR 系统场景，构建一个**至少 3 层**的简化 WBS，涵盖**需求、设计、开发、测试、部署**五类交付物。

### 参考答案

```
1. Requirements（需求）
   ├── 1.1 Requirement Gathering（需求收集）
   └── 1.2 Requirement Validation（需求验证）

2. Design（设计）
   ├── 2.1 System Architecture Design（系统架构设计）
   └── 2.2 UI/UX Design（界面与体验设计）

3. Development（开发）
   ├── 3.1 Front-end Development（前端开发）
   ├── 3.2 Back-end Development（后端开发）
   └── 3.3 Integration（集成）

4. Testing（测试）
   ├── 4.1 Unit Testing（单元测试）
   ├── 4.2 System Testing（系统测试）
   └── 4.3 User Acceptance Testing（用户验收测试）

5. Deployment（部署）
   ├── 5.1 Training & Documentation（培训与文档）
   └── 5.2 Production Deployment（生产环境部署）
```

### 几个值得注意的设计选择

| 观察 | 说明 |
|:---|:---|
| **Integration 单独列为 3.3** | **集成不是「前后端做完自然就有」的免费产物，而是独立的工作包** —— 这直接呼应 Week 4 lecture 里反复出现的「**低估集成成本**」 |
| **测试拆成三层** | 单元 → 系统 → **UAT**，**验收测试是有干系人参与的独立活动**，不能并进「测试」一笔带过 |
| **Training 归在部署下** | **培训是交付的一部分**，不是可选项 —— 讲义里 Hershey's ERP 失败的原因之一正是「培训不足」 |

> **WBS 与成本估算的连接**（考试常考的跨周关联）：\
> **自下而上估算之所以最准确，前提就是有一个足够细的 WBS。**\
> **成本要在「活动/工作包」层级分配** —— 也就是上面 1.1、2.2、3.3 这一层。**WBS 拆得越合理，估算越可靠。**

---

## 四、Part C：进度依赖与关键路径

> 💡 tutorial sheet 上标注了 **"try in your own time"** —— 这部分是**留给课后自己做**的。

### 题目

活动序列：

$$
\text{Requirements (2)} \to \text{Design (3)} \to \text{Development (6)} \to \text{Testing (4)} \to \text{Deployment (2)}
$$

（单位：周）

**要求**：

1. 画出 **AON（Activity-on-Node）** 图
2. 找出**关键路径**和**项目总工期**
3. 若 **Development 变成 8 周**，重新计算总工期

### 解答

#### ① AON 图

```
┌─────────────┐   ┌────────┐   ┌───────────────┐   ┌─────────┐   ┌────────────┐
│      A      │   │   B    │   │       C       │   │    D    │   │     E      │
│ Requirements│──▶│ Design │──▶│  Development  │──▶│ Testing │──▶│ Deployment │
│   2 weeks   │   │3 weeks │   │    6 weeks    │   │ 4 weeks │   │  2 weeks   │
└─────────────┘   └────────┘   └───────────────┘   └─────────┘   └────────────┘
```

全部是 **Finish-to-Start（完成–开始）** 依赖，**单一链条，没有并行分支**。

#### ② 关键路径与总工期

**路径**：**A – B – C – D – E**

$$
2 + 3 + 6 + 4 + 2 = \mathbf{17\ \text{周}}
$$

> **这题为什么「简单」，以及为什么值得想清楚**：\
> **因为只有一条路径，所以这条路径必然就是关键路径。**\
> **推论：链条上的每一个活动都是关键活动，浮动时间（float/slack）全部为 0。**\
> **任何一个活动延期 1 周，整个项目就延期 1 周** —— 没有任何缓冲。

#### ③ Development 改为 8 周

$$
2 + 3 + 8 + 4 + 2 = \mathbf{19\ \text{周}}
$$

**关键路径仍然是 A–B–C–D–E**。

> **为什么关键路径不变**：**因为压根只有一条路径可选。**\
> **这正是本题的教学意图**——在有**并行分支**的网络中，某个活动延期**可能会让关键路径转移**到另一条路径上；但在**纯串行**的网络中，**延期 100% 直接传导到总工期**，一周不差。
>
> 💡 **延伸思考**（题目没问但值得想）：如果 Testing 能和 Development 的后半段**部分重叠**（快速跟进 / fast-tracking），或者给 Development **加人手**（赶工 / crashing），总工期就能压缩——**这两个正是 Week 3 讲的进度压缩技术**。

---

## 五、Part D：小组组建

**要求**：组建 **4–5 人**小组，记录每位成员的 **student ID、unikey 和姓名**，交给 tutor（或邮件）。

| 要点 | 说明 |
|:---|:---|
| **确认状态** | 在 tutor 帮助下确认你是**已满员 / 部分成员 / 还没组队** |
| **没组队怎么办** | **找 tutor，他会在本 tutorial 内帮忙匹配** |
| **交换联系方式** | 大学邮箱 + 小组同意的其他方式 |
| **责任在你** | **确保你能联系上每一位队友**；缺谁的联系方式就问 tutor |
| ⚠️ **tutor 有最终决定权** | **成员仍可能被增减**，所以要保持信息畅通 |

> ⚠️ 注意 **tutorial 要求 4–5 人**，与 ELEC5620、COMP5318 等课的组队规模不同，别记混。

---

## 六、Part E：GitHub 项目看板

> ⚠️⚠️ **本节内容已于 Week 5 作废，保留仅作记录。**\
> **Week 5 tutorial 明确说明：团队仓库和看板已由课程在 GitHub 组织下统一创建好，不需要再用自己建的那个。**\
> **新做法**：去 **https://github.sydney.edu.au/INFO6007-S2-2026** 找 `INFO6007-TXX-GYY`（**注意改成连字符了**），并**填写 `README.md`**。\
> **若已在旧看板加过任务，需手动复制到新看板。** 详见 [Week 05 Tutorial 解析](/posts/info6007-week05-tutorial-evm-exercises.html)第五节。

> 💡 tutorial 说：**课上做不完没关系，下周可以接着做**。但 **下周要检查**。

### Step 1：创建仓库

| 步骤 | 说明 |
|:---|:---|
| **1. 登录** | 每人先各自登录 **https://github.sydney.edu.au/login**（用 Unikey 和密码） |
| **2. 选协调人** | 小组选**一人作为 team leader / coordinator**，由他代表团队创建仓库并完成初始设置 |
| **3. 命名** | **格式固定：`INFO6007 TXX-GYY`**<br>**XX = tutorial 编号，YY = 该 tutorial 内的小组编号** |
| **4. 可见性** | **设为 Private**，其余设置保持默认 |

### Step 2：添加协作者

在仓库 **Settings** 里，用 **unikey 或大学邮箱**添加：

- **所有小组成员**
- **你的 tutor**（需要问他要 unikey）
- **`info6007`**（课程账号）

> ⚠️⚠️ **一个必须注意的前提**：\
> **被添加的人必须已经用自己的 Unikey 登录过 https://github.sydney.edu.au/login，添加才会生效。**\
> **所以务必让每位成员先各自登录一次**——这是最容易卡住全组的一步。
>
> **验证方法**：让每位成员登录后确认**能看到这个仓库**。

### Step 3：创建项目看板

| 步骤 | 说明 |
|:---|:---|
| **1** | 打开 **Projects** 标签，创建新的 project board |
| **2** | **推荐选 Kanban 布局**——更便于组织和跟踪作业期间的工作 |
| **3** | 项目名**与仓库同名**（`INFO6007 TXX-GYY`） |

### 工作流五列

$$
\textbf{Backlog} \to \textbf{Ready} \to \textbf{In Progress} \to \textbf{In Review} \to \textbf{Done}
$$

> 这比经典的三列 Kanban 多了 **Ready** 和 **In Review**：\
> **Ready** 把「想到了」和「可以开工了」分开；**In Review** 让**评审成为显式的工作状态**而不是隐形的等待。

### 初始任务

每位成员想几个下周可做的任务，作为 **issue** 加到 **Backlog** 列并**认领给自己**。tutorial 给的示例：

- `draft a work plan`（起草工作计划）
- `research GitHub usage`（研究 GitHub 用法）
- `review the assignment guidelines`（审阅作业指引）
- `choose a project topic`（选定项目主题）

> 💡 也可以参考 Canvas 上 Group Project 模块里的 **"Suggested Weekly Progress"** 文档。

### 下周检查清单

- [ ] 仓库**已创建**，命名格式为 `INFO6007 TXX-GYY`，**Private**
- [ ] **协作者已添加**：全体成员 + tutor + **`info6007`**
- [ ] **每位成员都能看到该仓库**（都已登录过 github.sydney.edu.au）
- [ ] **项目看板已建立**，Kanban 布局，与仓库同名
- [ ] **已录入并认领了初始任务**

**GitHub 帮助文档**：https://docs.github.com/en/enterprise-server@3.16

---

## 七、考点重点

1. **范围蔓延的三大风险**：**延期、超支、质量下降** —— 对应铁三角的三条边。
2. **两条防控策略**：**正式变更控制流程**（事后闸门）+ **清晰的范围说明书与验证**（事前围栏，**务必写明 exclusions**）。
3. **三层 WBS 的构建**：需求 / 设计 / 开发 / 测试 / 部署五大类；**Integration 要独立成工作包**；**测试拆成单元、系统、UAT 三层**。
4. **WBS 是自下而上成本估算的前提** —— 成本在**工作包层级**分配。
5. **关键路径计算**：串行链 **2+3+6+4+2 = 17 周**；Development 改 8 周 → **19 周**。
6. **单一路径网络的三个性质**：**这条路径必然是关键路径**；**所有活动浮动时间为 0**；**任何延期 1:1 传导到总工期**。
7. **AON 图**：节点表示活动，箭头表示 **Finish-to-Start** 依赖。
8. **GitHub 看板**：仓库命名 **`INFO6007 TXX-GYY`**、**Private**、协作者含 **tutor 和 `info6007`**、**成员须先登录过才能被添加**、五列工作流。

---

## 八、与讲义的关系

| | Week 4 Lecture | Week 4 Tutorial |
|:---|:---|:---|
| **主题** | **成本管理与 EVM** | **范围蔓延、WBS、关键路径** |
| **实际对应周次** | Week 4 | **Week 3（时间管理）** |
| **计算内容** | CV / SV / CPI / SPI / EAC | 关键路径工期 |

> **所以复习时要注意**：\
> **EVM 的计算题只能在 lecture 的讲义算例和课后案例里练**（[Week 04 讲课总结](/posts/info6007-week04-cost-management.html)整理了两个完整算例），**tutorial 帮不上忙**。
>
> **不过两者有一条真实的连接**：**tutorial 的 WBS 正是 lecture 里「自下而上估算」的输入**。把 Part B 那棵 WBS 的每个叶子节点标上工时和费率，汇总起来就是一份自下而上的成本估算——**这也是小组项目里真正要做的事**。
