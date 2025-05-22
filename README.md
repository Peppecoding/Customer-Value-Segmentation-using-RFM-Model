# 🎯 Customer Segmentation Using RFM Analysis

This project applies the RFM (Recency, Frequency, Monetary) model to segment e-commerce customers based on their purchasing behavior. The goal is to identify the most valuable, at-risk, and inactive clients to support better marketing and retention strategies.

---

## 🧠 What is RFM?

RFM is a behavioral segmentation model based on:

- **Recency** – How recently a customer made a purchase
- **Frequency** – How often they purchase
- **Monetary** – How much they spend

---

## 🔧 Tools & Tech Stack

- **Python + Pandas** (in Google Colab) for data preparation  
- **Looker Studio** for interactive visual dashboard  
- Dataset: `Online Retail.xlsx` (public Kaggle dataset)  
- Visualizations: Pie chart, bar charts, combo chart, pivot heatmap, filters  

---

## ⚙️ Data Cleaning and RFM Scoring (Python)

**Notebook:** [`rfm_analysis.ipynb`](link-to-your-colab-if-public)

Steps:

1. Loaded and cleaned the dataset using `pandas`
2. Removed missing `CustomerID` rows
3. Calculated `TotalPrice = Quantity * UnitPrice`
4. Defined snapshot date for Recency calculation
5. Grouped by `CustomerID` to compute:
   - `Recency` (days since last purchase)
   - `Frequency` (total number of purchases)
   - `Monetary` (total spend)
6. Scored each metric from 1–5 using `pd.qcut()`
7. Created a full `RFM_Score` (e.g., 555)
8. Segmented customers into:
   - Champion, Loyal, At Risk, Lost, Need Attention, Potential Loyalist, Others
9. Exported final dataset as `rfm_segmented.csv`

---

## 📊 Interactive Dashboard (Looker Studio)

**Live Report:** [👉 View the Dashboard](link-to-your-looker-studio)

### 💡 Visuals Included:

| Chart Type            | Description                                              |
|-----------------------|----------------------------------------------------------|
| 🎯 Pie Chart          | Customer distribution by segment                         |
| 📉 Bar Chart          | Avg Recency by segment                                   |
| 📈 Bar Chart          | Avg Frequency by segment                                 |
| 💰 Combo Chart        | Avg Monetary (bars) vs Frequency (line) by segment       |
| 🧊 Pivot Heatmap      | Customer count by R_Score vs F_Score                     |
| 📋 Table View         | Customer-level details with segment filter               |

---

## 🔍 Key Insights

- **Champions** spend the most and buy most frequently.
- **Loyal** customers show strong frequency but lower spend.
- **At Risk / Lost** customers show high recency and low frequency.
- **Need Attention** & **Potential Loyalists** represent great re-engagement opportunities.
- The **R vs F heatmap** clearly highlights clusters of high-value and disengaged users.

---

## 🧑‍💼 Business Application

This dashboard can help any e-commerce or subscription business:
- Optimize marketing campaigns by targeting segments
- Focus retention on high-value or slipping customers
- Discover patterns of inactivity and act early

---

## ✨ Author

**Giuseppe Mendoza Noto**  
Data Analyst | Fitness Enthusiast | Creative Technologist  
Made with ❤️ using Python & Looker Studio

