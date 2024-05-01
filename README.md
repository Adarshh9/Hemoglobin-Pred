# Hemoglobin Prediction Model

## Introduction
This project aims to predict hemoglobin values based on various features extracted from images. The dataset consists of hemoglobin values along with other parameters such as image features and phone models.

## Problem Statement
The primary challenges addressed in this project were:
- Building predictive models for hemoglobin values based on image features.
- Calibrating models for new phone models where training data might be limited.

## Approach
### Part 1: Model Training
1. **Data Preprocessing**: The dataset was loaded and preprocessed. Features such as image name and phone model were dropped, and the target variable was isolated.
2. **Model Selection**: Two regression models, Random Forest and XGBoost, were trained using the preprocessed data.
3. **Model Evaluation**: Models were evaluated using Mean Squared Error (MSE) and R2 Score metrics.

### Part 2: Model Calibration for New Phone Models
1. **Data Filtering**: The dataset was filtered based on existing phone models.
2. **Model Averaging**: Average hemoglobin values for existing phone models were calculated.
3. **Calibration**: A Random Forest model was trained on the existing phone model data.
4. **Prediction**: The trained model was used to predict hemoglobin values for a new phone model.
5. **Evaluation**: Predictions were evaluated using MSE and R2 Score metrics against actual values of the new phone model data.

## Files
- **Python-Dev-Hemoglobin-Data-Sheet1.csv**: Initial dataset containing hemoglobin values and features.
- **phone_model1.csv**: Filtered data for Phone Model 1.
- **phone_model2.csv**: Filtered data for Phone Model 2.
- **models/rf_model.pickle**: Pickled Random Forest model.
- **models/xg_model.pickle**: Pickled XGBoost model.

## Usage
1. **Model Training**: Execute `Part 1` code to train Random Forest and XGBoost models.
2. **Model Calibration**: Execute `Part 2` code to calibrate the model for new phone models.
3. **Prediction**: Use the calibrated model to predict hemoglobin values for new phone models.

## Dependencies
- pandas
- scikit-learn
- xgboost

## Conclusion
The project successfully addressed the challenge of predicting hemoglobin values using image features. Additionally, it provided a framework for calibrating models for new phone models with limited data.

---

Feel free to customize this template according to your project specifics and add any additional information or sections as needed.