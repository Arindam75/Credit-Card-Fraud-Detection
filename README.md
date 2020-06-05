# Credit Card Fraud Detection

## 1. Problem Descrption
This is a Kaggle Problem by the same name. This involves a dataset with *Anonymized credit card transactions labeled as fraudulent or genuine*.
The dataset is already subjected to PCA with 28 features. The feature names are masked.  It's a classification problem involving heavy class imbalance. With over 28000 rows of data, there are only 500 positive classes. We intend to build a classification model that can give 
us a large AUC.

## 2. Visualizing the Dataset

We attempt to visualize the data across 28 dimensions by choosing tuples of 3 dimensions at a time.  This means , we'll visualize V1,V2,V3 followed by V5,V6,V7 and so on, till V18. Our objective is to vizualize if, both the classes are separable or not.
Interestingly ,in each case the rare class-1 samples show up clustered closely. This is indeed re-assuring !!

## 3. Pre-Processing

We split the data into 5-folds and keep the 5th fold as a hold-out set. The remaining 4-folds are used for Gridsearch. In each fold we generate oversampled data separately. 

## 3. Oversampling the Data

We oversample the data using both SMOTE and ADASYN techniques and build a baseline logistic regression model. The Logistic Regression AUC on the hold-out test set are as follows.
- No Oversampling 0.8213
- SMOTE 0.9461
- ADASYN 0.9169

Clearly SMOTE overshadows ADASYN

## 4. Model Building


