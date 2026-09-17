# Heart Stroke Prediction

My first end-to-end machine learning project — from raw data to a deployed web app with an interactive front end.

## Live Demo
*https://heart-stroke-predictor-basic.streamlit.app/*

## About This Project
This is my first complete ML project as a data science student. It covers the full pipeline: exploratory data analysis, cleaning, preprocessing, model training, evaluation, and deployment through a Streamlit web app.

The model is not perfect — the dataset is small and I am still learning. But building it end-to-end, from a raw CSV to a working front end, has been a great learning experience.

## Dataset
- **Source:** Kaggle — Heart Failure Prediction
- **Rows:** 918
- **Features:** Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope
- **Target:** HeartDisease (0 = No, 1 = Yes)

## Workflow
1. **EDA** — distributions, correlation heatmap, class balance
2. **Cleaning** — imputed zero values in Cholesterol and RestingBP with the mean
3. **Preprocessing** — one-hot encoding for categorical features, standard scaling for numerical features
4. **Modeling** — trained 5 classifiers: Logistic Regression, KNN, Naive Bayes, Decision Tree, SVM
5. **Evaluation** — compared using accuracy and F1-score

## Results

| Model | Accuracy | F1 Score |
|---|---|---|
| Logistic Regression | 0.8696 | 0.8857 |
| KNN | 0.8641 | 0.8815 |
| Naive Bayes | 0.8533 | 0.8683 |
| SVM | 0.8478 | 0.8679 |
| Decision Tree | 0.7717 | 0.7941 |

**Best Model:** Logistic Regression (~87% accuracy)

## Limitations
- Small dataset (918 rows), which limits performance
- No hyperparameter tuning yet
- Outliers in Cholesterol and Oldpeak could be handled better
- More feature engineering would likely help

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Streamlit
- Joblib

## How to Run Locally

1. Clone the repo:
```bash
git clone https://github.com/InYourMachine/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the app:
```bash
streamlit run app.py
```
