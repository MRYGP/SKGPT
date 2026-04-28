# SKGPT · GitHub 现读协议

> 版本：v0.1 · 2026-04-28  
> 用途：规定 ChatGPT Project / GPTS 什么时候必须读取 GitHub `MRYGP/SK` 当前文件  
> 原则：动态状态不靠项目上传缓存判断

---

## 一、核心原则

GitHub `MRYGP/SK` 是 SK 当前状态的可读取 SSOT。

项目上传文件只作为稳定知识缓存。

当问题涉及“当前状态”时，必须读取 GitHub 当前文件，不得只凭：

- Project 上传文件
- 历史对话
- 记忆
- 旧截图
- 旧导出文件

---

## 二、必须现读 GitHub 的问题

凡涉及以下问题，必须现读 GitHub：

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
- 某个文件的当前内容
- 某篇文章的最终版本
- 当前下一步应该做什么

---

## 三、默认读取顺序

涉及 SK 当前状态时，默认读取顺序是：

1. `README.md`
2. `ops/执行状态总表.md`
3. `cases/2026/case-index.md`
4. `cases/2026/case-cards.md`
5. 与任务直接相关的文件

---

## 四、不同任务的读取策略

### A. 判断当前总状态

读取：

1. `README.md`
2. `ops/执行状态总表.md`
3. `cases/2026/case-index.md`
4. `cases/2026/case-cards.md`

输出：

- 当前状态
- 是否存在状态漂移
- 最紧迫动作
- 最小修复方案

---

### B. 判断某篇文章状态

读取：

1. `README.md`
2. `ops/执行状态总表.md`
3. `cases/2026/case-index.md`
4. 该文章文件

必要时读取：

5. `cases/2026/case-cards.md`

输出：

- 已发布 / 定稿待发布 / 暂缓 / 冰冻 / 草稿
- 状态来源
- 是否有冲突
- 下一步动作

---

### C. 判断案例卡是否补齐

读取：

1. `cases/2026/case-cards.md`
2. `cases/2026/case-index.md`
3. `README.md`

输出：

- 已补案例卡
- 缺失案例卡
- 最小补卡顺序
- 是否影响下一步拆解

---

### D. 做文章生产

先使用 Project 上传的稳定文件：

- `北极星文档.md`
- `content/article_template.md`
- `content/公众号写作指南.md`
- `content/公众号内容生产经验手册.md`
- `content/文章发布SOP.md`

再按需读取 GitHub 当前文件：

- 文章文件
- 相关底稿
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`

---

### E. 做产品拆解

先使用 Project 上传的稳定文件：

- `core/product-teardown-template.md`
- `core/failure_modes.yml`
- `core/evidence_levels.yml`
- `core/三湘问道铁律.md`
- `core/产品评估决策清单-v1.0.md`

再按需读取 GitHub 当前文件：

- 相关案例
- 相关底稿
- `cases/2026/case-cards.md`
- `cases/2026/case-index.md`

---

### F. 做项目推演

先使用 Project 上传的稳定文件：

- `core/SKILL-推演SOP-v1.3.md`
- `core/项目审问清单.md`
- `core/评估引擎速查版.md`
- `core/failure_modes.yml`
- `core/evidence_levels.yml`

如果涉及诊断空白 / 中立角色 / 匹配引擎 / 三方错位，必须读取：

- `cases/2026/推演流水账-诊断vs匹配vs三方错位-2026-04-25.md`

---

### G. 做 GPTS / Project / SKGPT 配置维护

优先读取 `SKGPT` 本仓库中的文件：

1. `README.md`
2. `instructions/chatgpt-project-instructions.md`
3. `knowledge/upload-manifest.md`
4. `protocols/github-read-protocol.md`

如果涉及 SK 当前状态，再读取 GitHub `MRYGP/SK`：

1. `README.md`
2. `ops/执行状态总表.md`
3. `cases/2026/case-index.md`
4. `cases/2026/case-cards.md`

输出：

- 配置问题定位
- 是否涉及 SK 主仓库
- 是否需要同步 Project 上传文件
- 是否需要更新 SKGPT 配置仓库

---

## 五、状态冲突处理

当多个文件冲突时，不直接下结论。

处理顺序：

1. 明确列出冲突
2. 标注各文件的说法
3. 优先采用用户本轮明确确认
4. 其次采用 GitHub 中更新时间更新、位置更权威的文件
5. 给出最小修复方案

示例：

```txt
README.md：012/013 已发布
ops/执行状态总表.md：012/013 待发布
case-index.md：012/013 定稿待发布

判断：状态漂移
用户本轮确认：012/013 已发布
最小动作：同步执行状态总表与 case-index，而不是继续写新文章
```

---

## 六、动态文件不得长期上传

以下文件不得作为 Project 长期上传知识使用：

- `README.md`
- `ops/执行状态总表.md`
- `cases/2026/case-index.md`
- `cases/2026/case-cards.md`
- `ops/清单草稿-未验证教训.md`
- `ops/清单候选-待升级教训.md`
- `meta/changelog.md`
- `radar/product-radar.md`
- `radar/signals.md`

原因：

1. 更新频繁
2. 容易漂移
3. 上传后不自动同步
4. 容易让 GPT 使用旧状态作判断

---

## 七、Project 上传文件的正确用途

Project 上传文件用于提供稳定上下文，不用于判断当前状态。

适合上传：

- 北极星
- 系统指令
- 拆解模板
- 写作模板
- 推演 SOP
- 项目审问清单
- 产品评估清单
- 铁律
- failure_modes
- evidence_levels
- 写作指南
- 内容生产经验手册
- 发布 SOP
- 当前阶段主线方法论文件

不适合上传：

- 当前发布状态
- 当前执行进度
- 文章索引
- 案例卡进度
- 雷达状态
- changelog
- 高频草稿文件

---

## 八、输出要求

凡因 GitHub 现读发现冲突，输出必须包括：

1. 冲突文件
2. 冲突内容
3. 判断依据
4. 最小修复动作
5. 需要时给 Hermes / Cursor 指令

不得输出：

- “应该没问题”
- “我记得是”
- “根据之前文件”
- “可能已经更新”

除非已经读取 GitHub 当前文件。

---

## 九、最小验收标准

每次执行 GitHub 现读任务后，至少要能回答：

1. 我读了哪些 GitHub 当前文件？
2. 它们之间是否冲突？
3. 如果冲突，哪个是最可信来源？
4. 是否需要更新 SK 主仓库？
5. 是否需要更新 SKGPT 配置仓库？