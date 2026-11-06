---
title: "CSV import"
description: "Bring your existing customer list into Yourang in a few steps"
section: "Contacts"
slug: "contacts/csv-import"
---

# CSV import

Bring your existing customer list into Yourang in a few steps

_If you already have a customer archive in a spreadsheet or business system, you can import it into Yourang by uploading a CSV file. The system automatically recognises the main fields and links each row to a contact in the directory._

## File format <a id="formato-del-file"></a>

The file must be in CSV format (comma-separated values) with UTF-8 encoding. Excel sheets can be exported in this format directly from the "Save as" menu.

- Format: CSV (not XLS, XLSX, or ODS)
- Encoding: UTF-8 (required for accents and special characters)
- Maximum size: 10 MB per file
- Maximum rows: 10,000 per import
- The first row must contain the column headers

## Recognised headers <a id="intestazioni-riconosciute"></a>

The following headers are mapped automatically to the directory fields. Names are case-insensitive (capitalisation doesn't matter) and can be in Italian or English.

- nome / first_name, Contact's first name
- cognome / last_name, Contact's last name
- telefono / phone, Phone number (with international prefix)
- email, Email address
- lingua / language, Language code (e.g. it, en, fr, es, de)
- note / notes, Internal notes about the contact

## How to import a file <a id="come-importare"></a>

1. **Go to Contacts** — From the sidebar select "Contacts" and then click the "Import" button.
2. **Upload the CSV file** — Drag the file into the indicated area or click "Select file" to search for it on your computer.
3. **Verify the mapping** — Yourang shows a preview of the first rows and the automatic field mapping. Fix any incorrect matches before continuing.
4. **Choose how to handle duplicates** — Select whether contacts already in the directory should be updated with the new data or ignored.
5. **Start the import** — Confirm and wait for completion. You'll get a summary with the number of contacts imported, updated, and skipped.

## Handling duplicates <a id="gestione-duplicati"></a>

Yourang identifies duplicates by comparing phone numbers. If a contact with the same number already exists in the directory, you can choose between two behaviours:

- **Update** — The data from the file overwrites what's in the directory. Useful when the CSV contains more up-to-date information.
- **Skip** — The existing contact is left unchanged. Useful for adding only new customers without touching existing ones.

> [!WARNING]
> **Watch out for sensitive data**
> Before importing a CSV file, check that it doesn't contain unnecessary sensitive data, such as credit card numbers, health data, or other confidential information. Yourang is not designed to store this type of data and its presence could constitute a GDPR breach.
