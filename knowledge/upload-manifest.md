# SKGPT · ChatGPT Project 上传文件清单

> 版本：v0.1 · 2026-04-28
> 用途：管理 ChatGPT Project「SK 工作台」的 25 个知识库文件
> 原则：上传稳定内核，不上传动态状态；动态状态从 GitHub `MRYGP/SK` 现读

---

## 一、总原则

ChatGPT Project 上传文件不是 SK 仓库镜像。

上传文件只承担三个作用：

1. 给模型提供长期稳定的判断框架
2. 给模型提供写作、拆解、推演的操作模板
3. 给模型提供当前阶段高频使用的少数主线资产

以下文件不长期上传：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `ops/清单草稿-未验证教训.md`
- `ops/清单候选-待升级教训.md`
- `meta/changelog.md`
- `radar/product-radar.md`
- `radar/signals.md`

原因：这些是动态状态文件，上传后不会自动同步，容易造成旧状态误判。

---

## 二、推荐配额

Project 最多 25 个文件，推荐结构：

| 类型 | 数量 | 说明 |
|---|---:|---|
| 稳定内核文件 | 18 | 长期方法论、模板、铁律、证据规则 |
| 当前主线资产 | 5 | 当前阶段高频调用的赛道、推演、定位文件 |
| 任务机动文件 | 2 | 当前正在处理的文章、底稿、研究报告 |

---

## 三、当前建议上传清单

### A. 稳定内核文件：18 个

| 序号 | SK 路径 | 上传到 Project 后的用途 |
|---:|---|---|
| 1 | `meta/CLAUDE系统指令.md` | 作为历史主控指令与关键词表参考；与 ChatGPT 指令冲突时以后者为准 |
| 2 | `北极星文档.md` | 战略锚点、北极星、科学创业主路径 |
| 3 | `core/product-teardown-template.md` | AI 产品 10 维度拆解模板 |
| 4 | `content/article_template.md` | 公众号文章结构模板 |
| 5 | `content/公众号写作指南.md` | 语言规范、证据规则、禁用词 |
| 6 | `content/公众号内容生产经验手册.md` | 文章生产经验、检查清单、历史教训 |
| 7 | `content/文章发布SOP.md` | 发布前后流程 |
| 8 | `core/项目审问清单.md` | 项目评估前置排雷 |
| 9 | `core/SKILL-推演SOP-v1.3.md` | 从模糊想法到商业模型的推演流程 |
| 10 | `core/产品评估决策清单-v1.0.md` | 新产品方向进入深推前的硬筛子 |
| 11 | `core/三湘问道铁律.md` | 拆解和评估前的排除规则 |
| 12 | `core/failure_modes.yml` | 失败模式库 |
| 13 | `core/evidence_levels.yml` | 证据等级规则 |
| 14 | `core/SKILL-深度研究指令设计.md` | 多 AI 深度研究指令设计方法 |
| 15 | `core/SKILL-AI产品复制推演框架-v0.1.md` | 海外 AI 产品复制与对标推演 |
| 16 | `core/SKILL-多维综合产品推演框架.md` | 多维综合型机会判断 |
| 17 | `core/SKILL-MTP构思招募法.md` | 构思招募文 / MTP 文章写法 |
| 18 | `core/评估引擎速查版.md` | 7+3 步评估体系速查 |

---

### B. 当前主线资产：5 个

| 序号 | SK 路径 | 上传到 Project 后的用途 |
|---:|---|---|
| 19 | `cases/2026/诊断空白赛道拆解库.md` | 诊断空白系列的赛道母库 |
| 20 | `cases/2026/推演流水账-诊断vs匹配vs三方错位-2026-04-25.md` | 诊断空白系列最重要的方法论推演 |
| 21 | `content/公众号内容大纲-30篇规划.md` | 内容组合拳与文章序列规划 |
| 22 | `content/case-card-format-v1.0.md` | 案例卡字段规范 |
| 23 | `cases/2026/角色定位与变现路径.md` | 判断力合伙人定位与变现路径 |

---

### C. 任务机动文件：2 个

| 序号 | 当前建议 | 说明 |
|---:|---|---|
| 24 | `cases/2026/推演流水账-尝一口方法论-2026-04-18.md` | 当前阶段打法原点，暂时保留 |
| 25 | `meta/SK知识库使用方法-框架红队法.md` | 用自己的框架红队自己的产品，暂时保留 |

---

## 四、本地上传包目录

本地 `D:\SKGPT` 可以建立以下目录：

```txt
D:\SKGPT\_project-upload
├── stable-core
├── current-mainline
└── task-slots
```

说明：

- `_project-upload/stable-core`：放 18 个稳定内核文件
- `_project-upload/current-mainline`：放 5 个当前主线资产文件
- `_project-upload/task-slots`：放 2 个任务机动文件

`_project-upload` 只是本地上传包，默认不提交到 GitHub。

