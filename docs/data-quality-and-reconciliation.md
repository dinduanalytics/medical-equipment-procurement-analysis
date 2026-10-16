# Data Quality and KPI Reconciliation

This note records calculations made from the supplied `Procurement Dataset.xlsx` source workbook. It compares the numeric fields with the KPI figures displayed in the previously supplied dashboard screenshot so the published project does not silently present unreconciled figures as one consistent result.

## Workbook checks

The `Procurement Data` worksheet contains 260 data records and 19 named fields. All 260 records had nonblank values in the fields examined. The three supplier-contact fields have been excluded from the sanitized public-data copy.

| Metric | Recalculated from current source workbook | Dashboard screenshot | Status |
|---|---:|---:|---|
| Annual maintenance cost total | $462,600 | $461,400 | Difference to reconcile |
| Installation cost total | $275,700 | $275,100 | Difference to reconcile |
| Average unit price | $37,405 | $37,519 | Difference to reconcile |
| Average delivery time | 25.30 days | 25 days | Rounded display may explain difference |
| Procurement cost | $20,910,500 when calculated as quantity × unit price | $21,639,000 displayed as total procurement cost | Definition/formula needs confirmation |

These source-side values use the numeric columns as provided. The procurement figure shown is explicitly the result of `Quantity × Unit Price` summed across records; it should not be called the dashboard's procurement-cost KPI until the workbook's actual measure definition has been confirmed.

## Suggested reconciliation steps

1. Inspect the formulas or PivotTable aggregation used for each dashboard card.
2. Confirm whether unit price is being summed, averaged, or multiplied by quantity for the procurement measure.
3. Verify the PivotTable source range and refresh status.
4. Confirm whether the dashboard is based on the exact uploaded dataset version.
5. Update this table after the formulas and source version are reconciled.

## Descriptive observations from the source workbook

- There are 92 distinct hospital names, 35 distinct state values, 40 distinct supplier names, and 15 supplier-country values.
- Equipment condition counts: New (124), Used - Good (88), Refurbished (40), Used - Fair (8).
- Date-delivered minus date-ordered ranges from 23 to 29 days across the 260 records; the mean is approximately 25.30 days.
- Summing `Quantity × Unit Price` produces $20,910,500. The 10 hospitals with the highest value by this method begin with Minna Federal Medical Center ($1,815,000), Yenagoa Medical Center ($1,434,000), and Dutse General Hospital ($1,335,000).

These observations are descriptive and depend on the definitions above. They do not establish the reasons behind the recorded patterns.
