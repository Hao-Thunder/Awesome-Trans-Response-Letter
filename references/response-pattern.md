# Response Pattern

Use this structure as the default. Adapt headings only when the user's existing response-letter format requires it.

```latex
\noindent\textbf{Reviewer Comment:}
\begin{quote}
[Insert the original English comment verbatim. If the comment is in Chinese, provide a faithful English translation and label the heading as `Reviewer Comment (translated from Chinese)`.]
\end{quote}

\noindent\textbf{Response:}

We sincerely thank the reviewer for this constructive comment. [Acknowledge the precise limitation, ambiguity, or omission in the original manuscript.] [Provide the direct technical explanation that addresses the underlying concern.] [Describe the concrete changes made to the manuscript, including the relevant analysis, equation, figure, table, experiment, discussion, or wording.] [Explain why these changes resolve the concern and improve the manuscript.]

To further clarify [the specific issue], in the revised paper, we have [revised/added/expanded/clarified/corrected] [the relevant manuscript element] on page(s) XX--XX as follows:

\begin{quote}
\textcolor{blue}{[First revised manuscript paragraph or sentence.]}

\textcolor{blue}{[Second revised manuscript paragraph or sentence, if needed.]}

\begin{equation}
\textcolor{blue}{
[Revised mathematical expression]
}
\label{eq:placeholder}
\end{equation}

\textcolor{blue}{[Explanation of the equation, figure, table, experiment, or implication.]}
\end{quote}
```

## Style Rules

- Preserve an English reviewer comment verbatim except for obvious typographical normalization that does not change meaning.
- Translate a Chinese reviewer comment faithfully; do not intensify or soften the criticism.
- Prefer `We sincerely thank the reviewer for this constructive comment.` or a close restrained variant.
- Acknowledge a real issue with language such as `We agree that the original presentation did not make ... sufficiently clear.` Use `agree` only when the authors genuinely accept the point.
- When partially disagreeing, first validate the concern, then explain the technical distinction with evidence. Avoid `the reviewer misunderstood`.
- Name revisions precisely: `added a complexity comparison in Table X`, `revised the definition following Eq. (X)`, `included an ablation study in Section X`, or `clarified the assumption on page XX`.
- Explain causality: state how the added material removes ambiguity or supplies the missing evidence.
- Avoid unsupported superlatives, absolute guarantees, and claims such as `completely solves` unless mathematically justified.
- Keep the response self-contained enough that the reviewer can understand the resolution without searching the manuscript.

## LaTeX Rules

- Keep reviewer and response headings outside blue coloring.
- Use `\textcolor{blue}{...}` for revised manuscript prose.
- Do not wrap a blank line or multiple paragraphs in one `\textcolor` command.
- For multi-line mathematics, use a valid inner environment, for example:

```latex
\begin{equation}
\textcolor{blue}{
\begin{aligned}
A &= B + C, \\
D &= E - F.
\end{aligned}
}
\label{eq:example}
\end{equation}
```

- Preserve the user's labels and references when supplied. Use placeholders rather than fabricated identifiers.
- If a complete figure or table revision is required but the full float is not supplied, provide the revised caption or surrounding discussion and flag the missing float details in author-side checks.

## Evidence Alignment Checklist

For each sentence in the response that begins with or implies `we have`, confirm that the corresponding manuscript change appears in the blue text or is explicitly identified as a figure, table, equation, experiment, or section-level change. Remove or qualify any unsupported completion claim.

For planned but not yet completed work, choose one of these approaches:

1. Convert the user's plan into manuscript-ready blue text and phrase it as a revision ready to be incorporated.
2. Retain a visible placeholder and add an author-side check.
3. State that the revision still requires the specified experiment, figure, table, or numerical result; never invent it.
