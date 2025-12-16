# Bank Marketing Analysis

End-to-end data analysis and predictive modeling project based on a real-world
bank marketing dataset. The objective is to identify clients with a higher
probability of subscribing to a term deposit, allowing more efficient and
targeted marketing campaigns.

## Business Problem
A Portuguese bank conducted multiple phone-based marketing campaigns to sell
long-term deposits. These campaigns required significant human and financial
resources, and many clients were contacted multiple times with low conversion
rates.

The business goal is to predict which clients are more likely to subscribe
to the product in order to:
- Optimize marketing resources
- Reduce unnecessary client contacts
- Increase campaign conversion rates

## Dataset
- Source: UCI Machine Learning Repository
- Name: Bank Marketing Data Set
- Observations: 41,188
- Features: 20 input variables + 1 target variable
- Target variable: `y` (subscription to term deposit: yes / no)

The dataset contains demographic, financial, and campaign-related information
from real marketing calls conducted between 2008 and 2010.

## Key Challenges
- Strong class imbalance (~11% positive class)
- Presence of categorical variables with "unknown" values
- Risk of data leakage due to call duration feature
- Need for appropriate evaluation metrics beyond accuracy

## Project Structure
```
bank-marketing-analysis/
│
├── data/
│ └── bank-additional-full.csv
│
├── notebooks/
│ ├── 01_data_loading.ipynb
│ ├── 02_exploratory_data_analysis.ipynb
│ ├── 03_feature_engineering.ipynb
│ ├── 04_modeling_and_evaluation.ipynb
│
├── README.md
├── requirements.txt
```

## Methodology
1. **Data Loading & Inspection**
   - Dataset structure, dimensions, and data types
   - Identification of categorical and numerical variables
2. **Exploratory Data Analysis (EDA)**
   - Distribution analysis of numerical features
   - Conversion rate analysis by demographic and financial categories
   - Identification of high-impact variables
3. **Feature Engineering**
   - Encoding of categorical variables using One-Hot Encoding
   - Handling of class imbalance
   - Discussion and control of data leakage risks
4. **Predictive Modeling**
   - Model: Random Forest Classifier
   - Train-test split with stratification
   - Balanced class weights
5. **Evaluation**
   - Confusion Matrix
   - Precision, Recall, F1-score
   - ROC AUC and ROC Curve

## Key Results
- The dataset shows a strong class imbalance, making accuracy an unreliable metric
- Call duration is the most predictive feature, but introduces data leakage
- Previous successful campaigns significantly increase conversion probability
- Clients with fewer contact attempts tend to have higher acceptance rates

## Business Insights
- Focusing on large population segments (e.g., administrative and blue-collar workers)
  provides higher overall return than targeting small high-conversion groups
- Repeated calls reduce effectiveness
- Historical campaign outcomes are strong indicators of future success

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter / Google Colab

## Notes
This project was adapted from an academic assignment and reorganized to present
a professional, end-to-end data analysis workflow suitable for a data analytics
portfolio.
