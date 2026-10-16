# Public Dataset

The public-use Excel workbook is available in the [v1.0.0 project release](https://github.com/dinduanalytics/medical-equipment-procurement-analysis/releases/tag/v1.0.0).

**[Download the sanitized procurement dataset](https://github.com/dinduanalytics/medical-equipment-procurement-analysis/releases/download/v1.0.0/procurement_dataset_sanitized.xlsx)**

The workbook contains 260 procurement records and excludes supplier contact names, phone numbers, and email addresses. The original source workbook should remain private unless permission to publish its contact information has been confirmed.

The sanitization script is available at [scripts/sanitize_dataset.py](../scripts/sanitize_dataset.py). To create another public-use copy locally, run:

```bash
python scripts/sanitize_dataset.py "Procurement Dataset.xlsx"
```

Review the generated workbook before sharing it.
