# 1. Project Description and Summary

The increasing of obesity and obesity-associated complications is a major public health concern worldwide. Recent studies have shown that the microbiota of the gastrointestinal tract is an important factor in the development of obesity because the gut microbiota plays an important role in the harvesting, storage, and expenditure of energy obtained from one’s diet. This project builds upon the gut microbiome data processed from the American Gut database. We aim to conduct statistical analysis to identify differences in gut microbiota according to body mass index (BMI) in an American population.

Before doing statistical analysis, we pre-processed the data to filter, transform, and aggregate variables. We first did unsupervised learning using PCA, hierarchical clustering on the species-level OTUs, and aggregated genus level microbiome compositional data. Then we conducted Lasso, Ridge, and linear regressions to model BMI using genus level compositional data and PCs from OTUs data. Finally, we used LDA, SVM, and KNN to classify BMI categories and alcohol consumption frequency. Based on our analysis, we found gut microbiome compositional data and BMI were associated and their relationship was somehow gender-dependent. A strong association between gut microbiome compositional data and BMI category than gut microbiome and alcohol consumption frequency was also found. Further data analysis is needed to better understand the data.

# 2. Unsupervised Learning

## 2.1. Data Preprocessing

1. Filtering the dataset to include only those taxa (OTUs) that were at least 0.1% abundant in any sample following the approach of Gloor and Reid (2016).
2. Replacing zeros with multiplicative simple replacement method, which implementes non-parametric multiplicative simple imputation of left-censored (e.g. values below the detection limit, rounded zeros) and missing data in compositional data sets.
3. Conducted the Centered Log-Ratio (clr) Transformation to those OTUs to transform compositions into real space.

## 2.2. PCA Analysis

## 2.3. Hierachical Clustering

## 2.4. K-means Clustering

# 3. Supervised Learning

## 3.1. Microbiome Compositional Data Analysis

## 3.2. Regression for BMI
### 3.2.1. Lasso Regression Using Log-ratio Transformed Genus Level Data
### 3.2.2. Ridge Regression Using Log-ratio Transformed Genus Level Data
### 3.2.3. Linear Regression Using PCs

## 3.3. Classification for BMI Category
### 3.3.1. Linear Discriminant Analysis (LDA) Using Log-ratio Transformed Genus Level Data
### 3.3.2. Support Vector Machine (SVM) Using Log-ratio Transformed Genus Level Data

## 3.4. Classification for alcohol consumption frequency
### 3.4.1. K-Nearest Neighbors (KNN)
### 3.4.2. Support Vector Machine (SVM) Using Log-ratio Transformed Genus Level Data