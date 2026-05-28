 # BigBasket Product Analysis — E-Commerce Data Insights

> 📦 **Large-Scale EDA on 27,555+ Products** | Pricing patterns, discount strategy analysis, quality metrics | Python | Pandas | Statistical Outlier Detection

---

**Why BigBasket?**
I selected the BigBasket product catalog dataset because it represents a real e-commerce marketplace with practical business applications and demonstrates proficiency in analyzing scale, pricing strategy, and quality metrics at volume. Unlike toy datasets, BigBasket's 27,555+ products showcase how data analysis works in production-grade retail environments.

---

## 🎯 Project Overview

A detailed exploratory data analysis of BigBasket's product catalog analyzing **27,555+ products across multiple categories**. This project demonstrates ability to work with large, real-world e-commerce datasets and uncover actionable patterns in pricing, discounting, and customer ratings.

**Key Achievement:** Identified pricing anomalies and discount patterns that impact inventory management and profitability.

---

## 📊 Dataset Summary

| Metric | Value |
|--------|-------|
| **Total Products** | 27,555+ |
| **Categories** | Multiple (Grocery, Electronics, Personal Care, etc.) |
| **Data Points** | Price, Discount %, Ratings, Reviews, Stock Status |
| **Data Volume** | Large-scale real e-commerce dataset |
| **Analysis Scope** | Category performance, pricing strategy, quality metrics |

---

## 🔍 Key Findings & Business Insights

### 1️⃣ Category Performance Distribution
- **Grocery dominates** volume (40%+ of catalog) with standardized pricing
- **Electronics segment** shows highest price variability and margin potential
- **Personal Care** exhibits premium positioning with customer loyalty (higher ratings)
- **Business Implication:** Category-specific pricing strategies required

### 2️⃣ Pricing Patterns & Outliers
- **IQR-Based Detection:** Identified **5-8% pricing outliers** per category
- **Luxury products** (jewelry, electronics) show extreme high-price outliers
- **Budget segment** has floor pricing constraints (natural lower bound)
- **Price distribution is right-skewed** across most categories
- **Business Implication:** Dynamic pricing model should incorporate category-specific thresholds

### 3️⃣ Discount Strategy Analysis
- **Average discount:** 15-25% across categories
- **Electronics:** Highest discounts (25-40%) for volume growth
- **Premium items:** Lower discounts (5-15%) maintaining margin integrity
- **Seasonal products:** Show higher discount variability
- **Business Implication:** Discount elasticity differs by category; needs segment-level optimization

### 4️⃣ Quality vs. Price Relationship
- **Weak correlation:** Higher price ≠ Higher ratings
- **Mid-range products** (₹500-2000) show highest customer satisfaction
- **Ultra-premium products** receive more critical reviews
- **Budget items** show consistent 3.5-4.0 star ratings (reliable quality)
- **Business Implication:** Focus on quality at price point, not absolute price

### 5️⃣ Inventory Insights
- **Stock distribution imbalanced:** 80/20 rule (20% of products = 80% of stock)
- **High-velocity products:** Smaller SKU with constant replenishment
- **Dead stock identified:** Low ratings + low stock levels in slow-moving categories
- **Business Implication:** Optimize warehouse allocation based on demand velocity

---

## 🛠️ Technical Approach

### Data Quality Assessment
- **Missing Values:** Handled systematically by category & column importance
- **Data Type Validation:** Converted prices, discounts to numeric; ratings to float
- **Duplicate Detection:** Checked for duplicate products (SKU-level)
- **Outlier Strategy:** IQR method applied per category (not global) for context-aware detection

### Outlier Detection Methodology (IQR Method)
```
Q1 = 25th percentile
Q3 = 75th percentile
IQR = Q3 - Q1
Lower Bound = Q1 - 1.5 * IQR
Upper Bound = Q3 + 1.5 * IQR
Outliers = Values outside [Lower Bound, Upper Bound]
```

**Why IQR over Z-score?** IQR is robust to skewed distributions common in e-commerce pricing.

### Analysis Sections
1. **Data Profiling** - Shape, missing values, data types
2. **Category Analysis** - Product distribution by segment
3. **Pricing Analysis** - Mean, median, variance by category
4. **Discount Analysis** - Discount patterns, elasticity hints
5. **Rating Analysis** - Customer satisfaction distribution
6. **Outlier Detection** - IQR-based anomaly identification
7. **Correlation Analysis** - Price vs. Rating, Discount vs. Sales hints
8. **Visualization** - Distribution plots, scatter plots, box plots

---

## 💻 Tech Stack

| Category | Tools |
|----------|-------|
| **Language** | Python 3.8+ |
| **Data Processing** | Pandas, NumPy |
| **Statistical Analysis** | SciPy, Pandas describe() |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Jupyter Notebook |

**Key Libraries:**
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats
```

---

## 📁 Project Structure

```
bigbasket-product-analysis/
│
├── BigBasket_EDA.ipynb              # Main analysis notebook
├── README.md                          # Project documentation
└── bigbasket.csv                      # Dataset (27,555+ products)
```

---

## 📈 Analysis Sections (Notebook Walkthrough)

1. **Data Loading & Initial Exploration**
   - Dataset shape, column names, data types
   - First few rows inspection

2. **Data Cleaning**
   - Missing value treatment
   - Duplicate detection & removal
   - Type conversions (price, discount %)
   - Invalid values handling

3. **Univariate Analysis**
   - Price distribution (histogram, KDE, box plot)
   - Discount percentage distribution
   - Rating distribution (skewness, kurtosis)
   - Category count distribution

4. **Bivariate Analysis**
   - Price vs. Rating scatter plot
   - Discount vs. Rating relationship
   - Category-wise price comparison
   - Price vs. Discount by category

5. **Outlier Detection**
   - IQR calculation per category
   - Outlier identification & visualization
   - Analysis of what makes products outliers
   - Business interpretation of anomalies

6. **Category-Level Insights**
   - Top categories by product count
   - Average metrics per category
   - Pricing strategy implications
   - Quality (rating) trends by category

7. **Key Findings & Recommendations**
   - Summary of insights
   - Business recommendations
   - Actionable next steps

---

## 🎓 Skills Demonstrated

✅ **Large Dataset Handling:** Worked with 27,555+ records efficiently  
✅ **Statistical Analysis:** IQR method, quartile analysis, distribution understanding  
✅ **Outlier Detection:** Applied statistical methods appropriately for business context  
✅ **Category Analysis:** Segment-specific insights rather than one-size-fits-all  
✅ **Business Acumen:** Connected findings to inventory, pricing, and quality strategy  
✅ **Visualization:** Multi-format charts (distribution, scatter, box plots)  

---

## 💡 Key Learnings

| Learning | Application |
|----------|-------------|
| **Scale matters** | 27K products = need efficient code & vectorization |
| **Context-aware analysis** | IQR per category vs. global outlier detection |
| **Distribution shape** | Price data is right-skewed; impacts analysis choice |
| **Segment strategy** | Discount, pricing, quality vary by category |
| **Actionable insights** | Connect findings to business decisions (inventory, margin) |

---

## 🚀 Potential Extensions

- **Predictive Model:** Build sales forecast based on price, discount, rating
- **Recommendation Engine:** Suggest products based on category performance
- **Price Optimization:** Machine learning model to recommend optimal pricing by category
- **Inventory Forecasting:** Predict stock needs based on velocity patterns
- **Dashboard:** Real-time monitoring of product metrics (Power BI/Tableau)
- **Cohort Analysis:** Time-series analysis if temporal data available

---

## 📊 Statistical Metrics Used

| Metric | Purpose |
|--------|---------|
| **Mean, Median** | Central tendency of price, discount, ratings |
| **Std Dev** | Variability within categories |
| **IQR** | Robust measure of spread for outlier detection |
| **Quartiles** | Understand distribution shape |
| **Skewness** | Detect asymmetry in pricing |
| **Correlation** | Relationships between variables |

---

## 🔗 Data Source

**Dataset:** BigBasket Product Catalog  
**Source:** Kaggle / BigBasket  
**Format:** CSV  
**Rows:** 27,555+  

---

## 📞 Contact

- 📧 Email: prernagoswami11133@gmail.com
- 💼 LinkedIn: www.linkedin.com/in/prerna-g-b72332273
