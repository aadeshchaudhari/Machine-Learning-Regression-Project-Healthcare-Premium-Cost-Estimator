# Health Premium Prediction Model

This project implements a Health Premium Prediction Model that predicts health insurance premiums based on personal and medical attributes.
The model uses:

Multiple Linear Regression for the “age ≤ 25” group

XGBoost with Random Search Tuning for the “age > 25” group

A Streamlit web application is included, allowing users to input attributes and receive an estimated insurance premium instantly.

## 1. Project Overview

The Health Premium Prediction Model considers various factors such as age, BMI, smoking habits, and income to predict health insurance premiums.
This project is particularly useful for:

Insurance companies: to estimate customer premiums efficiently

Individuals: to understand premium variations based on lifestyle and health choices

## 2. Project Structure
ml-health-premium-prediction/
│
├── main.py                                # Streamlit application file
├── prediction_helper.py                   # Helper functions for preprocessing & prediction
├── requirements.txt                       # Python dependencies
├── README.md                              # Project documentation
│
├── ml_premium_prediction_young_with_gr.ipynb   # Modeling for age ≤ 25 group
├── ml_premium_prediction_rest_with_gr.ipynb    # Modeling for age > 25 group
│
└── artifacts/                             # Model artifacts
    ├── model_young.joblib                 # Serialized model (age ≤ 25)
    ├── model_rest.joblib                  # Serialized model (age > 25)
    ├── scaler_young.joblib                # Scaler (age ≤ 25)
    └── scaler_rest.joblib                 # Scaler (age > 25)

## 3. Features Used for Prediction

The model predicts insurance premiums using the following input features:

Feature	Description
Age	Input age between 18–100. Premiums increase with age.
Number of Dependants	More dependants may increase premiums.
Income (₹ Lakhs)	Higher income can indicate preference for premium plans.
Genetical Risk (0–5)	Higher genetic risk increases premium.
Insurance Plan	Choose between Bronze, Silver, or Gold.
Employment Status	Options: Salaried, Self-employed, Freelancer.
Gender	Male / Female. May influence health risk factors.
Marital Status	Married or Single. Impacts coverage needs.
BMI Category	Normal, Overweight, Obesity, Underweight.
Smoking Status	No Smoking / Regular / Occasional.
Region	Northwest, Southeast, Northeast, or Southwest.
Medical History	Conditions like diabetes or hypertension increase premiums.

## 4. Installation Instructions

Follow the steps below to set up the project locally:

# Clone the repository
git clone https://github.com/Vraj-Data-Scientist/ml-health-premium-prediction.git
cd ml-health-premium-prediction

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the Streamlit web app
streamlit run main.py

## 5. Modeling Approach
Preprocessing

Missing values handled appropriately

Categorical features encoded

Numerical features scaled using StandardScaler

Models

Age ≤ 25: Multiple Linear Regression

Age > 25: XGBoost with Random Search Hyperparameter Tuning

Feature Scaling

All numerical inputs are standardized to improve model stability and accuracy.

## 6. Results & Performance
For Age ≤ 25

Model: Multiple Linear Regression

Score: 98.87%

For Age > 25

Model: XGBoost (with Random Search Tuning)

Score: 99.70%

Key Output:

Predicted Premium — the estimated health insurance premium based on user inputs.

## 7. Streamlit Web Interface

Users can interactively enter their details in the Streamlit UI and view their predicted premium in real time.
Example workflow:

Input attributes (Age, BMI, Income, etc.)

Select insurance plan and lifestyle options

Get an instant premium estimate

## 8. Dependencies

All dependencies are listed in requirements.txt.
Key libraries include:

pandas

numpy

scikit-learn

xgboost

streamlit

joblib

## 9. Future Enhancements

Integration of more robust ensemble models

Addition of visual analytics in Streamlit

Support for real-world dataset updates
