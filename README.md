# SKGPT

**SKGPT** 是 [MRYGP/SK](https://github.com/MRYGP/SK) 的 **ChatGPT Project / GPTs 适配层**：把主仓库里适合在 ChatGPT 侧长期挂载的指令、清单与稳定知识副本，整理成可版本管理的配置包。

---

## 本仓库负责什么

| 内容 | 说明 |
|------|------|
| **Project Instructions** | ChatGPT Project 侧项目说明，见 `instructions/chatgpt-project-instructions.md` |
| **GPTs 指令** | 各 GPT 的 Instructions / Builder 说明，见 `instructions/`、`gpts/gpts-registry.md` |
| **上传清单** | Project 知识库文件配额与路径建议，见 `knowledge/upload-manifest.md` |
| **GitHub 现读协议** | 在对话中通过 GitHub 拉取 SK 主仓库现行内容的约定，见 `protocols/github-read-protocol.md` |
| **project-upload 快照** | `project-upload/`：当前建议上传到 ChatGPT Project 的文件副本之**版本化快照**（`stable-core` / `current-mainline` / `task-slots`） |

---

## 本仓库刻意不负责什么

- **不承载 SK 主仓库的「内容状态」**：执行进度、案例库当日状态、雷达备忘录等仍以 **MRYGP/SK** 为准。
- **不把下列动态类文件当作本仓库的权威副本**（与 `upload-manifest.md` 总原则一致）：主仓库根目录 `README.md`、`ops/执行状态总表.md`、`cases/2026/case-index.md`、`cases/2026/case-cards.md` 等；需要时请按现读协议从 GitHub 读取 SK 的 `main` 分支。

---

## 目录速览

```
instructions/     # Project / GPTs 指令文稿
gpts/             # GPT 注册与索引
knowledge/        # 上传清单等
protocols/        # GitHub 现读等协议
project-upload/   # 建议上传包的版本化快照（非 SK 全量镜像）
```

---

## 与主仓库的关系

| 仓库 | 角色 |
|------|------|
| **MRYGP/SK** | 操作系统与知识库正文、动态状态与案例 |
| **MRYGP/SKGPT**（本仓库） | ChatGPT / GPTs 侧配置、清单、协议与上传包快照 |
| **MRYGP/daiyixia** | 「戴一下」项目执行真源;头发试戴 GPT Project 的 Instructions 与知识库已迁至此仓库 |

**头发 AI / 戴一下 GPT Project**：`projects/头发AI产品推进台.md` 已弃用(2026-05-24)。请改用 `daiyixia/系统指令/GPT-Project-Instructions.md` 与 `github.com/MRYGP/daiyixia` 知识库。

维护主仓库内容后，按 `knowledge/upload-manifest.md` 更新 `project-upload/` 中的对应副本，再在本仓库提交，即可形成可追溯的上传包版本。
