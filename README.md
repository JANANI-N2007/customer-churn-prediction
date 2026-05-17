# Customer Churn Prediction

A machine learning project that predicts whether a customer is likely to churn from a bank using historical customer information.

## Project Overview

Customer churn prediction is crucial for banks to identify customers at risk of leaving and take proactive measures to retain them. This project builds a predictive model using machine learning algorithms to analyze customer data and predict churn probability.

## Dataset

The dataset used in this project is the [Bank Customer Churn Prediction Dataset](https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction) from Kaggle.

**Dataset Details:**
- **Rows:** 10,000 customers
- **Columns:** 14 features
- **Target Variable:** Exited (0 = Customer stays, 1 = Customer churns)

## Features

The dataset includes the following features:
- **CreditScore:** Customer's credit score
- **Geography:** Customer's location (France, Germany, Spain)
- **Gender:** Customer's gender (Male, Female)
- **Age:** Customer's age
- **Tenure:** Number of years with the bank
- **Balance:** Account balance
- **NumOfProducts:** Number of bank products the customer uses
- **HasCrCard:** Whether the customer has a credit card (0 = No, 1 = Yes)
- **IsActiveMember:** Whether the customer is an active member (0 = No, 1 = Yes)
- **EstimatedSalary:** Customer's estimated salary
- **Exited:** Target variable (0 = Stay, 1 = Churn)

## Technologies Used

- **Python:** Programming language
- **Pandas:** Data manipulation and analysis
- **NumPy:** Numerical computing
- **Scikit-learn:** Machine learning algorithms and metrics
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical data visualization

## Installation

1. Clone the repository:
```bash
git clone https://github.com/JANANI-N2007/customer-churn-prediction.git
cd customer-churn-prediction
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## How to Run

1. Ensure the dataset `Churn_Modelling.csv` is placed in the `dataset/` folder
2. Open the Jupyter notebook:
```bash
jupyter notebook customer_churn_prediction.ipynb
```
3. Run all cells sequentially from top to bottom

## Models Used

Three machine learning models were trained and compared:

1. **Logistic Regression:** A linear model for binary classification
2. **Random Forest Classifier:** An ensemble learning method using multiple decision trees
3. **Gradient Boosting Classifier:** An ensemble technique that builds models sequentially

## Results

### Model Performance Comparison

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 0.8155 |
| Random Forest | 0.8645 |
| Gradient Boosting | 0.8660 |

### Best Model: Gradient Boosting Classifier

**Evaluation Metrics:**
- **Accuracy:** 0.8660
- **Precision:** 0.7551
- **Recall:** 0.4707
- **F1-Score:** 0.5799

The Gradient Boosting Classifier achieved the highest accuracy and was selected as the final model for the prediction system.

## Output Screenshots

The following visualizations are saved in the `outputs/` folder:

1. **churn_distribution.png** - Distribution of customer churn
2. **gender_vs_churn.png** - Gender comparison with churn status
3. **age_distribution.png** - Age distribution of customers
4. **correlation_heatmap.png** - Correlation matrix of features
5. **balance_vs_churn.png** - Balance comparison between churned and retained customers
6. **model_comparison.png** - Accuracy comparison of all models
7. **confusion_matrix.png** - Confusion matrix for the best model

## Prediction System

The project includes a `predict_churn()` function that accepts customer details and returns a prediction:

```python
predict_churn(credit_score, geography, gender, age, tenure, balance, 
             num_products, has_cr_card, is_active_member, estimated_salary)
```

**Example Output:**
- "Customer likely to churn"
- "Customer likely to stay"

## Project Structure

```
customer-churn-prediction/
│
├── customer_churn_prediction.ipynb  # Main Jupyter notebook
├── requirements.txt                  # Python dependencies
├── README.md                         # Project documentation
├── dataset/                          # Dataset folder
│   └── Churn_Modelling.csv          # Customer churn dataset
└── outputs/                          # Generated visualizations
    ├── churn_distribution.png
    ├── gender_vs_churn.png
    ├── age_distribution.png
    ├── correlation_heatmap.png
    ├── balance_vs_churn.png
    ├── model_comparison.png
    └── confusion_matrix.png
```

## License

This project is licensed under the MIT License.

## Author

[JANANI-N2007](https://github.com/JANANI-N2007)
