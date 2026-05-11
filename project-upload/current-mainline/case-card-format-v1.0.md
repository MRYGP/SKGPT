# 案例卡格式 · 用于跨案例找规律

> 版本：v1.0
> 用途：每个案例拆解完后，额外提取一张"案例卡"，字段固定，方便跨案例检索和规律发现
> 与现有模板的关系：aichajie-案例模板是"深度版"（写文章用），本格式是"结构化版"（找规律用）
> 存储位置：所有案例卡集中存在一个文件里 → `cases/2026/case-cards.md`
> 未来可导入RAG/向量数据库，字段设计已考虑可检索性

---

## 为什么需要这个

现有的案例模板是叙事性的，适合深度分析和写文章。但当案例积累到20-30个以后，你想问的问题是：

- "所有小于50人团队做到$100M ARR的案例，他们的飞轮长什么样？"
- "所有死掉的AI产品，最高频的失败模式是哪个？"
- "所有被我们判为'复制'的产品，有什么共性？"
- "按结果付费的AI产品有几个？他们的LTV/CAC怎么样？"

叙事性的深度模板答不了这些问题。需要一个字段固定、可排序、可筛选的结构。

---

## 案例卡格式（每个案例一张）

```yaml
# ========== 基础信息 ==========
case_id: "CASE-XXX"
name: "产品名"
company: "公司名"
url: "官网"
status: "active / pivoted / dead / acquired"
death_date: ""  # 如果死了，什么时候
sector: "AI+教育 / AI+医疗 / AI+内容 / AI+金融 / AI+银发 / AI Agent / AI工具 / 其他"
sub_sector: "更细的分类"

# ========== 团队与融资 ==========
team_size: 0  # 人数
founding_date: "YYYY-MM"
founders_background: "技术/产品/行业/连续创业"
total_funding: "$XM"
latest_round: "种子/A/B/C/上市"
key_investors: ["投资人1", "投资人2"]

# ========== 产品与用户 ==========
one_line: "帮[谁]解决[什么问题]（不超过20字）"
target_user: "具体用户画像"
pricing_model: "订阅 / 按量 / 按结果 / 免费增值 / 一次性 / 其他"
price_point: "$X/月 或 具体定价"
user_count: "DAU/MAU/总注册"
arr: "$XM"  # 年收入
growth_signal: "增长数据（如：3个月10x）"

# ========== 核心机制 ==========
core_tech: "用了什么AI技术（GPT/自训练/RAG/Agent/多模态）"
moat_type: "数据壁垒 / 网络效应 / 切换成本 / 品牌 / 无明显壁垒"
acquisition_channel: "获客方式（SEO/社交裂变/社区/销售/合作伙伴）"

# ========== RRF判断 ==========
redefine: "它重新定义了什么问题？（一句话，没有就写'无'）"
redefine_dimensions: 0  # 重新定义了几个维度（0-6）
rule: "套利者 / 制定者 / 过渡中"
rule_level: "L1流量 / L2商业基础设施 / L3技术标准 / 无"
flywheel: "真飞轮 / 半飞轮 / 绞肉机 / 无飞轮"
flywheel_diagram: "A→B→C→A（画出闭环，画不出就写'无闭环'）"
rrr_verdict: "RRF全满 / 有R无RF / 有RF无R / 全无 / 不适用"

# ========== 失败模式（如适用） ==========
failure_modes: ["FM001", "FM015"]  # 匹配的FM编号
failure_cause_one_line: "一句话死因"
early_warning_signals: "事后看，什么信号能预警"

# ========== 中国机会 ==========
china_opportunity: "有 / 无 / 不确定"
china_status: "空白 / 有人做但差 / 强竞争"
china_target_user: "中国被忽视的用户群"
china_window: "窗口还有多久，判断依据"

# ========== 我们的决策 ==========
four_path: "复制 / 工具 / 代理 / 观察"
p0_action: "我们下周能做的一件事"
relevance_to_us: "跟我们（老年AI/活书/DCC2026）的关系"

# ========== 洞察与规律 ==========
counterintuitive: "这个案例最反直觉的一点（一句话）"
transferable_pattern: "可迁移到其他案例的规律（一句话）"
theory_match: "匹配的理论（DOC编号+理论名）"
comparable_cases: ["CASE-XXX", "CASE-YYY"]  # 最相似的其他案例

# ========== 元数据 ==========
source_quality: "A / B / C / X"
teardown_date: "YYYY-MM-DD"
article_published: "001 / 004 / 未发布"
last_updated: "YYYY-MM-DD"
```

---

## 怎么用：跨案例找规律的查询示例

案例卡积累到20+以后，可以做以下查询：

### 按字段筛选
- `team_size <= 50 AND arr >= $10M` → 小团队大收入的案例有哪些？
- `flywheel == "真飞轮"` → 哪些产品有真飞轮？它们的飞轮图长什么样？
- `failure_modes contains "FM015"` → 死于"无飞轮增长依赖"的案例
- `four_path == "复制"` → 所有被我们判为"复制"的产品，有什么共性？
- `china_opportunity == "有" AND china_status == "空白"` → 中国空白市场的机会

### 交叉分析
- `redefine_dimensions >= 3 AND status == "active"` → 高维度重新定义且还活着的 = 最值得学的
- `flywheel == "绞肉机"` → Ofo/WeWork式的案例，拿来做反面教材
- `pricing_model == "按结果"` → 所有按结果付费的产品，LTV怎么样？
- `theory_match contains "DOC-S032"` → 所有跟破坏式创新相关的案例

### 规律发现
- 统计 `moat_type` 分布 → 最常见的护城河类型是什么？
- 统计 `failure_modes` 频率 → 排名前3的死因
- 对比 `flywheel == "真飞轮"` vs `flywheel == "无飞轮"` 的存活率
- `counterintuitive` 字段聚类 → 反直觉洞察能不能归类成几种模式？

---

## 存储方案

### 短期（现在 → 50个案例）

所有案例卡集中存在一个文件：`cases/2026/case-cards.md`

格式：每个案例一个yaml块，用 `---` 分隔。Claude和其他AI可以直接读取这个文件做分析。

### 中期（50-200个案例）

迁移到结构化存储：
- 方案A：一个JSON文件（case-cards.json），每个案例是一个对象
- 方案B：Notion数据库（可视化筛选排序）
- 方案C：Airtable（更强的筛选和视图）

### 长期（200+个案例，真正的RAG）

接入向量数据库：
- 每张案例卡的 `one_line` + `counterintuitive` + `transferable_pattern` + `redefine` 做embedding
- 查询时用自然语言："有没有跟我们老年AI管家类似的案例？" → 向量检索最相似的5张卡
- 工具选择：Pinecone / Chroma / Weaviate（都有免费层）

---

## 跟现有流程的接口

```
场景A拆解完成
    ↓
用 aichajie-案例模板 写深度案例（叙事版，用于写文章）
    ↓
同时提取一张案例卡（结构化版，用于找规律）→ 填入 case-cards.md
    ↓
每10个案例做一次"规律发现"（杨+Claude跑一遍案例卡库）
    ↓
发现的规律 → 写进理论文件或文章（对应30篇规划的010/016/026等元分析型文章）
```

---

## 第一张案例卡示例（Lovable，基于已有的CASE-REF）

```yaml
case_id: "CASE-REF-Lovable"
name: "Lovable"
company: "Lovable"
url: "https://lovable.dev"
status: "active"
sector: "AI工具"
sub_sector: "AI代码生成/低代码"

team_size: 45
founding_date: "2023"
total_funding: "少量"
latest_round: "种子"
key_investors: []

one_line: "帮非技术人员用自然语言生成完整Web应用"
target_user: "非技术创始人、设计师、产品经理"
pricing_model: "订阅"
arr: "$100M+"
growth_signal: "45人做到$100M ARR"

core_tech: "GPT/Claude API + 代码生成 + 实时预览"
moat_type: "切换成本"
acquisition_channel: "社区/口碑/SEO"

redefine: "把'写代码'重新定义为'描述你想要什么'"
redefine_dimensions: 2
rule: "过渡中"
rule_level: "无"
flywheel: "半飞轮"
flywheel_diagram: "用户生成应用→分享→新用户看到→试用→生成自己的应用"
rrr_verdict: "有R无RF"

failure_modes: []
china_opportunity: "有"
china_status: "有人做但差"
china_target_user: "中国非技术创业者、私域运营者"
china_window: "6-12个月，国内低代码还没出现Lovable级别的产品"

four_path: "观察"
relevance_to_us: "参考案例，小团队做大产品的路径标杆"

counterintuitive: "不融资也能做到$100M ARR"
transferable_pattern: "极小团队+极高人效=不需要大量融资"
theory_match: "DOC-S037-从0到1（秘密理论）"
comparable_cases: ["CASE-002-Gamma"]

source_quality: "B"
teardown_date: "2026-02"
article_published: "未发布（参考案例）"
last_updated: "2026-03-24"
```
