---
name: readable-human-writing
description: "Improve Chinese answers and prose with reader-first structure: use conclusion-first writing, pyramid logic, SCQA, MECE checks, argument trees, useful document formats, and natural human voice while preserving facts, nuance, terminology, citations, and the user's voice. Use when drafting or revising chat replies, explanations, reports, proposals, strategy documents, meeting notes, documentation, emails, articles, or public-facing copy. Do not use for code formatting, factual verification, translation, or requests to impersonate a real person."
---

# Readable human writing

Use this skill when the content is factually settled but the reader needs a clearer structure, better flow, or more natural Chinese expression. It supports both drafting from an idea and revising an existing text.

## Operating modes

Choose one mode before editing:

- **Structure-first:** build or repair the argument before writing prose. Use for reports, proposals, strategy documents, research summaries, and long explanations.
- **Polish-only:** preserve the existing structure and make the language clearer and more natural. Use when the user asks for润色, 改错, or保持原意。
- **Deep rewrite:** reorganize and rewrite substantially while preserving facts and intent. Use only when the user permits structural changes or the source is difficult to use.

If the requested mode is unclear, default to **structure-first** for long or decision-oriented documents and **polish-only** for short text.

## Workflow

Apply these steps in order. For a short answer, compress them silently; for a long document, show the outline before drafting when that helps the user review the direction.

1. **Identify the reader and outcome.** Determine who will read this, what they need to decide or do, and what constraints matter: length, tone, channel, deadline, evidence, and format.
2. **State the core answer.** Write one sentence that answers “所以呢？” If the source cannot support a clear conclusion, state the uncertainty or ask for the missing decision criterion instead of inventing one.
3. **Choose a frame.** Use the smallest useful frame from [references/formats.md](references/formats.md): simple answer, recommendation, SCQA, problem-solution, one-page strategy, research/report, how-to, comparison, or rewrite.
4. **Build the pyramid.** Put the core answer at the top, then group the few reasons that support it, then place evidence, examples, risks, and details below. Each lower level must answer “为什么？” or “怎么证明？”.
5. **Check the grouping.** At each level, ensure items share one classification rule, are mutually exclusive enough to avoid obvious overlap, collectively cover the decision-relevant space, and appear in a meaningful order. Do not force artificial MECE when the source is incomplete; name the boundary.
6. **Choose the logic.** Use deduction when a general principle leads to a specific implication. Use induction when several facts support a pattern or conclusion. Use chronological, structural, priority, or cause-effect order only when it matches the reader's question.
7. **Draft with viewpoint headings.** Make headings state the conclusion or question the section resolves, not merely repeat the topic. Keep one main claim per paragraph and put the claim before its explanation.
8. **Humanize after structure.** Replace vague abstractions with concrete actors, actions, evidence, and consequences. Vary sentence length naturally, remove ritual transitions, and preserve the author's level of confidence and voice.
9. **Control the output.** Keep only formatting that reduces reading effort. Use bullets for parallel items or steps, tables for real comparisons, and numbered headings for sequences or long documents. Do not expand a short answer into a report.
10. **Run the final review.** Use [references/review-checklist.md](references/review-checklist.md). Confirm that the conclusion is visible early, each section earns its place, facts and caveats remain intact, and the ending gives a concrete decision, limitation, or next action when needed.

## Priority rules

When rules compete, follow this order:

1. Preserve factual correctness, user intent, citations, code, quoted text, and explicit uncertainty.
2. Put the user's answer, decision, or requested revision first.
3. Repair the reasoning and grouping before polishing sentences.
4. Use the smallest structure that makes the reading path clear.
5. Improve naturalness only after the structure is sound.
6. Add detail or formatting only when it lowers the reader's effort.

## Pyramid and MECE guardrails

- **Conclusion first:** state the answer, recommendation, or decision before background.
- **Answer–reason–evidence:** use the hierarchy `核心结论 → 一级理由 → 二级证据/例子/风险`.
- **One level, one question:** siblings should answer the same kind of question and stay at a comparable abstraction level.
- **One grouping rule:** sort by time, cause, structure, priority, or another explicit rule; do not mix rules casually.
- **MECE as a diagnostic:** look for material overlap and important omissions, but do not split one idea into artificial categories just to satisfy the acronym.
- **Evidence boundary:** distinguish fact, interpretation, assumption, proposal, and open question.
- **Title as navigation:** prefer “上线前必须补齐数据权限” over “数据权限”; prefer “方案 B 成本低但迁移风险更高” over “方案对比”.

## SCQA and document frames

Use SCQA when the reader needs context before the answer: **Situation → Complication → Question → Answer**. Do not force all four parts into a short response.

Use these defaults when the task matches them:

- **Recommendation:** recommendation → decision criteria → trade-offs → action.
- **One-page strategy:** facts → problem → idea → solution → metric/risk.
- **Project proposal:** current state → problem → objective → options → recommended plan → resources → risks → next step.
- **Review or retrospective:** goal → result → gap → cause → lesson → action owner and deadline.
- **Research/report:** executive takeaway → method/evidence → analysis → limits → implications/actions.
- **How-to:** outcome → prerequisites → numbered steps → verification → pitfalls.
- **Comparison:** decision rule → compact comparison → recommendation → caveats.
- **Email or chat:** purpose/answer → essential context → requested action → deadline or dependency.

See [references/formats.md](references/formats.md) for selection rules and compact templates.

## Context and formatting

Introduce background only when it helps the reader understand the answer. For longer documents, use `background → explanation → evidence/implementation → impact/next action` when all four layers exist.

- Preserve useful numbering and hierarchy; use `1.`, `1.1`, `2.` consistently.
- Preserve indentation in nested lists, quotes, tables, and code.
- Keep executable commands, SQL, JSON, YAML, and code examples unchanged except for clearly requested formatting fixes.
- Keep tables when readers need to compare items; otherwise prefer prose or bullets.
- Keep citations, URLs, proper nouns, exact numbers, and quoted material unchanged unless asked.
- Use Chinese punctuation consistently. Avoid decorative emoji, excessive bold, heavy em-dash use, and headings that merely repeat the topic.

## Remove mechanical AI patterns

Treat patterns as signals, not a forbidden-word list. Rewrite only when a phrase is empty, repeated, inflated, or out of register. Review [references/patterns.md](references/patterns.md) for examples.

- Delete throat-clearing openings such as “这是一个很好的问题。下面我将……”.
- Replace vague claims such as “意义重大”“影响深远”“发挥关键作用” with the concrete consequence or remove them.
- Reduce formulaic contrasts, stacked synonyms, repeated transition words, generic praise, fake quotations, and paragraph-ending mini-summaries.
- Replace nominalizations and hedging stacks with plain verbs: “能够进行处理” → “可以处理”; “可能会带来一定影响” → “可能影响”.
- Prefer a named actor over an abstract actor when the actor is known.
- Do not add jokes, anecdotes, mistakes, slang, or strong opinions solely to appear human.
- This improves naturalness but does not guarantee any AI-detector result and never justifies misrepresenting authorship or provenance.

## Output-size control

- Put the conclusion, essential evidence, and required action in a self-contained opening block.
- Answer in one or two short paragraphs when that is enough.
- Use a list only for explicit parallel items, choices, or ordered steps.
- Use a table only when the reader must compare multiple objects across the same dimensions.
- Remove optional detail before leaving any sentence, table, code fence, or section unfinished.
- Do not restate the user's question or append a generic “如果你还有问题……” ending.

## Final pass

Silently check:

- Is the answer visible in the first paragraph?
- Is the core conclusion supported by reasons at the next level?
- Do sibling points share an abstraction level and a grouping rule?
- Did I distinguish facts, interpretations, assumptions, proposals, and uncertainties?
- Does every heading, list, table, code block, or separator reduce effort?
- Did I preserve facts, caveats, citations, code, terminology, and intended tone?
- Did I remove empty transitions, inflated claims, repetition, and ritual conclusions?
- Did I avoid turning a short answer into a report?
- Does the ending give a concrete decision, limit, or next action when needed?

## Scope boundary

Use this skill to edit human-facing prose and the reasoning structure expressed in that prose. Do not override the domain skill responsible for factual correctness, file formats, citations, APIs, code, or external side effects. Apply it to the prose around those outputs, not to code or structured data itself.
