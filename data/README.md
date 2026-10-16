# Data Folder

This folder is intended for the public-safe procurement dataset only. Do not commit the unredacted source workbook because it contains supplier contact information.

## Generate the sanitized workbook

Place your original `Procurement Dataset.xlsx` outside the public repository or in a local working folder, then run:

```bash
python scripts/sanitize_dataset.py "Procurement Dataset.xlsx"
```

The script writes `data/procurement_dataset_sanitized.xlsx`, retaining the procurement table while excluding supplier contact, phone, and email fields. It also normalizes column headings and removes empty columns and unrelated worksheets.

Review the generated file before committing it. The repository does not currently include a sanitized workbook binary; the script is provided so the copy can be created and checked safely.