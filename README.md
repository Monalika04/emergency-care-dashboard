# Hospital Emergency Room Dashboard

An interactive **Power BI dashboard** for exploring hospital emergency room activity, patient flow, waiting times, admissions, department referrals, and patient satisfaction.

## Project Overview

This project uses hospital emergency room records to help users explore operational patterns and identify areas that may need attention. The Power BI report is included in the `powerbi/` folder, along with the source dataset, dashboard preview images, and a project report.

## Tools and Skills

- Microsoft Power BI
- Power Query
- DAX
- Data cleaning and transformation
- Data visualization
- Data modeling
- Business analysis

## Repository Contents

```text
emergency-care-dashboard/
├── README.md
├── assets/
│   └── hospital.png
├── dashboard/
│   ├── Consolidated View.png
│   ├── Key Insight.png
│   ├── Monthly View.png
│   └── Patients Details.png
├── dataset/
│   └── Hospital ER_Data.csv
├── docs/
│   └── Hospital Emergency Room Dashboard – Project Report.docx
└── powerbi/
    └── hospital-emergency-dashboard.pbix
```

## Dashboard Previews

### Monthly View
Month-wise view of patient volume, waiting time, satisfaction, and referral patterns.

![Monthly View](dashboard/Monthly%20View.png)

### Consolidated View
An overall view of hospital performance across the selected date range.

![Consolidated View](dashboard/Consolidated%20View.png)

### Patients Details
A detailed view of patient-level records.

![Patients Details](dashboard/Patients%20Details.png)

### Key Insights
A summary of findings and potential business recommendations.

![Key Insight](dashboard/Key%20Insight.png)

## Dataset

**File:** `dataset/Hospital ER_Data.csv`

The CSV contains **9,216 patient records and 12 columns** (excluding the header row). Fields include:

- Patient Id
- Patient Admission Date
- Patient First Inital
- Patient Last Name
- Patient Gender
- Patient Age
- Patient Race
- Department Referral
- Patient Admission Flag
- Patient Satisfaction Score
- Patient Waittime
- Patients CM

### Data-quality considerations

- Some patient satisfaction values are blank. Check their meaning before deciding whether to exclude or impute them.
- The `Department Referral` column contains `None` values. Confirm whether these represent no referral or missing information.
- The `Patient Gender` column includes `NC`. Confirm what this category means in the source data.
- Admission dates appear in `DD-MM-YYYY HH:MM` format. Verify that Power Query interprets them using the correct locale.
- The field name `Patient First Inital` appears to contain a spelling error in the source header. Confirm the original field name before renaming it in the report.

## Key Metrics and Findings

The existing dashboard summary reports the following figures:

- **Total patients:** 9,216
- **Average wait time:** 35.3 minutes
- **Patient satisfaction score:** 4.99 / 10
- **Patients referred:** 3,816

The existing project summary also highlights Monday as the busiest day, several peak traffic hours, General Practice as the leading referral department, and adults aged 30–39 as the largest patient group. Validate these findings against the current Power BI report and filter context before using them for decisions.

## Business Questions

The dashboard is designed to help explore:

- How does patient volume change by month, day, and hour?
- What is the average patient waiting time?
- How do admission and non-admission counts compare?
- Which departments receive the most referrals?
- How do patient demographics vary?
- What satisfaction scores are recorded, and how much data is missing?
- When are emergency room demand peaks?

## Open the Project

1. Open `powerbi/hospital-emergency-dashboard.pbix` in Microsoft Power BI Desktop.
2. If Power BI requests the source file, point it to `dataset/Hospital ER_Data.csv`.
3. Check the Power Query steps, column data types, date locale, relationships, and DAX measures.
4. Refresh the data and compare the report's totals with the source CSV.
5. Use the images in `dashboard/` as static previews of the report.

## Project Documentation

The accompanying report is stored at:

`docs/Hospital Emergency Room Dashboard – Project Report.docx`

## Limitations

This repository contains the Power BI report and supporting project files. The internal DAX expressions, Power Query steps, relationships, and visual interactions have not been independently validated as part of this README update. The findings listed above are reported project summaries and should be verified in Power BI before being treated as final.

## Conclusion

This project demonstrates the use of Power BI to turn emergency room records into operational views of patient volume, wait times, referrals, admissions, and satisfaction.
