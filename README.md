# Breast-Cancer-Prediction
A machine learning project that predicts breast cancer diagnosis using the Wisconsin Breast Cancer dataset.


# Breast Cancer Prediction using Machine Learning

## Overview
This project demonstrates the use of machine learning algorithms to predict breast cancer diagnoses. Using the Wisconsin Breast Cancer dataset, we implement different classification models to classify breast cancer cases as either **Malignant (M)** or **Benign (B)** based on features extracted from breast mass images. 

## Dataset Description
The dataset contains features computed from a fine needle aspirate (FNA) of a breast mass. Each sample represents a cell nucleus, and the features describe characteristics like radius, texture, area, perimeter, compactness, concavity, etc.

### Input Features:
- `radius`: Mean distance from the center to points on the perimeter
- `texture`: Standard deviation of gray-scale values
- `perimeter`: Perimeter of the cell nucleus
- `area`: Area of the cell nucleus
- `smoothness`: Local variation in radius lengths
- `compactness`: Calculated as (perimeter^2 / area - 1.0)
- `concavity`: Severity of concave portions of the contour
- `concave points`: Number of concave portions of the contour
- `symmetry`: Symmetry of the cell nucleus
- `fractal dimension`: "Coastline approximation" - 1

### Target Variable:
- Diagnosis (M = malignant, B = benign)

## Steps in the Analysis
1. **Data Loading & Cleaning**:
   - Load the dataset, remove unnecessary columns.
   - Convert categorical labels ('M' and 'B') to numerical values.
   
2. **Data Exploration**:
   - Visualize and analyze feature distributions for malignant and benign diagnoses.
   
3. **Model Building**:
   - Build and compare various machine learning models:
     - **Logistic Regression**
     - **Decision Trees**
     - **Random Forest**
     
4. **Model Evaluation**:
   - Evaluate model performance using accuracy, cross-validation, and feature importance.

## Key Findings
- **Random Forest** is the most effective model for breast cancer classification, achieving an accuracy of ~95% and cross-validation score of ~93%.
- Certain features like `radius_mean`, `area_mean`, and `concave points_mean` are most important for predicting malignancy.

## Conclusion
The Random Forest model with the top 5 features provides a high-performing solution for classifying breast cancer diagnoses. Future work could explore further model optimization and additional feature engineering to improve prediction accuracy.

## Installation
Clone this repository and install the required dependencies:
```bash
git clone https://github.com/your-username/breast-cancer-prediction.git
cd breast-cancer-prediction
pip install -r requirements.txt
