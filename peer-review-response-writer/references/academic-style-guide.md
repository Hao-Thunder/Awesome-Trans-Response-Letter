# Academic Response Style Guide

## Contents

1. Tone
2. Direct-answer patterns
3. Agreement patterns
4. Respectful disagreement
5. Completed versus planned work
6. Translation rules
7. Phrases to avoid

## 1. Tone

Use a professional, calm, and technically confident tone. Be appreciative without sounding submissive. Avoid implying that the reviewer failed to read the paper correctly.

Prefer:

- “We agree that the original manuscript did not explain this connection sufficiently.”
- “The reviewer raises an important distinction between the model-based update and the learned correction.”
- “We respectfully clarify that the requested comparison assumes a setting different from that considered in this work.”

Avoid:

- “The reviewer misunderstood our paper.”
- “This is obvious from Eq. (7).”
- “We have completely proved the superiority of the method.”

## 2. Direct-Answer Patterns

Place the answer before extended explanation:

- “Yes. The proposed module explicitly implements the gradient term in Eq. (X), while only the step-size mapping is learned.”
- “No. The reported result does not support robustness outside the tested SNR range; we have therefore narrowed the claim.”
- “The current evidence is insufficient to separate these two effects. We will add the following controlled experiment…”

## 3. Agreement Patterns

Use concise acknowledgment followed by action:

- “We agree that the original explanation was incomplete. We have added…”
- “This comment identifies a missing ablation. We have therefore evaluated…”
- “We appreciate this suggestion and have revised the manuscript to clarify…”

Do not over-apologize. One acknowledgment is usually enough.

## 4. Respectful Disagreement

Structure disagreement as:

1. acknowledge the concern;
2. state the assumption or scope;
3. provide evidence;
4. revise the manuscript to clarify the boundary.

Example:

> We appreciate the reviewer’s concern. However, the requested baseline assumes access to full-resolution observations, whereas our setting uses only sparse measurements. A direct numerical comparison would therefore conflate the algorithmic difference with a different information regime. We have clarified this distinction in Section [X] and added a comparison with methods operating under the same observation model.

## 5. Completed Versus Planned Work

Use completed tense only for completed actions:

- Completed: “We have added Fig. 6 and included the corresponding discussion.”
- Planned: “We will add a heatmap comparison in the revised manuscript.”
- Proposed draft: “The following paragraph is proposed for insertion after Eq. (12).”

Never use “we have added” when the user only states an intention.

## 6. Translation Rules

When translating author notes:

- preserve qualifiers such as “may,” “approximately,” “under the considered setting,” and “empirically”;
- preserve mathematical symbols and acronyms;
- do not convert a hypothesis into a conclusion;
- do not add claims of novelty, superiority, or generality;
- translate the intended scientific relationship, not the Chinese word order;
- keep response-letter prose more direct than manuscript prose.

## 7. Phrases to Avoid

Avoid or use sparingly:

- “obviously”;
- “clearly” when no evidence immediately follows;
- “undoubtedly”;
- “perfectly”;
- “completely solves”;
- “proves” for empirical evidence;
- repeated “Thank you for this valuable/insightful comment.”

Prefer evidence-bearing wording:

- “The results in Table X show…”
- “Under the assumptions in Section X…”
- “This observation supports, but does not establish…”
