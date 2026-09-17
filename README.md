# E-commerce Analytics

End-to-end analytics project combining SQL data extraction, Python
exploratory analysis, statistical hypothesis testing, and an interactive
Tableau dashboard — built on real e-commerce session, subscriber, and
order data.

**[Open the notebook](Ecommerce_Sales_Analytics.ipynb)**

## Project overview

This project analyzes user session and order data from an e-commerce
platform, joining six BigQuery source tables — sessions, session
metadata, subscriber accounts, orders, and products — into a single
analytical view covering traffic, device, geography, subscription, and
purchase behavior.

## What the analysis covers

1. **Data extraction (SQL + BigQuery):** a parameterized query joining
   six tables directly from a BigQuery data warehouse
2. **Dataset profiling:** structure, data types, completeness, missing
   value strategy (replace with meaningful labels, not drop)
3. **Sales & orders analysis by segment:** geography, product category,
   device type, traffic source, registration and subscription status
4. **Sales dynamics over time:** daily trends, weekly seasonality,
   breakdowns by continent, channel, and device
5. **Pivot tables:** four cross-cuts of the data along different
   dimension combinations
6. **Statistical analysis of relationships:** Pearson correlation
   between session count and revenue, cross-continent/channel/category
   correlation, and lag-correlation analysis (testing a delayed "halo"
   effect between paid and organic search)
7. **Statistical analysis of group differences:** normality testing
   (Shapiro-Wilk), Mann-Whitney U, Kruskal-Wallis, and chi-square tests
   of independence
8. **Tableau dashboard:** a two-page interactive dashboard summarizing
   the findings above

## Tools & libraries
Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, Google BigQuery
(google-cloud-bigquery), Tableau Public

## Key findings

- **Geography:** Americas leads in both revenue and order count; the
  United States alone drives the largest share of total sales
- **Device & channel:** Desktop dominates revenue (59.0%), followed by
  mobile (38.7%); Organic Search is the leading traffic driver (35.8% of
  revenue)
- **Subscription behavior:** unsubscribed users show a *higher*
  conversion rate than still-subscribed users — a counter-intuitive
  pattern worth further investigation
- **Correlation:** session count and daily revenue are strongly
  correlated (r = 0.79, p < 0.001); paid and organic search revenue show
  a lagged relationship, suggesting a real halo effect rather than same-day
  cannibalization
- **Group differences:** device choice shows no significant association
  with registration status (χ² test); average order value does not
  differ significantly across the top-3 continents (Kruskal-Wallis)

## Dashboard

- [Page 1 — Sales Performance Overview](https://public.tableau.com/app/profile/kateryna.kolesnyk/viz/SalesPerformanceOverview_17879385315220/Dashboard4)
- [Page 2 — Trends & Customer Behavior](https://public.tableau.com/app/profile/kateryna.kolesnyk/viz/TrendsCustomerBehavior/Dashboard5)

