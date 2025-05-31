
---

# 🦠 COVID-19 Data Analysis using Python (Google Colab)

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Colab](https://img.shields.io/badge/Platform-Google%20Colab-yellow?logo=googlecolab&logoColor=black)
![Pandas](https://img.shields.io/badge/Library-pandas-lightblue)
![Seaborn](https://img.shields.io/badge/Visualization-seaborn-orange)
![Matplotlib](https://img.shields.io/badge/Visualization-matplotlib-green)

---

## 📌 Project Overview

This project focuses on **data analysis and visualization of COVID-19 data** using **Python** in **Google Colab**. It demonstrates proficiency in data cleaning, transformation, exploratory data analysis, feature engineering, and deriving meaningful insights using **pandas, seaborn, and matplotlib**.

The dataset was sourced from [this public URL](https://raw.githubusercontent.com/SR1608/Datasets/main/covid-data.csv).

---

## 🧠 Objectives

- Perform high-level and low-level exploratory data analysis
- Clean and transform raw data
- Create new features for better insight extraction
- Visualize patterns in the spread of COVID-19 across continents
- Derive insights on key indicators like GDP per capita, HDI, and mortality ratios

---

## 🔧 Technologies Used

- Python 🐍
- Google Colab 📒
- Pandas 🧾
- Matplotlib 📊
- Seaborn 📈

---

## 📂 Project Steps

### 1. 📥 Data Import and Exploration
- Loaded data directly from URL using pandas
- Checked shape, types, null values, and statistical summary

### 2. 🔍 High-Level Analysis
- **Rows & Columns**: 1,213,879 entries, 45 features
- **Data types** and distributions were evaluated using `describe()` and `info()`

### 3. 🧬 Low-Level Understanding
- 216 unique locations
- **Europe** has the highest data representation
- Max total cases: `55,154,651`
- Avg total cases: `167,797`
- **HDI highest** in Europe
- **Lowest GDP per capita** in Africa

### 4. 🧹 Data Cleaning
- Filtered to key columns: `['continent', 'location', 'date', 'total_cases', 'total_deaths', 'gdp_per_capita', 'human_development_index']`
- Removed duplicates
- Handled missing values (filled with `0`, removed rows with missing continent)
- Converted date to datetime and extracted month

### 5. 🔎 Data Aggregation & Feature Engineering
- Grouped data by `continent`
- Created a new feature: `total_deaths_to_total_cases`

---

## 📊 Data Visualizations & Insights

### 📌 1. GDP per Capita - Distribution
```python
sns.histplot(df['gdp_per_capita'], kde=True)


📝 **Insight**: Most countries have a GDP per capita below 20,000. A few wealthy outliers heavily influence the distribution.

---

### 📌 2. Total Cases vs GDP per Capita

```python
sns.scatterplot(x='total_cases', y='gdp_per_capita', data=df)
```

📝 **Insight**:
The distribution is heavily right-skewed.

- Most countries have a low GDP per capita, while a few countries have significantly higher values (outliers).

- This suggests global inequality in wealth distribution, relevant when analyzing health system capacities and COVID-19 responses.


---

### 📌 3. Pairplot of Aggregated Data

```python
sns.pairplot(df_groupby)
```

📝 **Insight**: 
Helps visually analyze correlations between variables like total_cases, total_deaths, gdp_per_capita, human_development_index, etc.

- No strong linear relationships were observed.

- Distributions (diagonal) show:

 - Skewed GDP per capita (a few rich nations)

 - Death-to-case ratios are consistently low across continents.

 - Helps in identifying clusters or outliers.


---

### 📌 4. Total Cases by Continent

```python
sns.catplot(x='continent', y='total_cases', data=df_groupby, kind='bar')
```

🔍 **Insight**:
North America and Asia recorded the highest total COVID-19 cases.

- Africa and Oceania had the lowest numbers, indicating either fewer outbreaks or possibly limited testing/reporting.

- The plot shows a clear regional variation in total case counts.
---

## 📈 Outcome Summary

| Metric                  | Insight                                                         |
| ----------------------- | ---------------------------------------------------------------- |
| Highest Cases           | **North America** (~11M+ based on bar plot)                     |
| Avg Cases per Country   | ~167k                                                           |
| Quartiles (Deaths)      | Q1: 13, Q2: 84, Q3: 727                                         |
| HDI Leader              | Europe                                                          |
| Lowest GDP per Capita   | Africa                                                          |
| Mortality Ratio Insight | Death-to-case ratio is mostly low (under ~3%) across continents |

---

## 📊 Visual Insights

### 🔹 Total COVID-19 Cases by Continent

![Total Cases by Continent](images/barplot_cases_by_continent.png)

> **Insight**: North America leads with the highest number of reported total cases, followed by Asia. Oceania and Africa recorded the fewest.

---

### 🔹 GDP per Capita Distribution

![GDP per Capita](images/gdp_per_capita_distribution.png)

> **Insight**: Strong right-skewed distribution. Most countries fall under lower GDP ranges, with few outliers having very high GDP per capita.

---

### 🔹 Pairplot of Key Indicators (Grouped by Continent)

![Pairplot](images/pairplot_grouped_by_continent.png)

> **Insight**: Multi-variable comparison reveals no obvious linear relationship but helps detect patterns and outliers among continents.

---

## 🧹 Key Steps Covered

- Data Loading and Exploration
- High-level and Low-level EDA
- Data Cleaning & Null Handling
- Feature Engineering: `total_deaths_to_total_cases`
- Time Conversion: Month extraction from dates
- Aggregation by Continent
- Visual Storytelling using Matplotlib & Seaborn

---


## 💡 Key Learnings

* Practical use of **EDA**, **feature engineering**, and **data visualization**
* Hands-on experience with **data wrangling**
* Learned how economic and human development indicators relate to pandemic impact

---

## 📁 Project Link & Notebook

🔗 [View on Google Colab](#) ([Click here:](https://colab.research.google.com/drive/1MVQOdowUcyk-GWv-im6imuh6US_yvlsv?usp=sharing))
📎 \[PDF TASK]\(Attach PDF if needed)

---

## 📬 Contact & Connect

🔗 [LinkedIn](https://www.linkedin.com/in/kaustubh-narayankar-6651a9249/)
📧 Email: *k.narayankar3030@gmail.com*
📌 GitHub: [KaustubhSN12](https://github.com/KaustubhSN12)

---

## ⭐️ Give it a star if you found this project helpful or interesting!

```

