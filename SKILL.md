---
name: readable-human-writing
description: "Improve Chinese answers and prose for human reading: put the conclusion first, build a clear information hierarchy, control headings, lists, tables, and whitespace, remove repetitive AI-style phrasing, and preserve facts, nuance, terminology, and the user's voice. Use when drafting or revising chat replies, explanations, reports, documentation, emails, articles, or public-facing copy where the text feels mechanical, over-structured, verbose, generic, or difficult to scan. Do not use for code formatting, factual verification, translation, or requests to impersonate a real person."
---

# Readable human writing

Use this skill as a final editorial pass after the answer's facts and reasoning are settled. It applies both to responses written from scratch and to second-pass polishing of articles, documents, emails, reports, and public-facing copy. Optimize for a reader's next question, not for maximum structure or a detector score.

## Priority rules

When rules compete, follow this order:

1. Preserve factual correctness, user intent, citations, code, and explicit uncertainty.
2. Put the user's answer or requested revision first.
3. Use the smallest structure that makes the answer easier to understand.
4. Improve naturalness only after the reading path is clear.
5. Add detail, formatting, or explanation only when it lowers the reader's effort.

## Editorial order

Apply the following order:

1. **Preserve substance.** Do not invent facts, personal experience, sources, confidence, or emotion. Keep technical terms, numbers, citations, code, quoted text, and explicit uncertainty intact unless the user asks for a change.
2. **Choose the smallest useful shape.** A one-question answer may be one or two paragraphs. Use headings only when the reply has distinct sections. Use bullets for parallel items or a sequence, not as a substitute for prose. Use a table only for genuine comparisons.
3. **Put the answer where the reader expects it.** Lead with the conclusion, decision, or next action. Follow with the two or three reasons that matter. Put background and edge cases after the main path.
4. **Build a visible reading path.** Make each paragraph carry one idea. Keep paragraphs short enough to scan. Add a transition when the topic or abstraction level changes. End without a ritual summary if the answer is already clear.
5. **Humanize without falsifying.** Prefer concrete claims, direct verbs, natural Chinese rhythm, and appropriately specific judgment. Keep a professional tone unless the user asks for casual or stylized writing.

## Context before detail

For explanations, documents, and reports, introduce the situation before the mechanics. Move through **background → explanation → implementation or evidence → impact or next action** when the task has all four layers. Do not force this sequence onto a short answer or a task that only needs one layer.

Make headings answer a reader's navigation question. Prefer “为什么选择这个方案” over “方案”，and “上线前需要验证什么” over “验证”. If a reply can be understood without headings, omit them.

Keep each paragraph centered on one claim or thought. Start a new paragraph when the idea, audience, abstraction level, or decision changes. Leave enough whitespace to separate ideas, but do not insert blank lines between every sentence.

## Default formats

Select one format instead of combining all of them:

- **Simple answer:** conclusion → brief reason or caveat.
- **Recommendation:** recommendation → why → trade-off → next step.
- **How-to:** outcome → numbered steps → pitfalls or verification.
- **Comparison:** short conclusion → compact table or parallel bullets → decision rule.
- **Research/report:** executive takeaway → evidence → analysis → limits → actions.
- **Rewrite request:** revised text first; then a short note of material changes only if useful.

For a simple question, use no heading by default. For a longer response, give the reader a short orientation sentence before details so they know what the section is for and what comes next.

## Remove mechanical AI patterns

Patterns are signals to review, not words that are forbidden in every context. Rewrite only when the phrase is empty, repeated, inflated, or out of register.

Delete throat-clearing openings such as “这是一个很好的问题”“当然可以”“需要注意的是” when they add no information. Replace vague claims such as “意义重大”“影响深远”“发挥关键作用” with the actual consequence or remove them.

Avoid formulaic contrasts and rhetorical scaffolding: “不是 X，而是 Y”, “不仅……而且……”, “这不仅仅是……”, “让我们深入探讨”, “综上所述”, “总而言之”. State the positive claim directly when possible.

Reduce uniform three-part lists, stacked synonyms, repeated transition words, fake quotations, generic praise, empty calls to action, and paragraph-ending mini-summaries. Do not force two-item lists or sentence-length variation when the source needs precision.

Replace nominalizations and hedging stacks with plain verbs: “能够进行处理” → “可以处理”; “可能会带来一定影响” → “可能影响”. Prefer a named actor over an abstract actor when the actor is known.

Use first person only when it reflects the assistant's actual role (“我查到”“我建议”), never to fabricate lived experience. Do not add jokes, anecdotes, mistakes, slang, or strong opinions solely to appear human.

Use Chinese punctuation consistently. Avoid decorative emoji, excessive bold, em-dash-heavy prose, title-case headings, and headings that merely repeat the topic. Keep code, citations, URLs, proper nouns, and quoted material unchanged.

These edits improve naturalness and reduce common AI-writing signals. They are not a guarantee about any AI detector, and never justify misrepresenting authorship or provenance.

For a deeper second-pass review, read [references/patterns.md](references/patterns.md). Treat it as a diagnostic checklist, not a mechanical replacement table.

## Output-size control

- Complete the answer before expanding it. Put the conclusion, essential evidence, and required action in a self-contained opening block so the response still makes sense if later detail is omitted.
- When a full inventory would be long, group related items and report the decision-relevant differences first. Expand every item only when the user explicitly needs an exhaustive list.
- Never leave a sentence, list item, code fence, table, or section unfinished. If space is tight, remove optional detail rather than ending mid-thought.
- Answer in one or two short paragraphs when that is enough.
- Use a list only for explicit parallel items, choices, or ordered steps.
- Use a table only when the reader must compare multiple objects across the same dimensions.
- Avoid a heading, table, callout, or final summary that merely repeats the preceding sentence.
- Put background after the conclusion. Put implementation detail after the reader understands why it matters.
- Do not restate the user's question or append “如果你还有问题……” unless a concrete next action is genuinely needed.

## Final pass

Silently check before sending:

- Is the answer visible in the first paragraph?
- Does every heading, list, table, and separator reduce effort for this reader?
- Did I preserve facts, caveats, citations, code, and intended tone?
- Did I remove empty transitions, inflated claims, repetition, generic praise, and ritual conclusions?
- Did I avoid turning a short answer into a report?
- Is the response complete and closed, with no essential conclusion deferred to the end?
- Does it sound natural without adding fabricated personality or deliberate errors?

## Scope boundary

Use this skill to edit human-facing prose. Do not override the domain skill responsible for factual correctness, file formats, citations, APIs, code, or external side effects. Apply it to the prose around those outputs, not to code or structured data itself.
