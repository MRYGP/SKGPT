# SKGPT · ChatGPT Project 上传文件清单

> 版本：v0.5 · 2026-07-05
> 变更：同步 SK 当前态入口链：`ops/当前态.md`、项目看板、case-index、case-cards 均属于动态现读文件，不进入长期 Project Knowledge；确认本轮需手工替换的上传快照为 `北极星文档.md`、`三湘问道铁律.md`、`SKILL-AI研究报告评估法.md`；保持 **18 稳定内核 + 5 当前主线 + 2 任务机动** 结构不变。
> 维护仓库：`MRYGP/SKGPT`（本文件**不**占用 ChatGPT Project 的 25 个知识库上传位，仅为**上传包说明书**）

---

## 本文件是什么、不是什么

| 维度 | 说明 |
|---|---|
| **用途** | 管理 ChatGPT Project「SK 工作台」**最多 25 个**知识库上传位应放哪些来自 `MRYGP/SK` 的文件副本，以及哪些路径**不要**长期放进 Project。 |
| **不是什么** | 本 `upload-manifest.md` **不是** Project 里要被上传的「知识正文」之一；它只在 **SKGPT** 仓库中维护，供人类与模型在**配置/对齐**任务时阅读。 |
| **与现读的关系** | 动态状态、执行态、以及下列「不建议长期上传」类文件，应以 **GitHub / 本地 `MRYGP/SK` 当前内容**（或 SKGPT 配置仓库）**现读**为准，**不要**依赖 Project 内过期副本。 |

**重要**：GitHub 或本地 **SKGPT** 中的本清单更新后，**不会**自动增删或替换 ChatGPT Project 里已上传的文件。Project 侧仍需**手动**删除、上传、替换；本文件只是**上传包说明书**。

---

## 一、总原则

ChatGPT Project 上传文件**不是** SK 仓库镜像。

上传文件只承担三个作用：

1. 给模型提供长期稳定的判断框架
2. 给模型提供写作、拆解、推演的操作模板
3. 给模型提供当前阶段高频使用的少数主线资产

---

## 二、25 个上传位结构

ChatGPT Project 知识库最多 **25** 个文件，本清单采用：

| 类型 | 数量 | 说明 |
|---|---:|---|
| 稳定内核文件 | 18 | 长期方法论、模板、铁律、证据规则 |
| 当前主线资产 | 5 | 当前阶段高频调用的案例库、推演、定位与评估法 |
| 任务机动文件 | 2 | 理论单篇、校正类 SOP，或按任务替换为当次底稿 |

---

## 三、建议上传清单（路径相对 `MRYGP/SK` 根目录）

### A. 稳定内核文件：18 个

| 序号 | SK 路径 | 上传到 Project 后的用途 |
|---:|---|---|
| 1 | `北极星文档.md` | 战略锚点、北极星、科学创业主路径 |
| 2 | `content/article_template.md` | 公众号结构与底线（**v2.6**：开篇以 **30 秒规则** 为硬口径；机会类等 **显性前置判断卡**，**不**要求所有文种固定 `## 先说结论` 小标题） |
| 3 | `content/公众号写作指南.md` | 语言规范、证据规则、禁用词 |
| 4 | `content/公众号内容生产经验手册.md` | 文章生产经验、检查清单、历史教训（须含 **教训38**；若主仓库已增后续条目以 SK main 当前为准） |
| 5 | `content/文章发布SOP.md` | 发布前后流程 |
| 6 | `core/product-teardown-template.md` | AI 产品 10 维度拆解模板（**v4.8**，含可选第十二章「反向 teardown」；继承 v4.7 出海/跨境政策变量核查与 9.5 时间变量推敲等） |
| 7 | `core/项目审问清单.md` | 项目评估前置排雷（**v1.5**，强调“建造 > 否决”：问题用于设计应对方案，否决只用于法律/道德/资金/无反馈四条红线） |
| 8 | `core/三湘问道铁律.md` | 拆解和评估前的排除规则 |
| 9 | `core/failure_modes.yml` | 失败模式库 |
| 10 | `core/evidence_levels.yml` | 证据等级规则 |
| 11 | `core/评估引擎速查版.md` | 7+3 步评估体系速查 |
| 12 | `core/产品评估决策清单-v1.0.md` | 新产品方向进入深推前的硬筛子（**文件名不变**；正文当前 **v1.4**） |
| 13 | `core/SKILL-推演SOP-v1.3.md` | 从模糊想法到商业模型的推演流程 |
| 14 | `core/SKILL-深度研究指令设计.md` | 多 AI 深度研究指令设计方法 |
| 15 | `core/SKILL-AI产品复制推演框架-v0.1.md` | 海外 AI 产品复制与对标推演 |
| 16 | `core/SKILL-多维综合产品推演框架.md` | 多维综合型机会判断 |
| 17 | `core/SKILL-MTP构思招募法.md` | 构思招募文 / MTP 文章写法 |
| 18 | `core/SKILL-真实产品外部体检与机会推演SOP.md` | 真实早期产品体检与机会推演主 SOP |

### B. 当前主线资产：5 个

| 序号 | SK 路径 | 上传到 Project 后的用途 |
|---:|---|---|
| 19 | `cases/2026/诊断空白赛道拆解库.md` | 诊断空白系列的赛道母库 |
| 20 | `cases/2026/推演流水账/推演流水账-诊断vs匹配vs三方错位-2026-04-25.md` | 诊断空白系列最重要的方法论推演 |
| 21 | `cases/2026/推演流水账/推演流水账-尝一口方法论-2026-04-18.md` | 当前阶段打法原点 |
| 22 | `cases/2026/角色定位与变现路径.md` | 判断力合伙人定位与变现路径 |
| 23 | `core/SKILL-AI研究报告评估法.md` | 研究报告质量与可行动性评估 |

### C. 任务机动文件：2 个

| 序号 | SK 路径 | 说明 |
|---:|---|---|
| 24 | `theory/DOC-D029-客户采用六因子的收敛律.md` | 客户采用与收敛律；可按任务替换为当次底稿 |
| 25 | `core/SKILL-坐标系校正判断.md` | 坐标系与判断校正；可按任务替换 |

**机动位替换示例**（从 `MRYGP/SK` 现读或临时上传，不挤占上述固定文件名时）：当次文章定稿、`meta/SK知识库使用方法-框架红队法.md` 等。

---

## 四、不建议长期上传 Project 的文件（应从 `MRYGP/SK` 现读）

下列文件**不要**作为「长期同步的知识库正文」依赖 Project 内副本；任务需要时在 **GitHub / 本地 SK** 打开当前版本：

- `README.md`
- `ops/当前态.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `ops/项目看板/*`
- `ops/清单草稿-未验证教训.md`
- `ops/清单候选-待升级教训.md`
- `meta/changelog.md`
- `radar/product-radar.md`
- `radar/signals.md`
- `content/公众号内容大纲-30篇规划.md`
- `content/case-card-format-v1.0.md`
- `meta/SK知识库使用方法-框架红队法.md`
- `meta/CLAUDE系统指令.md` — **仅**作 Claude Project / 本地（如 `D:\sk`）工作流参考；**不是** ChatGPT Project 的最高规则；与 `MRYGP/SKGPT/instructions/chatgpt-project-instructions.md` 冲突时，**以 Project Instructions 为准**。

注意：`ops/当前态.md` 是 SK 当前状态一号入口，但仍是高频动态状态文件；项目看板、case-index、case-cards 同理，不进入长期 Project Knowledge。任务需要时现读 GitHub / 本地当前文件。

---

## 五、不进入 25 个上传位的 SKGPT 文件（配置维护任务中现读）

下列文件位于 **`MRYGP/SKGPT`**，用于 Project / GPTS / 现读协议配置，**不要**把其副本当作 SK 方法论「25 件之一」塞进 Project 知识库（除非你在做元任务且明确需要临时粘贴）：

- `SKGPT/README.md`
- `SKGPT/instructions/chatgpt-project-instructions.md`
- `SKGPT/knowledge/upload-manifest.md`（本文件）
- `SKGPT/protocols/github-read-protocol.md`

---

## 六、本地上传包目录（可选）

本地 `D:\SKGPT` 可建立：

```txt
D:\SKGPT\project-upload
├── stable-core
├── current-mainline
└── task-slots
```

将上表 **A / B / C** 对应文件从 **`MRYGP/SK`** 导出副本放入，便于版本化与手工上传 ChatGPT Project。

**`project-upload/` 扁平文件名（须与 §三 一一对应，共 25 个）**

| 目录 | 文件名 |
|---|---|
| `stable-core/`（18） | `北极星文档.md`、`article_template.md`、`公众号写作指南.md`、`公众号内容生产经验手册.md`、`文章发布SOP.md`、`product-teardown-template.md`、`项目审问清单.md`、`三湘问道铁律.md`、`failure_modes.yml`、`evidence_levels.yml`、`评估引擎速查版.md`、`产品评估决策清单-v1.0.md`、`SKILL-推演SOP-v1.3.md`、`SKILL-深度研究指令设计.md`、`SKILL-AI产品复制推演框架-v0.1.md`、`SKILL-多维综合产品推演框架.md`、`SKILL-MTP构思招募法.md`、`SKILL-真实产品外部体检与机会推演SOP.md` |
| `current-mainline/`（5） | `诊断空白赛道拆解库.md`、`推演流水账-诊断vs匹配vs三方错位-2026-04-25.md`、`推演流水账-尝一口方法论-2026-04-18.md`、`角色定位与变现路径.md`、`SKILL-AI研究报告评估法.md` |
| `task-slots/`（2） | `DOC-D029-客户采用六因子的收敛律.md`、`SKILL-坐标系校正判断.md` |

---

## 七、2026-05-16 与 SK 主仓库核对摘要

以下基于 `MRYGP/SK` 当前主仓库核对；Project 上传文件只是稳定缓存，动态状态与最新方法论仍以 GitHub 当前文件为准。

| 文件 | 核对结论 |
|---|---|
| `content/article_template.md` | **v2.6**；开篇以 **30 秒规则** 为正式长文主口径，机会类需显性前置判断卡；不把固定 `## 先说结论` 当作所有文种唯一硬规则。 |
| `core/product-teardown-template.md` | **v4.8**；新增可选第十二章「反向 teardown」，继承 v4.7 出海/跨境政策变量核查与 9.5 时间变量推敲。 |
| `core/项目审问清单.md` | **v1.5**（版本号未变）；2026-06-03 正文已新增「复制×换地两步筛」与「切入点×大机会双层检验」——**须替换 Project 上传文件**；仍强调“建造 > 否决”，问题用于设计应对方案，否决只用于法律/道德/资金/无反馈四条红线。 |
| `content/公众号内容生产经验手册.md` | 2026-05-12 更新，须包含教训34–38；若 SK 后续迭代，以主仓库当前文件头为准。 |
| `meta/CLAUDE系统指令.md` | 不进入 25 个长期上传位；仅作 Claude Project / 本地工作流参考。ChatGPT Project 以 `instructions/chatgpt-project-instructions.md` 为准。 |

**刷新建议**：每次调整写作/拆解硬规则后，从 `MRYGP/SK` **main** 重新导出上表 **A** 中与规则相关的 `content/*`、`core/*` 副本到 `SKGPT/project-upload/stable-core/`，并同步 **B/C** 后替换 ChatGPT Project 内旧文件；**勿**把 `ops/`、`cases/2026/case-index.md`、`cases/2026/case-cards.md`、`radar/` 等动态状态当作上传包稳定部分。

---

## 八、与上一版指令的关系

若曾使用「`content/case-card-format-v1.0.md` 默认进主线」等旧排列：以 **本 v0.4 清单 §三** 为准；case-card 类仍建议**任务时从 SK 现读**，不占 25 位中的固定名。
