# 🎓 AI Conference Reviewer

**AI 顶会研究与审稿助手 · 从研究想法到有证据的投稿方案**

面向 **ACL · EMNLP · AAAI · ICML · ICLR · NeurIPS**。帮助你找到值得研究的差异、设计有效实验、解释结果，并准备论文与审稿回复。

📖 官方指南与主席经验凝练　 ·　 💬 默认中文交流　 ·　 🧩 克隆即可安装

[能帮你做什么](#-能帮你做什么) · [快速安装](#-快速安装) · [开始使用](#-开始使用) · [内容导航](#-内容导航)

> 这是供 AI 助手读取的 **skill 指令与知识包**，需要支持本地 skills 的宿主；不独立运行，也不保证录用。无需 Zotero 或全文库，本包不要求额外 API key。

## 🧭 能帮你做什么

| 你现在的问题 | 助手提供的具体指导 |
|---|---|
| **想法还不清楚** | 梳理研究问题，找出最有价值的贡献与关键缺口 |
| **创新不够明确** | 对照最接近的研究，提出候选路线及最小验证方案 |
| **实验不知道怎么补** | 设计基线、控制变量、数据划分、指标与预算 |
| **有了结果，不知下一步** | 判断继续验证、缩小主张、重新设计或停止 |
| **论文主线不够清晰** | 将贡献与证据对应起来，组织论证和关键图表 |
| **准备投稿，心里没底** | 区分必须解决、表达可修复、可选拓展和待确认事项 |

还可以辅助 **会议匹配、热点选题、模拟审稿、AC 分歧分析与 rebuttal**。按你的问题选择流程，无须每次走完所有步骤。

## 🚀 快速安装

准备好 **Git + 支持本地 skills 的 Codex**。查询最新政策和文献还需要宿主联网。

**macOS / Linux**

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/chaokuboy/ai-conference-reviewer.git "$HOME/.agents/skills/ai-conference-reviewer"
```

<details>
<summary>🪟 Windows PowerShell</summary>

```powershell
New-Item -ItemType Directory -Force "$HOME/.agents/skills" | Out-Null
git clone https://github.com/chaokuboy/ai-conference-reviewer.git "$HOME/.agents/skills/ai-conference-reviewer"
```

</details>

安装后输入 **`$ai-conference-reviewer`**。若未出现，重启 Codex 后查看技能列表。

<details>
<summary>⚙️ 安装路径、项目内使用与更新</summary>

上述命令使用 `~/.agents/skills`。部分已有环境使用 `~/.codex/skills`，请按宿主配置选择一处，避免重复安装。参考 [官方 skills 文档](https://learn.chatgpt.com/docs/build-skills)。

仅供当前项目使用时，在项目根目录运行：

```bash
mkdir -p .agents/skills
git clone https://github.com/chaokuboy/ai-conference-reviewer.git .agents/skills/ai-conference-reviewer
```

若要随另一个 Git 项目发布，请使用 submodule 或复制文件，避免把嵌套仓库误当普通文件夹提交。

更新用户级安装：

```bash
git -C "$HOME/.agents/skills/ai-conference-reviewer" pull --ff-only
```

目录已存在时，先确认它属于本仓库；保留本地修改，不直接覆盖。使用其他路径时相应调整命令。其他支持 Agent Skills 的宿主请按其安装约定放置整个目录，并保留 `references/`；尚未逐一验证兼容性。

</details>

## 💬 开始使用

提供已有的**想法、相关论文、实验结果和资源限制**即可；材料不齐也能先做有限诊断。

**💡 发展研究想法**

> 使用 $ai-conference-reviewer。根据我的想法和相关论文，找出关键研究缺口，提出两条候选创新路线，说明如何验证，以及什么结果意味着应该停止。

**🧪 改良实验方案**

> 使用 $ai-conference-reviewer。根据我的主张、已有结果和预算，设计必要基线、对照实验、数据划分与指标。说明每个实验要排除什么解释，区分必做与可选。

**📝 复查论文与投稿准备**

> 使用 $ai-conference-reviewer。检查稿件的贡献是否有证据支持，比较 ACL 与 ICLR 的契合度，列出投稿前必须解决的问题和仍需核验的事项。

**🤝 回复审稿意见**

> 使用 $ai-conference-reviewer。根据稿件和审稿意见，核对争议并起草 rebuttal。每项事实标明依据；缺少的结果保留待补，不写成实验已经完成。

## 📚 内容导航

| 文档 | 什么时候读 |
|---|---|
| [SKILL.md](SKILL.md) | 了解入口、任务路由与判断原则 |
| [研究发展指导](references/research-development.md) | 使用六类研究升级与验证流程 |
| [创新工作台](references/innovation.md) | 比较最近邻、设计候选贡献路线 |
| [证据审查](references/evidence-review.md) | 检查主张、实验与 LLM／agent 风险 |
| [会议画像](references/venues.md) | 比较六会定位与贡献契合度 |
| [主席经验卡](references/chair-lessons.md) | 理解组织者复盘及其适用边界 |
| [审稿与回复](references/review-rebuttal.md) | 模拟评审、分析分歧、准备回复 |
| [问题地图](references/research-map.md) | 从研究方向寻找可检验的问题 |
| [投稿检查](references/submission.md) | 核验目标届次、track 与投稿流程 |
| [来源账本](references/sources.md) | 追溯出处、读取范围与核验状态 |

## 🔎 来源与边界

知识快照：**2026-09-10**，以 2026 届官方指南和部分 2025 年主席复盘为主。实际投稿需重新核验目标届次与 track。

- **建议与规则分开：**官方资料不自动等于硬性要求；推断、假说和未核验信息明确标注。
- **证据不足就保留未知：**未提供材料不等于没做实验；模拟意见不冒充真实评审。本版没有真实公开审稿个案集。
- **选题不等于录用预测：**热点地图是定性方向，不是热度排名；不推断个人录用概率或委员会偏好。
- **六会不全等同于 CCF-A：**分类版本与核验限制见[会议画像](references/venues.md)，考核以适用目录和单位文件为准。
- **正式代审另有约束：**须遵守目标会议的 AI 使用与保密规则，不将私人稿件写入公共知识库。

## 🌱 参与完善

欢迎通过 **issue / PR** 提交政策更新、来源纠错与使用反馈。经验请附来源、年份和适用范围；请勿上传未获授权的稿件、私人评审记录或身份信息。

本仓库原创指令、凝练文本与配置采用 [MIT License](LICENSE)。外链论文与会议材料保留各自权利。
