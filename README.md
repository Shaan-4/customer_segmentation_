# Customer Segmentation Project

## Overview

This project applies **unsupervised machine learning** to segment a customer base of **2,240 individuals** using **K-Means clustering**.
The objective is to identify distinct customer personas based on **income and spending behavior**, enabling targeted and data-driven marketing strategies.

---

## Dataset

* **Name:** Customer Personality Analysis
* **Size:** 2,240 customers
* **Key Features:**

  * Income
  * Year of Birth
  * Spending across multiple product categories (Wines, Fruits, Meat, etc.)


---

## Methodology

### 1. Data Cleaning

* Handled missing values in the 'Income` column using **median imputation**
* Removed non-informative features:

  * `ID`
  * `Z_CostContact`
  * `Z_Revenue`

### 2. Feature Engineering

* Derived **Age** from `Year_Birth`
* Created **Total_Spending** by aggregating spending across all product categories

### 3. Data Transformation

* Applied **StandardScaler** to normalize numerical features
* Scaling was necessary since **K-Means is a distance-based algorithm**

### 4. Model Selection

* Used the **Elbow Method** to determine the optimal number of clusters
* Selected **K = 4** based on the Within-Cluster Sum of Squares (WCSS)

---

## Customer Segments Identified

### Cluster 0 — *VIPs*

* **Profile:** High income, high spending
* **Strategy:** Loyalty programs, premium products, exclusive offers

### Cluster 1 — *Budget-Conscious*

* **Profile:** Low income, low spending
* **Strategy:** Discounts and value-for-money promotions

### Cluster 2 — *Aspirants*

* **Profile:** Low-to-mid income, high spending
* **Strategy:** Trend-based campaigns, influencer marketing

### Cluster 3 — *Steady Base*

* **Profile:** Mid-to-high income, moderate spending
* **Strategy:** Consistent engagement via newsletters and offers

---

## Technologies Used

* **Python 3.11**
* **Pandas**, **NumPy**
* **Matplotlib**, **Seaborn**
* **Scikit-learn** (KMeans, StandardScaler)

---

## How to Run

```bash
pip install -r requirements.txt
```

Then open the notebook:

```
Customer_Segmentation_Analysis.ipynb
```

---

## Key Takeaways

* Feature scaling is critical for clustering algorithms
* Income and total spending strongly influence customer segmentation
* Unsupervised learning can generate actionable business insights
