# spacex-launch-prediction
Predicting the success of SpaceX rocket launches using real-time API data and logistic regression.
# 🚀 Space Launch Predictions

Predicting the success of SpaceX rocket launches using real-time API data and logistic regression.

## 🔍 Overview
This project pulls live launch data from the SpaceX API and uses logistic regression to predict the likelihood of success for future launches based on key features.

## 🧰 Tools & Libraries
- Python
- pandas
- requests
- sklearn
- matplotlib
- seaborn
- Jupyter Notebook

## 🌐 Data Source
- [SpaceX Launch API](https://github.com/r-spacex/SpaceX-API)

## ⚙️ Process
1. API integration for real-time launch data
2. Data cleaning and preprocessing
3. Feature selection and exploratory analysis
4. Logistic regression modeling
5. Model evaluation using accuracy, precision, and confusion matrix

## 📊 Results
- Model achieved ~XX% accuracy predicting launch success
- Top influencing features: `rocket_type`, `launch_site`, `payload_mass`

## 🧠 Takeaways
- Real-time API data can enhance predictive modeling
- Logistic regression provides explainable insights for decision-making
- Strong foundation for expanding into classification models with more complex inputs

## 🧪 Next Steps
- Add more advanced models (e.g., Random Forest, XGBoost)
- Integrate frontend to visualize predictions interactively
- Monitor API shifts to maintain model accuracy

## 📁 How to Run
```bash
pip install -r requirements.txt
jupyter notebook final_project_space_x_manuel_velazquez.ipynb
