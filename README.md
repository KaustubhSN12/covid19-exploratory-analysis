# 🦠 COVID-19 Data Analysis Report

This project analyzes the global spread and impact of COVID-19 using real-world data and Python libraries such as Pandas, Plotly, and Scikit-learn. The goal is to uncover patterns and provide insights using visualizations and machine learning.

---

## 📈 Total COVID-19 Cases Over Time

![Time Series and Heatmap](b73f5fa7-045b-40b5-acdd-430e5b3ecab2.png)

### 🔍 Key Insights:
- **Periodic spikes** in reported cases indicate reporting lags or episodic outbreaks.
- The **7-day moving average** reveals a clearer, smoother trend.
- Overall trajectory shows **rising cumulative cases** globally throughout 2020.

---

## 🌡️ Correlation Heatmap of Key Indicators

- Shows relationships between `total_cases`, `total_deaths`, `gdp_per_capita`, and `human_development_index`.

### 🔍 Key Insights:
- `total_cases` and `total_deaths` have a **strong correlation (0.91)**.
- **No strong correlation** between economic indicators and case/death counts.
- `human_development_index` has a **moderate correlation** with reported cases.

---

## 🤖 KMeans Clustering of Continents by COVID Metrics

![Clustering Output](6f73413d-2acc-4679-bec9-1bc09e541e85.png)

We grouped continents using KMeans clustering on:
- `total_cases`
- `total_deaths`
- `gdp_per_capita`
- `human_development_index`

### 🔍 Cluster Analysis:
- **Cluster 0 (Blue):** Moderate impact regions.
- **Cluster 1 (Magenta):** High GDP, lower case/death count.
- **Cluster 2 (Yellow):** High impact areas, very high case and death counts.

---

## 🧠 Tools Used
- **Python 3**, **Pandas**, **Plotly**, **Seaborn**, **Scikit-learn**
- **Jupyter Notebook**, **Google Colab**

---

## ✅ Next Steps
- Time series forecasting (ARIMA/Prophet)
- Mapping with Folium or Choropleth
- Adding vaccination data
- Streamlit dashboard for real-time interaction

---

## 📄 Data Source
- [Our World in Data – COVID Dataset](https://github.com/SR1608/Datasets/blob/main/covid-data.csv)

---

*Crafted with ❤️ by [Your Name] as part of Vaishnav Technologies Internship.*
