# Medical Equipment Procurement Analysis

<p align="center">
  <img src="dashboard/project-cover.svg" width="100%" alt="Medical Equipment Procurement Analysis project cover" />
</p>

**Prepared by:** Nwaba Chimdindu  
**Tools:** Microsoft Excel · PivotTables · Dashboarding  
**Focus:** Procurement cost control, asset condition, supplier performance and lifecycle cost analysis

---

## Project Overview

Hospitals depend on reliable medical equipment, timely supplier deliveries, and careful cost management. This project explores a procurement dataset containing hospital, equipment, supplier, cost, condition, warranty, and delivery information.

The analysis is organised around seven business questions from the supplied project brief. The goal is to make procurement patterns easier to examine and support evidence-based discussions about cost management, sourcing, and equipment lifecycle planning.

## Business Questions

1. Which hospitals spend the most on equipment procurement?
2. What is the distribution of equipment by condition across departments, and which areas may need upgrades?
3. How do maintenance costs vary by equipment type?
4. What is the average delivery time for equipment from different suppliers?
5. Which states have the highest installation costs for medical equipment?
6. What proportion of equipment suppliers comes from each country?
7. How does equipment condition vary with installation costs?

## Dataset

The supplied workbook contains **260 records and 19 named fields**. The public copy has been prepared separately to exclude supplier contact names, phone numbers, and email addresses. The original workbook is not included in the public repository.

| Field group | Included fields |
|---|---|
| Hospital and location | Hospital, State, Location, Department |
| Equipment | Equipment, Quantity, Equipment Condition, Warranty Period (Months) |
| Cost | Unit Price, Maintenance Cost (USD/year), Installation Cost (USD) |
| Supplier | Supplier, Supplier Country |
| Dates | Date Ordered, Date Delivered |

See the [data dictionary](docs/data-dictionary.md), [project brief](docs/project-brief.md), and [data-quality note](docs/data-quality-and-reconciliation.md).

## Analytical Workflow

**Business questions → data inspection → preparation → metric definition → analysis → dashboard → recommendations**

The analysis compares records by hospital, department, equipment type, supplier, state, and supplier country. Delivery time is calculated as the difference between delivery and order dates, while cost measures should follow the exact definitions documented in the workbook.

## Dashboard Preview

The cover above introduces the areas explored in the dashboard. The full dashboard screenshot is planned as a separate repository asset; it has not yet been committed as an image file. The original workbook's Pivot and Dashboard tabs were not populated as normal cell tables when inspected, so the supplied screenshot is the visual evidence for the dashboard layout.

## Source-Data Observations

- **260 records** in the Procurement Data worksheet.
- **92 distinct hospital names**, **35 distinct state values**, **40 distinct supplier names**, and **15 supplier-country values**.
- Equipment condition counts: **New (124)**, **Used - Good (88)**, **Refurbished (40)** and **Used - Fair (8)**.
- Delivery minus order date ranges from **23 to 29 days** in the current source; mean delivery time is approximately **25.30 days**.
- By the specific measure `Quantity × Unit Price`, the highest hospital totals begin with Minna Federal Medical Center (**$1,815,000**), Yenagoa Medical Center (**$1,434,000**) and Dutse General Hospital (**$1,335,000**).

These are descriptive observations from the source workbook. They do not, by themselves, explain why the patterns occurred.

## KPI Reconciliation

The dashboard screenshot displays total procurement cost of **$21,639,000**, average delivery time of **25 days**, annual maintenance cost of **$461,400**, installation cost of **$275,100**, and average unit price of **$37,519**.

Recalculation from the current uploaded source worksheet produces different values for some cards: the sum of the maintenance-cost column is **$462,600**, installation cost sums to **$275,700**, average unit price is **$37,405**, and the sum of `Quantity × Unit Price` is **$20,910,500**. The average delivery time is **25.30 days**, which could explain a display rounded to 25 days.

The procurement KPI may use a different definition than `Quantity × Unit Price`. Formulas, PivotTable source range, refresh status, and dashboard data version should be confirmed before treating the displayed values as reconciled. Full details are in [Data Quality and KPI Reconciliation](docs/data-quality-and-reconciliation.md).

## Recommendations to Evaluate

After reconciling the measures, the analysis can support a review of:

- High-spending hospitals and states, including the drivers of their totals.
- Departments with higher shares of equipment recorded as used or refurbished.
- Equipment types with relatively high annual maintenance costs.
- Supplier delivery-time differences and potential follow-up requirements.
- Supplier-country concentration and sourcing resilience.
- Installation-cost differences across condition groups, while considering equipment type, quantity, and price.

Recommendations should be tied to figures visible in the final workbook, and should not infer causation from descriptive comparisons alone.

## Repository Structure

| Path | Purpose |
|---|---|
| `README.md` | Main case study and project cover |
| `dashboard/project-cover.svg` | Visual cover graphic |
| `docs/project-brief.md` | Field descriptions and original analysis questions |
| `docs/data-dictionary.md` | Field-level definitions and sanitization notes |
| `docs/data-quality-and-reconciliation.md` | Recalculated metrics and KPI differences |
| `data/` | Guidance for a sanitized source-data copy |
| `dashboard/` | Dashboard visuals |
| `video/` | Walkthrough information or a hosted-video link |

## Data Privacy

The source workbook contains supplier contact names, phone numbers, and emails. Do not publish the original workbook without permission to share these details. The repository documents the analysis and source definitions without reproducing those contact details.

## Limitations

- Recorded data does not explain all reasons behind procurement cost or equipment condition.
- Delivery-time comparisons depend on valid order and delivery dates.
- Cost comparisons can be affected by differences in equipment type, quantity, unit price, and installation requirements.
- Supplier distribution depends on whether the analysis counts rows, unique suppliers, or quantities; the selected method should be stated.

---

*This case study documents the path from procurement questions to data validation and visual analysis. It will be updated as the workbook calculations and project assets are finalised.*
