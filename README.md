# Retail & Marketing Analytics

Customer segmentation, retention and lifetime-value analysis on the UCI *Online Retail II* dataset (UK online retailer, Dec 2009 – Dec 2011).

**Tech:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## Pipeline
1. **Cleaning:** removed missing customer IDs, cancelled invoices, returns, zero prices, duplicates and non-product rows (postage, fees)
2. **RFM analysis:** Recency, Frequency, Monetary value + 1–5 scores for every customer
3. **K-Means clustering:** log-transformed and scaled RFM, k chosen with elbow and silhouette plots, 6 named segments
4. **Cohort retention:** monthly cohort heatmap by first-purchase month
5. **Customer Lifetime Value:** AOV × purchase frequency × expected lifetime

## Results
| Metric | Value |
|---|---|
| Clean transactions | 776,609 |
| Customers | 5,852 |
| Revenue | £17.07M |
| Segments | 6 |

| Segment | Customers | Share of revenue |
|---|---|---|
| Champions | 471 | 54.3% |
| Loyal Customers | 909 | 23.6% |
| Potential Loyalists | 830 | 8.3% |
| At Risk (high value) | 1,309 | 9.4% |
| New / Promising | 860 | 2.3% |
| Lost / Hibernating | 1,473 | 2.2% |

## Key insights
- **8% of customers (Champions) bring in 54% of revenue**
- **65% of customers did not buy again within 2 months** of their first purchase; average month-1 retention is only 21%
- 1,309 "At Risk" customers used to spend well but have not bought in ~9 months, so they are a clear win-back target
- **Top 1% of customers (59) have projected CLV ≥ £51,215** and account for 32% of revenue

