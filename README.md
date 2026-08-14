# Customer Segmentation for E-Commerce

Customer analytics project for segmenting online-retail users into behaviorally meaningful groups using **RFM analysis, K-means clustering, and PCA**.

The project explores how transaction history can be transformed into customer-level features and used to identify segments that support retention, targeting, and customer-lifetime-value analysis.

## Problem

Raw e-commerce transaction data is difficult to use directly for customer strategy. The goal of this project is to convert purchase history into interpretable customer features and group users according to purchasing behavior.

## Analysis Workflow

```text
Retail Transactions
        ↓
Data Cleaning
        ↓
Customer-Level Aggregation
        ↓
RFM Features
Recency · Frequency · Monetary Value
        ↓
Feature Scaling
        ↓
K-Means Clustering
        ↓
PCA for Visualization
        ↓
Customer Segments
        ↓
CLV / Business Interpretation
```

## Methods

### RFM analysis

Customer behavior is represented through:

- **Recency** — how recently a customer purchased
- **Frequency** — how often they purchase
- **Monetary value** — how much they spend

These features provide a compact representation of purchasing behavior for downstream clustering.

### K-means clustering

K-means is used to partition customers into groups with similar transaction characteristics, enabling a data-driven alternative to manually defined customer tiers.

### PCA

Principal Component Analysis is used to reduce the dimensionality of the customer feature space and make cluster structure easier to visualize and interpret.

### Customer lifetime value context

The analysis connects behavioral segmentation with customer-value metrics so that clusters can be interpreted in commercially meaningful terms rather than as purely mathematical groups.

## Tech Stack

- Python
- Pandas / NumPy
- scikit-learn
- K-means clustering
- PCA
- RFM analysis
- Jupyter Notebook

## Repository Structure

```text
Customer-segmentation/
├── Customer_segmentation_online_retail.ipynb
├── data.csv.zip
└── README.md
```

## Running the Analysis

```bash
git clone https://github.com/paluuuk/Customer-segmentation.git
cd Customer-segmentation
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook
```

Open `Customer_segmentation_online_retail.ipynb` and run the analysis after extracting the included dataset archive.

## Current Status

This repository is a notebook-based exploratory data-science project. It is best viewed as supporting evidence of clustering, dimensionality reduction, customer analytics, and feature-engineering experience rather than as a production ML system.

Potential improvements include separating feature engineering from exploration, adding automated data validation, documenting cluster-selection criteria, reporting cluster stability, and moving the raw dataset outside the Git repository.