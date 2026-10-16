# Metric Definitions and Source Comparison

This note describes calculations from the supplied source workbook and compares them with KPI figures visible in the supplied dashboard screenshot. The two sets of figures are kept distinct so each metric can be interpreted in context.

## Dataset checks

The Procurement Data worksheet contains **260 records and 19 named fields**. The public-use workbook excludes supplier contact names, phone numbers, and email addresses.

## Metric comparison

| Metric | Calculation from source worksheet | Value displayed in dashboard |
|---|---:|---:|
| Annual maintenance cost | Sum of maintenance-cost column: $462,600 | $461,400 |
| Installation cost | Sum of installation-cost column: $275,700 | $275,100 |
| Average unit price | Mean of unit-price column: $37,405 | $37,519 |
| Average delivery time | Mean of delivery date minus order date: 25.30 days | 25 days |
| Procurement value | Sum of quantity multiplied by unit price: $20,910,500 | $21,639,000 |

The delivery-time figures are consistent with rounding the source mean to a whole day. The other differences may reflect different calculation definitions, source ranges, refresh states, or workbook versions. The screenshot values are presented as displayed; the source calculations above use the named fields and formulas stated in the table.

For interpretation, distinguish the **dashboard KPI as displayed** from a **recalculated source metric**. In particular, the sum of Quantity × Unit Price is a defined calculation for this project and should not be treated as interchangeable with a procurement KPI unless the KPI uses that same formula.

## Additional descriptive observations

- Distinct values: **92 hospital names**, **35 state values**, **40 supplier names**, and **15 supplier-country values**.
- Equipment condition counts: **New (124)**, **Used - Good (88)**, **Refurbished (40)**, and **Used - Fair (8)**.
- Delivery time ranges from **23 to 29 days**; the mean is approximately **25.30 days**.
- By the Quantity × Unit Price calculation, the highest hospital totals begin with Minna Federal Medical Center (**$1,815,000**), Yenagoa Medical Center (**$1,434,000**), and Dutse General Hospital (**$1,335,000**).

## Interpretation

These metrics support descriptive comparisons of procurement values, equipment condition, maintenance costs, installation costs, and supplier delivery times. Conclusions should reflect the calculation used and the fields available. The dataset does not, by itself, explain why a hospital, supplier, or equipment category has a particular value.
