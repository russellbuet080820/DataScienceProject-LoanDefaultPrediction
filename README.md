# Loan Default Prediction

## Overview
This project tackles an industry-relevant machine learning problem: predicting loan defaults using a real-world dataset. Financial institutions use such models to identify high-risk borrowers, reduce default rates, and allocate resources effectively. By implementing machine learning models, we aim to develop a robust solution to predict default probabilities.

## Dataset
The dataset consists of borrower information and loan-specific data for individuals who received loans in 2021. The dataset is divided into:

- **`train.csv`**: Includes 70% of the data (255,347 rows) with the target column (`Default`), indicating whether the borrower defaulted.
- **`test.csv`**: Includes the remaining 30% (109,435 rows) without the `Default` column for prediction.

The dataset features include various numerical and categorical variables relevant to the prediction task.

## Project Goals
1. Build a machine learning model to predict whether borrowers will default on loans.
2. Evaluate multiple models to determine the best-performing one.
3. Provide actionable insights to financial institutions for risk management.

## Machine Learning Models
The following models were implemented and compared:

- Logistic Regression
- Random Forest
- XGBoost

Key evaluation metrics include:
- Accuracy
- Precision
- Recall
- F1-Score

## Workflow
1. **Data Preprocessing:**
   - Cleaned the dataset and handled categorical variables.
   - Checked for class imbalance and applied stratified train-test splitting.

2. **Exploratory Data Analysis:**
   - Analyzed feature distributions and relationships with the target variable.
   - Plotted correlation heatmaps and variable trends.

3. **Model Training & Evaluation:**
   - Performed hyperparameter tuning using GridSearchCV.
   - Evaluated models using ROC-AUC and other metrics.

4. **Threshold Optimization:**
   - Used the ROC curve to find the optimal threshold for predictions.

## Results
The XGBoost model showed the best performance, balancing precision and recall effectively. Predictions from this model can help financial institutions identify high-risk borrowers and take preventive actions.

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/russellbuet080820/loan-default-prediction.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the main script:
   ```bash
   python main.py
   ```

## Files
- `train.csv` and `test.csv`: Dataset files.
- `main.py`: Main script for model training and prediction.
- `utils.py`: Helper functions for preprocessing and evaluation.
- `README.md`: Project documentation.
