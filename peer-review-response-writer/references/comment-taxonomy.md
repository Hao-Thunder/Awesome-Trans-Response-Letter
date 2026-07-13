# Reviewer Comment Taxonomy

## Contents

1. Novelty and contribution
2. Interpretability and model grounding
3. Theory and derivation
4. Experiments and ablations
5. Baselines and fairness
6. Complexity and practicality
7. Robustness and generalization
8. Reproducibility
9. Presentation and notation
10. Scope, limitations, and overclaiming

## 1. Novelty and Contribution

**Typical concern:** The contribution appears incremental or insufficiently distinguished from prior work.

**Minimum useful response:**

- identify the closest alternatives;
- state the exact technical difference;
- explain why the difference matters;
- revise the contribution statement to avoid broad or vague claims.

**Common failure:** Listing many features without explaining which one is novel and consequential.

## 2. Interpretability and Model Grounding

**Typical concern:** The model appears black-box or disconnected from the stated physical, probabilistic, or optimization model.

**Minimum useful response:**

- map each important network operation to a model variable, constraint, or update step;
- distinguish learned components from fixed model-driven components;
- explain what structure should be recovered;
- add qualitative or quantitative evidence such as heatmaps, support recovery, correlation, sensitivity, or intermediate-state visualization.

**Common failure:** Calling a method “model-driven” without showing the mathematical correspondence.

## 3. Theory and Derivation

**Typical concern:** Assumptions, intermediate steps, convergence, identifiability, dimensions, or boundary conditions are unclear.

**Minimum useful response:**

- state assumptions explicitly;
- supply missing derivation steps;
- define dimensions and notation;
- clarify whether a statement is a theorem, approximation, heuristic, or empirical observation;
- narrow claims that exceed the proof scope.

## 4. Experiments and Ablations

**Typical concern:** The evaluation does not isolate a component or support a major claim.

**Minimum useful response:**

- identify the exact claim being tested;
- add the smallest experiment that directly tests that claim;
- control other factors;
- report settings, metric, and interpretation;
- avoid presenting a broad benchmark when a targeted ablation is needed.

## 5. Baselines and Fairness

**Typical concern:** The comparison may use unequal data, tuning, parameter budgets, training epochs, or evaluation protocols.

**Minimum useful response:**

- align datasets and splits;
- disclose tuning and training budgets;
- report parameters, FLOPs, latency, or memory when relevant;
- explain unavoidable implementation differences;
- add or remove baselines based on scientific relevance rather than popularity alone.

## 6. Complexity and Practicality

**Typical concern:** Computational cost, latency, memory, hardware, or deployment feasibility is unclear.

**Minimum useful response:**

- define the complexity metric;
- report input size, batch size, precision, hardware, and software conditions;
- separate theoretical complexity from measured runtime;
- compare accuracy-cost trade-offs rather than only one metric.

## 7. Robustness and Generalization

**Typical concern:** Performance may depend on a narrow distribution, SNR, dataset, seed, geometry, or scenario.

**Minimum useful response:**

- identify the relevant distribution shift;
- test multiple seeds or scenarios when appropriate;
- report confidence intervals or variability where available;
- state the tested scope and avoid universal claims.

## 8. Reproducibility

**Typical concern:** Hyperparameters, preprocessing, implementation, data splits, or code availability are incomplete.

**Minimum useful response:**

- provide exact settings and versions;
- specify preprocessing and randomization;
- describe data splits and evaluation procedure;
- state code or data availability accurately.

## 9. Presentation and Notation

**Typical concern:** The paper is difficult to follow, symbols are undefined, or figures and captions are unclear.

**Minimum useful response:**

- define symbols at first use;
- add a notation table if needed;
- revise captions to be self-contained;
- improve section transitions and cross-references;
- avoid claiming that a presentation-only revision resolves a scientific concern.

## 10. Scope, Limitations, and Overclaiming

**Typical concern:** The abstract, conclusion, or contribution statement exceeds the evidence.

**Minimum useful response:**

- narrow the claim;
- state operating assumptions;
- add limitations and failure cases;
- align the abstract, introduction, results, and conclusion.
