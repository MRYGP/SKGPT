# SKGPT · GPTS 注册表

> 版本：v0.4 · 2026-05-02
> 变更：SK-产品对标初拆 GPTS 指令稿入库；Knowledge 扩充（必传 / 建议 / 动态读取）
> 历史：v0.3 新增 SK-产品对标初拆 GPTS；v0.2 同步写作工坊、第一读者、深度研究员、SK 前置生产 GPT 的新规则边界
> 用途：登记 SK 体系下各 GPTS 的角色、调用边界、正式指令来源与建议知识库配置
> 原则：SKGPT 只登记和校正，不复制 SK 中的 GPTS 正文指令

---

## 一、GPTS 家族总表

| GPTS | 定位 | 正式指令来源 | 建议 Knowledge |
|---|---|---|---|
| SK 前置生产 GPT | 原料清洗 / 半成品生产器 | `MRYGP/1SK/SK 前置生产系统指令.md` | `MRYGP/1SK` 轻量知识包：`repo_index.yml`、`知识包02-核心规则包.md`、`知识包03-仓库导航包.md`、`知识包04-产品雷达规则包.md`、`知识包06-案例格式包.md`、`知识包07-内容生产规则包.md`、`知识包08-高质量样本包.md`、`知识包09-理论压缩包A.md`、`知识包10-理论压缩包B.md` |
| 写作工坊 GPTS | 公众号文章改写器 | `MRYGP/SK/meta/写作工坊-系统指令.md` | `content/article_template.md`（必）、`content/公众号写作指南.md`、`content/公众号内容生产经验手册.md`、`content/文章发布SOP.md`；均须为 `MRYGP/SK` 当前版 |
| 第一读者 GPTS | 发布前读者检测器 | `MRYGP/SK/meta/第一读者-系统指令.md` | 必传：`content/公众号写作指南.md`、`content/公众号内容生产经验手册.md`；建议传：`content/article_template.md` |
| SK-GPTS：三湘问道知识库主控副驾 | 固定入口 / 主控副驾 | `MRYGP/SKGPT/instructions/sk-gpts-system-instructions.md` | 待定 |
| 深度研究员 GPTS | 资料搜集 / 证据验证 / 多源研究报告 | `MRYGP/SK/meta/gpts-deep-researcher-design.md` | `core/研究员输出模板.md`、`core/failure_modes.yml`、`core/evidence_levels.yml`、`content/公众号写作指南.md` |
| SK-产品对标初拆 GPTS | 38 产品对标库的批量初拆 / 10 维度对标分析底稿生成器 | `MRYGP/SKGPT/instructions/sk-product-teardown-gpts-builder-instructions.md` | **完整操作协议（Knowledge）：** `MRYGP/SKGPT/instructions/sk-product-teardown-gpts-instructions.md`。**必传：** `core/product-teardown-template.md`、`core/SKILL-AI产品复制推演框架-v0.1.md`、`core/产品评估决策清单-v1.0.md`、`core/failure_modes.yml`、`core/evidence_levels.yml`、`core/三湘问道铁律.md`、`content/case-card-format-v1.0.md`、`core/评估引擎速查版.md`；建议：`core/SKILL-深度研究指令设计.md`；动态读取：`README.md`、`ops/执行状态总表.md`、`cases/2026/产品对标库-38个AI产品复制价值排名.md`、`cases/2026/case-cards.md`、`cases/2026/case-index.md`、`cases/2026/深度底稿/`（路径均相对 `MRYGP/SK`，须 GitHub 当前版） |

---

## SK 前置生产 GPT 配置

### 定位

SK 前置生产 GPT 是「三湘问道·AI应用拆解工作室」的前置生产器。

它不是泛化聊天助手，也不是最终发布器。  
它负责把外部资料、链接、截图、访谈、RSS、讨论记录和模糊想法，转成可落库的 Markdown 半成品草稿。

一句话：

> SK 前置生产 GPT = 外部资料 -> 可落库 Markdown 半成品。

### 常见产物

- `radar_item`
- `research_note`
- `case_card`
- `article_draft`
- `repo_update` 草稿

### 正式指令来源

```txt
MRYGP/1SK/SK 前置生产系统指令.md
```

### 知识包来源

```txt
MRYGP/1SK
```

当前知识包包括：

- `README.md`
- `repo_index.yml`
- `SK 前置生产系统指令.md`
- `refresh_manifest.yml`
- `protocols/1sk-self-audit-protocol.md`
- `知识包02-核心规则包.md`
- `知识包03-仓库导航包.md`
- `知识包04-产品雷达规则包.md`
- `知识包06-案例格式包.md`
- `知识包07-内容生产规则包.md`
- `知识包08-高质量样本包.md`
- `知识包09-理论压缩包A.md`
- `知识包10-理论压缩包B.md`

### 使用边界

适合：

- 外部资料转雷达条目
- 产品资料转拆解底稿
- 讨论记录转方法论草稿
- 文章素材转半成品 Markdown
- `repo_update` 草稿生成

不适合：

- 判断 SK 当前状态
- 替代 SK 工作台 Project
- 直接宣布入库
- 直接宣布发布
- 维护主仓库状态
- 代替写作工坊生成最终公众号文章
- 代替第一读者做发布前检测

### 状态判断规则

`1SK` 不保存当前状态。

凡涉及以下问题，必须读取 GitHub `MRYGP/SK` 当前文件，或要求用户贴出最新 canonical files：

- 当前发布状态
- 哪篇已发、哪篇待发、哪篇冰冻
- 执行状态
- `case-index`
- `case-cards`
- `radar` 状态
- 最新文件是否存在

### 与其他 GPTS 的关系

- SK 前置生产 GPT：外部资料 -> 半成品 Markdown
- 写作工坊 GPTS：半成品底稿 -> 可发布公众号文章
- 第一读者 GPTS：发布前事实风险 + 传播力 + 读者感受检测
- 深度研究员 GPTS：资料搜集 / 证据验证 / 多源研究报告
- SK 工作台 Project：最终判断、仓库维护、状态校准、Cursor/Hermes 指令

### 状态判断边界（硬性）

- `MRYGP/1SK` 不是当前状态源。
- SK 前置生产 GPT 不得依据 `MRYGP/1SK` 判断“当前发布状态、执行状态、雷达状态、case-index/case-cards 是否最新”。
- 涉及当前状态时，必须按 `protocols/github-read-protocol.md` 读取 GitHub `MRYGP/SK` 当前文件。

### 与本轮 SK 写作规则的同步

SK 前置生产 GPT 产出 `article_draft` 时，必须遵守 `MRYGP/1SK` 最新**知识包 07**（内容生产规则包）：

1. 文章草稿必须包含 `## 先说结论`
2. 机会招募型草稿必须前置真位置
3. 机会判断类草稿必须加入「时间变量推敲」
4. 真实产品体检转招募时，必须按机会招募型输出

但 `1SK` 仍不保存 SK 当前状态。涉及当前发布状态、文章编号、执行状态时，必须读取 `MRYGP/SK` 当前文件。

---

## 二、写作工坊 GPTS 配置

### 定位

写作工坊 GPTS 是公众号文章改写器，不是分析师、顾问、框架设计者。

### 新增能力要求

写作工坊 GPTS 必须执行：

1. 所有文章在标题后生成 `## 先说结论`
2. 机会招募型文章必须在前文打出「真位置」
3. 诊断空白 / MTP / 真实产品体检转招募类文章，必须包含：真问题、真位置、真模式、真门槛、真人群、真请求
4. 机会型文章必须加入 150–300 字的「时间变量推敲」
5. 不得把文章只写成行业问题分析
6. 若用户给的底稿没有摘要，写作工坊必须自动补一版「先说结论」

**正式指令来源**：

`MRYGP/SK/meta/写作工坊-系统指令.md`

### 推荐 Knowledge

必传：

- `content/article_template.md`
- `content/公众号写作指南.md`
- `content/公众号内容生产经验手册.md`
- `content/文章发布SOP.md`

以上路径均相对 `MRYGP/SK`；**须使用主仓库 `main` 上最新版**。尤其 `content/article_template.md` 与 `content/公众号内容生产经验手册.md` 已包含「先说结论 / 机会招募型 / 时间变量推敲」等硬规则；旧版会导致写法漂移。

任务时临时提供：

- 当前文章底稿
- 当前拆解底稿
- 第一读者反馈
- 用户指定的“那一刀”

不建议上传：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `radar/product-radar.md`
- `radar/signals.md`
- `meta/changelog.md`
- 大量理论库文件
- `content/公众号内容大纲-30篇规划.md`

---

## 三、第一读者 GPTS 配置

### 定位

第一读者 GPTS 是公众号发布前的外部读者模拟器，不是内部审稿人。

### 新增审查能力

第一读者 GPTS 必须检查：

1. 摘要 / 「先说结论」检查
2. 机会摘要检查
3. 招募信号评分 0–5
4. 时间变量检查
5. 医疗 / 法律 / 监管类表达风险
6. 若无「先说结论」，必须判定未过稿
7. 若机会招募文章未在前三分之一写出「真正空着的位置」，必须判定未过稿
8. 若存在明显「杀死」变量却完全不提，必须判定未过稿

**正式指令来源**：

`MRYGP/SK/meta/第一读者-系统指令.md`

### 推荐 Knowledge

必传：

- `content/公众号写作指南.md`
- `content/公众号内容生产经验手册.md`

建议传：

- `content/article_template.md`

**原因**：

`article_template.md` 已承载「先说结论 / 机会招募型 / 时间变量推敲」的硬规则；第一读者不读该文件时容易漏检模板级要求。

必须开启：

- 联网搜索 / Web browsing

不建议上传：

- `北极星文档.md`
- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `theory/` 全量理论库
- `radar/` 全量雷达文件
- `meta/changelog.md`
- `research-wechat-visibility.md`
- `content/公众号内容大纲-30篇规划.md`

---

## 四、深度研究员 GPTS 配置

### 定位

深度研究员 GPTS 是三湘问道体系里的研究员。

它不是聊天助手，不是搜索入口，不是最终决策者。

它负责：

- 数据收集
- 证据验证
- 竞品扫描
- 失败案例搜索
- 市场与赛道资料补齐
- 输出有证据等级的研究报告

一句话：

> 深度研究员 GPTS = 搜索 -> 验证 -> 分级 -> 输出研究报告。

---

### 正式指令来源

```txt
MRYGP/SK/meta/gpts-deep-researcher-design.md
```

该文件是深度研究员 GPTS 的设计源文件。  
更新该文件后，不会自动同步到 ChatGPT GPTS 页面，需要手动复制最新版 Instructions。

### 新增研究要求

深度研究员 GPTS 必须：

1. 所有关键事实附可核对来源（链接或明确出处）
2. 区分「官方披露事实」与「独立验证结论」
3. 必须搜索失败案例和反例
4. 中国竞品不能只有名单，须整理为「战场地图」式结构
5. 输出待验证假设
6. 输出下一步 7 天可执行任务
7. 对创业机会类方向，须加入轻量「时间变量推敲」
8. 不做最终判断，不宣布入库、不宣布发布

### 推荐 Knowledge

必须上传以下 4 个文件，且必须来自 `MRYGP/SK` 当前文件：

- `core/研究员输出模板.md`
- `core/failure_modes.yml`
- `core/evidence_levels.yml`
- `content/公众号写作指南.md`

**建议增加**（可选、有助于输出稳定与方法论一致）：

- `core/SKILL-深度研究指令设计.md`（`MRYGP/SK`）

**原因**：

该文件承载深度研究指令设计方法，可帮助深度研究员稳定输出高质量研究报告。  
正式设计说明仍以 `MRYGP/SK/meta/gpts-deep-researcher-design.md` 为准；若与 GPTS 内 Instructions 冲突，以 GPTS 页及设计文档的更新版为准。

不建议上传：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `radar/product-radar.md`
- `radar/signals.md`
- `meta/changelog.md`
- `北极星文档.md`
- `1SK` 全套知识包
- `SKGPT` 注册表

原因：

深度研究员负责搜索、验证、分级和输出研究报告；不负责当前状态判断、仓库维护、战略判断或最终发布。

### 必须开启

- 联网搜索 / Web browsing

原因：

深度研究员的核心能力是外部资料搜集、证据验证、竞品扫描和失败案例搜索。没有联网能力，它只能做内部摘要，不是真正的深度研究员。

### 适合调用的任务

适合：

- 新产品拆解前的数据补齐
- X 级假设验证
- 中国机会扫描
- 竞品全景研究
- 失败案例搜索
- 市场规模与赛道判断资料收集
- 产品雷达研究
- 数据矛盾核查
- 把 B 级证据升级为 A 级来源

### 不适合调用的任务

不适合：

- 判断当前文章发布状态
- 判断 `case-index` 是否最新
- 判断 `case-cards` 是否补齐
- 判断 014 现在要不要发
- 维护 SK 仓库状态
- 替代 SK 工作台 Project 做最终决策
- 替代写作工坊 GPTS 写公众号成稿
- 替代第一读者 GPTS 做传播力检测
- 替代 1SK 做前置 Markdown 半成品生产

### 状态判断规则

深度研究员 GPTS 不保存、不判断 SK 当前状态。

凡涉及以下问题，必须读取 GitHub `MRYGP/SK` 当前文件，或交回 SK 工作台 Project：

- 当前发布状态
- 哪篇已发、哪篇待发、哪篇冰冻
- 执行状态
- `case-index` 是否最新
- `case-cards` 是否补齐
- `radar` 状态
- 最新文件是否存在

### 与其他 GPTS 的关系

- SK 前置生产 GPT：外部资料 / 链接 / 截图 / 讨论记录 -> 半成品 Markdown 草稿
- 深度研究员 GPTS：研究问题 -> 证据验证 / 竞品扫描 / 失败案例 / 市场资料
- 写作工坊 GPTS：半成品底稿 + 研究材料 -> 可发布公众号文章
- 第一读者 GPTS：发布前事实风险 + 传播力 + 真实读者感受检测
- SK 工作台 Project：最终判断、仓库维护、状态校准、Cursor/Hermes 指令

### 输出边界

深度研究员 GPTS 输出：

- 研究摘要
- 关键发现
- 证据等级
- 数据来源
- 矛盾与争议
- 待验证假设
- 竞品 / 对标速查表
- 推荐下一步研究

不输出：

- 不做最终决策
- 当前发布状态判断
- 公众号最终成稿
- 仓库更新声明
- “已入库”“已发布”类结论

---

## SK-产品对标初拆 GPTS 配置

### 正式指令来源（GPT Builder Instructions）

```txt
MRYGP/SKGPT/instructions/sk-product-teardown-gpts-builder-instructions.md
```

### 完整操作协议 / Knowledge

```txt
MRYGP/SKGPT/instructions/sk-product-teardown-gpts-instructions.md
```

### 定位

SK-产品对标初拆 GPTS 是 38 产品对标库的批量初拆器。

它负责把 `cases/2026/产品对标库-38个AI产品复制价值排名.md` 中尚未完成 10 维度分析的产品，转化为可供 Claude / SK 工作台审核的 Markdown 初拆底稿。

一句话：

> SK-产品对标初拆 GPTS = 38 产品队列 -> 初拆底稿 -> Claude 审核提示词。

### 适合

- 列出 38 产品中尚未拆解的产品
- 按 A/B/C/D 优先级生成拆解队列
- 对单个产品输出 10 维度初拆
- 生成证据账本
- 生成 Claude 审核提示词
- 生成 Cursor / Hermes 入库建议

### 不适合

- 判断最终是否押注
- 替代 Claude 审核
- 写公众号终稿
- 宣布仓库已更新
- 维护 SK 当前状态
- 跳过 GitHub 现读直接用 Knowledge 判断拆解进度

### 状态判断规则

凡涉及以下问题，必须读取 GitHub `MRYGP/SK` 当前文件：

- 38 产品当前分析状态
- 哪些产品已完成 10 维度分析
- 哪些产品已有案例卡
- 是否存在状态漂移
- 是否需要更新产品对标库

默认读取：

1. `MRYGP/SK/README.md`
2. `MRYGP/SK/ops/执行状态总表.md`
3. `MRYGP/SK/cases/2026/产品对标库-38个AI产品复制价值排名.md`
4. `MRYGP/SK/cases/2026/case-cards.md`
5. `MRYGP/SK/cases/2026/case-index.md`
6. `MRYGP/SK/cases/2026/深度底稿/`（按产品名检索）

### 推荐 Knowledge（GPTS 页上传）

必传（路径相对 `MRYGP/SK`，须主分支当前版）：

- `core/product-teardown-template.md`
- `core/SKILL-AI产品复制推演框架-v0.1.md`
- `core/产品评估决策清单-v1.0.md`
- `core/failure_modes.yml`
- `core/evidence_levels.yml`
- `core/三湘问道铁律.md`
- `content/case-card-format-v1.0.md`
- `core/评估引擎速查版.md`

建议：

- `core/SKILL-深度研究指令设计.md`

动态读取（与 Step 0 / 状态校准一致，不得仅凭 Knowledge 替代现读）：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/产品对标库-38个AI产品复制价值排名.md`
- `cases/2026/case-cards.md`
- `cases/2026/case-index.md`
- `cases/2026/深度底稿/`

### 输出边界

输出 Markdown 初拆稿，不输出最终发布文章。

每次必须附：

- 建议保存路径
- 证据账本
- Claude 审核提示词
- 下一步最小动作

---

## 五、状态判断铁律

`MRYGP/1SK` 也不得作为 SK 当前状态来源。它只是 SK 前置生产 GPT 的轻量知识包。

写作工坊 GPTS、第一读者 GPTS、SK 前置生产 GPT、深度研究员 GPTS、SK-产品对标初拆 GPTS、SK-GPTS 都不得凭自身 Knowledge 判断 SK 当前状态。

任何 GPTS 都不得凭自身 Knowledge 判断以下问题：

- 当前发布状态
- 哪篇已发、哪篇待发、哪篇冰冻
- case-index 是否最新
- case-cards 是否补齐
- 执行状态
- 雷达状态
- 最新文件是否存在

---

涉及上述问题时，必须按：

`protocols/github-read-protocol.md`

读取 GitHub `MRYGP/SK` 当前文件。
