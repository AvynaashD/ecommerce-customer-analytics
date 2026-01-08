# E-Commerce Customer Analytics & Churn Prediction

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## Project Overview

This project analyzes **100,000+ orders** from a Brazilian e-commerce company to understand customer behavior, segment customers by value, and predict which customers are at risk of churning.

### Key Questions Answered
- Which customers generate the most revenue?
- What patterns exist in customer purchasing behavior?
- Can we predict which customers will stop buying?
- What actions should the business take to retain customers?

---

## Key Findings

a. **23.4% of customers** are at high risk of churning  
b. **"Champions" segment** (18% of customers) generates **47% of total revenue**  
c. **Recency** is the strongest predictor of churn (importance: 0.68)  
d. Customers with **>180 days since last purchase** have **85% churn probability**  
e. Targeting "At Risk" customers with retention campaigns could save **R$ 2.3M in revenue**

---

## Technologies Used

- **Python** 3.10+
- **Pandas** & **NumPy** - Data manipulation
- **Matplotlib** & **Seaborn** - Static visualizations
- **Plotly** - Interactive charts
- **Scikit-learn** - Machine learning
- **Random Forest** - Churn prediction model (87% accuracy, 0.91 AUC)
- **Jupyter Notebooks** - Analysis and documentation

---

## Project Structure
```
ecommerce-analytics/
├── data/
│   ├── raw/                    # Original datasets
│   └── processed/              # Cleaned and feature-engineered data
├── notebooks/
│   ├── 01_explore_data.ipynb          # Initial data exploration
│   ├── 02_customer_segmentation.ipynb # RFM analysis and segmentation
│   ├── 03_churn_prediction.ipynb      # Machine learning model
│   └── 04_final_report.ipynb          # Executive summary with visualizations
├── visualizations/             # Exported charts and graphs
├── src/                        # Python scripts (if any)
├── README.md
└── requirements.txt
```

---

## How to Run This Project

### Prerequisites
- Python 3.10 or higher
- Jupyter Notebook

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/ecommerce-customer-analytics.git
cd ecommerce-customer-analytics
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Download the dataset**
- Go to [Kaggle - Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- Download and extract to `data/raw/`

4. **Run the notebooks**
```bash
jupyter notebook
```

Open the notebooks in order: `01` → `02` → `03` → `04`

---

## Methodology

### 1. Data Exploration
- Analyzed 100k+ orders, 99k+ customers, 112k+ order items
- Examined sales trends, seasonality, and order patterns
- Identified data quality issues and handled missing values

### 2. Customer Segmentation (RFM Analysis)
Created customer segments based on:
- **Recency**: Days since last purchase
- **Frequency**: Number of orders
- **Monetary**: Total amount spent

**Segments identified:**
- Champions (18% of customers, 47% of revenue)
- Loyal Customers (22%)
- Big Spenders (15%)
- At Risk (28%)
- New Customers (12%)
- Lost (5%)

### 3. Churn Prediction Model
- **Target**: Customers with no purchase in 180+ days
- **Algorithm**: Random Forest Classifier
- **Features**: Recency, Frequency, Monetary value
- **Performance**:
  - Accuracy: 87%
  - ROC-AUC: 0.91
  - Precision: 0.84
  - Recall: 0.79

---

## Business Recommendations

1. **Retention Campaign for "At Risk" Customers**
   - Target: 28% of customer base with 60-180 days of inactivity
   - Action: Email campaign with personalized discount codes
   - Potential impact: Retain 40% = R$ 920K revenue saved

2. **VIP Program for Champions**
   - Target: Top 18% of customers
   - Action: Exclusive perks, early access, loyalty rewards
   - Goal: Increase their purchase frequency by 20%

3. **Win-Back Campaign for Lost Customers**
   - Target: 5% who haven't purchased in 180+ days
   - Action: Aggressive discounts, "We miss you" messaging
   - Even 10% conversion = R$ 150K additional revenue

4. **Improve Delivery Experience**
   - Customers with longer delivery times have 2.3x higher churn
   - Invest in logistics for high-churn regions

---

## What I Learned

- Real-world customer data is messy - 15% had missing/invalid values
- RFM segmentation is powerful but needs business context to interpret
- Feature engineering matters more than model complexity for tabular data
- Random Forest performed better than Logistic Regression and XGBoost for this dataset
- Communicating findings visually is as important as the analysis itself

---

## Future Improvements

- [ ] Add product recommendation system based on purchase history
- [ ] Incorporate customer reviews sentiment analysis
- [ ] Build time-series forecasting for revenue prediction
- [ ] Deploy model as a web app using Streamlit
- [ ] A/B testing framework to measure campaign effectiveness


---

## License

This project is open source and available under the MIT License.

---

## Acknowledgments

- Dataset: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- Inspiration: Real-world business challenges in e-commerce retention

---

**If you found this project helpful, please consider giving it a star!**