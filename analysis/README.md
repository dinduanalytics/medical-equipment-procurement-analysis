# Analysis Methodology

This folder documents the calculations and interpretation principles used in the Medical Equipment Procurement Analysis.

## Dataset and measures

- **Source worksheet:** Procurement Data
- **Source size:** 260 records and 19 named fields
- **Delivery time:** Date Delivered minus Date Ordered; values range from 23 to 29 days, with a mean of approximately 25.30 days.
- **Calculated procurement value:** sum of Quantity × Unit Price, equal to $20,910,500 in the supplied source workbook.
- **Cost measures:** maintenance and installation totals are calculated from their respective source columns; average unit price is calculated from the unit-price field.

## Interpretation principles

- State the calculation used when reporting a metric.
- Keep screenshot KPI values distinct from independently calculated source values where their definitions differ.
- Treat comparisons as descriptive unless additional evidence supports a causal explanation.
- Consider equipment type, quantity, and condition when comparing cost measures.

For the detailed comparison between dashboard figures and source calculations, see [Metric Definitions and Source Comparison](../docs/data-quality-and-reconciliation.md).
