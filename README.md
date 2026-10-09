# Hospital Admissions Analysis & Length of Stay Prediction (Python)

## Tools & Skills
- **Tools:** Python in Google Colab – pandas, NumPy, Plotly, seaborn, Matplotlib, scikit-learn
- **Data cleaning:** Standardising columns, datetime conversion, recoding categories, median imputation, missingness flags, IQR outlier detection, duplicate removal
- **Visualisation:** Interactive line charts, histograms, boxplots, violin plots, heatmaps and pair plots
- **Machine learning:** K-Means clustering; Linear Regression, Random Forest and Gradient Boosting regression in scikit-learn pipelines with scaling and one-hot encoding
- **Evaluation:** MAE, RMSE, R², residual analysis and feature importance

## What I Did
This was an assignment for the Data Analytics & Visualisation module of my Data Analytics MSc. I designed an interactive analytical workflow to help hospital administrators understand patient demand and plan resources such as beds and staffing.

- **Dataset:** Two years of cardiology admissions data (15,757 rows, 56 columns) covering demographics, admission details, lab results, diagnoses and outcomes.
- **Cleaning:** I standardised column names, converted dates, recoded single-letter categories into labels and converted lab values to numbers. I handled missing data by removing rows with no dates, imputing medians and adding flags for heavily missing fields. I also derived and validated length of stay, removed duplicates, and checked outliers, keeping genuine extreme clinical values. This left 11,738 rows and 61 columns.
- **Exploratory analysis:** I built 12 interactive visualisations covering admissions over time, patient demographics, biomarkers, diagnoses, length of stay, outcomes and correlations, plus K-Means clustering of patient profiles.
- **Modelling:** I predicted length of stay as a measure of resource use, excluding columns that would leak future information. I trained three regression models on 80% of the data, tested them on the remaining 20%, and compared them with interactive charts.

## Key Findings
- Admissions rose steadily across 2017–2018 with seasonal peaks. Emergency admissions consistently outnumbered outpatient (OPD) admissions and had much longer, more variable stays.
- Most patients were aged around 55–65. Acute coronary syndrome was the most common diagnosis, followed by heart failure, and most admissions ended in discharge.
- Urea and creatinine were the most strongly correlated variables. K-Means identified three patient groups based on kidney function (creatinine) and heart function (ejection fraction).
- All three models performed similarly. Gradient Boosting was slightly best (MAE 2.87 days, RMSE 4.52, R² 0.19), so predictions were typically within about three days, though long stays were underestimated.
- Recommendations include flagging abnormal biomarkers early to plan for longer stays and preparing surge capacity for emergency and winter peaks. Adding operational data such as bed occupancy and staffing would improve the predictions.

## Files
| File | Description |
|------|-------------|
| `CW1_Task_3_25259628.pdf` | Report covering system design, data cleaning, interactive analysis, modelling and recommendations |
| `CW1_Task_3_25259628.ipynb` | Python notebook with the full cleaning, visualisation and modelling workflow |
