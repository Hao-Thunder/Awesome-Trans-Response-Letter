---
name: ieee-twc-response-letter
description: rewrite, reorganize, and strengthen a single-reviewer-comment response letter for ieee transactions on wireless communications or closely related ieee wireless communications journals. use when the user provides one reviewer comment, a draft response, and manuscript revisions or planned revisions, and wants a formal english latex response that gives a technically rigorous explanation, identifies concrete manuscript changes, and supplies polished blue-marked replacement text without inventing page numbers, equations, experiments, or results.
---

# IEEE TWC Response Letter

## Overview

Produce a publication-ready response to one reviewer comment. Accept Chinese or English source material, but write the main response letter in formal English LaTeX. Ensure that the response does not merely explain the issue: it must connect each substantive claim to a concrete manuscript revision.

Read `references/response-pattern.md` before drafting the final answer.

## Required Input

Identify these three inputs:

1. The reviewer's original comment.
2. The author's draft response.
3. The manuscript text already revised or the exact revisions the author plans to make, including relevant equations, figures, tables, experiments, analyses, or section changes.

Process one reviewer comment per invocation.

If a required input is missing, request only the missing item. Do not ask for information that is already present. If page, section, equation, figure, or table numbers are unknown, retain explicit placeholders such as `XX--XX`, `Section X`, `Eq. (X)`, or `Fig. X`; never invent them.

## Workflow

### 1. Diagnose the reviewer concern

Infer the central concern behind the literal wording. Classify it as one or more of the following:

- missing technical explanation;
- unclear novelty or contribution;
- unsupported claim;
- incomplete derivation or notation;
- inadequate experiment or comparison;
- ambiguity in assumptions, scope, or system model;
- inconsistency among text, equations, figures, tables, or references;
- presentation or language problem.

State the answer to the real concern, not merely a paraphrase of the comment.

### 2. Audit the proposed revision

Check whether the supplied manuscript change actually resolves the concern. Verify that:

- every major response claim is reflected in the revised manuscript text;
- the response distinguishes explanation from manuscript modification;
- technical claims are supported by a derivation, assumption, citation, figure, table, experiment, or explicit discussion when needed;
- symbols, dimensions, indices, acronyms, terminology, and equation references are consistent;
- no new claim creates an obvious follow-up objection.

When the supplied revision is insufficient, strengthen it using only information supported by the user's materials. Do not fabricate numerical results, citations, experiments, implementation details, reviewer intentions, or manuscript locations. Mark unresolved items as author-side checks after the LaTeX artifact.

### 3. Draft the explanatory response

Use a restrained and professional IEEE journal tone. Follow this logical sequence:

1. Thank the reviewer for the constructive comment.
2. Acknowledge the specific ambiguity, omission, or weakness in the original manuscript without using exaggerated self-criticism.
3. Explain the technical point directly and rigorously.
4. Enumerate the concrete revisions made in the manuscript.
5. Explain why those revisions resolve the concern.

Avoid generic statements such as "we have revised the manuscript accordingly" unless immediately followed by precise changes. Avoid defensive, emotional, promotional, or overly deferential language.

### 4. Introduce the revised manuscript text

Use this sentence pattern, adapting the object and action to the actual revision:

```latex
To further clarify [this point or the specific issue], in the revised paper, we have [revised/added/expanded/clarified/corrected] [the relevant section, analysis, equation, figure, table, experiment, or discussion] on page(s) XX--XX as follows:
```

Prefer a specific noun phrase over "this point" when the issue can be named concisely. Use singular `page` or plural `pages` correctly. Use `page(s) XX--XX` only when the location is unknown.

### 5. Produce manuscript-ready replacement text

Polish the supplied revision so that it can be pasted directly into the paper. Preserve the technical meaning while correcting grammar, logic, terminology, notation, redundancy, and possible sources of renewed reviewer concern.

Mark all added or revised prose with `\textcolor{blue}{...}`. Apply coloring in compilable units:

- wrap each continuous prose paragraph or sentence separately;
- do not place multiple paragraphs inside one `\textcolor` command;
- inside a display equation, color the mathematical content rather than wrapping the entire equation environment;
- for figures or tables, color the revised caption text or the added explanatory sentences rather than wrapping a complete float environment.

Preserve valid LaTeX commands, labels, citations, cross-references, equation numbering, and mathematical notation. Escape literal special characters when required.

### 6. Run the final consistency check

Before responding, verify all of the following:

- one reviewer comment only;
- main output is formal English LaTeX;
- the reviewer concern is answered explicitly;
- original weakness is acknowledged precisely;
- concrete manuscript modifications are named;
- the explanatory response and blue manuscript text are mutually consistent;
- no page, section, equation, figure, table, citation, experiment, or result has been invented;
- all placeholders are visible and actionable;
- the revised text is grammatically and technically polished;
- the wording does not overclaim that a planned change has already been completed unless the supplied revised text is ready for incorporation;
- the LaTeX is structurally plausible and directly reusable.

## Output Contract

Return the following in order:

1. A complete LaTeX response-letter block following `references/response-pattern.md`.
2. Only when necessary, a short section titled `Author-side checks (not part of the response letter)` after the LaTeX block. Use the user's language for these checks. List only unresolved issues such as missing page numbers, unsupported numerical claims, notation conflicts, absent experiments, or figure/table synchronization.

Do not add a general essay about response-letter writing. Do not provide multiple stylistic variants unless the user explicitly requests them.
