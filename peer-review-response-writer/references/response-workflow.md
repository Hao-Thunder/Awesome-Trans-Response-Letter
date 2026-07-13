# Response Workflow

## Contents

1. Input map
2. Concern diagnosis
3. Evidence ledger
4. Stance selection
5. Response architecture
6. Revision mapping
7. Multi-comment consistency

## 1. Input Map

For each comment, map the available information into five groups:

| Group | Typical contents |
|---|---|
| Reviewer request | Full comment, explicit questions, requested experiments or clarifications |
| Author position | Agree, partly agree, disagree, or undecided |
| Scientific evidence | Equations, derivations, experiments, tables, figures, citations, implementation details |
| Manuscript state | Original text, completed edits, proposed edits, known locations |
| Output constraints | Venue, language, tone, length, response format |

When the user provides only a reviewer comment and a rough plan, continue by distinguishing what can be drafted now from what still requires evidence.

## 2. Concern Diagnosis

Convert the surface wording into a precise concern statement:

> The reviewer doubts **[claim]** because **[missing explanation/evidence]** and requests **[specific remedy]**.

Then identify the claim-to-evidence link. Examples:

- “The method is a black box” → architecture-to-model mapping plus qualitative or quantitative interpretability evidence.
- “The comparison is unfair” → matched data, training budget, tuning policy, complexity, and evaluation protocol.
- “The novelty is unclear” → closest prior work, exact difference, and consequence of that difference.
- “The experiments are insufficient” → identify which manuscript claim lacks direct evidence.

## 3. Evidence Ledger

Create a compact ledger before drafting:

| Item | Status | Can be claimed? | Required wording |
|---|---|---:|---|
| Existing derivation | confirmed | Yes | Present tense |
| New ablation completed | completed | Yes | Past/present-perfect tense |
| Heatmap planned | planned | No, not as completed | Future or proposed tense |
| Page number unknown | missing | No | Placeholder |
| Requested test irrelevant | not applicable | Only with justification | Explain scope and add clarification |

Do not infer numerical values from qualitative descriptions. Do not create citations from memory when exact bibliographic information is not supplied or verified.

## 4. Stance Selection

### Agree

Use when the concern reveals a real omission or weakness. State the correction without excessive self-criticism.

### Partially agree

Separate the valid concern from the part that exceeds the paper's scope. Accept the valid part, clarify scope, and add the minimum revision needed.

### Respectfully disagree

Use only when the scientific premise is unsupported, the requested experiment is outside scope, or the manuscript already answers the point under a different assumption. Provide evidence and improve the manuscript so the same misunderstanding is less likely.

### Additional evidence required

Do not write a fully affirmative final response when the evidence does not yet exist. Provide:

1. a provisional response;
2. the minimum required experiment or analysis;
3. a results placeholder;
4. the manuscript text that can be drafted independently of the result.

## 5. Response Architecture

A strong response normally contains:

1. one brief acknowledgment;
2. one direct answer;
3. technical reasoning;
4. evidence or result;
5. manuscript revision;
6. exact location or placeholder.

The direct answer should appear early. A response should not require the reviewer to infer whether the authors agree or what changed.

## 6. Revision Mapping

Maintain a one-to-one or clearly explained mapping:

| Reviewer concern | Response evidence | Manuscript revision |
|---|---|---|
| Missing physical interpretation | Equation-to-module mapping | Added explanatory paragraph and architecture description |
| Missing validation | New heatmap or metric | Added figure, caption, and discussion |
| Overstated generalization | Scope limitation | Revised abstract, conclusion, and limitation statement |

Check that the revised manuscript text does not make a stronger claim than the response.

## 7. Multi-Comment Consistency

Across a full response letter, verify:

- the same method component is described consistently;
- experiment settings do not conflict;
- section and figure numbering are consistent;
- one response does not promise a revision contradicted by another;
- novelty and limitation statements use the same scope;
- repeated reviewer concerns receive compatible answers rather than copied text with inconsistent details.
