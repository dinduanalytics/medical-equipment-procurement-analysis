# Medical Equipment Procurement Analysis

> A business-focused analysis of medical equipment procurement across hospitals, examining spending, equipment condition, maintenance, installation costs, supplier geography, and delivery performance.

**Author:** Nwaba Chimdindu  
**Tools:** Microsoft Excel · Power Query · PivotTables · Dashboarding  
**Project type:** Procurement analytics / operational cost analysis

---

## Project Overview

Medical equipment procurement involves purchase, installation, and ongoing maintenance costs. This project uses a hospital procurement dataset to investigate questions about spending, equipment condition, supplier geography, and delivery timelines.

The objective is to turn procurement records into a decision-focused dashboard that helps stakeholders compare costs, identify patterns, and decide where further review may be useful.

## Business Questions

The supplied project brief lists seven questions:

1. **Which hospitals spend the most on equipment procurement?**
2. **What is the distribution of equipment by condition across departments?** Which areas may need upgrades?
3. **How do maintenance costs vary by equipment type?** Which types are most and least costly to maintain?
4. **What is the average delivery time for equipment from different suppliers?**
5. **Which states have the highest installation costs for medical equipment?**
6. **What proportion of equipment suppliers comes from each country?**
7. **How does equipment condition vary with installation costs?**

Together, these questions concern procurement efficiency, cost management, supplier performance, and equipment lifecycle management.

## Dataset

The supplied workbook has a procurement worksheet with 260 records and 19 columns.

| Category | Fields |
|---|---|
| Hospital and location | Hospital, State, Location, Department |
| Equipment details | Equipment, Quantity, Equipment Condition, Warranty Period (Months) |
| Costs | Unit Price (USD), Maintenance Cost (USD/year), Installation Cost (USD) |
| Supplier details | Supplier, Supplier Contact, Supplier Phone, Supplier Email, Supplier Country |
| Order timeline | Date Ordered, Date Delivered |

### Data privacy

The original workbook contains supplier contact names, phone numbers, and email addresses. **Do not publish the original workbook publicly without reviewing and removing or anonymising contact details.** Upload only a sanitized copy if the dataset is cleared for public sharing.

## Analytical Workflow

1. **Understand the questions** — map each question to the relevant fields.
2. **Inspect the data** — review field meanings, data types, missing values, and consistency.
3. **Prepare the data** — clean text, check dates, and validate numeric cost fields as needed.
4. **Define metrics** — document calculations and aggregation choices so figures are reproducible.
5. **Analyse patterns** — compare hospitals, departments, equipment types, suppliers, states, and supplier countries.
6. **Visualise results** — use KPIs and charts that fit the question being answered.
7. **Communicate findings** — explain what the results show and make recommendations supported by the analysis.

## Metric Definitions to Verify

Use the exact calculations from the completed workbook when finalising this section.

- **Procurement spend:** confirm the workbook definition. Quantity multiplied by unit price is a possible calculation, but do not assume it matches a separately defined procurement-cost KPI without checking the dashboard formula.
- **Delivery time (days):** date delivered minus date ordered, after checking missing, reversed, or invalid dates.
- **Maintenance cost:** the annual maintenance-cost field supplied in the dataset.
- **Installation cost:** the installation-cost field supplied in the dataset.
- **Supplier distribution by country:** specify whether the analysis counts records, unique suppliers, or equipment units.

Definitions should align with formulas and aggregations in the final dashboard.

## Dashboard Preview

The dashboard screenshot will be added here once it has been exported and uploaded to this repository.

<!-- After uploading dashboard/medical-procurement-dashboard.png, replace this note with:
![Medical Equipment Procurement Dashboard](dashboard/medical-procurement-dashboard.png)
-->

## Findings and Recommendations

This section should contain findings verified against the completed workbook and dashboard. It is intentionally not filled with assumed results.

For each major finding, document:

- **Finding:** What the chart or calculation shows.
- **Evidence:** The measure, comparison, or values supporting the finding.
- **Interpretation:** Why this pattern may matter to procurement operations.
- **Recommendation:** A practical action that follows from the evidence.

Areas to review may include high-spending hospitals or states, equipment condition by department, maintenance costs by equipment type, supplier delivery performance, and sourcing concentration. These are analysis areas, not conclusions established before checking results.

## Project Files

| Path | Contents |
|---|---|
| `README.md` | Project overview, business questions, method, and findings |
| `data/` | Sanitized dataset, if cleared for public release |
| `dashboard/` | Exported dashboard image |
| `docs/` | Data description, project brief, and supporting documentation |
| `video/` | Walkthrough link or video, subject to file-size limits |

## Limitations

- Procurement records show recorded costs and equipment attributes; they do not by themselves explain why a cost occurred or why an item has a particular condition.
- Delivery-time comparisons depend on reliable order and delivery dates and a consistent calculation.
- Comparisons across equipment types may be affected by differences in quantity, unit price, and installation requirements.
- Supplier-country proportions depend on the counting method. State the method clearly.
- Recommendations should be proportional to the evidence and should not imply causation from descriptive comparisons alone.

---

## Project Summary

This project applies a business-question-led analytics workflow to medical equipment procurement data. The intended outcome is a documented dashboard analysis that makes procurement costs, equipment condition, and supplier performance easier to examine.
