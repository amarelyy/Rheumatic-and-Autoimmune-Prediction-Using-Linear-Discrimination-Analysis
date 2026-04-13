# **Linear Discriminant Analysis for Rheumatic & Autoimmune Disease Classification**
## **Overview**
This project applies Linear Discriminant Analysis (LDA) to classify rheumatic and autoimmune diseases based on patient data.
The goal is to improve diagnostic accuracy by leveraging supervised machine learning and identifying patterns in clinical features.
Autoimmune diseases often share overlapping symptoms and biomarkers, making them difficult to distinguish. This project demonstrates how LDA can enhance class separability and support data-driven medical decision-making.

## **Objectives**
* Apply Linear Discriminant Analysis (LDA) for multi-class disease classification
* Reduce dimensionality while preserving discriminative information
* Accurately predict disease labels
* Evaluate model performance using multiple metrics
* Validate model reliability using cross-validation

## **Dataset**
* Dataset: Rheumatic & Autoimmune Disease Dataset
* Format: Excel (.xlsx)
* Features:
  * Demographic data (e.g., Gender)
  * Clinical biomarkers (HLA-B27, ANA, Anti-Ro, Anti-La, Anti-dsDNA, Anti-Sm)
* Target Variable:Disease (categorical label)
* Source: (Add your dataset link here — Google Drive / Kaggle / etc.)

## **Methodology**
1. Data Preprocessing
* Handle missing values:
Numerical → mean imputation
Categorical → mode imputation
* Encode categorical variables into numerical form
* Shuffle dataset to remove ordering bias
* Split into:
  * X → feature matrix
  * y → labels

2. Stratified Sampling
Reduce dataset size for computational efficiency
Preserve class distribution across diseases
Prevent bias due to class imbalance

3. Linear Discriminant Analysis (LDA)
* LDA is a supervised method that:
  * Maximizes between-class variance (Sb)
  * Minimizes within-class variance (Sw)
* Steps:
  * Compute class means
  * Compute scatter matrices (Sw and Sb)
  * Solve eigenvalue problem
  * Select top components (K−1)
  * Project data into LDA space
    
4. Classification
* Compute centroids for each disease in LDA space
* Assign each sample to the nearest centroid
* This forms a Nearest Centroid Classifier
  
5. Evaluation Metrics
* Accuracy → overall correctness
* Precision → correctness of predictions
* Recall → ability to detect true cases
* F1 Score → balance between precision & recall
* MSE / MAE → numerical error indicators

Note: In medical applications, recall is especially important to avoid missed diagnoses.

6. Validation
* K-Fold Cross Validation (k=5)
* Ensures model stability
* Reduces bias from single split
* Provides mean accuracy and standard deviation
  
7. Visualization
* LDA projection plots (2D scatter)
* Class separation across components
* Feature importance analysis
  
## Results
* LDA successfully improves separation between disease classes
* Some overlap remains due to similar biomarker profiles
* Model achieves strong performance across evaluation metrics
* More reliable than unsupervised approaches for this dataset

## Contribution to SDG 3
This project contributes to Sustainable Development Goal 3: Good Health and Well-Being by:
* Supporting early and accurate diagnosis
* Reducing potential misclassification of diseases
* Promoting data-driven healthcare solutions
* Enhancing decision-making in clinical environments

## Authors
* Aurelia Safa Madrim
* Ursula Maurentti Amarely
