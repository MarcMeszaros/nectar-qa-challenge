Nectar QA Challenge
===================

You have 2 data sets - one data set is collected from the sensors (`used.csv`) and another one is collected from the point of sale system (`sold.csv`).

Rows are matched based on the `product_id` (this is the product that is being tracked by a given sensor or sold), `time` (this is the time when the products was used or sold) and `used_ml`/`sold_ml` (the amount that was used/sold) using the following rules:

- `product_id` should be matched 1:1 btw used and sold
- `time` should be within 20 minutes btw sold and used
- Closest `used_ml` vs `sold_ml` is picked within the time window to get a 1:1 match
- There will be rows that won't match - these are simply ignored

The following data and graphs are computed post the correlation (matching).

1. Number of products
2. Number of matches per product
3. Total used = Sum ( Sum of used per product)
4. Total poured = Sum (Sum of sold per product)
5. Ranking = Total used / Total poured
6. The distribution of the absolute difference between the `used_ml` and `sold_ml`, aggregated across all products and times are plotted as shown in the attached graph. Assume this is on a web page.

All data points from 1 to 5 are shown on a web page along with the graph.

![Screenshot](/screenshots/sample_1.png?raw=true "Sample Graph Screenshot")

## Exercise

Design a overall system test plan. Consider all aspects of the system. Feel free to assume the data availability in any database or data repo format (it's fine to use it as CSV only). Feel free to write scripts in language of your choice to compute the numbers and also test the results.


Good Luck!
Don't hesitate to contact us if you have any questions.
