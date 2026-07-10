# Case 框架库（精简版 · 内置）

> 这是 case-review skill 内置的精简框架库，只保留各题型答题框架的**结构骨架**。
> 用途：复盘时根据识别出的 Case 类型，对照骨架找出面试者**漏掉的关键 branch**。
> 注意：这是骨架，不是教学。框架可以有变体，只要"核心问题对齐 + 基本 MECE"就算合格，不逐字硬比。

---

## 题型识别速查

| 题型 | 典型表述 |
|---|---|
| Market Sizing | 估算某市场 / 某产品规模有多大 |
| Profitability | 利润 / 利润率下降了，怎么办 |
| Growth Strategy | 怎么增长 / 营收增长 X% |
| Market Entry | 要不要进入某市场 |
| Pricing | 某产品定价多少 |
| M&A | 要不要收购某公司 |
| Operations | 生产 / 运营效率问题 |
| New Product Launch | 要不要 / 怎么发新产品 |
| Opportunity Assessment | 是否应该做 A / Should our client...？ |

---

## 01 · Market Sizing

**核心逻辑**：规模 = 销量 × 价格；价格相对固定，关键是测销量（供给侧 or 需求侧）。

**步骤骨架**：
1. 澄清问题（地区、口径）
2. 判断供给侧 / 需求侧（供给受限→供给侧，否则需求侧）
3. 列总公式（粗）
4. 向下拆解二级/三级公式
5. 分类（人群/地域/时间段）
6. 汇总成答案
7. **总结 & 优化**（数字是否 make sense、关键假设是什么、怎么校验）← 高频漏点

- 供给侧：最大产能 × 产能利用率 × 单价 × 时间
- 需求侧：总人口 × 目标客户比率 × 购买该产品比率 × 购买该品牌概率 × 使用频次 × 金额

---

## 02 · Profitability

**核心逻辑**：先定位是 R 还是 C 的问题，再解决。

**步骤骨架**：
1. **定位问题**：R - C = Profit；R、C 分别看趋势（纵向自己历史、横向对标同行），锁定异常最大的品类
   - 内部 vs 外部判断：自身增速 vs 行业增速
2. **解决对应问题**：
   - Revenue 提升 → 现有营收（Price × Volume）+ 新增营收
   - Cost 下降 → 拆 Fixed / Variable，再看每个成本项的 Price × Volume

> 关键：很少 R 和 C 同时出问题，第一步快速扫描锁定重点；R 或 C 是市场整体性问题时，聚焦"我们比同行差"的部分。

---

## 03 · Growth Strategy

**核心逻辑**：先找在哪里增长，再看具体怎么增长（Ansoff）。

**步骤骨架**：
1. **在哪里增长**：公司分析（拆客户/区域/产品）+ 行业分析（自身增速 vs 行业增速）
2. **具体怎么增长**：
   - 现有营收（Market Penetration）：Price（提价/动态定价）× Volume（客户数 / 单客购买量 / 购买频次）
   - **新营收来源**：Product Development（新品）/ Market Development（新市场/新地域）/ Diversification ← 高频可加板块
3. **Deep Dive 机会**（可能有）：Objective / Cost-Benefit / Synergies / Capabilities
4. 风险及其他

---

## 04 · Market Entry

**核心逻辑**：判断"要不要进 + 怎么进"，本质是这件事对公司有没有吸引力。

**步骤骨架**：
1. **要不要进**：
   - 蛋糕多大：市场大小、增速、市场环境、进入壁垒
   - 怎么分蛋糕：竞争格局（CR4/CR8）、核心玩家 KSF
   - 为什么是我：是否符合目标（ROI/PP）、核心优势（资源/品牌/渠道）、对现有业务影响（**Cannibalization / Synergies**）
2. **怎么进**：Organic Growth / Inorganic Growth（M&A、JV）
3. **风险及其他因素**

> Cannibalization / Synergies 是 Market Entry 的高频漏点。

---

## 05 · Pricing

**核心逻辑**：定上下限，中间用 3 大调节力量收窄价格带。

**步骤骨架**：
1. **了解行业与产品**：产业链话语权、Barrier to entry；产品特征、客户需求、synergies/cannibalization
2. **定价**：
   - 上限：Willingness to Pay（替代品法 / 效益法）
   - 下限：Cost-based（保本价 = 总成本/预计销量）
   - 调节力量：① 公司目标 ② Regulatory ③ Competitor Pricing
3. **风险 & 下一步**：Price Elasticity、动态定价、跟随市场调整

---

## 06 · M&A

**核心逻辑**：行业有没有吸引力 → 这家公司好不好 → 价格划不划算（= Market Entry + 估值）。

**步骤骨架**：
1. **Target 是否有吸引力**：
   - 所在行业：Size / Growth / 竞争
   - 业务：财务现状、竞争优势、未来发展
   - 价格是否合适：DCF / Book Value / Multiples（**需计算**）
2. **能力 & 匹配度**：公司目标、价格是否符合预期、Synergies/Cannibalization、品牌影响、收购后管理难度

---

## 07 · Operations

**核心逻辑**：找卡点 → 分析卡点原因 → 改善。

**步骤骨架**：
1. **了解现状找卡点**：业务分类 + 拆生产/运营流程 + 评估每环节效率
2. **分析卡点原因**：内部（人工/技术/设备/流程搭配）+ 外部（消费者/供应商）
3. **改善**：内部改善（流程/人工/技术/设备）+ 外部手段（收购产线 / Outsource）

---

## 08 · New Product Launch

**核心逻辑**：漏斗——大行业品类 → 具体细分产品 → 发行策略（= Market Entry + Product Selection）。

**步骤骨架**：
1. **要不要发某类型产品**：市场吸引力（大小/增速/竞争）+ 产品本身吸引力（替代品/核心数字/对公司价值）+ 公司能力（壁垒/Synergies&Cannibalization/竞争优势）
2. **发什么产品**：评估不同选项的 Gross Revenue / Profit Margin / ROI
3. **怎么发**：定价 + 试点（0-1：渠道/地域/营销）+ 扩张（1-100）

---

## 09 · Opportunity Assessment

**核心逻辑**：机会本身有没有吸引力 → 是否与公司匹配。

**步骤骨架**：
1. **评估机会**（A、B 分别评估）：
   - 微观：机会概况（产品特性、**利弊都要说**、竞争力）+ 经济效益 ROI + 对公司影响（短期/长期）
   - 宏观：市场环境 + 外部竞争
   - 其他机会（记心里）
2. **是否与公司匹配**：公司目标 + 自身能力 + Synergies/Cannibalization

> 高频漏点：把目的设太死，只 identify 一个点，**不讨论优劣势**。机会类一定要正反两面都说。
