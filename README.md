# Australia vs New Zealand Workforce Qualifications

A data science project comparing **industry structure and workforce qualification profiles in Australia and New Zealand** using the **2021 Australian Census** and **2023 New Zealand Census**.

The project investigates whether differences in national qualification levels are mainly caused by:

1. the two countries having different mixes of industries, or
2. workers within the same industries having different qualification profiles.

This project was completed for **CITS2402 – Introduction to Data Science** at The University of Western Australia.

---

## Research Question

> **How do the post-school qualification profiles of the Australian (2021) and New Zealand (2023) workforces differ across industries, from no post-school qualification to postgraduate degree? Are the differences mainly explained by the industries that employ people in each country, or by differences in qualification levels within the same industries?**

---

## Project Overview

Australia and New Zealand have similar labour markets, but their census datasets use different qualification classifications.

This creates an interesting data science problem: the two datasets cannot simply be joined and compared directly.

The project therefore:

- cleans and restructures raw census data;
- aligns Australian and New Zealand industry categories;
- creates comparable qualification groups;
- compares qualification profiles across industries;
- examines broader sector-level patterns;
- measures similarity using **Spearman rank correlation**;
- decomposes national differences into:
  - **industry-mix effects**, and
  - **within-industry effects**;
- performs a **sensitivity analysis** for uncertain qualification mappings;
- extends the analysis from workers with post-school qualifications to the **whole workforce**.

---

## Data Sources

### Australia

Data comes from the **2021 Australian Census General Community Profile DataPack**, published by the Australian Bureau of Statistics (ABS).

The project uses:

- `G53A`
- `G53B`
- `G53C`

These contain information on:

**Highest non-school qualification × industry of employment**

The project also uses:

- `G54A`
- `G54B`
- `G54C`
- `G54D`

These provide total employment counts by industry and are used to extend the analysis to the whole workforce.

### New Zealand

Data comes from the **2023 New Zealand Census**, accessed through Stats NZ's Aotearoa Data Explorer.

The dataset used is:

```text
STATSNZ_CEN23_EDU_003_1_0_2023_9999___99.csv
