# 🛒 E-Commerce Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Manipulation-orange.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Data%20Visualization-green.svg)

## 📌 Project Overview
This project aims to conduct **Exploratory Data Analysis (EDA)** and **Feature Engineering** on an e-commerce dataset using Python. This analysis is designed to understand sales patterns, identify key revenue drivers, and analyze monthly and daily transaction trends to provide data-driven business recommendations.

---

## 🎯 Objectives & Requirements
- **Data Understanding & Cleaning**: Identify data types, detect missing values, and handle duplicate data.
- **Feature Engineering**: Create new variables such as date components (`year`, `month`, `day_name`) and `total_price` ($\text{Quantity} \times \text{UnitPrice}$).
- **Multivariate Analysis**: Analyze correlations between numerical variables using a *Correlation Heatmap*.
- **Exploratory Data Analysis**: Answer business questions using data manipulation techniques (`groupby`, `aggregation`, `datetime` manipulation) and intuitive data visualizations.

---

## 📊 Key Insights & Findings

### 1. Correlation Analysis (Multivariate)
- **Quantity & Total Price ($r \approx 0.79$)**: Displays a very strong positive correlation. Item volume is the main factor driving the company's total revenue.
- **UnitPrice & Total Price ($r \approx 0.09$)**: Displays a very weak correlation, indicating that sales are dominated by high-volume standard-margin products rather than expensive items.

### 2. Monthly Revenue Trend
- **Low Season**: Sales tend to be stable and stagnant from January to April.
- **Growth & Peak Season**: Sales begin to rise mid-year and experience exponential growth in Quarter 4, with peak sales (**Peak Season**) occurring in **November and December**.

### 3. Daily Transaction Pattern
- Transactions are most active on **weekdays**, with the highest peak in unique transactions recorded on **Thursday**.

---

## 💡 Business Recommendations
1. **Inventory & Logistics Management**: Ahead of Q4, top-selling inventory and shipping capacity should be prepared starting in September to prevent stockouts during the year-end surge.
2. **Promotional Strategy**: Create targeted marketing campaigns or loyalty programs during the low season (January–April) to maintain steady revenue flow.

---

## 🛠️ Tools & Libraries Used
- **Environment**: Google Colaboratory / Jupyter Notebook
- **Language**: Python 3.x
- **Libraries**:
  - `pandas` - Data Manipulation & Aggregation
  - `numpy` - Numerical Computations
  - `matplotlib` & `seaborn` - Data Visualization

---

## 📂 Repository Structure
```text
├── dataset/
│   └── ecommerce.csv       # Raw Dataset
├── notebook/
│   └── EDA_Ecommerce.ipynb # Google Colab Notebook
└── README.md               # Project Documentation
```
---

## 🚀 Cara Menjalankan
Anda dapat menjalankan kode ini dengan dua cara:

### 1. Google Colab
*    Klik file .ipynb yang ada di repositori ini atau link berikut https://colab.research.google.com/drive/18RyKawKNKPYh7VxFXFcW_GBNygRV8TUx?usp=sharing.
*    Klik tombol "Open in Colab" jika tersedia, atau unggah file tersebut ke Google Colab.

### 2. Lokal
*    Pastikan Anda telah menginstal Python.
*    Instal Jupyter Notebook dengan perintah: pip install notebook.
*    Buka terminal, arahkan ke direktori file, dan jalankan perintah: jupyter notebook.
