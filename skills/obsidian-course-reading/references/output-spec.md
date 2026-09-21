# Output specification

## Shared language and source rules

Follow the language mode in SKILL.md. Chinese source plus Chinese preference means Chinese throughout, with no added English headings, summaries, or answers. Preserve original foreign-language references/names where appropriate. In bilingual mode, pair substantive Guide content in source language and preferred reading language, including findings and optional sections; diagrams use only the preferred language. Adapt example labels below to the user's language.

PDF anchors are required in both notes. Use actual PDF page order (1-based); distinguish printed page numbers if shown. A displayed range such as `PDF 第 6–8 页` links to its first page, not an invented range destination. Use vault-relative paths where necessary, and escape alias pipes inside Markdown tables: `[[path/source.pdf#page=6\|PDF 第 6–8 页]]`. Verify the destination and correspondence. If a location is uncertain, check it rather than fabricate an anchor.

## Reading

- Week-prefixed original title, translated title only in bilingual mode, then authors.
- Links to the companion Guide and an existing course home page; do not create a broken course-home link when none exists.
- Brief usage note explaining the selected layout and module-level PDF links.
- Preserve all substantive source information, original section order, footnotes, figures, captions, tables, and references. Repair extraction artifacts without rewriting source claims.
- Bilingual: source paragraph left, aligned translation right in native Markdown table cells. One table per continuous section, one paragraph pair per row, empty headers hidden in reading view. Native Live Preview editing and `==highlight==` must work. No raw HTML prose wrappers. Use a subtle continuous center divider, ordinary prose spacing, no cards or per-paragraph borders. On narrow screens stack columns and hide the divider; use available width on wide screens.
- Chinese-only/original-only: ordinary single-column Markdown, no empty second column or bilingual CSS. Translate-only when explicitly requested: single-column translation with original PDF anchors.
- Recreate source tables as tables; translate content only for modes requiring it. Embed figures where they occur with corresponding captions. Keep references in their original language.
- One source link at each section or figure/table module, covering its pages; do not repeat per paragraph.
- Store the PDF alongside notes and embedded figures in `assets/`.

## Guide & Notes: baseline

Use this stable order, adapting method labels to article type. Provide useful explanation rather than a bare outline; avoid exhaustive reporting and repetition. Start each major section with its source link(s), adding item-level links when concepts, experiments, or findings have distinct locations. Do not make readers rely only on recall-question links.

### 1. Titles and orientation — 先知道这篇文章在讲什么

Use the week and article title, authors, and a link to the Reading. Preserve an accessible, connected narrative: explain the phenomenon or puzzle, why it matters, the author's approach, and the broad answer. Let a reader unfamiliar with the article get a feel for it before technical details. Do not reduce this to keywords or an abstract-like checklist. In bilingual mode include a corresponding concise overview, without adding a second layer of information. A short retrieval cue may name themes, concepts, or debates useful for finding this reading at term end; do not draft essay applications. Link to the relevant introduction/summary pages.

### 2. 文章的核心问题

State the question the article tries to answer, distinguishing it from the broad topic. Keep subordinate questions only when they clarify the main investigation. Provide source location.

### 3. 问题背景与学术争论

From the article's background and literature review, identify the relevant scholars or approaches, their answers, and the inadequacies the author identifies. If an explicit interlocutor exists, explain that position fairly and the author's specific objection. Distinguish extending an approach from opposing it. Present this as the article's account of the debate, not a verified complete history of the field. Do not invent an opponent or initiate a separate literature survey by default. Cite the relevant pages.

### 4. 理论支持和关键概念

Explain the concepts needed to follow the article. In bilingual mode use columns `Concept`, `中文概念与解释` (adapt to preferred language), and `English explanation from the article` (adapt to source language). Use brief exact original wording for the source-explanation column, with quotations clearly marked; do not invent quotations. If no concise definition appears, label a paraphrase explicitly. In Chinese-only mode use `概念`, `解释`, `原文依据`. Anchor concepts individually when their sources differ, otherwise group a shared source link. Explain what the concept means here; describe measurement/operationalization in research design rather than repeating it.

### 5. 研究设计

Make this an independent section. Use a compact table and enough explanation to understand how the evidence was produced. Select applicable dimensions instead of forcing all articles into an experiment template:

- Setting/site, participants or objects, and data/material sources.
- Sample size with units and relevant stages/groups, sampling/recruitment/selection criteria, or field-entry/access process.
- Duration, timing, waves, and concrete procedure.
- Operationalization: how concepts become variables, indicators, measures, manipulations, observation dimensions, or coding categories.
- Data collection and analysis: describe what the quantitative or qualitative procedure does and how it supports the question; avoid merely listing technique names.
- Experiments/quasi-experiments: groups, comparison/control, assignment/randomization or identification basis, manipulation/intervention, outcome measurement, and design details necessary to interpret findings. Distinguish participants from observations and initial from analyzed samples when material. Locate separate experiments separately.
- Qualitative work: field access, researcher role when relevant, interviews/observations/documents, recording and coding/interpretive process, and duration where reported.
- Mixed methods: explain how the parts connect.

For important unreported details, say `文中未说明`; do not treat non-reporting as automatically a flaw. For theoretical/review/other non-empirical articles, use `材料与论证路径` or another accurate label and explain source selection or reasoning approach; do not invent empirical design fields. Every design/experiment module must link to its PDF location.

### 6. 文章结构与关键论证、发现

Provide a Mermaid article-structure diagram that covers the whole major arc in the article's actual order, using only the preferred reading language. Label nodes by what each part contributes, not just `Introduction` or `Results`. Expand key arguments or findings selectively; use a simpler diagram for simple articles and an extra level for complex ones. Do not reproduce every paragraph or default to an exhaustive mind map. Derive it from the cached outline. A research-procedure diagram does not substitute for this article-wide map.

Then explain major arguments/findings with supporting evidence and their role in the argument. In bilingual mode use one concise, aligned paragraph pair per claim, source left and translation right in a native Markdown table. Both sides must carry corresponding information. Guide-authored English is a summary, not an original quotation; mark actual quotations and supply anchors. Do not switch this section to Chinese-only in bilingual mode. Group links by finding; link specific tables/figures when helpful. Explain material evidence boundaries alongside the claim rather than hiding them in optional analysis.

### 7. 最终结论

State the author's answer and its scope, with brief central original quotations plus interpretation and PDF locations. Use aligned bilingual explanation in bilingual mode and Chinese throughout Chinese-only mode. Avoid repeating all findings.

### 8. 你可能还想知道 — optional additional analysis

Preserve substantive specialist/helper analyses that exceed the baseline instead of rejecting them based on assumed classroom relevance. Include only when extra analysis exists; no fixed item count or manufactured content. Use collapsed, specifically titled callouts, e.g. `> [!info]- 操纵检验说明了什么`. Explain the issue and its relationship to this article with enough substance to be useful, and include PDF anchors. Separate what the author states from analytical interpretation, uncertainties, and externally sourced context; verify external claims or label them unverified rather than stating them as fact. Never treat helper criticism as inherently correct.

Merge duplicates. Keep core comprehension requirements in their baseline sections. If supplemental analysis is unusually long, put it in a linked supplemental note and give a meaningful preview here; keep the default package at two notes otherwise. Readers choose what to expand. Bilingual mode applies inside these callouts too.

### 9. 反思与讨论

Offer 1–3 concrete questions tied to a concept, inference, case, measurement, or evidence-to-conclusion step, each with its PDF location. Invite scrutiny without presuming a defect. Distinguish author-acknowledged limitations from Guide-raised questions. A brief thinking cue is allowed, but do not supply a mandatory answer. Adapt to article type; do not reflexively criticize sample size, missing randomization, or generalizability without considering the author's actual claim. Use paired questions/cues in bilingual mode. This section invites thought; the optional preceding section supplies additional analysis.

### 10. 五个快速回忆问题

Exactly five useful collapsed questions with answers, covering concepts, cases, design, or major findings. Avoid trivia and questions answered only by saying the article cannot establish something. Source references supplement answers, not replace them.

Bilingual example (adapt languages as needed):

```markdown
> [!question]- 1. English question?／中文问题？
> **中文**：准确、简洁的中文答案。
>
> **English**: A concise, accurate English answer.
>
> [[source.pdf#page=3|原文 PDF 第 3 页]]
```

Chinese-only example:

```markdown
> [!question]- 1. 中文问题？
> 准确、简洁的中文答案。
>
> [[source.pdf#page=3|原文 PDF 第 3 页]]
```

### 11. 我的记录

End with one empty `## 我的记录` section (localize for other reading languages). No subheadings, writing prompts, or separate classroom-notes section.

## Presentation constraints

Keep Guide and Reading separate for independent scrolling and review. Prefer direct statements; avoid repetitive `不是……而是……` / `not X but Y` framing. Omit redundant publication metadata, a separate research-subject field, visible audits, and attachment inventories unless requested. Preserve source accuracy, annotations, and meaningful detail while avoiding repetition. Never generate submit-ready assignments from these notes.
