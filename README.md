# ✈️ Flight Ticket Price Analysis

End-to-end exploratory data analysis on Indian domestic flight pricing
to identify what actually drives airfare variation across airlines, routes, and cities.

---

## What I found

- Vistara is the priciest airline (median ₹14,805) but the gap between
  airlines is small — route matters more than brand
- One-stop flights cost *more* than direct (₹13,803 vs ₹13,035) —
  stopovers correlate with expensive routes, not convenience pricing
- Duration has near-zero correlation with price (-0.002) — longer flights
  aren't meaningfully more expensive
- Original `total_stops` column had mismatches with actual route data —
  corrected via route-string validation before any analysis was run

---

## Visualizations

### Price Distribution
![Price Distribution](images/price_distribution.png)

### Top 10 Most Frequent Routes
![Top Routes](images/top_routes.png)

### Top 10 Most Expensive Routes
![Expensive Routes](images/expensive_routes.png)

### Flight Duration vs Ticket Price
![Duration vs Price](images/duration_vs_price.png)

### Stop Distribution per Airline
![Stop Share](images/stop_share.png)

### Average Price by Source → Destination
![Route Heatmap](images/route_heatmap.png)

### Correlation Matrix
![Correlation Matrix](images/correlation_matrix.png)

---

## Stack
Python · Pandas · Seaborn · Matplotlib

## Run locally

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Flight_Ticket_Analysis_EDA.ipynb
```

## Next step
Feature encoding → XGBoost regression → fare prediction pipeline