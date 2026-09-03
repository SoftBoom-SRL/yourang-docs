---
title: "Data export"
description: "Export your call history as a CSV file for analysis, reporting, and sharing with your team."
section: "Calls"
slug: "calls/export"
---

# Data export

Export your call history as a CSV file for analysis, reporting, and sharing with your team.

_Yourang lets you export call data as a CSV file. You can use the exported file for advanced analysis, to generate internal reports, or to share the data with your team or an external consultant._

## How to export calls <a id="come-esportare-le-chiamate"></a>

1. **Apply the desired filters** — Before exporting, use the filters to select the period or criteria you're interested in. The export will only include the calls visible in the filtered list.
2. **Start the export** — Click the "Export CSV" button at the top of the history, next to the filters. The system will process the request.
3. **Download the file** — Once ready, the CSV file will be downloaded automatically by your browser. The file name includes the date and the time range of the export to make archiving easier.

## Columns included in the CSV file <a id="colonne-incluse-nel-file-csv"></a>

The exported file contains the following columns for each call:

- Call ID (unique identifier)
- Date and time (ISO 8601 format)
- Duration in seconds
- Caller number
- Outcome (answered, abandoned, transferred, voicemail, unanswered)
- Voice agent name
- Associated property
- AI-generated summary

> [!NOTE]
> **Transcripts not included**
> For file-size reasons, the full text of the transcripts is not included in the CSV. The file exports the automatic summary of each call, which is generally enough for analysis and reporting. Full transcripts remain available from the platform.

## Using the exported file <a id="utilizzo-del-file-esportato"></a>

The CSV format is compatible with the main data analysis programs such as Microsoft Excel, Google Sheets, and LibreOffice Calc. You can open it directly, build charts on call outcomes, calculate average duration, or filter by keyword inside the summaries.

> [!TIP]
> **Monthly export**
> Set a monthly reminder to export the calls from the previous month. Archive the CSV files with a structured name (e.g. "calls-2025-05.csv") to build, over time, a history that's accessible even outside Yourang.
