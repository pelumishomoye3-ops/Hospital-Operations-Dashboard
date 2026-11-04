# Hospital Operations and Financial Intelligence Dashboard

 What this is
A five-page Power BI dashboard built from a hospital dataset of 27,891 encounters, 47,701 procedures and 974 patients (January 2011 to 5 February 2022). It looks at encounter volumes, claim costs, payer coverage and procedure use.

 Key findings
- Payers covered only 30.6% of the $101.5M in recorded claim costs.
- 13,586 encounters (48.7%) have zero recorded payer coverage. 4,779 of them are insured patients, concentrated in five private payers.
- Only 75 encounters (0.27%) lasted more than 24 hours.
- Electrical cardioversion is the most costly frequent procedure.

 What is in this repository
- dashboard/ : the Power BI file
- screenshots/ : each dashboard page and the validation checks
- docs/ : project report, data-quality assessment and KPI definitions

 Data
The dataset was supplied by AnalystLab Africa and is not included here because it contains patient-level records. Names, addresses and coordinates were removed from the patient table before building the model.

 How I built it
1. Imported five CSV files through Power Query and fixed data types.
2. Built a star-style model: encounters in the middle, linked to patients, payers, a date table and procedures.
3. Wrote DAX measures for each KPI (definitions are in docs/).
4. Built five pages: Overview, Trends, Encounter Class, Cost and Coverage, Procedures.
5. Checked the main figures against the raw files outside Power BI.

 Limitations
One hospital, possibly simulated data, 2022 is incomplete, and zero coverage cannot be split into unpaid and unrecorded.

 Tools
Power BI, Power Query, DAX, Excel. I used Claude, an AI assistant, to help explore the data, run checks and draft documentation.

Author: Oluwapelumi Shomoye
