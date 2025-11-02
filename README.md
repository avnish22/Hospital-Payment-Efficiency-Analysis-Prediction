# 🏥 Hospital Payment Efficiency Analysis & Prediction
### A Data Analytics and Machine Learning Project using Python & Power BI

## 📊 Business Problem

Hospitals often experience a large gap between the charges billed to Medicare and the actual payments received.
This leads to inefficiency in reimbursements, cash flow issues, and unclear insights into which hospitals, regions, or DRG procedures are underperforming financially.

This project analyzes hospital payment data to:
-> Identify payment inefficiencies

-> Predict expected reimbursements

-> Provide data-driven insights to optimize billing and cost recovery

## 🎯 Business Objectives

-> Analyze hospital cost efficiency across states, cities, and DRG types.

-> Predict Medicare reimbursement amounts using regression models.

-> Identify top drivers behind payment gaps and inefficiency.

-> Build a Power BI dashboard for leadership to visualize performance.

## 🧠 Project Workflow
##### Phase 1 – Data Understanding & Cleaning (Python)

Dataset: Medicare Hospital Payments – Kaggle Dataset

163,065 records, 12 features

###### Key Columns:
DRG Definition, Provider Id, Provider Name, City, State, Total Discharges,
Average Covered Charges, Average Total Payments, Average Medicare Payments

#### Cleaning Steps:

-> Removed duplicates and trimmed whitespaces

-> Converted currency columns to numeric

-> Standardized column names and fixed missing values


###### Phase 2 – Exploratory Data Analysis (EDA)

#### Key findings:

-> Certain states (e.g., CA, TX, FL) dominate in hospital discharges.

-> Payment gaps exist across hospitals, even for the same DRG.

-> Higher billed charges ≠ higher Medicare reimbursements.

-> DRG procedures show strong cost variation — suggesting pricing inefficiency.

##### Phase 3 – Feature Engineering

Added derived metrics:

🏦 Payment Gap = Average Covered Charges - Average Total Payments

💰 Medicare Coverage Ratio = Average Medicare Payments / Average Total Payments

⚙️ Payment Efficiency = Average Total Payments / Average Covered Charges

These helped quantify how efficiently hospitals recover billed costs.

##### Phase 4 – Statistical Testing

Correlation: Weak correlation between total discharges and payments (corr ≈ -0.016).

ANOVA: Significant difference in average payments across DRG categories.

Chi-square: Strong link between region and high/low payment efficiency.

✅ Business takeaway: Volume doesn’t guarantee profitability — pricing strategy matters more.

Phase 5 – Predictive Modeling

###### Goal: Predict Average Medicare Payments using regression.

Model	R² Score	RMSE	Insights
Linear Regression	0.72	Moderate	Simplicity, baseline model
Random Forest	0.88	Low Error	Captures nonlinear patterns
XGBoost Regressor	0.91	Best	High accuracy, efficient

###### ✅ XGBoost selected as final model.

Phase 6 – Power BI Dashboard

Built interactive dashboards with Fact + Dimension schema:

Fact Table: HospitalPayments
Dimensions: Provider, DRG

###### 📈 Pages:

Overview Page: KPIs (Avg Payment, Avg Efficiency, Total Discharges)

State Comparison: Map & bar charts for payment gap across states

DRG Analysis: Cost vs payment variation by DRG

Insights Page: Summary + Recommendations

##### 🔢 KPIs:

Average Payment Efficiency

Average Payment Gap

Top 5 Efficient Hospitals

Top 5 Costliest DRGs

##### 💡 Key Insights

Average hospital payment efficiency = 68% → large scope for cost recovery

10 DRG types account for >60% of inefficiency

Some states consistently show low reimbursements (<60%)

Medicare dependency is a financial risk for smaller hospitals

###### 🚀 Business Impact

By optimizing pricing and billing for top 10 DRGs, hospitals can:

Improve payment efficiency by 10–20%

Increase Medicare reimbursement rate

Strengthen financial sustainability and transparency
