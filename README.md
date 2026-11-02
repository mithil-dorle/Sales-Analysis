# E-commerce Consumer Behavior Analysis

An exploratory analysis of e-commerce customer and purchase data. The project cleans the source CSV, summarizes customer behavior, and visualizes purchase amounts, categories, channels, discounts, satisfaction, and monthly sales.

## Project contents

```text
.
├── analysis.ipynb
├── data_cleaning.ipynb
├── data/
│   ├── Ecommerce_Consumer_Data_Raw.csv
│   └── Ecommerce_Consumer_Data_clean.csv
└── reports/
    ├── consumer_behavior_business_insights.md
    └── figures/
```

- `data/` contains the original and cleaned datasets.
- `data_cleaning.ipynb` inspects and prepares the source data.
- `analysis.ipynb` performs descriptive analysis and plots results.
- `reports/consumer_behavior_business_insights.md` summarizes the findings; `reports/figures/` contains the report charts.

## Methods

1. **Inspect the source data:** review its shape, columns, data types, missing values, and duplicate rows.
2. **Clean the data:** trim whitespace from text, convert purchase amounts to numeric values, parse purchase dates, label unanswered social-media and ad-engagement responses as `Unknown`, and remove exact duplicate rows. Category labels are preserved rather than guessed or renamed.
3. **Summarize behavior:** calculate overall purchase amount statistics and group records by purchase intent, loyalty-program membership, product category, and purchase channel.
4. **Review trends and distributions:** plot purchase-amount distribution and category/channel comparisons, and aggregate purchase amounts by month.
5. **Interpret cautiously:** the comparisons are descriptive. They do not establish that discounts, loyalty membership, or any other factor caused a change in purchasing behavior.

## Findings and business suggestions

The current dataset contains **1,000 records** and **1,000 unique customer IDs**, dated **January 1 through December 30, 2024**. Its recorded purchase amounts total **$275,063.88**, with a mean of **$275.06** and median of **$276.16**. These are descriptive statistics for this dataset, not verified company revenue.

| Finding in this dataset | Suggested business action |
|---|---|
| **Jewelry & Accessories** has the highest recorded category total: **$15,139.36** across 50 customers. | Review stock availability and margins in this category before increasing investment; compare results over a longer period. |
| Online purchases have the highest average satisfaction, **5.57/10**. | Identify which parts of the online experience customers value and test whether they improve satisfaction in other channels. |
| **52.1%** of records indicate a discount. Average purchase amount is **$273.99** for discount users and **$276.23** for others. | Use a controlled test to assess whether targeted offers improve conversion or profit; this comparison alone does not measure discount impact. |
| Wants-based purchases have the highest average amount: **$292.01** across 249 customers. | Test intent-aware recommendations on a small audience and measure conversion, average purchase amount, and margin. |
| Average purchase amount is **$261.27** for loyalty-program members and **$288.37** for non-members. | Compare repeat purchases, retention, and program costs over time before changing member benefits; this snapshot does not show program effectiveness. |
| **April 2024** has the highest recorded monthly total: **$28,617.22**. | Check promotion calendars, seasonality, and data completeness before using the peak to plan inventory or campaigns. |

## Limitations

- The dataset documentation does not establish how records were sampled, whether purchase amounts represent completed transactions, the currency context, or profit/margin.
- Group differences may reflect customer mix and are not evidence of causation.
- `Social_Media_Influence` has 247 unanswered values and `Engagement_with_Ads` has 256. Treat results based on these fields cautiously.
- The source includes the category label `Packages)`. It is retained because its intended meaning is unknown.
- Validate business decisions with additional periods, margin and retention data, and controlled experiments where appropriate.
