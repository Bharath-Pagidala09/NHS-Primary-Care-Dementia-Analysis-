# UK Dementia Data Visualisation - NHS Primary Care Analysis

## Overview
This project analyses NHS Primary Care dementia data for the UK, 
focusing on adults aged 65 and over. Two interactive visualisations 
were built using Tableau Public — one targeting a public news audience 
and one aimed at NHS Directors for internal planning and resource 
allocation. Data preprocessing was carried out using Excel Power Pivot 
and Python before visualisation.

---

## What Was Done

### 1. Data Preprocessing
Two NHS datasets were used and required significant cleaning before 
analysis:

- The Cognitive Impairment dataset had an unclean measure column 
  containing values like MCI_GENDER_AGED_X_Y. Using Power Pivot and 
  a delimiter, this was split into two separate fields Gender and 
  Age Range
- The Dementia Type dataset originally stored dementia types as row 
  values in a single column. Using Python, the dataset was transposed 
  so that each dementia type became its own column
- The Summary dataset was filtered to September 2024 only, with 
  missing ODS codes removed
- An inner join was performed between the Summary and Dementia Type 
  datasets using the ONS Code, resulting in a final dataset of 
  42 rows and 15 columns

---

### 2. Visualisation 1 - Dementia by Gender (Public News Audience)
**Tableau Link:**
https://public.tableau.com/views/1main/Public

Key findings from the charts produced:

- Females account for 54% of all dementia cases, males 46%
- The 75 to 79 age group had the highest number of cases for 
  both genders each month
- The 40 to 44 age group had the fewest cases
- Females accounted for 65% of cases in the 90+ age group
- Sub-ICB locations recorded the most cases across all months 
  and age groups
- Dementia cases grew consistently from June to September 2024

Charts used: bar chart, tree map, pie chart and bubble chart 
with interactive tooltip showing the top 10 care boards by 
dementia patient count.

---

### 3. Visualisation 2 - Estimated Diagnosis Rates in Adults 65+ (NHS Directors)
**Tableau Link:**
https://public.tableau.com/views/2Main/NHS

Key findings from the charts produced:

- Most care boards (11 in total) have diagnosis rates between 
  60% and 62%, suggesting consistent identification practices 
  across regions
- Top three care boards by estimated patients: QRL (17,084), 
  QKS (15,535) and QU9 (14,626)
- NHS North East and North Cumbria had the highest estimated 
  cases at 41,154, followed by NHS Cheshire and Merseyside 
  (34,733) and NHS Greater Manchester (30,489)
- The scatter plot showed a weak positive relationship between 
  estimated patient numbers and diagnosis rates — R-squared of 
  0.0226 and p-value of 0.342, meaning patient volume alone does 
  not explain diagnosis accuracy
- Alzheimer's disease was the most common dementia type with 
  115,465 estimated cases, followed by Other Dementia Types 
  (86,620) and Vascular Dementia (42,990)
- Less common types: Mixed Dementia (18,550), Lewy Body (8,810), 
  Inconclusive (4,515) and Frontotemporal (1,945)

Charts used: histogram, bullet graph, scatter plot and bar chart 
with interactive tooltips.

---

## Key Takeaway
Women are disproportionately affected by dementia, particularly in 
older age groups. Regional diagnosis rates vary significantly across 
NHS care boards, highlighting gaps in screening and awareness. 
Alzheimer's disease dominates across all regions and should remain 
a priority for NHS resource allocation and research. Data-driven 
visualisations like these can directly support NHS Directors in 
identifying high-need regions and planning early intervention 
strategies.

---

## Tools Used
- **Tableau Public** — interactive data visualisations
- **Excel Power Pivot** — data cleaning and preprocessing
- **Python** — dataset transposing and restructuring
- **NHS England Datasets** — Primary Care Dementia Data, 
