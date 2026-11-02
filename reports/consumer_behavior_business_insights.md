# E-commerce Consumer Behavior — Business Insight Report

## Executive summary

This exploratory analysis uses the cleaned customer dataset. It covers 1,000 records and 1,000 unique customer IDs, with purchase dates from 2024-01-01 through 2024-12-30. The recorded purchase amount total is $275,063.88; average and median amounts are $275.06 and $276.16. These amounts are descriptive summaries of this file, not verified company revenue.

## Findings and actions to consider

1. **Dataset snapshot:** 1,000 customer records represent $275,063.88 in recorded purchase amounts, with an average of $275.06 and a median of $276.16 per record.
2. **Category opportunity:** Jewelry & Accessories has the highest total recorded sales ($15,139.36) across 50 customers. Review inventory and availability for this category, then compare margin before increasing investment.
3. **Channel experience:** Online has the highest average satisfaction (5.57/10). Compare its customer journey with other channels and test whether the most helpful elements can be reused.
4. **Discount check:** 52.1% of records indicate a discount was used. Average purchase amount is $273.99 for discount users versus $276.23 for others. This is descriptive, not proof that discounts reduce or increase spending; test offers with a controlled experiment.
5. **Purchase intent:** Wants-based customers have the highest average purchase amount ($292.01; 249 customers). Try tailoring product recommendations to this intent and measure conversion in a small test.
6. **Loyalty program:** average purchase amount is $261.27 among members and $288.37 among non-members. Compare repeat purchase and program costs over time before changing program benefits; membership alone does not establish program impact.

## Monthly context

The highest recorded-sales month is April 2024 ($28,617.22). Monthly totals depend on the date coverage and records represented in this file; investigate unusual peaks against promotions, seasonality, and data completeness before making plans.

## Charts

- [purchase_amount_distribution.png](figures/purchase_amount_distribution.png)
- [top_categories_by_sales.png](figures/top_categories_by_sales.png)
- [purchase_channel_comparison.png](figures/purchase_channel_comparison.png)
- [discount_comparison.png](figures/discount_comparison.png)
- [satisfaction_by_channel.png](figures/satisfaction_by_channel.png)
- [monthly_sales.png](figures/monthly_sales.png)

## Method and limitations

- The raw CSV was not edited. Text whitespace was trimmed, purchase amounts were converted to numbers, dates were parsed, and unanswered social-media/ad-engagement fields were labeled `Unknown`.
- Exact duplicate rows were removed (if any); category names were otherwise preserved. The source includes the label `Packages)`, which was not renamed because its intended meaning is unverified.
- Group comparisons are descriptive and may reflect differences in customer mix. They do not prove causation. Validate recommendations with experiments or additional time-period data.
- The file does not document how the records were sampled, whether amounts represent completed transactions, currency context, profit/margin, or the definitions of fields such as `Frequency_of_Purchase` and `Return_Rate`.
- Survey fields have missing answers: `Social_Media_Influence` (247) and `Engagement_with_Ads` (256). Treat findings from these fields with that limitation in mind.

## Generated data

- Cleaned dataset: `../data/Ecommerce_Consumer_Behavior_Analysis_Clean.csv`
- Charts: `figures/`
