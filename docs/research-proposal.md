# Research Proposal: Statistical Analysis and Comparison of Unsupervised Anomaly Detection Models

## 1. Research Objective

The objective of this project is to analyze potential anomalies in the UCI Online Retail dataset and compare statistical and machine learning-based anomaly detection methods.

The study focuses on comparing detection rates, agreement between methods, sensitivity to parameter choices, stability, computational cost, and interpretability.

## 2. Dataset

- **Name:** Online Retail
- **Source:** UCI Machine Learning Repository
- **Records:** 541,909
- **Features:** 8 columns

The dataset contains retail transaction information, including invoice numbers, product codes, quantities, unit prices, invoice dates, customer identifiers, and countries.

## 3. Proposed Methods

The following methods are proposed for comparison:

1. Z-Score
2. Interquartile Range (IQR)
3. Modified Z-Score using Median Absolute Deviation (MAD)
4. Isolation Forest
5. Local Outlier Factor (LOF)

The methods represent statistical, robust statistical, and machine learning-based approaches.

## 4. Evaluation Criteria

The comparison will consider:

- Anomaly detection rate
- Agreement and overlap between methods
- Sensitivity to thresholds and parameters
- Stability of detection results
- Computational cost and execution time
- Interpretability of detected cases

Because the dataset does not provide verified anomaly labels, detection counts and agreement alone will not be treated as proof of accuracy or superiority.

## 5. Research Limitations

The dataset contains skewed numerical distributions, negative quantities, zero prices, missing customer identifiers, and potentially legitimate extreme transactions.

Therefore, extreme observations will not automatically be considered errors or anomalies. Their interpretation will depend on the transaction context and the detection method.

## 6. Project Stages

### Stage 1: Exploratory Analysis and Research Design

- Inspect the dataset structure and data quality.
- Analyze numerical distributions and potential extreme values.
- Assess the dataset's suitability for the research objective.
- Define the proposed methods and evaluation criteria.
- Obtain client approval of the research scope and experimental plan.

### Stage 2: Implementation and Experimental Evaluation

This stage will begin only after client approval.

- Finalize feature selection and data preparation.
- Implement the approved detection methods.
- Conduct experiments and sensitivity analyses.
- Compare and interpret the results.
- Prepare the final report.

## 7. Pending Client Approval

Before Stage 2 begins, the client should confirm:

- The dataset and research scope
- The features to be analyzed
- The proposed detection methods
- The evaluation criteria and experimental plan