# AI Conference Reviewer · AI 顶会研究与审稿助手

面向 **ACL、EMNLP、AAAI、ICML、ICLR、NeurIPS** 的中文研究辅助 skill：从想法梳理、创新设计和证据诊断，到会议匹配、模拟审稿与 rebuttal。

独立维护 AI/NLP 六个会议的研究与投稿知识。以官方指南、主席复盘与经验凝练为主，无需 Zotero、论文全文库或额外 API key。

## 快速安装

这是供支持 `SKILL.md` 的 AI 助手读取的指令与知识包，不是独立运行的审稿模型。需要 Git 和支持本地 skills 的 Codex；实时核验投稿政策与最近邻文献还需要宿主的联网能力。

### Codex 用户级安装（macOS / Linux）

将仓库直接克隆到用户 skills 目录：

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/chaokuboy/ai-conference-reviewer.git "$HOME/.agents/skills/ai-conference-reviewer"
```

### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force "$HOME/.agents/skills" | Out-Null
git clone https://github.com/chaokuboy/ai-conference-reviewer.git "$HOME/.agents/skills/ai-conference-reviewer"
```

安装后在 Codex 输入 `$ai-conference-reviewer`。如果未出现，重启 Codex 后再查看技能列表。
当前官方用户级路径为 `~/.agents/skills`；部分已有环境使用 `~/.codex/skills`，请按宿主实际配置选择一个路径，避免重复安装同名 skill。详见 [OpenAI 官方 skills 文档](https://learn.chatgpt.com/docs/build-skills)。

若只供某个项目使用，可在项目根目录执行：

```bash
mkdir -p .agents/skills
git clone https://github.com/chaokuboy/ai-conference-reviewer.git .agents/skills/ai-conference-reviewer
```

以上命令用于本地安装；若要把 skill 随另一个 Git 项目发布，请使用 submodule 或复制文件，避免将嵌套仓库误当普通文件夹提交。

更新已安装版本：

```bash
git -C "$HOME/.agents/skills/ai-conference-reviewer" pull --ff-only
```

若目标目录已存在，先检查它是否是本仓库，再更新；不要覆盖本地修改。其他支持 Agent Skills 的工具可按其安装约定放置整个目录，需保留 `references/` 的相对路径；尚未对所有宿主做兼容验证。

## 使用示例

**梳理想法**

> 使用 $ai-conference-reviewer。我想研究多智能体讨论能否提高学术审稿质量。请逐轮追问，帮我区分真正的研究问题与简单组件组合。

**设计创新**

> 使用 $ai-conference-reviewer。根据我提供的三篇最近邻论文，提出两条不同的创新路线，说明最小判别验证、计算预算和停止条件。

**论文诊断与选会**

> 使用 $ai-conference-reviewer。请基于附件论文比较 ACL 与 ICLR 的契合度，区分已证实的问题和待确认项，列出最重要的三个证据缺口。

**模拟审稿与回复**

> 使用 $ai-conference-reviewer。根据稿件和真实审稿意见，检查争议是否成立，模拟 AC 对分歧的判断，并起草有证据定位的 rebuttal。没有完成的实验不要写成已经完成。

**研究升级与实验改良**

> 使用 $ai-conference-reviewer。根据我的想法、最近邻、已有结果和预算，诊断最重要的研究差距，提出两条候选创新路线。为首选路线设计最小判别验证、必要基线、数据划分和决策条件；根据不同结果说明继续、缩小主张或停止的选择，不承诺录用。

**论文论证与成熟度复查**

> 使用 $ai-conference-reviewer。把现有结果整理成贡献—证据映射，检查摘要是否超出结果范围，并区分投稿前必须解决、表达可修复、可选拓展和待确认事项。

**投稿规则**

> 使用 $ai-conference-reviewer。核验我指定届次和 track 的官方投稿要求，明确正文页数、附件、匿名、commitment 和回复规则。

## 内容导航

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 入口、工作流路由与判断纪律 |
| [会议画像](references/venues.md) | 六会定位、NLP 与机器学习／综合 AI 的选会比较 |
| [研究发展指导](references/research-development.md) | 差距诊断、创新升级、实验改良、结果决策、论文论证和成熟度复查 |
| [创新工作台](references/innovation.md) | 最近邻、创新路径、资源约束与判别验证 |
| [证据审查](references/evidence-review.md) | 主张—证据匹配及 LLM/agent 特有风险 |
| [主席经验卡](references/chair-lessons.md) | 官方复盘、审稿要求与经验转化 |
| [审稿与回复](references/review-rebuttal.md) | 模拟 reviewer、AC、rebuttal 与修改计划 |
| [问题地图](references/research-map.md) | 热点切口、可检验问题与研究风险 |
| [投稿检查](references/submission.md) | 动态规则核验及投稿实践 |
| [来源账本](references/sources.md) | 官方链接、适用年份与核验范围 |

## 来源与边界

知识快照：**2026-09-10**，主要覆盖 2026 届指南与部分 2025 年主席复盘。实际投稿须重新核验目标届次及 track。

- 分开记录来源身份与陈述性质：官方资料不自动等于硬性要求；评价建议、历史事实和假说各自标明。
- 本版未收集真实公开审稿个案数据集；示例评论是模拟意见。
- 热点地图为定性研究方向，不是六会论文普查或录用偏好排名。
- 六个会议不全等同于 CCF-A。EMNLP 官方历史条目列 B；最新总目录核验限制见来源账本，考核以适用目录和单位文件为准。
- 不预测录用概率，不代表会议委员会；正式受托审稿需遵守相应 AI 使用与保密规则。

## 维护与贡献

欢迎通过 issue 或 PR 提交官方政策更新、来源纠错及可复现的使用反馈。新增经验请注明来源、年份、适用范围，并区分官方规定与个人建议。请勿提交未获授权的稿件、私人审稿记录或身份信息。

## 许可

本仓库原创指令、凝练文本与配置采用 [MIT License](LICENSE)。链接所指向的第三方论文、会议网页和其他材料保留各自权利；本许可不为这些外部材料重新授权。
