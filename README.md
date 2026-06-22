**Machine Learning Analysis of Metabolic Syndrome**

This repository contains the analysis code used for a master's thesis on the application of machine learning methods to the study of metabolic syndrome.

The project investigates metabolic syndrome not only as a binary diagnostic category, but also as a broader systemic metabolic condition reflected in clinical, anthropometric, and biochemical markers. The analysis includes supervised classification of metabolic syndrome, model interpretation, validation on an independent clinical cohort, clustering of obesity-related metabolic phenotypes, and analysis of associations with cognitive test performance.

**Project overview**

The study was based on three analytical blocks:

1. Metabolic syndrome classification using NHANES 2017–2018
Machine learning models were trained to classify participants with and without metabolic syndrome using three feature sets:
diagnostic features;
all available clinical and biochemical features;
non-diagnostic features only.
2. Reproducibility check on an independent clinical cohort
The main classification and feature-importance analyses were repeated on a smaller clinical dataset from Kaliningrad, Russia.
3. Obesity phenotype clustering and cognitive analysis using NHANES 2011–2014
Participants with obesity were clustered using metabolic markers. The resulting metabolic phenotypes were then compared by cognitive test performance in older adults.

**Research aims**

The main goal of the project was to evaluate whether metabolic syndrome can be characterized not only through formal diagnostic criteria, but also through a broader clinical and biochemical profile.

The analysis addressed the following questions:

1. Can machine learning models classify metabolic syndrome using diagnostic and non-diagnostic features?
2. Do non-diagnostic biochemical markers contain information associated with metabolic syndrome status?
3. Which features contribute most strongly to model predictions?
4. Can participants with obesity be separated into metabolically distinct phenotypes?
5. Are metabolic phenotypes and individual metabolic markers associated with cognitive test performance?

**Data sources**

NHANES

The main open data source was the National Health and Nutrition Examination Survey (NHANES), conducted by the National Center for Health Statistics.

The analysis used:

NHANES 2017–2018 for metabolic syndrome classification;
NHANES 2011–2014 for obesity phenotype clustering and cognitive analysis.

NHANES data are publicly available from the official website:

https://www.cdc.gov/nchs/nhanes/

Clinical cohort

An independent clinical cohort was used to check whether the main patterns observed in NHANES were reproducible in a smaller clinical sample.

The clinical dataset itself is not included in this repository because it contains non-public biomedical data. Only the analysis code is provided.

**Methods**

The project includes the following methods:

data preprocessing and feature engineering;
metabolic syndrome status definition;
calculation of derived indices:
HOMA-IR;
TyG index;
TG/HDL ratio;
descriptive statistics;
Mann–Whitney U tests;
Spearman and partial Spearman correlations;
multiple testing correction using Benjamini–Hochberg FDR;
supervised machine learning:
Logistic Regression;
Random Forest;
XGBoost;
train/test evaluation and cross-validation;
ROC-AUC comparison using DeLong test;
model interpretation using SHAP values and feature importance;
K-means clustering;
silhouette score analysis;
PCA visualization;
Cohen’s d effect size estimation;
multiple linear regression for cognitive outcomes.

**Feature sets for metabolic syndrome classification**

Three feature sets were used:

Feature set	Description
A	Diagnostic features used to define metabolic syndrome
B	Full feature set including diagnostic and additional biochemical markers
C	Non-diagnostic features only

The non-diagnostic feature set was used to test whether metabolic syndrome status is reflected in broader metabolic changes beyond the formal diagnostic criteria.

**Main results**

The main findings of the thesis were:

Models trained on diagnostic features showed high classification performance, as expected.
Models trained on the full feature set showed comparable or improved performance.
Models trained only on non-diagnostic features still classified metabolic syndrome better than random, indicating that metabolic syndrome is associated with broader biochemical changes.
SHAP and feature-importance analyses highlighted markers related to inflammation, liver metabolism, purine metabolism, insulin resistance, and general cardiometabolic status.
Clustering of participants with obesity identified two metabolic phenotypes: relatively metabolically favorable and unfavorable obesity.
The separation between obesity phenotypes was not absolute, supporting the interpretation of metabolic health in obesity as a continuum.
Cognitive differences between metabolic phenotypes were modest and mainly related to processing speed and semantic fluency.
Individual markers such as HDL cholesterol and glucose showed weak but statistically significant associations with cognitive test performance.

**Python environment**

The analysis was performed using Python 3.11.

Main libraries:

pandas
numpy
scipy
scikit-learn
xgboost
imbalanced-learn
shap
statsmodels
pingouin
matplotlib
seaborn

**Reproducibility**

Where applicable, a fixed random seed was used:

random_state = 42

Due to differences in local file paths and data availability, some scripts may require path adjustment before execution.

**Data availability and privacy**

NHANES data are publicly available from the official NHANES website.

The independent clinical dataset is not included in this repository due to privacy and ethical restrictions. Any scripts referring to the clinical dataset are provided for transparency and reproducibility of the analytical workflow, but the raw clinical data cannot be shared publicly.

**Citation**

If you use or refer to this repository, please cite the thesis or repository as appropriate.

Suggested citation format:
Koshel A. Machine learning methods for the analysis of metabolic syndrome. Master's thesis, 2026.
