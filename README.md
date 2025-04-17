# 🚀 Space Launch Predictions

Predicting the success of SpaceX rocket launches using real-time API data and logistic regression.

## 🔍 Overview

This project uses SpaceX launch data retrieved from a public API to build a logistic regression model for predicting launch success. By analyzing features such as payload mass and booster reuse, we aim to derive actionable insights about the conditions influencing successful launches.

## 🧰 Tools & Libraries

- Python
- `pandas`
- `requests`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- Jupyter Notebook

## 🌐 Data Source

- [SpaceX Launch API](https://github.com/r-spacex/SpaceX-API)

## ⚙️ Process

1. **API Integration**
   - Pulled JSON data from endpoints: `/launches`, `/payloads`, `/cores`
2. **Data Cleaning & Merging**
   - Normalized nested fields
   - Merged launch, payload, and core data on relevant keys
   - Removed null values and duplicates
3. **Exploratory Data Analysis (EDA)**
   - Histogram of payload masses
   - Scatterplots of reused vs. success
   - Analysis of booster landings
4. **Model Development**
   - Rejected linear regression due to poor performance on binary classification
   - Trained a logistic regression model
   - Used binary success/failure outcome for classification
5. **Model Evaluation**
   - **Accuracy**: 94.7%
   - **F1 Score**: 97.3%
   - Confusion matrix showed perfect classification of successful launches, but missed failed launches due to class imbalance.

## 📊 Key Results

- Logistic regression was a good first step but highlighted the challenge of imbalanced classes.
- Payload mass showed some correlation with success, but other variables (e.g., reuse, core reuse count) need deeper feature engineering.
- All failed launches were misclassified due to heavy skew in training data.

## 🧠 Takeaways

- Public APIs can provide dynamic, real-time datasets for machine learning
- Logistic regression is a good starter model, but lacks nuance with imbalanced data
- Future efforts should involve balancing techniques (SMOTE, class weighting) and more robust classifiers

## 🚧 Next Steps

- Implement tree-based models (Random Forest, XGBoost)
- Introduce new features (weather, orbit type, mission type)
- Create a simple frontend to allow real-time prediction based on new API calls
- Set up a live cron job for model retraining using fresh launch data

## 📁 How to Run

```bash
pip install -r requirements.txt
jupyter notebook final_project_space_x_manuel_velazquez.ipynb
