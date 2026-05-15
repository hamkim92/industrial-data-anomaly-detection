# Industrial Data Anomaly Detection

This repository is a portfolio project for applying data science and machine learning to anomaly detection and quality monitoring problems in industrial, scientific, and operational data.

The goal is to build a practical workflow that starts from raw public datasets and ends with interpretable model outputs for decision-making.

## Project Motivation

Real-world industrial data often contains missing values, sensor noise, abnormal patterns, class imbalance, and domain-specific failure modes.

This project focuses on building a reproducible workflow for:

- Data understanding
- Data cleaning and validation
- Exploratory data analysis
- Baseline anomaly detection
- Model evaluation
- Error analysis
- Interpretation for quality monitoring and decision support

## Dataset

This project will first use the SECOM dataset from the UCI Machine Learning Repository.

SECOM is a public semiconductor manufacturing dataset for pass/fail classification and feature relevance analysis. It contains manufacturing process measurements, missing values, and highly imbalanced quality labels.

Dataset summary:

- Source: UCI Machine Learning Repository
- Domain: Semiconductor manufacturing
- Instances: 1,567
- Features: 591
- Label:
  - `-1`: Pass
  - `1`: Fail
- Missing values: Yes
- License: Creative Commons Attribution 4.0 International (CC BY 4.0)

No proprietary or confidential company data will be used.

## Planned Dataset

This project will use public datasets only.

Candidate datasets:

1. SECOM semiconductor manufacturing dataset
2. Wafer map defect classification dataset
3. Public industrial sensor anomaly datasets
4. Financial market anomaly or regime-change datasets

No proprietary or confidential company data will be used.

## Initial Scope

The first version will focus on a public industrial dataset and include:

- Missing value analysis
- Feature distribution analysis
- Outlier detection
- Baseline anomaly detection model
- Evaluation metrics
- Interpretation of false positives and false negatives

## Initial EDA Results

The first exploratory data analysis was performed using the SECOM dataset from the UCI Machine Learning Repository.

The initial EDA focuses on three basic questions:

1. How imbalanced is the pass/fail label distribution?
2. How much missing data exists across process features?
3. Are missing values concentrated in specific features or samples?

### Dataset Shape

The dataset was loaded from the original UCI SECOM raw files.

- Number of samples: 1,567
- Number of process features: 590
- Target label:
  - `-1`: Pass
  - `1`: Fail

Note: Some dataset descriptions report 591 variables. In this project, the feature matrix is loaded directly from `secom.data`, while the target label is loaded separately from `secom_labels.data`.

### Label Distribution

The SECOM dataset is highly imbalanced. Most samples are pass cases, while fail cases are rare.

This makes simple accuracy insufficient as an evaluation metric. For later modeling, fail-class recall, precision, F1-score, balanced accuracy, and confusion matrix analysis will be more important.

![SECOM Label Distribution](reports/figures/label_distribution.png)

### Missing Value Analysis

The dataset contains missing values across process features.

Feature-level missing ratio was calculated as:

```text
missing_ratio = number of missing values in a feature / number of samples


## Repository Structure

```text
industrial-data-anomaly-detection/
├── README.md
├── LICENSE
├── .gitignore
├── data/
│   └── README.md
├── notebooks/
│   └── 01_eda.ipynb
├── src/
│   └── placeholder.py
└── reports/
    └── figures/
