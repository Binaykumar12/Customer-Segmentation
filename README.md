# Customer Segmentation Analysis

## Project objective
Segment customers using purchasing behavior and demographics. The project uses RFM features (Recency, Frequency, Monetary) and K-Means clustering in Python, then presents segment profiles in Power BI.

> **Dataset note:** The included data is synthetic and generated for learning and portfolio practice. It does not represent real customers or a real company.

## Dataset
- `Dataset/customer_demographics.csv`: one row per customer, with age, gender, city, region, signup date, and membership tier.
- `Dataset/transactions.csv`: one row per order, with order date, product category, quantity, unit price, discount, amount, payment method, and sales channel.

The files are joined using `Customer_ID`.

## Planned workflow
1. Load and inspect both CSV files.
2. Clean data types, missing values, duplicates, and invalid values.
3. Aggregate transactions into customer-level RFM metrics.
4. Scale suitable numerical features.
5. Select a cluster count using the elbow method and silhouette score.
6. Fit K-Means and profile the resulting clusters.
7. Export customer segment assignments and summary tables.
8. Build an interactive Power BI report.
9. Document business insights and segment-specific recommendations.

## Tools
- Python, pandas, NumPy
- scikit-learn
- Matplotlib / Seaborn
- Power BI Desktop

## Repository structure (target)
```text
Customer-Segmentation/
├── Dataset/
│   ├── customer_demographics.csv
│   └── transactions.csv
├── Notebooks/
│   └── customer_segmentation.ipynb
├── Outputs/
│   ├── customer_segments.csv
│   └── segment_summary.csv
├── PowerBI/
│   └── Customer_Segmentation_Dashboard.pbix
├── Screenshots/
│   └── dashboard_overview.png
├── requirements.txt
└── README.md
```

## How to reproduce
1. Install the packages listed in `requirements.txt`.
2. Open the notebook in `Notebooks/`.
3. Run cells from top to bottom.
4. Import the generated output CSV files into Power BI.

## Business questions
- Which customer groups generate the highest revenue?
- Which segments purchase most frequently?
- Which customers have not purchased recently?
- How do customer age, region, and membership tier vary by segment?
- What marketing action should be taken for each segment?

## Important
Do not treat cluster numbers (0, 1, 2, ...) as meaningful labels by themselves. Interpret clusters only after reviewing their RFM and demographic profiles.
