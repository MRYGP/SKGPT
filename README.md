# SKGPT · 三湘问道知识库主控副驾配置仓库

> 本仓库是 `MRYGP/SK` 的 ChatGPT Project / GPTS 适配层，也是站在 SK 外部的观察者与校正者。
> 它不是 SK 知识库副本，不承载文章、案例、执行状态或动态进度。
> SK 的内容、案例、方法论正文与执行状态 SSOT 始终是 `MRYGP/SK`。
> SKGPT 只规定 ChatGPT / GPTS 如何读取、上传、校验和避免误判 SK。

---

## 一、仓库定位

`SKGPT` 只做四件事：

1. 保存 ChatGPT Project / GPTS 的系统指令
2. 管理 Project 知识库上传清单
3. 规定 GPTS 如何读取 GitHub 上的 SK 当前状态
4. 登记 SK 体系下各 GPTS 的角色边界、调用入口与建议知识库配置

### 角色边界

`SKGPT` 对 `SK` 的关系不是“并行维护”，而是“外部校正”。

- `SK` 继续保持原有维护模式：内容、案例、方法论、执行状态都在 `MRYGP/SK`
- `SKGPT` 不写入 SK 的动态状态，不复制 SK 的 case-index、case-cards、README、执行状态总表
- `SKGPT` 负责校正 ChatGPT Project / GPTS 是否误用旧上传文件、旧记忆或错误读取顺序
- 当发现状态冲突时，SKGPT 只提供读取协议和修复建议，最终状态仍以 `MRYGP/SK` 当前文件为准

一句话：

> SK 是主体，SKGPT 是观察者、校正者和适配器。

---

## 二、与 SK 的关系

| 仓库 | 角色 |
|---|---|
| `MRYGP/SK` | 内容、案例、方法论、状态、执行的 SSOT |
| `MRYGP/SKGPT` | ChatGPT / GPTS 的配置、适配、校验仓库 |

`SKGPT` 不复制 `SK` 的文章、案例、状态文件。

凡涉及以下问题，必须从 GitHub `MRYGP/SK` 现读：

- 当前发布状态
- 文章编号
- 哪篇已发、哪篇待发、哪篇冰冻
- 文件是否存在
- 目录结构
- 案例卡是否补齐
- 执行状态
- 雷达状态
- 最新方法论版本
- 仓库是否存在冲突或漂移

---

## 三、为什么不直接放在 SK 仓库

`SK` 是长期知识系统和判断系统。

`SKGPT` 是工具适配层。

两者分离可以避免：

- ChatGPT Project 专用规则污染 SK 主仓库
- Claude 本地工作流规则与 ChatGPT 规则混在一起
- Project 上传文件缓存被误认为当前状态
- GPTS 配置变化影响内容生产主链路

---

## 四、核心规则

### 1. SKGPT 不做内容 SSOT

不得在本仓库维护以下内容的副本：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `radar/product-radar.md`
- `radar/signals.md`
- `meta/changelog.md`

这些文件统一从 `MRYGP/SK` 现读。

### 2. Project 上传文件只放稳定内核

ChatGPT Project 最多 25 个文件，推荐结构：

- 18 个稳定内核文件
- 5 个当前主线资产文件
- 2 个任务机动文件

动态状态文件不长期上传。

### 3. 冲突时的处理顺序

当 Project 上传文件、GitHub 当前文件、用户本轮说明冲突时，优先级为：

1. 用户本轮明确确认
2. GitHub `MRYGP/SK` 当前文件
3. Project 上传文件
4. 历史对话记忆

---

## 五、目录结构

```txt
SKGPT/
├── README.md
├── instructions/
│   └── chatgpt-project-instructions.md
│
├── knowledge/
│   └── upload-manifest.md
│
├── protocols/
│   └── github-read-protocol.md
│
├── gpts/
│   └── gpts-registry.md
│
└── _project-upload/
    ├── stable-core/
    ├── current-mainline/
    └── task-slots/
```

说明：

- `instructions/`：存 ChatGPT Project / GPTS 系统指令
- `knowledge/`：存 Project 上传文件清单
- `protocols/`：存 GitHub 现读与漂移检查协议
- `gpts/`：登记 SK 体系下各 GPTS 的角色、调用边界、正式指令来源与建议知识库配置；不复制 GPTS 正文指令
- `_project-upload/`：本地临时上传包，不提交 GitHub

## 六、当前阶段目标

第一阶段：把 ChatGPT Project 建成稳定工作台。  
第二阶段：从 Project 中提炼 SK-GPTS：三湘问道知识库主控副驾。  
第三阶段：用 SKGPT 维护 GPTS 指令、上传清单、漂移检查协议。


