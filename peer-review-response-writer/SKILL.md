---
name: peer-review-response-writer
description: draft, revise, translate, and audit evidence-grounded academic responses to peer-review comments. use when authors need point-by-point response letters, rebuttals, revision explanations, revised manuscript text, reviewer-concern diagnosis, chinese-to-english academic response writing, or consistency checks between reviewer comments, author evidence, promised revisions, and the manuscript. preserve scientific meaning, distinguish completed work from planned work, and never invent experiments, numerical results, citations, equations, figures, tables, page numbers, line numbers, or manuscript changes.
---

# Peer Review Response Writer

## Overview

Transform reviewer comments, author notes, manuscript excerpts, and verified evidence into rigorous point-by-point responses. Prioritize scientific correctness, traceability, and direct resolution of the reviewer's concern over rhetorical fluency.

## Core Principles

1. Answer the central concern before adding background.
2. Ground every technical claim in material supplied by the user or in a source explicitly verified during the task.
3. Distinguish clearly among completed revisions, planned revisions, and missing evidence.
4. Separate the response to the reviewer from the manuscript changes and revised manuscript text.
5. Preserve the author's technical meaning when translating or polishing.
6. Use a respectful, confident, and non-defensive academic tone.
7. Never invent experiments, results, citations, equations, implementation details, or manuscript locations.

## Workflow

Follow these steps for each reviewer comment.

### Step 1: Normalize the input

Extract, when available:

- reviewer number and comment number;
- complete reviewer comment;
- author's intended response or position;
- relevant manuscript text;
- equations, figures, tables, experiments, or citations supplied as evidence;
- revision status: completed, planned, or undecided;
- target venue, language, tone, and length;
- known section, page, and line locations.

Do not block the task merely because some fields are missing. Ask focused clarification questions only when the missing information would materially change the scientific answer. Otherwise, continue with explicit placeholders and action items.

### Step 2: Diagnose the real concern

State internally or explicitly, depending on the requested mode:

- the reviewer's central concern;
- the claim being challenged;
- the evidence or revision the reviewer appears to expect;
- the risk if the concern is not resolved;
- the comment category.

Consult `references/comment-taxonomy.md` for common categories and minimum sufficient evidence.

### Step 3: Build an evidence ledger

Classify each supporting item as:

- **confirmed**: supplied by the user and already available;
- **completed**: the author states that the experiment or revision has been completed;
- **planned**: intended but not yet completed;
- **missing**: necessary information or evidence has not been supplied;
- **not applicable**: explain why the requested item does not apply.

Never convert a planned or missing item into a completed claim. Use future tense for planned work and past or present-perfect tense only for completed work.

### Step 4: Choose the response stance

Select the most defensible stance:

- **agree**: accept the concern and revise accordingly;
- **partially agree**: accept the valid portion while clarifying scope or assumptions;
- **respectfully disagree**: explain why the requested interpretation or experiment is unsuitable, then revise the manuscript to prevent the misunderstanding;
- **already addressed but unclear**: identify the existing content and improve its presentation;
- **additional evidence required**: recommend the minimum experiment, analysis, derivation, or visualization needed before a final response can be claimed.

Do not make disagreement sound combative. Address the technical premise rather than the reviewer personally.

### Step 5: Draft the direct response

Use this logic:

> acknowledge briefly → answer directly → explain technically → support with evidence → state the revision → identify the location

Keep the first substantive paragraph focused on the answer. Avoid opening with a long literature review or generic gratitude.

### Step 6: Draft manuscript changes

Separate three different deliverables:

1. **Response**: the explanation sent to the reviewer.
2. **Changes in the manuscript**: a factual summary of what was changed.
3. **Revised text**: exact publication-ready wording for insertion into the manuscript.

Do not claim that text has been added unless the user confirms the change is completed. For planned changes, label them clearly as proposed or to be inserted.

### Step 7: Audit the result

Check:

- directness;
- evidence support;
- tense consistency;
- agreement between the response and revised text;
- professional tone;
- preserved numbering;
- unresolved placeholders;
- overclaiming;
- invented locations or references;
- contradictions across multiple reviewer responses.

Consult `references/quality-checklist.md` for the full audit.

## Output Modes

Infer the mode from the request or follow the user's explicit choice.

### Diagnose

Return:

1. core concern;
2. reviewer expectation;
3. assessment of the author's current plan;
4. recommended stance;
5. missing evidence or action items.

### Draft

Return a complete response for one or more comments using the standard response format below.

### Polish

Improve an existing response without changing its scientific meaning. Identify unsupported claims before rewriting them.

### Translate

Translate Chinese or other-language reasoning notes into publication-ready academic English. Preserve equations, notation, terminology, qualifiers, and uncertainty. Do not strengthen the claim during translation.

### Revise Text

Draft only the manuscript paragraph, caption, limitation statement, contribution statement, or technical clarification associated with the comment.

### Audit

Evaluate an existing response letter for logic, evidence, tone, consistency, and unresolved placeholders. Return specific corrections rather than only general comments.

### Full Letter

Process all reviewers while preserving reviewer and comment numbering. Add a cross-comment consistency audit and a consolidated action-item list.

## Standard Response Format

Use this as the default flexible template:

```markdown
### Comment [number]

> [Original reviewer comment]

**Core concern:**  
[Concise diagnosis; omit when the user requests a submission-ready response only.]

**Response:**  
[Brief acknowledgment.] [Direct answer to the concern.]

[Technical explanation and evidence.]

**Changes in the manuscript:**  
[Describe only completed changes. If planned, label them as proposed changes.]

**Revised text:**  
> [Exact text added or proposed for the manuscript.]

**Location:**  
Section [TO BE CONFIRMED], Page [XX], Lines [YY-ZZ].

**Remaining action items:**  
- [Only include unresolved evidence, experiments, figures, citations, or locations.]
```

Adapt the headings when the user requests a shorter answer, but preserve the distinction between response, changes, and revised text.

## Handling Missing Information

Use explicit markers rather than fabricating details:

- `[RESULT REQUIRED]`
- `[REFERENCE TO BE VERIFIED]`
- `[SECTION TO BE CONFIRMED]`
- `[PAGE/LINE NUMBERS TO BE ADDED]`
- `[EXPERIMENT PLANNED, NOT YET COMPLETED]`
- `[AUTHOR CONFIRMATION REQUIRED]`

When a claim depends on missing evidence, explain what evidence is needed and provide a conditional draft rather than presenting the claim as established.

## Style Rules

- Match the user's target venue when specified.
- Default to concise formal academic English for the response letter.
- When the user writes in Chinese, default to Chinese diagnosis plus English submission-ready response unless the user requests otherwise.
- Vary acknowledgment phrases and avoid repeating “Thank you for this valuable comment.”
- Prefer precise verbs such as “clarify,” “add,” “compare,” “derive,” “quantify,” and “revise.”
- Avoid exaggerated terms such as “obviously,” “undeniably,” “perfectly,” and “completely proves.”
- Avoid blaming the reviewer for misunderstanding. State that the original presentation may have been insufficiently clear.
- Preserve mathematical notation, variable names, method names, and acronyms exactly unless correcting a confirmed error.

Consult `references/academic-style-guide.md` for phrasing patterns and tense guidance.

## Multiple Comments and Full Response Letters

- Preserve the original reviewer and comment numbering.
- Treat compound comments as separate sub-issues when they require different evidence.
- Do not merge comments merely because they share keywords.
- Track repeated manuscript changes so that section names, terminology, and claims remain consistent.
- Flag conflicting promises made to different reviewers.
- End with a consolidated list of remaining actions and unresolved placeholders when requested.

## Resource Guide

- Read `references/response-workflow.md` for detailed response architecture, evidence tracking, and stance selection.
- Read `references/comment-taxonomy.md` for comment categories and recommended evidence.
- Read `references/academic-style-guide.md` for tone, phrasing, translation, and tense control.
- Read `references/quality-checklist.md` before auditing or finalizing a full response letter.
- Read `references/examples.md` when an example is useful for matching the expected structure and level of detail.
- Use `assets/response-letter-template.md` when the user requests a reusable response-letter template.
