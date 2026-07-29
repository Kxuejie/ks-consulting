# Case 框架附件索引

## 定位

`references/` 中的题型附件是供模型运行时读取的“分析说明书”，不是原课程文档的备份。

每份可发布附件应当：

1. 保留用户确认的标准框架骨架、层级与顺序；
2. 保留每个板块的目的、分析逻辑和信息映射方式；
3. 保留关键判断方法与阶段性总结方向；
4. 用重新组织的简洁表达承载必要解释；
5. 删除完整话术、长篇教学解释、大量案例、现成 brainstorm 清单和其他不影响产出的内容。

Reference 用来约束结构和保证覆盖，不替代模型对具体 Case 的独立思考。

## 附件与状态

| 编号 | 框架 | 典型核心问题 | 附件 | 当前状态 |
|---|---|---|---|---|
| 02 | Profitability | 利润为什么变化，问题在 Revenue 还是 Cost，如何解决 | [02-profitability.md](02-profitability.md) | 已精简 v1 |
| 03 | Growth Strategy | 在哪里增长、通过什么方式增长 | [03-growth-strategy.md](03-growth-strategy.md) | 已精简 v1 |
| 04 | Market Entry | 是否进入某市场，以及如何进入 | [04-market-entry.md](04-market-entry.md) | 已精简 v1 |
| 05 | Pricing | 产品或服务应该如何定价 | [05-pricing.md](05-pricing.md) | 已精简 v1 |
| 06 | M&A | 是否收购、标的是否有吸引力与匹配度 | [06-ma.md](06-ma.md) | 已精简 v1 |
| 07 | Operations | 运营问题在哪里，如何提升效率或产能 | [07-operations.md](07-operations.md) | 已精简 v1 |
| 08 | New Product Launch | 是否及如何推出新产品 | [08-new-product-launch.md](08-new-product-launch.md) | 已精简 v1 |
| 09 | Opportunity Assessment | 是否做某个机会，或在 A/B 中选择 | [09-opportunity-assessment.md](09-opportunity-assessment.md) | 已精简 v1 |

本 Skill 不包含 Market Sizing reference；纯 Market Sizing 题交给独立 Tutor。

## 路由规则

1. 先完整读取并分类 Casebook 材料，再识别题型；不要先选框架再倒推材料。
2. 纯 Market Sizing 题交给独立的 Market Sizing Tutor；综合 Case 中的市场规模计算留在主框架对应节点内处理。
3. Casebook 明确标注题型时优先参考，但仍以客户真正要回答的核心问题校验。
4. 默认只读取一个主框架。
5. 主框架已内置 mini 子逻辑时，使用内置版本。例如 Profitability 的 Revenue Growth 不再加载整份 Growth Strategy。
6. 只有题目明确切换为独立问题时，才读取第二个附件。例如主问题为 Profitability，后续独立问“应选择机会 A 还是 B”，可再读取 Opportunity Assessment。
7. 不得把多份完整框架重新拼成一个新框架。

## 保真与思考规则

- 保留附件中的一级板块、顺序和主逻辑。
- 可以按本题删去明显无关或已直接解决的分支，但必须简短说明。
- 不向附件原框架新增一级或二级板块。
- 观点与假设放在最接近的已有节点下，不能改变框架结构。
- 框架只是分析边界。模型仍需独立识别关键矛盾、判断节点重要性、把 Given 转化为 implication，并形成 case-specific hypothesis。
- 阶段性总结必须依据本题材料形成；不得复制附件里的通用判断方向当作本题结论。

## 从付费源材料转化附件的规则

逐个更新题型时：

1. 以用户提供的框架图为标准骨架。
2. 原 Case 框架库只查看该题型的“详细版框架”部分，用于识别哪些解释会影响产出。
3. 用自己的语言重写必要逻辑，不逐句摘录。
4. 每个一级板块至少保留：板块目的、子节点含义、分析动作、阶段性总结方向。
5. 仅保留极少量用于消除歧义的典型例子；不保留大规模案例枚举或 brainstorm 库。
6. 更新一份、核对一份，不批量复制源文件。
