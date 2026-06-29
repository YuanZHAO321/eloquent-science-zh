# 科技写作之道 —— 一个 Claude Code Skill(中文版)

> 清晰地写作、修改和展示科学成果。

一个 [Claude Code](https://claude.com/claude-code) **Skill**,做为 Claude 可按需调用的可操作体系 —— 起草论文、收紧摘要、设计图表、
准备报告,或评审同行的稿件。书中建议适用于任何技术学科。

> 🇬🇧 English version: [`eloquent-science`](../eloquent-science)

---

## 它能做什么

当你请 Claude 起草、组织或修改科技文字时,本 Skill 会自动加载,并应用书中原则:

- **写作/修改漏斗** —— 从最大尺度(文档)逐级向下修改到最小尺度(词语、细节),在结构稳固之前绝不打磨句子。
- **简洁 + 精确** —— 用尽可能少的字说清楚,并说出你*确切*想表达的意思。
- **具体、即用的指南** —— 主动/被动决策表、啰嗦短语 → 简短替代对照表、段落连贯机制、图设计规则、"每个要点约 5 分钟"的报告法则,以及逐章节的论文模板。

## 安装

把本仓库克隆(或复制)到你的 Claude Code skills 目录:

```bash
# 个人级 —— 在所有项目中可用
git clone https://github.com/<you>/eloquent-science-zh.git \
  ~/.claude/skills/eloquent-science-zh

# …或项目级 —— 仅在某个仓库中可用
git clone https://github.com/<you>/eloquent-science-zh.git \
  /path/to/project/.claude/skills/eloquent-science-zh
```

Claude Code 会发现 `.claude/skills/` 下任何包含 `SKILL.md` 的文件夹。
无需构建步骤,也无依赖。

## 使用

直接描述写作任务 —— Skill 会自行触发:

```
用 eloquent-science-zh 帮我收紧这段摘要
<粘贴摘要>
```

```
按 eloquent-science-zh 的原则,为一篇关于 <主题> 的论文起草引言
```

```
作为同行评审人评审这一节稿件
```

也可用 `/eloquent-science-zh` 显式调用。

## 仓库结构

```
eloquent-science-zh/
├── SKILL.md                       # 核心:理念、漏斗、工作流程、首要习惯
├── README.md                      # 你正在看的文件
└── references/                    # 按需为具体任务加载
    ├── paper-structure.md         # 标题、摘要、引言、方法、结果、讨论……
    ├── clear-writing.md           # 段落连贯 + 句子构造
    ├── word-usage.md              # 简洁对照表、应避免的词、精确性陷阱
    ├── figures-tables.md          # 图设计、图题、字体/配色、引用
    ├── revision-checklist.md      # 把漏斗变成 6 遍检查清单 + 伦理
    ├── presentations.md           # 聚焦信息、幻灯片设计、时间控制、紧张
    └── peer-review.md             # 如何阅读、组织并撰写评审意见
```

`SKILL.md` 保持精简(它始终在上下文中);`references/` 文件仅在任务需要时拉入,
让 Claude 的上下文保持聚焦。

## Skill 的工作原理

一个 Skill 就是一个含 `SKILL.md` 的文件夹,其 YAML frontmatter 带有 `name` 和
`description`。`description` 告诉 Claude *何时*使用该 Skill;正文告诉它*如何*用。
支撑文件(此处的 `references/`)采用渐进式披露,使大段指南不会拖累每次对话。
详见 [Claude Code 文档](https://docs.claude.com/en/docs/claude-code)。

## 许可证

本仓库中的 skill 文件以 [MIT 许可证](LICENSE) 发布。该许可证仅涵盖这些文件的
原创措辞与组织,并不授予对受版权保护的原书的任何权利。
