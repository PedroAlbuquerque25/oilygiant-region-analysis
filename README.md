# 🛢️ Oil Well Profit Optimization using Machine Learning

Identifying the most profitable region for oil well development using Linear Regression and risk analysis with Bootstrapping.

---

## 📌 Project Overview

You work for the mining company **OilyGiant**, tasked with selecting the best region to develop new oil wells. 

Using geological data from three regions, this project builds a predictive model to estimate oil reserves and evaluates **profitability and financial risk** to support strategic investment decisions.

---

## 🎯 Business Objective

The goal is to determine **which region offers the highest expected profit with acceptable risk** when developing 200 new oil wells.

Key decisions include:
- Predicting oil reserves in new wells
- Selecting the most productive drilling locations
- Estimating total profit potential
- Assessing financial risk using bootstrapping

---

## 🗂️ Dataset Description

Geological exploration data from three regions:
- `geo_data_0.csv`
- `geo_data_1.csv`
- `geo_data_2.csv`

### Features:
- **id** — unique well identifier
- **f0, f1, f2** — geological characteristics
- **product** — oil reserves volume (thousand barrels)

---

## ⚙️ Project Constraints

- Only **Linear Regression** was used for modeling
- 500 wells explored per region
- Top 200 wells selected for development
- Development budget: **$100 million**
- Revenue per unit (thousand barrels): **$4,500**
- Maximum acceptable risk of loss: **2.5%**

---

## 🧠 Methodology

### 🔹 1. Data Preparation
- Loaded and inspected geological datasets
- Verified distributions and summary statistics
- Checked data consistency

### 🔹 2. Model Training & Validation
- Train/validation split: **75 / 25**
- Model: **Linear Regression**
- Metrics: RMSE and Mean predicted reserves

### 🔹 3. Profit Calculation
- Selected 200 wells with highest predicted reserves
- Calculated revenue and net profit
- Compared with break-even production threshold (**~111.1 units**)

### 🔹 4. Risk Analysis (Bootstrapping)
- 1000 bootstrap simulations per region
- Sample 500 wells per iteration
- Computed: Average profit, 95% Confidence Interval, and Probability of loss.

---

## 📊 Model Performance

| Region | Avg Predicted Reserves | RMSE |
|--------|------------------------|------|
| 0      | 92.40                  | 37.76|
| 1      | 68.71                  | **0.89** |
| 2      | 94.77                  | 40.15|

*Region 1 achieved extremely low prediction error due to stronger linear relationships in the data.*

---

## 💰 Estimated Profit (Top 200 Wells)

| Region | Estimated Profit | Avg Volume |
|--------|-----------------|-----------|
| 0      | $33.6M          | 148.43    |
| 1      | $24.1M          | 137.95    |
| 2      | $26.0M          | 139.98    |

---

## 📉 Risk & Profit Analysis (Bootstrap)

| Region | Avg Profit | 95% Confidence Interval | Risk of Loss |
|--------|-----------|------------------------|-------------|
| 0      | $4.07M    | -$0.96M to $9.26M      | 5.20%       |
| **1** | **$4.49M**| **$0.52M to $8.41M** | **1.70%** |
| 2      | $3.84M    | -$1.35M to $9.04M      | 7.20%       |

---

## ✅ Final Recommendation

**Region 1** is the optimal choice for development.

### ✔ Why?
- **Highest average profit** in simulation ($4.49M).
- **Lowest financial risk** (1.70%), well below the 2.5% limit.
- **Positive confidence interval**: Even in the lower bound (2.5% quantile), the project remains profitable.

---

## 🛠️ Tech Stack

- **Python** (Pandas, NumPy, Scikit-learn, SciPy)
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

---

## 📂 Project Structure
```text
├── datasets/     # CSV files with geological data
├── notebook/     # Jupyter Notebook with full analysis
├── .gitignore    # Files excluded from Git
├── environment.yml    # Conda environment configuration
└── README.md # Project documentation
```

---

## ▶️ How to Run

# Clone the repository
git clone [https://github.com/PedroAlbuquerque25/oilygiant-region-analysis.git](https://github.com/PedroAlbuquerque25/oilygiant-region-analysis.git)

# Navigate to the folder
cd oilygiant-region-analysis

# Create and activate environment
conda env create -f environment.yml
conda activate oilygiant-env

# Run Jupyter
jupyter notebook

---

## 👤 Author
Pedro Albuquerque

## 🤝 Contato
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/phaa/)