# Closing Speaker（四辩）

从稿件证据中提炼核心发现及文章价值，用于撰写、修改、压缩或核查学术论文的摘要与结论。

An academic-writing skill for drafting, revising, shortening, and auditing abstracts and conclusions against manuscript evidence.

## 功能 / Features

- **摘要 / Abstracts**：组织具体问题、目的、必要方法、主要发现与文章价值；默认英文摘要及关键词，支持按要求输出中文或双语。默认格式受期刊及本次要求约束。
  Organize the problem, objective, essential methods, findings, and contribution. Default to an English abstract and keywords; follow requested language and journal format.
- **结论 / Conclusions**：通读全文和相关图表，提取并排序独立判断，先提交候选供作者确认，再写结论；已有确认或用户明确要求直接写作时沿用其指示。以3–4项核心判断为目标，不为凑数添加发现。
  Read the manuscript and relevant figures, extract and rank candidate findings, and seek the author's selection before drafting. Reuse prior decisions or follow an explicit request to draft directly. Aim for 3–4 substantive findings without inventing findings to meet that target.
- **一致性核查 / Consistency audits**：逐项检查主张的正文依据、数值、比较对象、条件与推论强度，并给出可回查位置和最小修改建议。
  Trace claims to inspected evidence, check values, comparators, qualifications, and claim strength, and propose targeted corrections.

## 安装 / Installation

将整个仓库放入本地 Codex 技能目录，保留 `references/` 和 `agents/` 结构：

Clone the complete repository into the local Codex skills directory, preserving its folder structure:

```bash
git clone https://github.com/AISlowDown/closing-speaker.git ~/.codex/skills/closing-speaker
```

安装后，在支持技能的 Codex 对话中用 `$closing-speaker` 或“四辩”调用。本技能为 Markdown/YAML 工作流程；读取稿件所需的文件工具由宿主环境提供。

Invoke `$closing-speaker` in a skill-enabled Codex chat. This repository supplies Markdown/YAML instructions; manuscript-reading tools come from the host environment.

## 示例 / Examples

`manuscript.docx` 代表用户提供的当前稿件。

`manuscript.docx` is a placeholder for the manuscript supplied in the chat.

```text
请使用 $closing-speaker，依据 manuscript.docx 起草约200词的英文摘要，
保留决定性证据和适用条件，最后一句说明本文增加了什么认识或能力。
```

```text
Use $closing-speaker to revise the Conclusion in manuscript.docx.
Read the full manuscript and relevant figures, then present the candidate
findings and evidence for my selection before drafting the final section.
```

## 证据限制 / Evidence boundaries

只使用实际检查过的稿件内容；现有摘要或结论不能代替正文证据。材料不完整时明确阅读范围和缺口，不能声称完成全文验证。保持因果状态、单位、比较方向与不确定性；不虚构结果、机制、验证、引文、定位或新颖性。只编辑用户授权的章节。

Use inspected materials and identify missing evidence. An existing abstract or conclusion is a comparison target, not independent proof. Preserve causal status, units, comparisons, and uncertainty. Do not invent findings, mechanisms, validation, citations, locators, or novelty, and keep edits within the requested scope.

## 目录 / Contents

```text
closing-speaker/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── abstract-protocol.md
│   ├── conclusion-protocol.md
│   └── consistency-audit.md
├── README.md
└── .gitignore
```

写作规则以 [SKILL.md](SKILL.md) 及其引用文件为准。

The workflow is defined by [SKILL.md](SKILL.md) and its linked references.

## 许可 / License

源技能未提供 `LICENSE` 文件；此分发副本未另行指定许可。

The source skill contains no `LICENSE` file. This distribution does not assign a license.
