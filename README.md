# Age Prediction Task

## Task: Predict a Person’s Age from Brain Image Data

This repository contains the code and dataset for Task 1 of the Advanced Machine Learning course at ETH. The goal of this task is to predict a person’s age based on brain MRI data.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Specifications](#dataset-specifications)
- [Task Specifications](#task-specifications)
- [Evaluation and Rules](#evaluation-and-rules)
- [Files Description](#files-description)

## Introduction

Magnetic Resonance Imaging (MRI) is a key technology in medical imaging. It uses a magnetic field and radio waves to produce 3D detailed anatomical images. MRI is non-invasive and non-radiative, making it a preferred method for investigating sensitive organs like the brain.

### Why Brain Age Estimation is Interesting
Aging does not affect everyone uniformly. Individual rates of aging are influenced by environmental, genetic, and epigenetic factors. Brain MRI studies have shown a relationship between accelerated aging and brain atrophy. Predicting brain age can improve early diagnosis and risk assessments for neurodegenerative and neuropsychiatric diseases such as Alzheimer’s, Parkinson’s, and Huntington’s diseases.

## Dataset Specifications

- **Features Size**: Approximately 830 features
- **Dataset Size**: Approximately 1200 samples

MRI feature extraction for this project uses around 800 anatomical features derived from image data using FreeSurfer. The dataset includes:
- **X_train.csv**: Training features
- **y_train.csv**: Training labels (ages)
- **X_test.csv**: Testing features
- **sample.csv**: Sample submission file

## Task Specifications

### Subtask 1: Filling Missing Values
- **Background**: The dataset contains missing values represented as NaNs.
- **Requirement**: Fill the missing values in the training and test sets using suitable imputation methods (mean, median, most frequent, etc.).

### Subtask 2: Outlier Detection
- **Background**: The training set contains outliers.
- **Requirement**: Build an outlier detection model to classify samples in the training set as outliers or non-outliers.

### Subtask 3: Feature Selection
- **Background**: The dataset includes additional manual features that require selection.
- **Requirement**: Use feature selection methods to label features as selected or unselected (irrelevant and redundant features).

### Main Task: Age Prediction
- **Background**: After preprocessing and dimensionality reduction, the main task is regression-based age prediction.
- **Requirement**: Use suitable regression methods to predict the age from brain MRI features.

## Evaluation and Rules

The main evaluation metric is the Coefficient of Determination (R²). It measures the proportion of variance in the dependent variable that is predictable from the independent variable, ranging from 1 (best) to negative infinity.

```python
from sklearn.metrics import r2_score
score = r2_score(y_true, y_pred)
```

## Files Description

- **X_train.csv**: Training features
- **y_train.csv**: Training labels (ages)
- **X_test.csv**: Testing features
- **sample.csv**: Sample submission file
- **task1.ipynb**: Main task solution file
- **requirements.txt**: File with the requirements on the environment to run the notebook