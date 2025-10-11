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

<img width="1010" height="539" alt="Screenshot 2025-10-12 002740" src="https://github.com/user-attachments/assets/99b6cd4e-f9b3-4423-ae2f-3df2c6ecbebb" />


## 3. Features Used for Prediction

The model predicts insurance premiums using the following input features:

Feature	Description
| **Feature**              | **Description**                                             |
| ------------------------ | ----------------------------------------------------------- |
| **Age**                  | Input age between 18–100. Premiums increase with age.       |
| **Number of Dependants** | More dependants may increase premiums.                      |
| **Income (₹ Lakhs)**     | Higher income can indicate preference for premium plans.    |
| **Genetical Risk (0–5)** | Higher genetic risk increases premium.                      |
| **Insurance Plan**       | Choose between **Bronze**, **Silver**, or **Gold**.         |
| **Employment Status**    | Options: Salaried, Self-employed, Freelancer.               |
| **Gender**               | Male / Female. May influence health risk factors.           |
| **Marital Status**       | Married or Single. Impacts coverage needs.                  |
| **BMI Category**         | Normal, Overweight, Obesity, Underweight.                   |
| **Smoking Status**       | No Smoking / Regular / Occasional.                          |
| **Region**               | Northwest, Southeast, Northeast, or Southwest.              |
| **Medical History**      | Conditions like diabetes or hypertension increase premiums. |


## 4. Installation Instructions

Follow the steps below to set up the project locally:

**Clone the repository**
git clone https://github.com/aadeshchaudhari/Machine-Learning-Regression-Project-Healthcare-Premium-Cost-Estimator.git
cd Machine-Learning-Regression-Project-Healthcare-Premium-Cost-Estimator

**Create and activate a virtual environment**
python -m venv venv
source venv/bin/activate    # On Windows use: venv\Scripts\activate

**Install dependencies**
pip install -r requirements.txt

**Run the Streamlit web app**
streamlit run main.py


**Create and activate a virtual environment**
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate

**Install dependencies v**
pip install -r requirements.txt

**Run the Streamlit web app**
streamlit run main.py


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
