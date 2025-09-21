# Fraudulent-Claim-Detection-ML


# Fraudulent Claim Detection

## Project Overview
This project focuses on detecting fraudulent insurance claims using machine learning techniques. By analyzing historical claim data, the goal is to identify patterns and predict which claims are likely to be fraudulent, enabling insurers to flag high-risk claims for manual review and reduce losses due to fraud.

## Author
- Swati

## Dataset
The dataset contains various features related to insurance claims, including customer details, claim amounts, incident specifics, and claim outcomes. The analysis revealed significant class imbalance: only about 24% of claims are fraudulent, which makes detection challenging.

## Exploratory Data Analysis & Feature Engineering
- Correlation heatmaps were used to analyze numerical features.
- Redundant features related to claim components were identified.
- Feature engineering was applied to extract meaningful predictors and handle class imbalance issues.
- Key features include policy details, customer demographics, claim amounts, incident severity, and time-based features like incident hour.

## Models Used
Two primary models were employed:
- **Logistic Regression**: Highlights demographic and policy-related features as key predictors. Offers interpretability for understanding fraud drivers.
- **Random Forest**: Focuses on claim behavior patterns such as claim amounts per month and injury-vehicle ratios. Provides better accuracy in flagging suspicious claims but showed overfitting on training data.

## Model Performance
- Logistic Regression achieved an ROC AUC of 0.91, indicating strong discriminative ability.
- Random Forest had perfect training accuracy but showed overfitting. On validation data, it detected 1 in 4 fraud cases accurately while clearing 9 in 10 genuine claims.
- Both models struggle with low recall due to class imbalance, resulting in missed fraud cases.

### Key Metrics (Validation Data)
| Metric       | Logistic Regression | Random Forest |
|--------------|---------------------|---------------|
| Accuracy     | 78%                 | 75%           |
| Precision    | 44%                 | 44%           |
| Recall       | 20%                 | 20%           |
| F1-Score     | 0.28                | 0.38          |

## Insights
- Incident severity consistently emerged as the strongest predictor of fraud across models.
- Policy state, education level, and occupation are significant for explaining fraud drivers.
- Behavioral and claim pattern features provide better prediction power.

## Recommendations for Improvement
- Address class imbalance using techniques like SMOTE (Synthetic Minority Over-sampling Technique), undersampling, or cost-sensitive learning to improve recall.
- Explore boosting algorithms such as XGBoost, CatBoost, and Gradient Boosting to enhance precision and reduce false positives.
- Continue refining feature engineering to capture subtle fraud patterns.

## Usage
- The models can be used to assign fraud risk scores to new claims, enabling flagging of high-risk claims for detailed human review.
- This helps insurers focus their resources efficiently to reduce fraud losses.


