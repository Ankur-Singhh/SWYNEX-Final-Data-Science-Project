# Intelligent Network Security Monitoring and Attack Analysis

## Overview
An end-to-end data science project using CIC-IDS2017 network traffic data to explore traffic patterns and evaluate a baseline machine-learning classifier.

## Project Workflow
1. Data preparation and validation
2. Exploratory Data Analysis
3. Decision Tree model development
4. Model evaluation and interpretation
5. Findings, limitations, and future improvements

## Dataset
- **Dataset:** CIC-IDS2017
- **Subset:** Tuesday Working Hours
- **Original records:** 445,909
- **Cleaned records:** 421,626
- **Features:** 78 numerical features
- **Target:** `Label`
- **Classes:** BENIGN, FTP-Patator, SSH-Patator

Official source: https://www.unb.ca/cic/datasets/ids-2017.html

## Technologies
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and Google Colab.

## Modeling
A Decision Tree classifier was trained using an 80/20 stratified train-test split, with class weighting to account for class imbalance.

The notebook reports accuracy, balanced accuracy, precision, recall, macro F1-score, a confusion matrix, and feature importance.

## Key Findings
- The dataset is highly imbalanced, with 97.83% BENIGN traffic.
- Forward and backward packet counts have a correlation of approximately 0.9995.
- `Destination Port` dominates baseline model feature importance.
- The model maintains high performance when `Destination Port` is excluded.
- Independent evaluation is needed to establish real-world generalization.

## Limitations
The results are based on a single dataset subset and a random train-test split. They do not establish real-world intrusion detection reliability.

## Future Work
- Compare multiple classification algorithms.
- Investigate feature importance and redundancy.
- Evaluate performance on independent attack scenarios.
- Explore deployment in a network security monitoring system.
