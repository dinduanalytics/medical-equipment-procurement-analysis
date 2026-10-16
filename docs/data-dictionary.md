# Data Dictionary

The current source worksheet has 260 records and the following 19 named fields. The supplied workbook includes extra whitespace in some original column labels; the sanitized copy uses trimmed labels.

| Field | Type / meaning | Notes |
|---|---|---|
| Serial No | Integer identifier | Row-level serial number. |
| Hospital | Text | Hospital name. |
| State | Text | State/location grouping supplied in source. |
| Location | Text | More specific location. |
| Department | Text | Department using the equipment. |
| Equipment | Text | Equipment type/name. |
| Quantity | Integer | Number of units. |
| Unit Price | Numeric, USD | Per-unit cost field; check formula for procurement total. |
| Supplier | Text | Supplier name. |
| Supplier Contact | Text | Excluded from sanitized public copy. |
| Supplier Phone | Text | Excluded from sanitized public copy. |
| Supplier Email | Text | Excluded from sanitized public copy. |
| Supplier Country | Text | Supplier country of origin. |
| Date Ordered | Date | Order date. |
| Date Delivered | Date | Delivery date. |
| Warranty Period (Months) | Integer | Warranty length. |
| Maintenance Cost (USD/year) | Numeric, USD/year | Annual maintenance cost. |
| Installation Cost (USD) | Numeric, USD | Installation cost. |
| Equipment Condition | Categorical text | New, Used - Good, Refurbished, Used - Fair in current data. |

## Sanitization

Supplier Contact, Supplier Phone and Supplier Email are omitted from the public dataset copy. The source workbook is preserved separately and should not be committed directly to a public repository without permission to share these details.
