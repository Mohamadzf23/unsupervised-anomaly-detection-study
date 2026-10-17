
# Research Proposal: Statistical Analysis and Comparison of Unsupervised Anomaly Detection Methods

## 1. Research Objective

The objective of this project is to compare classical statistical, robust statistical, and unsupervised machine learning methods for anomaly detection in skewed retail transaction data.

The study will examine differences in detection rates, agreement between methods, sensitivity to thresholds and parameters, stability, computational cost, and interpretability.

## 2. Research Question

How do classical and robust statistical methods differ in their detection rates, sensitivity to threshold changes, stability, and interpretability when detecting anomalies in skewed data, and how do their results compare with unsupervised machine learning algorithms?

## 3. Dataset

The UCI Online Retail dataset is the primary candidate for this study.

| Property | Description |
|---|---|
| Dataset | Online Retail |
| Source | UCI Machine Learning Repository |
| Records | 541,909 |
| Columns | 8 |
| Domain | Retail transactions |
| Format | Excel (`.xlsx`) |

Dataset source: https://archive.ics.uci.edu/dataset/352/online+retail

The preliminary analysis identified skewed numerical distributions, negative quantities, zero and negative unit prices, extreme observations, and missing customer identifiers.

The dataset does not contain verified anomaly labels. If it is found unsuitable for the research question, MetroPT-3 may be considered as an alternative after evaluating scientific relevance and processing complexity. Any dataset change will be discussed with the client before proceeding.

## 4. Proposed Detection Methods

The initial comparison will include five methods.

| Method | Category | Principle |
|---|---|---|
| Z-Score | Classical statistical | Measures distance from the mean in standard deviation units |
| IQR | Classical statistical | Uses quartile-based bounds to flag extreme observations |
| Modified Z-Score using MAD | Robust statistical | Uses the median and median absolute deviation |
| Isolation Forest | Unsupervised machine learning | Identifies observations that are relatively easy to isolate |
| Local Outlier Factor (LOF) | Unsupervised machine learning | Compares local density with the density of neighboring observations |

MAD is a robust dispersion measure used by Modified Z-Score, not an independent detection algorithm by itself.

An additional robust method or adaptive thresholding approach may be considered if justified by the research question and approved scope. Additional methods will not be introduced solely to increase the number of algorithms.

## 5. Feature and Comparison Design

The initial exploratory analysis has focused on `Quantity` and `UnitPrice`.

The final feature set and analysis population will be established after approval. Numeric-looking identifiers such as `CustomerID`, `InvoiceNo`, and `StockCode` will not automatically be treated as continuous numerical features.

The experimental design will distinguish univariate statistical analysis from multivariate machine learning analysis where applicable. Differences in feature space and method assumptions will be documented to support a fair interpretation of results.

## 6. Evaluation Protocol

The proposed evaluation will consider:

- Number and proportion of observations flagged by each method
- Agreement and disagreement between methods
- Sensitivity to thresholds and algorithm parameters
- Stability across suitable repeated samples or data partitions
- Computational cost and execution time
- Interpretability of detected observations
- Feasibility of controlled synthetic anomaly injection

If synthetic anomalies are introduced, the injection procedure and its assumptions will be documented. Synthetic evaluation will supplement, rather than replace, the limitations of working without verified real-world anomaly labels.

Detection counts and agreement alone will not be treated as evidence of true accuracy or superiority.

## 7. Research Limitations

The study must account for:

- Strongly skewed numerical distributions
- Negative quantities and potential cancellation or return records
- Zero and negative prices and special accounting transactions
- Missing customer identifiers
- The absence of verified anomaly labels
- Differences between univariate statistical methods and multivariate algorithms
- The limited realism of artificially injected anomalies
- The effect of parameter settings and computational conditions

Extreme observations will not automatically be considered errors or genuine anomalies without appropriate context.

## 8. Project Stages

### Stage 1: Dataset Assessment and Research Design

- Inspect the dataset structure, quality, and numerical distributions.
- Investigate extreme values and potential anomalies.
- Assess dataset suitability for the research question.
- Define the research question and proposed detection methods.
- Establish the evaluation criteria and experimental plan.
- Submit the methodology and project scope for client approval.

### Stage 2: Implementation and Experimental Evaluation

Stage 2 will begin only after client approval.

- Finalize feature selection and data preparation.
- Implement the approved detection methods.
- Conduct experiments and parameter sensitivity analyses.
- Evaluate stability, method agreement, and runtime.
- Assess synthetic anomaly injection if included in the approved protocol.
- Analyze and interpret results.
- Prepare comparative tables, visualizations, and the final technical report.

## 9. Pending Client Approval

The client should confirm:

1. The research question and project scope.
2. The primary dataset and whether an alternative dataset needs further investigation.
3. The proposed methods and whether an additional robust or adaptive method is justified.
4. The feature scope and comparison design.
5. The evaluation protocol, including stability and synthetic anomaly evaluation.
6. The expected final deliverables.

## 10. Scope Control

The proposed methodology is subject to client review and approval. Changes that materially expand the dataset, methods, experiments, or deliverables will be discussed before implementation.

No model implementation or comparative performance results are claimed in this proposal.
