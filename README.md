# Anomaly Detection with XGBoost and CatBoost

## Table of Contents

- [Introduction](#introduction)
- [Company Overview](#company-overview)
- [Problem Statement](#problem-statement)
- [Data Description](#data-description)
- [Prerequisites](#prerequisites)
- [Data Preparation](#data-preparation)
  - [Downloading the Dataset](#downloading-the-dataset)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preprocessing](#data-preprocessing)
  - [Feature Engineering](#feature-engineering)
  - [Train-Test Split](#train-test-split)
- [Model Training and Evaluation](#model-training-and-evaluation)
  - [XGBoost Classifier](#xgboost-classifier)
  - [Handling Class Imbalance](#handling-class-imbalance)
    - [Random Over-Sampling](#random-over-sampling)
    - [SMOTE (Synthetic Minority Over-Sampling Technique)](#smote-synthetic-minority-over-sampling-technique)
  - [Model Evaluation](#model-evaluation)
- [Making Predictions](#making-predictions)
- [Conclusion](#conclusion)

## Introduction

This repository contains code for performing anomaly detection using ensemble models such as XGBoost and CatBoost. The dataset used in this project is from the Kaggle competition [Anomaly Detection](https://www.kaggle.com/c/anomaly-detection).

## Company Overview

Let us assume that we have a company called "Splash," and you are a newly joined Machine Learning Engineer at our company, with a salary of 30 LPA CTC. At Splash, we help retailers with pricing intelligence and business monitoring. One of our main challenges is monitoring and analyzing our client's business metrics in real time for instant detection of incidents that may impact their revenue. A subpart of this challenge is Anomaly Detection, which generates alerts on our client's business metrics.

## Problem Statement

The Problem Statement presented below highlights the problem which we are tackling right now:

Data Description

The description of the column is as follows:

- `timestamp` [float]: provided as a Unix epoch in seconds.
- `value` [int]: is a real value measurement of some metric at the timestamp.
- `is_anomaly` [boolean]: is a boolean value which is True if the corresponding value is identified as an anomaly.
- `predicted` [float]: is a real value prediction coming from a black box forecasting model for that timestamp. This black box forecasting model is assumed to be aware of only the true data distribution.

Since the company is concerned about the anomaly data more than non-anomaly data, we have to be careful in making the predictions for the anomaly cases. Here we have used different ML models to compare their performances in determining the anomaly cases.

## Prerequisites

Before running the code, you need to install the following Python packages:

- pandas
- seaborn
- matplotlib
- xgboost
- scikit-learn
- imbalanced-learn
- catboost
- kaggle

You can install these packages using `pip` by running the following command:

```bash
pip install pandas seaborn matplotlib xgboost scikit-learn imbalanced-learn catboost kaggle
```

Make sure you have Python and pip installed on your system before running the above command. Additionally, you will need a Kaggle API key to download the dataset using the Kaggle API. Follow the Kaggle API setup instructions on the Kaggle website.

## Data Preparation

### Downloading the Dataset

To get started, download the competition dataset from Kaggle using the Kaggle API. Follow these steps to set up your environment and download the data.

### Exploratory Data Analysis (EDA)

Start by loading the training dataset and performing some exploratory data analysis.

## Data Preprocessing

### Feature Engineering

Preprocess the data by converting timestamps to datetime, extracting additional features, and splitting it into training and testing sets.

### Train-Test Split

Split data into training and testing sets.

## Model Training and Evaluation

### XGBoost Classifier

Train an XGBoost classifier without handling class imbalance.

### Handling Class Imbalance

To address class imbalance, explore two techniques: Random Over-Sampling and SMOTE (Synthetic Minority Over-Sampling Technique).

#### Random Over-Sampling

Use Random Over-Sampling to balance the dataset.

#### SMOTE (Synthetic Minority Over-Sampling Technique)

Use SMOTE to generate synthetic data and balance the dataset.

### Model Evaluation

Evaluate the models using metrics like F1-score and precision-recall curves.

## Making Predictions

Use the trained model to make predictions on the test dataset.

## Conclusion

In conclusion, this project explores the use of ensemble models, specifically XGBoost and CatBoost, for anomaly detection. Both models offer ways to handle class imbalance and provide good recall scores, which are crucial for identifying anomalies in imbalanced datasets. The choice between XGBoost and CatBoost may depend on specific use cases and performance requirements.
Handling class imbalance using techniques like SMOTE significantly improved the recall, making it an effective method for anomaly detection in this project.
