# 📦 Capstone Project: Demand Forecasting in Supply Chain (Avnet – Team008)

## 👥 Team Members
-  Maria Sequeira  
- Yuchin Chen  
- Balbir Singh  
- Rasika Teli  
- Harsh Kevadiya

## 🎯 Project Sponsor
**Company Name:** Avnet, Inc.  
**Division:** Avnet Velocity  
**Location:** 2211 S 47th St, Phoenix, AZ 85034  

---

## 📌 Executive Summary

This capstone project aimed to improve **weekly shipment forecasts** for Avnet from **January to May 2025**. The team compared actual shipment data with **customer-submitted forecasts** and developed advanced models—SARIMAX, Prophet, Random Forest, and **XGBoost**. XGBoost was selected for its **highest accuracy** (MAPE: 2.05%).

We also analyzed the potential influence of **NASDAQ trends** on demand and customer-specific forecasting behaviors. The study revealed a weak correlation with market trends but highlighted key operational improvements.

---

## 🧩 Problem Statement

Avnet relies heavily on **customer forecasts** to plan shipments, but these often misalign with actual demand. This leads to:
- Overstocking and stockouts  
- Inventory cost inefficiencies  
- Delivery delays  

Our objective:  
> Can a **machine learning model outperform** human forecasts and improve demand visibility?

---

## 📊 Scope of Work

1. **Data Processing & Cleaning**  
   - Cleaned historical shipment data (2023–2024, 20,587 rows)  
   - Verified key attributes (Customer ID, Region, Factory)

2. **Forecasting Model Development**  
   - Compared actual vs. customer forecasts  
   - Built predictive models: SARIMAX, Prophet, Random Forest, XGBoost  
   - Selected **XGBoost** based on RMSE and MAPE

3. **Customer Forecast Behavior Analysis**  
   - Evaluated over/under forecasting patterns  
   - Compared customer "Old Forecast" vs. "New Forecast" vs. ASU Model

4. **NASDAQ Correlation Analysis**  
   - Tested demand sensitivity to market shifts  
   - Simulated NASDAQ ±5% movements to see demand impact

5. **Delivery & Supply Chain Tracking**  
   - Tracked CRD vs. ATP vs. Actual Ship Date  
   - Analyzed On-Time Delivery (OTD) performance  

---

## 🧠 Exploratory Data Insights

- 920 unique Material IDs  
- 67.84 million units shipped in 2023–2024  
- AMER region had the highest volume (~24M units)  
- Top 3 customers by volume: Customer 1, 5, 8  

### Trends:
- Demand surged in March and declined post-October  
- Clear variability in monthly and regional shipment behaviors  

---

## 🤖 Model Performance

## 🤖 Model Performance Summary

| Model         | MAPE (%) | RMSE      | Comments                          |
|---------------|----------|-----------|-----------------------------------|
| SARIMAX       | 0.57     | 803,865   | Captured trend but limited future accuracy |
| Prophet       | 209.98   | 1,069,484 | Over-forecasted significantly     |
| Random Forest | 1.75     | **704,709** | Best RMSE, but limited temporal awareness |
| XGBoost       | **2.05** | 768,209   | Balanced generalizability and performance |


### 📌 Why XGBoost?
Despite RF’s RMSE edge, **XGBoost** was preferred due to:
- Lower forecast deviation across customers  
- Stronger correlation with forecast change behavior  
- Interpretability and robustness

---

### 🧰 Libraries Used for Modeling:

- `pandas` – data loading and transformation  
- `numpy` – numerical operations and reshaping  
- `matplotlib.pyplot` – visualizations of trends and predictions  
- `xgboost.XGBRegressor` – core model for forecasting  
- `sklearn.metrics` – evaluation using MAPE and RMSE  
- `re` – regular expressions for column cleaning and feature parsing  
- `statsmodels` – used in SARIMAX model development  
- `prophet` – used for baseline trend modeling

> ✅ > ✅ All models were built using **Python** in **Jupyter Notebooks** 🧪, with visualizations and dashboards created in **Tableau** 📊 and **Power BI** 📈.

---

## 📈 Key Takeaways

- **Customer Forecasts Vary Widely**: Some customers over-predict, while others miss spikes.  
- **ASU Model Adds Stability**: Machine learning offered consistency and outperformed customer inputs.  
- **NASDAQ Impact**: Weak short-term correlation. Useful only for scenario planning, not precise forecasting.  
- **High-Inspection Zones**: Certain customers or products needed frequent updates or corrections.  

---

## ⚠️ Risks & Challenges

- **Limited Data Access**: Only partial visibility into Avnet’s systems  
- **Supplier Lead Time**: Long lead times make accurate planning harder  
- **Market Disruptions**: Global events like chip shortages or political unrest affect demand  
- **Forecast Feedback Delays**: Customer response times affect model tuning  

---

## 📢 Business Value

- 📦 Reduced inventory imbalance through more accurate forecasting  
- ⏱️ Improved on-time delivery performance  
- 🧠 Enhanced production planning with predictive insights  
- 📊 **Interactive dashboards via Tableau** for real-time decision-making  
- 🤖 Strategic use of machine learning for scalable forecasting

---

## 🛠️ Tools & Technologies

- 🐍 Python (`Pandas`, `Scikit-learn`, `XGBoost`, `Prophet`, `Statsmodels`)  
- 📊 **Tableau** – used for interactive visualizations and dashboarding  
- 📉 Excel – for initial data cleanup and inspection  
- 🖼️ PowerPoint – for stakeholder presentations  
- 📈 Power BI – planned for future executive dashboards  


---

## 📅 Timeline & Milestones

- 📍 Jan 2025: Kickoff & Data Acquisition  
- 📍 Feb 2025: Model Prototyping  
- 📍 Mar 2025: Midterm Presentation  
- 📍 Apr 2025: Final Model Evaluation  
- 📍 Apr 25, 2025: Final Presentation  

---

## ✅ Conclusion

This project demonstrated that **machine learning models**—especially XGBoost—can significantly improve demand forecasting accuracy for electronic component distribution. Avnet can benefit from automated forecasts, smarter inventory planning, and more resilient supply chains.

---

**Reference:**  
[Avnet Americas](https://www.avnet.com/americas/)

[NASDAQ Data](https://finance.yahoo.com/quote/%5EIXIC)
