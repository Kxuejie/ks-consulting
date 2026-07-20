# KS Consulting

K 学姐的咨询求职 Agent Skill 工具箱。

这个仓库既是整套 skill 的一键安装入口，也是咨询求职任务的导航中枢。用户只需要记住 `ks-consulting`：它会判断你现在更该先做求职定位、简历润色、Market Sizing 学习还是 Case 复盘，再把任务交给对应的专业 skill。

可在 Codex、Claude Code、Cursor 等支持 Agent Skills 的工具中使用。

作者：K 学姐（[小红书](https://xhslink.com/m/4evgCZqfNRR)｜全网同名「K 学姐」，可自行搜索）

---

## 支持作者

如果这套免费开源工具对你有帮助，也可以通过 K 学姐整理的付费资料与课程继续学习。购买不是使用本仓库的前提，仓库中的核心 Skills 仍然免费开源。

<table>
  <tr>
    <th width="50%">咨询 Case 面试全攻略</th>
    <th width="50%">战略咨询基本功课程</th>
  </tr>
  <tr>
    <td align="center"><img src="assets/support/case-interview-guide-qr.png" width="220" alt="咨询 Case 面试全攻略商品二维码"></td>
    <td align="center"><img src="assets/support/consulting-fundamentals-course-qr.png" width="220" alt="战略咨询基本功课程商品二维码"></td>
  </tr>
  <tr>
    <td>面向准备咨询面试的同学，把分散的 Case 方法、常见题型和练习重点整理成一份可以反复查阅的系统攻略。</td>
    <td>围绕战略咨询常用的结构化思考、问题拆解和表达方式，适合希望系统补齐咨询基本功、跟随课程练习的同学。</td>
  </tr>
  <tr>
    <td align="center"><a href="https://xhslink.com/m/1j6S5TAIGI1"><strong>打开文档商品页</strong></a><br>微信扫码或点击链接</td>
    <td align="center"><a href="https://xhslink.com/m/8jlzN1YYWrl"><strong>打开课程商品页</strong></a><br>微信扫码或点击链接</td>
  </tr>
</table>

---

## 一键安装整套工具

推荐使用开源的 [Agent Skills CLI](https://github.com/vercel-labs/skills)：

```bash
npx -y skills add Kxuejie/ks-consulting -g --all
```

这条命令会安装仓库中的 5 个 skill：1 个主入口和 4 个专业工具。

只安装到指定 Agent：

```bash
# Codex
npx -y skills add Kxuejie/ks-consulting -g -a codex -s '*' -y

# Claude Code
npx -y skills add Kxuejie/ks-consulting -g -a claude-code -s '*' -y
```

### 让 Agent 帮你安装

如果你的 Agent 可以联网、运行终端命令并写入 skills 目录，可以把下面这段话直接发给它：

```text
请帮我安装 K 学姐咨询求职 skill 工具箱，并安装其中的全部 skills：
https://github.com/Kxuejie/ks-consulting

安装完成后，请告诉我识别到的 skill 名称和安装路径。
```

不同 Agent 的权限设置不同。如果它不能直接安装，请使用上面的 `npx` 命令，或手动下载仓库。

---

## 工具箱

| Skill | 什么时候用 | 你会得到什么 |
|---|---|---|
| `ks-consulting` | 不确定该用哪个工具，或完成一项后想知道下一步 | 任务路由与准备顺序 |
| `consulting-career-planner` | 判断咨询求职胜率、主投公司层级和背景 gap | 公司定位、目标清单、4-8 周行动计划 |
| `consulting-resume` | 把真实经历写成咨询招聘者看得懂的 bullet points | 工作链路、能力标签、2-3 个润色版本 |
| `market-sizing-tutor` | 系统学习 Market Sizing，或讲解一道具体估算题 | 路径选择、公式树、合理区间、Sanity Check 与面试表达 |
| `ks-case-review` | 复盘一问一答的 Case 面试文稿 | 6 维度评分、漏点、重大问题和练习方案 |

### 常见准备路径

```text
Career Planner：先判断投哪里、缺什么
        ↓
Consulting Resume：把真实能力写进筛选材料
        ↓
Market Sizing Tutor：掌握高频估算题的方法与表达
        ↓
Case Review：用实战文稿持续复盘面试表现
```

这不是强制顺序。想专项学习估算题的人可以直接进入 Market Sizing Tutor；已经有完整模拟 Case 文稿的人可以直接从 Case Review 开始；目标明确但简历偏弱的人可以直接进入 Consulting Resume。

---

## 如何使用主入口

安装后，在对话中说：

```text
用 ks-consulting 帮我看看，我现在应该先做什么。
```

也可以直接描述问题：

```text
我准备参加咨询秋招，但不知道目前背景能投到什么层级，简历和 Case 也都还没开始准备。
```

主入口只负责分流，不会用一套简化流程替代专业工具。它会先识别你的当前瓶颈，再切换到对应 skill 完整执行。

---

## 只安装一个 Skill

从主仓库选择安装：

```bash
# 求职定位与行动规划
npx -y skills add Kxuejie/ks-consulting -g -s consulting-career-planner -y

# 咨询简历润色
npx -y skills add Kxuejie/ks-consulting -g -s consulting-resume -y

# Case 面试复盘
npx -y skills add Kxuejie/ks-consulting -g -s ks-case-review -y

# Market Sizing 教学与解题
npx -y skills add Kxuejie/ks-consulting -g -s market-sizing-tutor -y

# 只安装主入口
npx -y skills add Kxuejie/ks-consulting -g -s ks-consulting -y
```

每个专业工具也有独立仓库和介绍页：

- [Kxuejie-Consulting-Career-Planner](https://github.com/Kxuejie/Kxuejie-Consulting-Career-Planner)
- [Kxuejie-Consulting-Resume](https://github.com/Kxuejie/Kxuejie-Consulting-Resume)
- [Kxuejie-Market-Sizing-Tutor](https://github.com/Kxuejie/Kxuejie-Market-Sizing-Tutor)
- [Kxuejie-Case-Review](https://github.com/Kxuejie/Kxuejie-Case-Review)

---

## 如何更新

重新运行安装命令即可更新整套工具：

```bash
npx -y skills add Kxuejie/ks-consulting -g --all
```

主仓库中的专业 skill 是各自独立仓库正式版本的发布快照。独立仓库先更新，经过验证后再同步到这里。

---

## 项目结构

```text
ks-consulting/
├── README.md
├── assets/
│   └── support/              # 作者资料与课程二维码
└── skills/
    ├── ks-consulting/
    │   └── SKILL.md
    ├── consulting-career-planner/
    │   ├── SKILL.md
    │   └── references/
    ├── consulting-resume/
    │   ├── SKILL.md
    │   └── references/
    ├── market-sizing-tutor/
    │   ├── SKILL.md
    │   ├── agents/
    │   └── references/
    └── ks-case-review/
        ├── SKILL.md
        └── reference/
```

---

## 隐私与判断边界

- 仓库不会主动接收或保存用户的简历、面试文稿或个人信息
- 实际数据如何处理取决于你使用的 Agent 平台和模型服务
- 求职定位与胜率判断是经验型参考，不代表咨询公司的官方筛选结论
- 工具不会承诺面试或 offer，也不会为增强表达而虚构经历和数字

上传真实材料前，请根据所用 Agent 平台的隐私政策判断是否需要先删除姓名、联系方式、公司敏感信息等内容。

---

## 后续计划

- 继续发布咨询面试、商业分析和求职准备相关 skills
- 增加版本同步与发布检查，确保主仓库和各独立仓库一致

---

## About K 学姐

K 学姐是 Ex-MBB 咨询顾问，长期分享战略咨询求职、Case 训练和商业思维内容。

KS Consulting 的目标，是把咨询求职中不同阶段的判断方法做成一套可以单独使用、也可以连续协作的 Agent Skills。用户不需要先研究工具，只需要说清楚自己遇到的问题。

小红书：[K 学姐](https://xhslink.com/m/4evgCZqfNRR)  
全网同名「K 学姐」，可自行搜索。
