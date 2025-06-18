---
layout: project
title: Fraud Detection by Machine Learning
date: 2020-08-01
screenshot:
  src: /assets/img/projects/poster1.png
  #max_height: 850px  # Custom height for this specific project
  srcset:
    1920w: /assets/img/projects/poster1.png
    960w: /assets/img/projects/poster1@0.5x.png
    480w: /assets/img/projects/poster1@0.25x.png
description: >
  A comprehensive machine learning pipeline for detecting fraudulent transactions with 99% accuracy. This project tackles extreme class imbalance using advanced techniques including SMOTE, ensemble methods, and automated hyperparameter optimization to protect financial systems in real-time.
links:
  - title: Repository
    url: https://github.com/YannaCS/Fraud-Detection-By-Machine-Learning
featured: true
---

## Project Details

Here's more detailed information about it:

- **Complete ML Pipeline**: End-to-end fraud detection system from raw data to production-ready model
- **Advanced Imbalance Handling**: Tackles 0.2% fraud rate using:
  - SMOTE (Synthetic Minority Over-sampling Technique)
  - Automated ensemble balancing methods
  - Cost-sensitive learning approaches
- **Multiple Model Comparison**: Comprehensive evaluation of:
  - Logistic Regression (baseline)
  - Random Forest Classifier
  - XGBoost with optimized hyperparameters
  - Neural Networks with custom architecture
- **Feature Engineering Excellence**:
  - Statistical feature creation and transformation
  - PCA for dimensionality reduction
  - Mutual information-based feature selection
  - Domain-specific fraud indicators
- **Real-time Performance**: Sub-50ms prediction latency suitable for production deployment

### Key Achievements

- **53.46% Fraud Detection Rate**: Catches more than half fraudulent transactions
- **<0.5% False Positive Rate**: Minimizes customer friction
- **0.76 AUC-ROC Score**: Good model discrimination
- **Production Ready**: Scalable architecture for real-world deployment  

<img src="/assets/img/projects/poster2.png" alt="Baseline vs Optimized & Optimized Models Performance Comparison">   
<img src="/assets/img/projects/poster3.png" alt="XGBoost Evaluation"> 


### Technology Stack

- Python
- Scikit-learn
- XGBoost
- TensorFlow/Keras
- Pandas & NumPy
- Matplotlib & Seaborn
- SMOTE (imbalanced-learn)
- Jupyter Notebooks