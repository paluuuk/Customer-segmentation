# E-Commerce Customer Segmentation

An exploratory retail-analytics notebook that builds product and customer segments from transaction history, then compares classifiers for assigning customers to those segments.

## What the notebook implements

1. Clean missing customer records, cancelled orders, and transaction adjustments.
2. Build product-description features with NLTK tokenization, noun selection, stemming, and price-band indicators.
3. Cluster products into five groups with K-means and inspect silhouette scores and PCA projections.
4. Aggregate customer basket statistics and spending shares across those product groups.
5. Scale the customer features, build eleven customer clusters, and inspect their separation.
6. Compare supervised segment classifiers, including SVM and Random Forest, and inspect a later transaction period.

The customer clustering uses basket counts, minimum/maximum/mean basket value, and product-category spending shares. Purchase-recency fields are also derived, but this is not simply a three-feature RFM model or a deployed lifetime-value predictor.

## Start here

- [Analysis notebook](Customer_segmentation_online_retail.ipynb)
- [Dependency list](requirements.txt)
- `data.csv.zip`: transaction archive used by the original analysis

```bash
git clone https://github.com/paluuuk/Customer-segmentation.git
cd Customer-segmentation
python -m venv .venv
# Activate .venv using the command for your shell.
python -m pip install -r requirements.txt
jupyter notebook Customer_segmentation_online_retail.ipynb
```

Extract the archive so the notebook can read `input_data/data.csv`. It uses ISO-8859-1 encoding. NLTK tokenization and tagging resources may need downloading in the local environment.

## Reproducibility and interpretation

This is a historical exploratory notebook. It contains legacy pandas calls such as `DataFrame.append` and `as_matrix`, so a current environment may need compatibility edits before an end-to-end rerun. The dependency list records imported packages; it is not a locked environment.

Cluster IDs are analytical groupings, not ground-truth business outcomes. A classifier learning those IDs does not independently validate the segments or prove future customer value. No new benchmark or production deployment is claimed.

**Stack:** Python, pandas, NumPy, NLTK, scikit-learn, K-means, PCA, Matplotlib, seaborn, wordcloud.
