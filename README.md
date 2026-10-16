# Medical Equipment Procurement Analysis

<p align="center">
  <strong>Healthcare Procurement · Cost Analysis · Supplier Performance</strong><br/>
  A business-focused analytics case study exploring procurement spending, equipment condition, maintenance, installation costs, and delivery performance across hospitals.
</p>

<p align="center">
  <img src="dashboard/medical-procurement-dashboard.jpg" alt="Medical Procurement Dashboard" width="100%" />
</p>

**Prepared by:** Nwaba Chimdindu  
**Tools:** Microsoft Excel · PivotTables · Dashboarding  
**Project type:** Procurement and operational cost analysis

---

## Project Overview

Hospitals depend on reliable medical equipment, timely supplier deliveries, and careful cost management. This project explores a procurement dataset containing hospital, equipment, supplier, cost, condition, warranty, and delivery information.

The analysis is organised around seven business questions from the supplied project brief. The goal is to make procurement patterns easier to examine and support evidence-based discussions about cost management, sourcing and equipment lifecycle planning.

## Business Questions

1. Which hospitals spend the most on equipment procurement?
2. What is the distribution of equipment by condition across departments, and which areas may need upgrades?
3. How do maintenance costs vary by equipment type?
4. What is the average delivery time for equipment from different suppliers?
5. Which states have the highest installation costs for medical equipment?
6. What proportion of equipment suppliers comes from each country?
7. How does equipment condition vary with installation costs?

## Dataset

The supplied workbook contains **260 records and 19 named fields**. The public copy is planned to omit supplier contact names, phone numbers, and email addresses.

| Field group | Included fields |
|---|---|
| Hospital and location | Hospital, State, Location, Department |
| Equipment | Equipment, Quantity, Equipment Condition, Warranty Period (Months) |
| Cost | Unit Price, Maintenance Cost (USD/year), Installation Cost (USD) |
| Supplier | Supplier, Supplier Country |
| Dates | Date Ordered, Date Delivered |

See the [data dictionary](docs/data-dictionary.md) and [original brief transcription](docs/project-brief.md).

## Analytical Workflow

**Business questions → data inspection → preparation → metric definition → analysis → dashboard → recommendations**

The analysis groups and compares records by hospital, department, equipment type, supplier, state and supplier country. Delivery time is calculated as the difference between delivery and order dates, and cost measures should use the exact definitions documented in the workbook.

## Dashboard and Current Observations

The dashboard preview above is the visual solution supplied for this project. It shows KPI cards for procurement costs, average delivery time, annual maintenance costs, installation costs and average unit price, along with views of high-spending hospitals, frequently purchased equipment, supplier spend and delivery-time patterns.

The screenshot currently displays the following headline figures: total procurement cost **$21,639,000**, average delivery time **25 days**, annual maintenance cost **$461,400**, total installation cost **$275,100**, and average unit price **$37,519**. These are transcribed from the visual and remain subject to reconciliation with the source worksheet.

### KPI reconciliation note

Independent calculations from the uploaded source worksheet produce different values for some dashboard cards. For example, the sums of the source maintenance-cost and installation-cost columns are **$462,600** and **$275,700**, respectively. The average of the Unit Price column is **$37,405**. Multiplying each record's quantity by its unit price and summing gives **$20,910,500**. The mean difference between delivery and order dates is approximately **25.30 days**, which is consistent with a rounded display of 25 days.

The procurement calculation may use a different definition from `Quantity × Unit Price`. Before treating the displayed and recalculated numbers as reconciled, the workbook's formulas, PivotTable source range, refresh status and dashboard data version should be reviewed. Full details are recorded in [Data Quality and KPI Reconciliation](docs/data-quality-and-reconciliation.md).

## Verified Source-Data Observations

- **260 records** in the Procurement Data worksheet.
- **92 distinct hospital names**, **35 distinct state values**, **40 distinct supplier names**, and **15 supplier-country values**.
- Equipment condition counts: **New (124)**, **Used - Good (88)**, **Refurbished (40)** and **Used - Fair (8)**.
- Delivery minus order date ranges from **23 to 29 days** in the current source; mean delivery time is approximately **25.30 days**.
- By the specific measure `Quantity × Unit Price`, the highest hospital totals begin with Minna Federal Medical Center (**$1,815,000**), Yenagoa Medical Center (**$1,434,000**) and Dutse General Hospital (**$1,335,000**).

These are descriptive observations from the source workbook. They do not, on their own, establish why the patterns occurred or prove that equipment condition causes higher installation costs.

## Recommendations to Evaluate

After reconciling the measures, the analysis can support a review of:

- High-spending hospitals and states, including the drivers of their totals.
- Departments with higher shares of equipment recorded as used or refurbished.
- Equipment types with relatively high annual maintenance costs.
- Supplier delivery-time differences and potential follow-up requirements.
- Supplier-country concentration and sourcing resilience.
- Installation-cost differences across condition groups, while considering equipment type, quantity and price.

Recommendations should be tied to figures visible in the final workbook, and should not infer causation from descriptive comparisons alone.

## Repository Structure

| Path | Purpose |
|---|---|
| `README.md` | Main case study and dashboard preview |
| `docs/project-brief.md` | Field descriptions and original analysis questions |
| `docs/data-dictionary.md` | Field-level definitions and sanitization notes |
| `docs/data-quality-and-reconciliation.md` | Recalculated metrics and discrepancy checks |
| `data/` | Sanitized dataset, once added and cleared for publication |
| `dashboard/` | Dashboard image assets |
| `video/` | Walkthrough information or a hosted video link |

## Data Privacy

The raw workbook contains supplier contact names, phone numbers and emails. The repository should only contain the sanitized copy unless permission to publish those details is confirmed. The workbook's original Pivot and Dashboard sheets were not populated as normal cell tables when inspected; the dashboard preview is therefore represented by the separate supplied screenshot.

## Limitations

- Recorded data does not explain all reasons behind procurement cost or equipment condition.
- Delivery comparisons assume ordered and delivered dates are valid.
- Cost comparisons can be affected by differences in equipment, quantity, unit price and installation requirements.
- Supplier distribution depends on whether the analysis counts rows, unique suppliers, or quantities; the chosen method must be stated.

---

*This case study documents the path from procurement questions to data validation and visual analysis. It will be updated as the workbook calculations and published artifacts are finalised.*
