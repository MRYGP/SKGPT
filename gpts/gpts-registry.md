# SKGPT · GPTS 注册表

> 版本：v0.1 · 2026-04-28
> 用途：登记 SK 体系下各 GPTS 的角色、调用边界、正式指令来源与建议知识库配置
> 原则：SKGPT 只登记和校正，不复制 SK 中的 GPTS 正文指令

---

## 一、GPTS 家族总表

| GPTS | 定位 | 正式指令来源 | 建议 Knowledge |
|---|---|---|---|
| 写作工坊 GPTS | 公众号文章改写器 | `MRYGP/SK/meta/写作工坊-系统指令.md` | `article_template.md`、`公众号写作指南.md`、`公众号内容生产经验手册.md`、`文章发布SOP.md` |
| 第一读者 GPTS | 发布前读者检测器 | `MRYGP/SK/meta/第一读者-系统指令.md` | `公众号写作指南.md`、`公众号内容生产经验手册.md` |
| SK-GPTS：三湘问道知识库主控副驾 | 固定入口 / 主控副驾 | `MRYGP/SKGPT/instructions/sk-gpts-system-instructions.md`（待创建） | 待定 |
| 深度研究员 GPTS | 研究任务执行器 | `MRYGP/SK/meta/gpts-deep-researcher-design.md` | 研究指令、目标项目素材、必要模板 |

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

## 四、状态判断铁律

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
