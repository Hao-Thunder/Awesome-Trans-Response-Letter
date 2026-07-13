# Examples

## Example 1: Interpretability Concern

### Input

**Reviewer comment**

> The network appears to be a black-box residual optimizer. It is unclear whether it recovers the intended physical structure or merely overfits residual errors.

**Author plan**

- explain the model-driven gradient update;
- map network modules to physical variables;
- use an intermediate gradient representation to estimate the structure;
- add heatmaps comparing estimated and ground-truth structure.

**Evidence status**

- mathematical update: confirmed;
- heatmap experiment: planned, not yet completed.

### Appropriate Output Pattern

**Core concern:**  
The reviewer requests both a mathematical explanation of the model-driven structure and direct evidence that the learned correction recovers the intended physical pattern rather than fitting generic residuals.

**Response:**  
We appreciate this important comment. The proposed network is not designed as an unconstrained residual optimizer. Its update follows the model-derived gradient step, while the learned modules refine the initial sparse channel estimate within that update structure. We will revise the manuscript to make the correspondence between each network operation and the underlying variables explicit.

To evaluate whether the network recovers the intended structure, we will additionally visualize the structure estimated from the intermediate gradient representation and compare it with the ground truth. Because this visualization has not yet been completed, the quantitative and qualitative conclusions should remain marked as pending until the experiment is available.

**Proposed changes in the manuscript:**  
Add an equation-to-module explanation after Eqs. [X]-[Y] and add a heatmap comparison in the simulation section.

**Remaining action items:**

- `[EXPERIMENT PLANNED, NOT YET COMPLETED]` Generate the estimated and ground-truth heatmaps.
- `[RESULT REQUIRED]` Add a quantitative structure-recovery metric if available.
- `[PAGE/LINE NUMBERS TO BE ADDED]` Confirm the final revision locations.

### Why This Works

- It directly answers the black-box concern.
- It separates confirmed architectural reasoning from planned validation.
- It does not claim that the heatmap already proves the point.

## Example 2: Respectful Disagreement About a Baseline

**Reviewer comment**

> Please compare against Method A.

**Relevant fact**

Method A assumes full observations, while the paper studies sparse observations.

**Response pattern**

> We appreciate the reviewer’s suggestion. A direct comparison with Method A would not be technically matched because Method A assumes access to full observations, whereas our method operates from sparse measurements. The resulting performance difference would therefore reflect both the algorithm and the observation regime. To address the underlying concern regarding comparative performance, we have added [or propose adding] baselines that use the same sparse observation model and have clarified the distinction in Section [X].

## Example 3: Chinese Notes to English

**Chinese note**

> 当前结果只能说明在测试的SNR范围内比较稳定，不能说明对所有噪声都具有鲁棒性，所以需要收缩结论。

**English response sentence**

> The current results demonstrate stable performance only within the evaluated SNR range and do not establish robustness to arbitrary noise conditions. We have therefore narrowed the corresponding claim in the abstract and conclusion.
