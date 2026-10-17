
# Unsupervised Anomaly Detection Study

A research study comparing classical statistical, robust statistical, and unsupervised machine learning methods for anomaly detection in skewed retail transaction data.

The project investigates detection rates, agreement between methods, sensitivity to thresholds and parameters, stability, computational cost, and interpretability.

## Table of Contents

- [Overview](#overview)
- [Research Objectives](#research-objectives)
- [Dataset](#dataset)
- [Proposed Methods](#proposed-methods)
- [Evaluation Protocol](#evaluation-protocol)
- [Research Limitations](#research-limitations)
- [Project Workflow](#project-workflow)
- [Repository Structure](#repository-structure)
- [Technologies](#technologies)
- [Project Status](#project-status)
- [References](#references)

## Overview

Anomaly detection identifies observations that differ from expected patterns in a dataset. In retail transactions, unusual observations may represent exceptional purchases, cancellations, returns, accounting adjustments, or data quality issues.

This project proposes a comparison of statistical rules, a robust statistical detection method, and unsupervised machine learning algorithms.

An observation flagged by a detection method is not necessarily an error or a genuine anomaly. Results must be interpreted in the context of the dataset and the assumptions of each method.

## Research Objectives

- Assess the structure, quality, and numerical distributions of the dataset.
- Investigate extreme values and potentially unusual transactions.
- Compare classical and robust statistical methods with unsupervised machine learning algorithms.
- Measure detection rates and agreement between methods.
- Analyze sensitivity to thresholds and model parameters.
- Evaluate stability across suitable data samples.
- Compare computational cost and interpretability.
- Document the limitations of evaluation without verified anomaly labels.

## Dataset

The primary candidate is the **Online Retail** dataset from the UCI Machine Learning Repository.

| Property | Description |
|---|---|
| Dataset | Online Retail |
| Source | UCI Machine Learning Repository |
| Records | 541,909 |
| Columns | 8 |
| Domain | Retail transactions |
| Format | Excel (`.xlsx`) |

### Features

| Feature | Description |
|---|---|
| `InvoiceNo` | Invoice identifier |
| `StockCode` | Product code |
| `Description` | Product description |
| `Quantity` | Quantity of items |
| `InvoiceDate` | Transaction date and time |
| `UnitPrice` | Price per item |
| `CustomerID` | Customer identifier |
| `Country` | Customer's country |

Numeric-looking identifiers will not automatically be treated as continuous numerical measurements.

Dataset source: [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)

If the primary dataset is found unsuitable for the research question, MetroPT-3 may be considered as an alternative after assessing scientific relevance and processing complexity. Any change will be discussed with the client.

## Exploratory Data Analysis

The preliminary analysis covers:

- Dataset structure and data types
- Missing values and data quality
- Numerical summary statistics and distribution shapes
- Extreme values in `Quantity` and `UnitPrice`
- Negative quantities and potential cancellation-related records
- Zero and negative unit prices
- Preliminary dataset suitability

The dataset contains unusual observations that may have legitimate business explanations and should not automatically be classified as errors.

## Proposed Methods

| Method | Category | Main principle |
|---|---|---|
| Z-Score | Classical statistical | Uses distance from the mean in standard deviation units |
| Interquartile Range (IQR) | Classical statistical | Uses quartile-based bounds |
| Modified Z-Score using MAD | Robust statistical | Uses the median and median absolute deviation |
| Isolation Forest | Unsupervised machine learning | Uses random partitioning to isolate observations |
| Local Outlier Factor (LOF) | Unsupervised machine learning | Compares local density with neighboring observations |

MAD is a robust dispersion measure used by Modified Z-Score rather than an independent detection algorithm by itself.

An additional robust or adaptive-threshold method may be considered if scientifically justified and approved.

## Evaluation Protocol

The proposed comparison will consider:

- Detection counts and proportions
- Agreement and disagreement between methods
- Sensitivity to thresholds and parameters
- Stability across suitable repeated samples or data partitions
- Execution time and computational cost
- Interpretability
- Feasibility of controlled synthetic anomaly injection

The original dataset does not provide verified anomaly labels. Detection counts and agreement alone cannot establish true accuracy or superiority. Synthetic anomaly experiments, if included, will be interpreted with their limitations.

## Research Limitations

- Skewed numerical distributions may affect statistical detection rules.
- Negative quantities may be associated with returns or cancellations.
- Zero and negative prices may reflect special transactions or accounting adjustments.
- Extreme observations may be legitimate.
- Missing customer identifiers may limit customer-level analysis.
- The absence of verified anomaly labels limits direct accuracy evaluation.
- Univariate statistical methods and multivariate algorithms may operate on different feature spaces.

These limitations will be considered when designing and interpreting the experiments.

## Project Workflow

### Stage 1 — Dataset Assessment and Research Design

- Inspect the dataset structure and quality.
- Analyze numerical distributions and extreme values.
- Assess dataset suitability.
- Define the research question and proposed methods.
- Establish evaluation criteria and the experimental plan.
- Submit the methodology for client approval.

### Stage 2 — Implementation and Experimental Evaluation

This stage will begin **only after client approval**.

- Finalize feature selection and data preparation.
- Implement the approved methods.
- Conduct experiments and sensitivity analyses.
- Evaluate agreement, stability, and runtime.
- Assess synthetic anomaly injection if included in the approved plan.
- Interpret results and prepare the final technical report.

## Repository Structure

```text
unsupervised-anomaly-detection-study/
├── data/
│   └── raw/
│       └── Online Retail.xlsx
├── docs/
│   └── research-proposal.md
├── notebooks/
│   └── anomaly_detection_study.ipynb
├── README.md
└── .gitignore
```

## Technologies

| Technology | Purpose |
|---|---|
| Python | Data analysis and implementation |
| Jupyter Notebook | Exploratory analysis and documentation |
| Pandas | Data manipulation |
| NumPy | Numerical computation |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning methods |
| Git | Version control |
| GitHub | Private project collaboration |

## Project Status

**Current phase: Stage 1 — Research Design and Client Review**

The preliminary exploratory analysis and research methodology have been documented. The final methodology and experimental scope require client approval before Stage 2 begins.

No comparative model performance results are claimed at this stage.

## References

1. Chen, D. (2015). *Online Retail*. UCI Machine Learning Repository.  
   https://doi.org/10.24432/C5BW33

2. Liu, F. T., Ting, K. M., & Zhou, Z.-H. (2008). *Isolation Forest*. IEEE International Conference on Data Mining.

3. Breunig, M. M., Kriegel, H.-P., Ng, R. T., & Sander, J. (2000). *LOF: Identifying Density-Based Local Outliers*. ACM SIGMOD.

---

*This repository is maintained for research and educational purposes. The methodology and experimental scope remain subject to client approval.*
