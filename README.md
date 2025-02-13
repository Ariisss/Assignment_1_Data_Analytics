# Balanced Risk Set Matching Implementation

## Contributors

- Pantino, Prince Isaac
- Singh, Fitzsixto Angelo

## Objective

This project aims to apply **Balanced Risk Set Matching (BRSM)** as a statistical technique to improve causal inference in observational studies where treatment assignment is based on evolving patient conditions rather than randomization. The study focuses on:

- Matching treated and untreated patients with similar symptom histories.
- Optimizing matches using integer programming.
- Conducting sensitivity analyses to assess hidden biases.

## Workflow

### Step 1: Data Collection & Preprocessing

- Load or simulate the dataset, ensuring it contains treatment times, symptom histories, and follow-up measures.
- Standardize symptom measures for comparability.
- Identify treated vs. untreated patients and structure data for time-sequenced analysis.

**Output:** Cleaned dataset with time-ordered symptom histories and treatment indicators.

---

### Step 2: Risk Set Matching

- Identify **risk sets** by finding untreated patients who have a **similar symptom history** as a treated patient up to the time of treatment.
- Ensure that **future data is not used** for matching.
- Compute **Mahalanobis distance** to measure similarity between treated and untreated patients.

**Output:** Initial pool of potential matches.

---

### Step 3: Optimal Matching via Integer Programming

- Implement **integer programming** to:
  - Minimize **Mahalanobis distance** between treated and control pairs.
  - Ensure **balanced covariate distributions** across groups.
- Use **network flow optimization** to efficiently find the best matches.

**Output:** Finalized matched dataset with treatment-control pairs.

---

### Step 4: Sensitivity Analysis for Hidden Bias

- Introduce an **unobserved covariate** to simulate hidden biases.
- Evaluate how much hidden bias would be needed to **invalidate the results**.
- Conduct **proportional hazards modeling** to analyze potential confounders.

**Output:** Bias-adjusted estimates of treatment effects.

---

### Step 5: Statistical Analysis & Interpretation

- Perform **hypothesis testing** to compare treatment vs. control groups:
  - **Wilcoxon Signed-Rank Test** for pairwise comparisons.
  - **Permutation tests** to validate significance.
  - **Multivariate analysis** if multiple symptom outcomes are evaluated.
- Generate **visualizations** (boxplots, histograms) to inspect trends in symptom changes.

**Output:** Statistical validation of treatment effects.

---

### Step 6: Reporting & Conclusion

- Summarize **methodology, findings, and potential biases**.
- Present results through:
  - **Summary tables** (descriptive statistics).
  - **Graphs & charts** (symptom trends over time).
  - **Sensitivity analysis conclusions** (robustness of findings).

**Output:** Final research paper/report with validated conclusions.
