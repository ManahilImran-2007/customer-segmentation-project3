# Customer Segmentation — Unsupervised Learning

## Overview
This project segments 200 mall customers into distinct groups using unsupervised
learning, based on Age, Annual Income, and Spending Score. No labels were provided —
the goal was to discover natural groupings and translate them into actionable
business personas.

## Method
1. **Standardization** — scaled all features (mean 0, std 1) using StandardScaler
   so no single feature dominates distance calculations.
2. **PCA** — reduced features to 2 principal components (77.6% variance retained)
   for visualization.
3. **K selection** — used the Elbow Method and Silhouette Score to mathematically
   justify K=6 (highest silhouette score: 0.428).
4. **K-Means clustering** — fit final model with K=6.
5. **Persona translation** — mapped cluster centroids back to real-world units
   and defined a business persona per cluster.

## Results

| Cluster | Persona | Age | Income | Spend Score | Action |
|---|---|---|---|---|---|
| 0 | Mature Steady Spenders | 56.3 | $54.3k | 49.1 | Loyalty programs |
| 1 | Young Average Shoppers | 26.8 | $57.1k | 48.1 | General promotions |
| 2 | Affluent Conservatives | 41.9 | $88.9k | 17.0 | High-touch outreach |
| 3 | High-Value Trendsetters | 32.7 | $86.5k | 82.1 | Premium/early access perks |
| 4 | Budget-Conscious Explorers | 25.0 | $25.3k | 77.6 | Flash sales, BNPL |
| 5 | Conservative Minimizers | 45.5 | $26.3k | 19.4 | Price-value messaging |

## Dataset
Mall Customer Segmentation Data (200 records) — Kaggle.

## Tools
Python, pandas, scikit-learn (StandardScaler, PCA, KMeans, silhouette_score), matplotlib
