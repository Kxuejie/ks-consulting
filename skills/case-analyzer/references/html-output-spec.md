# Case Analyzer HTML 输出规范

仅在用户选择 HTML 报告时读取。

生成时以 `../assets/case-report-template.html` 为固定骨架。不要每次重新设计页面；仅替换内容、目录项和适应该 Case 所需的卡片数量。

## 视觉基础

沿用 Case Review 报告的编辑感：

- 暖米色纸张背景
- 深墨色正文
- 蓝色与紫色作为层级强调色
- 衬线标题 + 无衬线正文
- 左侧粘性目录
- 响应式布局
- 支持打印 / 保存 PDF

不要包含评分、学员诊断或练习建议组件。
不要包含 Skill 测试结论、Skill 改进建议、内部 QA、规则冲突或开发备注。

## 固定页面尺寸与布局

桌面端必须保持以下基线：

- 整体 `.layout`：`max-width: 1500px`，左右两栏。
- 左侧目录：宽 `250px`、`position: sticky`、高 `100vh`、深墨色背景。
- 主内容：`max-width: 1180px`，左右至少 `24px` 留白，`min-width: 0`。
- 封面 `.hero`：最小高度 `520px`，圆角 `22px`，大标题 + 中英副标题 + 一句话判断。
- 内容 `.section`：圆角 `22px`，相邻区块间距 `22px`，保留编号方块。
- 内容卡片：圆角 `16px`；框架房子和表格保持暖白纸张感。
- 右下角固定两个按钮：`打印 / Print`、`回到顶部 / Top`。

响应式基线：

- `980px` 以下隐藏左侧目录，主内容宽 `calc(100% - 24px)`，所有网格最多两列。
- `650px` 以下所有内容卡片改为单列。
- `main`、`.section`、`.scroll` 必须设 `min-width: 0`；宽表格只在自身 `.scroll` 容器内横向滚动，禁止撑宽整页。
- 移动端验收：`document.documentElement.scrollWidth === document.documentElement.clientWidth`。

## 页面结构

1. 封面 / Overview：Case 中英文名称、类型、来源、生成日期、一句话判断
2. Case 基本信息 / Case Brief
3. 资料来源审计 / Source Audit：Candidate Material 与 Casebook Answer Key 分层
4. 完整框架与覆盖状态 / Framework Coverage
5. 逐模块分析 / Module Analysis（每个模块结束有 Stage Conclusion）
6. 风险与下一步 / Risks & Next Steps
7. 行业认知补充 / Industry Context
8. Case 总结与建议 / Recommendation

仅在确有答案校验价值时展示独立的 `Casebook Answer Check`。不得增加“Skill Test”或“开发建议”章节。

## 双语规范

中文为主、英文为辅，不要求正文逐句翻译；下列内容必须中英双语：

- 浏览器 `<title>` 与封面 Case 标题
- 左侧目录
- 章节标题
- 框架一级、二级节点
- 来源标签、覆盖状态、阶段性判断
- 打印和回到顶部按钮

固定标签：

| 中文 | English |
|---|---|
| 候选人已知 | Candidate Given |
| 按需提供 | Upon Request |
| 候选人任务 | Candidate Task |
| 候选人材料 | Candidate Exhibit |
| Casebook 示例答案 | Casebook Sample Answer |
| Casebook 参考计算 | Casebook Sample Calculation |
| 分析器计算 | Analyst Calculation |
| 观点与假设 | Point of View & Hypothesis |
| 已给 | Given |
| 部分已给 | Partial |
| 未给 | Missing |
| 不适用 | N/A |
| 阶段性判断 | Stage Conclusion |

## 框架“房子”组件

每个一级板块生成一个独立组件：

- 顶部宽长方形：原框架一级板块名称，作为横梁。
- 下方网格：每个二级模块是一张较窄、较长的竖向卡片。
- 卡片内部按框架子节点逐项展示，不使用一个聚合框笼统装入多条信息。
- 每个子节点必须包含：双语节点名、覆盖状态、已有 Candidate Material、观点与假设。
- 顶部横梁使用轻微蓝紫渐变；子模块使用更浅的同色系渐变。
- `Candidate Given` 使用浅蓝或浅绿背景，并标明是开题直接给出、按需提供还是 Exhibit。
- `观点与假设｜Point of View & Hypothesis` 使用浅紫背景或紫色边线。
- `Casebook Sample Answer / Sample Calculation` 只出现在独立的答案校验区，使用浅红或灰色，不能和 Candidate Given 混排。
- 同时使用文字标签，不能只靠颜色区分来源。
- 超宽框架在桌面端横向展开；移动端变成单列或可局部横向滚动。
- 打印时让一个一级板块尽量不跨页断裂。

推荐的子节点结构：

```html
<div class="coverage-row partial">
  <div class="coverage-name">市场环境｜Market dynamics</div>
  <span class="status">部分已给｜Partial</span>
  <div class="evidence">已有：...</div>
  <div class="hypothesis">观点与假设：最可能的判断 + 因果与佐证 + 同段不确定性</div>
</div>
```

状态规则：

- `Given`：题目材料足以覆盖该节点。
- `Partial`：有部分事实；分析器必须对缺失部分形成 base-case 假设。
- `Missing`：题目没有直接提供；分析器仍须基于题目语境和通用商业逻辑形成有方向的观点假设。
- `N/A`：与本题明确无关，并说明原因。

## 阶段性判断组件

每个一级模块分析结束后必须出现统一高亮组件：

```html
<div class="stage-conclusion">
  <strong>阶段性判断｜Stage Conclusion</strong>
  <p>明确投票 + 1-2 个依据 + 最重要的不确定性。</p>
</div>
```

要求：

- 结论必须推进总问题，不能只复述本页数据。
- Market Entry 的阶段判断明确说明“更支持进入 / 更不支持进入”，不得用“只能有条件推进”回避判断。
- How to Enter 明确说明优先模式、关键落地要素和切换条件。
- Profitability 等其他题型按其核心问题说明“问题在哪里、什么最关键”。

推荐色值：

```css
:root {
  --bg: #f6f1e7;
  --paper: #fbf8f1;
  --ink: #242433;
  --muted: #656477;
  --blue: #4b7eb4;
  --purple: #7655a8;
  --blue-soft: #e5edf5;
  --purple-soft: #ece4f2;
  --framework-gradient: linear-gradient(90deg, #dbe9f5 0%, #e8dff2 100%);
}
```

渐变用于表达层级，不使用高饱和炫光、紫色渐变按钮或大面积装饰渐变。

## 内容规则

- HTML 与聊天版使用同一分析结果，不得改结论。
- 框架节点名称和顺序与 Skill 所选附件一致；Casebook 示例框架不得覆盖自有框架。
- 每个模块结论前置。
- Candidate Given、Casebook Answer Check 与观点假设始终分区呈现。
- 每个框架子节点显示 Given / Partial / Missing / N/A 状态、Candidate Material 和观点假设。
- 每个一级模块都有 Stage Conclusion，并直接回答 Case 核心问题。
- 同一截图同时包含问题和答案时，必须拆分来源展示。
- 缺失 Exhibit / Appendix 必须显式提示；答案页反推的数字只能标为“答案校验，非 Given”。
- 风险与下一步保持精炼，并收束前文观点假设中的关键不确定性。
- 最终 Recommendation 第一行先做 Yes / No 或 A / B 选择，随后完整呈现核心依据、核心风险与下一步。
- 行业补充突出流程、产业链和本题命门。

## 技术要求

- 单文件 HTML，UTF-8，无外部运行依赖。
- 桌面端和手机端均可阅读。
- 提供“回到顶部”和“打印 / 存为 PDF”按钮。
- 使用语义化 HTML 和清晰标题层级。
- 为长表格和框架提供横向滚动容器。
- 添加 `@media print`，隐藏工具栏并避免关键卡片分页断裂。
- 生成后检查：标题、目录链接、移动端、打印样式、所有内容占位符均已替换。
- 检查报告中不存在 `Skill 测试`、`Skill 改进`、`内部 QA` 等开发信息。
