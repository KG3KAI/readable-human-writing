# readable-human-writing

一个面向中文回答和文章二次编辑的 Agent Skill。它先搭建读者能快速理解的论证结构，再组织信息顺序，最后减少空洞、机械、模板化的 AI 写作痕迹。

它适用于对话回复、技术说明、报告、邮件、文档、文章和对外文字。核心规则包括：

- 先交付结论，再解释依据；
- 用金字塔原理组织“核心结论 → 一级理由 → 二级证据”，并用 SCQA、MECE 和论证树检查结构；
- 根据场景选择推荐、方案、一页战略、复盘、研究报告、教程或对比框架；
- 支持将多轮问答重组为独立文档，并在读者、用途、篇幅或信息口径缺失时进行一次简洁确认；
- 一个段落只承载一个主要意思；
- 简单问题不用标题，列表和表格只在降低理解成本时使用；
- 长内容按背景、解释、实现或证据、影响或下一步逐层展开；
- 删除空洞开场、机械排比、泛化结论、过度强调和模板化过渡；
- 保留事实、数字、引用、代码、术语和明确的不确定性；
- 长回复先完成核心闭环，再展开可选细节，避免中途截断。

它不会为了“像人”而虚构经历、情绪或错误，也不承诺通过任何 AI 检测器。

## 安装

在支持 Agent Skills 的工具中，让 Agent 安装这个仓库：

```text
帮我安装这个 Skill：https://github.com/KG3KAI/readable-human-writing
```

Codex 也可以使用内置 `skill-installer` 从该 GitHub 地址安装。安装后新建一个会话，让 Skill 元数据重新加载。

## 使用

Skill 可根据描述自动触发，也可以显式调用：

```text
使用 $readable-human-writing 重写这段回复，让结论更早出现，减少机械 AI 腔。
```

将问答整理为文档时，可以直接说明目标：

```text
使用 $readable-human-writing，把当前问答整理成正式文档。
如果读者、用途、篇幅或信息口径会影响结构，请先用一个合并问题向我确认；
不要按对话顺序拼接，未确认内容标记为“待确认”。
```

Skill 不会为简单回复和普通润色机械追问。只有缺失信息会实质改变正式文档时，才会先提出带默认值的简洁确认；如果用户说“直接生成”或“你决定”，则跳过确认并采用合理默认值。

## 结构

```text
readable-human-writing/
├── SKILL.md
├── agents/openai.yaml
├── references/formats.md
├── references/patterns.md
├── references/review-checklist.md
└── evals/cases.yaml
```

`SKILL.md` 保存核心流程；`references/formats.md` 提供文档结构模板；`references/patterns.md` 是 AI 写作模式复查清单；`references/review-checklist.md` 用于结构、表达和交付前检查；`evals/cases.yaml` 提供覆盖短问答、长清单、技术文本和对外文案的评测场景。

## 来源

本 Skill 综合并重新组织了以下公开方法：

- [Beautiful Markdown Writing Skill](https://github.com/alexandre-schaffner/revv/blob/main/beautiful_md.skill.md)：阅读动线、视觉密度、Markdown 结构和叙事节奏。
- [Humanizer-zh](https://github.com/op7418/Humanizer-zh)：中文 AI 写作模式识别与自然表达。
- 当前仓库的规则设计、触发边界、输出闭环和评测样例为本项目新增内容。

上游项目均采用 MIT License。具体归属见 [NOTICE](NOTICE)。本项目关注可读性和自然表达，不把任何检测器结果作为真实性或质量证明。

## License

[MIT](LICENSE)
