# 📈 Gold Price Prediction Using Yearly Data

## 📌 Project Overview
This project focuses on analyzing and predicting gold prices using historical **yearly data**.  
The goal is to understand long-term price trends, engineer time-based features, and apply machine learning models to forecast future gold prices.

The project follows a complete data science workflow including data loading, cleaning, feature engineering, exploratory data analysis (EDA), model training, evaluation, and visualization.

---

## 🎯 Project Objectives
- Analyze historical yearly gold price trends  
- Perform feature engineering for time series data  
- Compare linear and non-linear regression models  
- Evaluate model performance using standard regression metrics  
- Visualize actual vs predicted gold prices  

---

## 🛠️ Tools & Technologies
- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **Machine Learning (Regression Models)**

---

## 📂 Dataset Description
- **Source:** Annual gold price dataset  
- **Time Span:** 1980 – recent years  
- **Features Include:**
  - Date
  - Gold price in USD
  - Prices in other currencies (EUR, GBP, INR, AED, CNY)

---

## 🧹 Data Cleaning & Preparation
- Converted date column to datetime format  
- Ensured price column was numeric  
- Handled missing values:
  - Removed invalid date/price rows
  - Filled missing CNY values using median imputation  
- Sorted data chronologically  
- Extracted **Year** from the Date column  

---

## ⚙️ Feature Engineering
To improve predictive performance, time-based features were created:

- **Lag1:** Gold price from the previous year  
- **Rolling3:** 3-year rolling average of gold prices (shifted)  
- **Year:** Extracted numerical year value  

These features help capture historical trends and momentum in yearly data.

---

## 📊 Exploratory Data Analysis (EDA)
EDA was conducted to understand price behavior and trends:

### Key Analyses:
- Gold price trend over time  
- Yearly price fluctuations  
- Rolling average trend analysis  
- Summary statistics of gold prices  

### Key Insights:
- Gold prices show long-term upward and downward cycles  
- Rolling averages smooth short-term volatility  
- Significant variation exists across different decades  

---

## 🧪 Model Preparation
- Time-based train-test split (80% train, 20% test)
- Feature set:
  - `Lag1`
  - `Rolling3`
  - `Year`
- Target variable:
  - `Price`

---

## 🤖 Models Used
Two regression models were trained and compared:

### 1️⃣ Linear Regression
- Captures linear trends over time
- Performs well on small datasets with clear temporal patterns  

### 2️⃣ Random Forest Regressor
- Captures non-linear relationships
- Ensemble-based approach  

---

## 📏 Model Evaluation
Models were evaluated using standard regression metrics:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score**

### Performance Summary:
| Model | MAE | RMSE | R² |
|------|-----|------|----|
| Linear Regression | Lower error | Better RMSE | Positive R² |
| Random Forest | Higher error | Higher RMSE | Negative R² |

✅ **Linear Regression outperformed Random Forest**, likely due to the small dataset size and strong temporal structure.

---

## 📉 Visualization
- Actual vs Predicted gold prices for:
  - Linear Regression
  - Random Forest
- Year-wise comparison highlights model accuracy and trend alignment  

---

## 💡 Key Takeaways
- Time-based feature engineering significantly improves forecasting accuracy  
- Simpler models like Linear Regression can outperform complex models on small, structured datasets  
- Gold prices exhibit strong long-term trends suitable for regression-based forecasting  

---

## 🚀 Future Improvements
- Use higher-frequency data (monthly or daily)  
- Apply advanced time series models (ARIMA, SARIMA, LSTM)  
- Include macroeconomic indicators (inflation, interest rates)  
- Hyperparameter tuning for ensemble models  


