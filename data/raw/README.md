# Dataset — Real Estate Valuation (Taipei)

| Property | Value |
|---|---|
| Source | [UCI Machine Learning Repository — Real Estate Valuation](https://archive.ics.uci.edu/dataset/477/real+estate+valuation+data+set) |
| Original Study | Yeh, I-Cheng and Hsu, Tzu-Kuang (2018). Building real estate valuation models with comparative and cluster analysis. *Applied Soft Computing*, 70, 260–271. |
| License | CC BY 4.0 |
| Instances | 414 |
| Features | 6 numeric predictors + 1 numeric target |
| Time Period | June 2012 – May 2013 |
| Geography | Taipei City and New Taipei City, Taiwan |
| File Size | ~20 KB (committed directly) |

## Variables

| Column | Description | Units |
|---|---|---|
| `tr_date` | Transaction date (fractional year) | Year |
| `house_age` | Age of the property | Years |
| `dist_mrt` | Distance to the nearest MRT station | Metres |
| `n_stores` | Number of convenience stores within walking distance | Count |
| `lat` | Latitude coordinate | Decimal degrees |
| `long` | Longitude coordinate | Decimal degrees |
| `price` | **Target** — house price per unit area | 10,000 NTD / Ping |

## Notes

- No missing values in the original dataset.
- Latitude and longitude values are in the range of Taipei City and New Taipei City.
- One Ping ≈ 3.3058 m².
