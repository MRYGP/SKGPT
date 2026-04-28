# SKGPT · GPTS 注册表

> 版本：v0.1 · 2026-04-28
> 用途：登记 SK 体系下各 GPTS 的角色、调用边界、正式指令来源与建议知识库配置
> 原则：SKGPT 只登记和校正，不复制 SK 中的 GPTS 正文指令

---

## 一、GPTS 家族总表

| GPTS | 定位 | 正式指令来源 | 建议 Knowledge |
|---|---|---|---|
| SK 前置生产 GPT | 原料清洗 / 半成品生产器 | `MRYGP/1SK/SK 前置生产系统指令.md` | `MRYGP/1SK` 轻量知识包：`repo_index.yml`、`知识包02-核心规则包.md`、`知识包03-仓库导航包.md`、`知识包04-产品雷达规则包.md`、`知识包06-案例格式包.md`、`知识包07-内容生产规则包.md`、`知识包08-高质量样本包.md`、`知识包09-理论压缩包A.md`、`知识包10-理论压缩包B.md` |
| 写作工坊 GPTS | 公众号文章改写器 | `MRYGP/SK/meta/写作工坊-系统指令.md` | `article_template.md`、`公众号写作指南.md`、`公众号内容生产经验手册.md`、`文章发布SOP.md` |
| 第一读者 GPTS | 发布前读者检测器 | `MRYGP/SK/meta/第一读者-系统指令.md` | `公众号写作指南.md`、`公众号内容生产经验手册.md` |
| SK-GPTS：三湘问道知识库主控副驾 | 固定入口 / 主控副驾 | `MRYGP/SKGPT/instructions/sk-gpts-system-instructions.md`（待创建） | 待定 |
| 深度研究员 GPTS | 资料搜集 / 证据验证 / 多源研究报告 | `MRYGP/SK/meta/gpts-deep-researcher-design.md` | `core/研究员输出模板.md`、`core/failure_modes.yml`、`core/evidence_levels.yml`、`content/公众号写作指南.md` |

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

---

## 二、写作工坊 GPTS 配置

### 定位

写作工坊 GPTS 是公众号文章改写器，不是分析师、顾问、框架设计者。

### 推荐 Knowledge

必传：

- `content/article_template.md`
- `content/公众号写作指南.md`
- `content/公众号内容生产经验手册.md`
- `content/文章发布SOP.md`

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

### 推荐 Knowledge

必传：

- `content/公众号写作指南.md`

建议传：

- `content/公众号内容生产经验手册.md`

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

### 推荐 Knowledge

必须上传以下 4 个文件，且必须来自 `MRYGP/SK` 当前文件：

- `core/研究员输出模板.md`
- `core/failure_modes.yml`
- `core/evidence_levels.yml`
- `content/公众号写作指南.md`

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

## 五、状态判断铁律

`MRYGP/1SK` 也不得作为 SK 当前状态来源。它只是 SK 前置生产 GPT 的轻量知识包。

写作工坊 GPTS、第一读者 GPTS、SK 前置生产 GPT、深度研究员 GPTS、SK-GPTS 都不得凭自身 Knowledge 判断 SK 当前状态。

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
