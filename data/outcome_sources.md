# Outcome Data Sources

Compiled for: Kenya county-level development outcome data (47 counties), to be matched with
county fiscal data for FY2013/14–FY2023/24. All figures in the CSV outputs were read directly
from the sources listed below (page/table references given); nothing was estimated or interpolated
unless explicitly noted.

## 1. Gross County Product (GCP) — `county_gcp.csv`

- **KNBS Gross County Product – 2019 edition** (covers 2013–2017, current & constant 2009 prices,
  per-capita GCP)
  URL: https://www.knbs.or.ke/wp-content/uploads/2023/08/Kenya-Gross-County-Product-2019.pdf
  Tables used: Table 4 (GCP current prices 2013–2017), Table 6 (GCP constant prices 2013–2017),
  Table 7 (per-capita GCP, current prices, 2013–2017)
  → Used for years 2013–2017 in the final CSV.

- **KNBS Gross County Product – 2021 edition** (covers 2013–2020, current & constant 2016 prices)
  URL: https://www.knbs.or.ke/wp-content/uploads/2023/08/Kenya-Gross-County-Product-2021.pdf
  Tables: Table 1 (current prices 2013–2020), Table 2 (constant prices 2013–2020).
  → Downloaded and reviewed for cross-validation/revision context (the 2021 edition revises the
  2013–2017 series relative to the 2019 edition — national GCP totals differ, e.g. Nairobi 2013
  nominal GCP = 1,003,072 KSh mn in the 2019 edition vs 1,328,511 KSh mn in the 2021 edition,
  reflecting a rebasing to 2016 prices). This edition's 2013–2017 and 2018–2020 values were NOT
  used in the final CSV (superseded by the 2019 edition for 2013–2017, for per-capita-table
  completeness, and by the 2023/2025 editions for 2018–2020) — see Gaps section below. The 2021
  edition does not contain a full per-capita-by-county-by-year table (only narrative figures for
  4 counties in 2019: Nairobi City 596,467; Mombasa 394,281; Nyeri 257,268; Elgeyo/Marakwet
  231,239 KSh, p.11 of the PDF).

- **KNBS Gross County Product – 2023 edition** (covers 2018–2022, current & constant 2016 prices)
  URL: https://www.knbs.or.ke/wp-content/uploads/2024/05/Gross-County-Product-2023-min.pdf
  Tables used: Table 1 (GCP current prices 2018–2022), Table 3 (GCP constant 2016 prices,
  2018–2022), Annexe IV (GCP per capita, 2018–2022).
  → Used for years 2018–2019 in the final CSV (2020–2022 superseded by the 2025 edition below).

- **KNBS Gross County Product – 2025 edition** (covers 2020–2024, current & constant 2016 prices)
  URL: https://www.knbs.or.ke/wp-content/uploads/2025/12/2025-Gross-County-Product.pdf
  Tables used: Table 8 (GCP current prices 2020–2024), Table 10 (GCP constant 2016 prices,
  2020–2024), Annexe IV (GCP per capita, 2020–2024). Table 1 of this edition also provides 2019
  census population and KNBS population projections for 2020–2024 by county (not used in the
  final population CSV, which is restricted to actual census years, but available in this PDF
  if projected-population figures are wanted for intercensal years).
  → Used for years 2020–2024 in the final CSV.

**Selection rule applied:** where multiple editions cover the same year, the most recent edition
was used, EXCEPT for 2013–2017, where the 2019 edition was used in preference to the revised 2021
edition because the 2019 edition is the only one with a complete nominal+real+per-capita table for
those years (the 2021 edition lacks a per-capita-by-year table). `county_gcp.csv` records the
edition, source URL and table used for every row (`source_edition`, `source_url`, `source_table`
columns).

## 2. County poverty headcount rate — `county_poverty.csv`

- **KNBS "Basic Report on Well-Being in Kenya" (based on the 2015/16 KIHBS)**
  URL (direct PDF download): https://statistics.knbs.or.ke/nada/index.php/catalog/13/download/60
  Table used: Table 4.3 "Overall Poverty Estimates (individual) by residence and County, 2015/16"
  (p.50 of the PDF). Survey year recorded as "2015/16".
  Note: the companion "KIHBS 2015/16 Basic Report" (the main socio-economic survey report,
  https://open.africa/dataset/4abbeb30-10c2-4842-96c4-188dd5745a84/resource/e6101063-3303-49fd-afd3-e9206cca53b1/download/kihbs-2015_16-basic-report.pdf)
  was also downloaded and checked — it does NOT contain a poverty chapter (poverty analysis was
  published separately in the "Basic Report on Well-Being in Kenya" cited above).

- **KNBS "The Kenya Poverty Report 2022"** (based on the 2022 Kenya Continuous Household Survey)
  URL: https://www.knbs.or.ke/wp-content/uploads/2024/10/The-Kenya-Poverty-Report-2022.pdf
  Table used: Table 4.4 "Overall poverty rates (individuals) by residence and county, 2022" (p.36).
  Survey year recorded as "2022".

**Gap:** 2005/06 KIHBS county-level poverty headcount was NOT retrieved. The "Basic Report on
Well-Being in Kenya (2015/16)" only gives a NATIONAL-level 2005/06-vs-2015/16 trend comparison
(Table 4.5, p.57 — national overall poverty rate 46.8% in 2005/06 vs 36.1% in 2015/16), not a
county-level breakdown. The primary 2005/06 KIHBS "Basic Report on Well-Being" report presents
results by the 158 pre-2010 districts, not the 47 current counties, and reconciling district-level
2005/06 figures to the 47 counties would require an assumption-based mapping, which was avoided
per the "never estimate" rule. Not included in the CSV.

## 3. County population — `county_population.csv`

- **KNBS 2019 Kenya Population and Housing Census, Volume I** (Population by County and Sub-County)
  URL: https://open.africa/dataset/9b94fe50-9d75-4b92-be00-6354c6e6cc88/resource/778659b5-c5ab-4d13-9f89-f61baf9cf32a/download/volume-1-kphc-2019.pdf
  Table used: Table 2.2 "Distribution of Population by Sex and County" (p.7). Census year 2019.

- **2009 Kenya Population and Housing Census county totals**
  URL: https://en.wikipedia.org/wiki/List_of_counties_of_Kenya_by_population
  Used as a secondary compilation citing the official 2009 KNBS census, because the primary KNBS
  2009 volume that was downloaded and inspected
  (https://open.africa/dataset/68e742cd-07cf-4560-8d60-f710715c73e8/resource/926b197a-f5fd-4608-851a-4d3c009a44a9/download/kenya-population-and-housing-census-2009.pdf,
  546 pages) tabulates the 2009 census by the 158 pre-devolution districts/provinces (Table 1:
  "Population Distribution by Age, Sex, Province and District"), not by the 47 current counties,
  and a dedicated "Volume 1B – Population Distribution by Political Units" (which the KNBS
  metadata catalogue says covers counties/constituencies) could not be located as a distinct,
  directly downloadable file in the time available (the KNBS webpage titled "Volume 1B" that was
  found actually redistributes the same age/sex-by-district volume).
  Cross-validation: the Wikipedia table's 2019 figures were checked against the KNBS 2019 Census
  Volume I table above for all 47 counties and matched exactly (e.g., Nairobi City 4,397,073;
  Kiambu 2,417,735; Nakuru 2,162,202), which supports confidence in its sourcing/accuracy for the
  2009 column as well, though the 2009 figures themselves are not independently re-verified against
  a primary KNBS county-level table.

## 4. County development project outcomes — `county_projects.csv`

- **National Treasury, "A list of Stalled Projects" (Treasury Circular No. 9-2018)**
  URL: https://libraryir.parliament.go.ke/bitstreams/e1d68f36-4eed-4303-a2f6-6efaed65b90d/download
  (38 MB, 38 pages). DOWNLOADED but found to be a scanned/garbled-encoding document — text
  extraction (via PyMuPDF) returns corrupted/unreadable characters (broken font-to-Unicode mapping,
  not plain scanned images either), and no OCR engine (e.g. Tesseract) was available in the
  environment to attempt image-based extraction. No usable county-level figures could be extracted
  from this document. Recorded as a located-but-unreadable source; zero rows derived from it.

- **Office of the Controller of Budget (OCoB), "County Governments Budget Implementation Review
  Report for the Financial Year FY 2022/23"** (September 2023)
  URL: https://cob.go.ke/download/county-governments-budget-implementation-review-report-for-the-financial-year-fy-2022-23/?wpdmdl=15957
  (748 pages). This is the source actually used in `county_projects.csv`. Each county chapter
  contains a table titled "[County] County, List of Development Projects with the Highest
  Expenditure" — a curated list (typically 8–25 projects) of each county's highest-value
  development projects in FY 2022/23, with a "Contract Sum / Budget / Amount Paid to Date /
  Implementation Status (%)" (or, for Vihiga and West Pokot, a free-text "Remarks" column instead
  of a numeric status). For each county the table extracted: `projects_total` = number of rows in
  this table; `projects_completed` = number of those rows reported at 100% implementation status
  (or, for Vihiga, rows whose remarks state "Works complete"). `projects_stalled` is left NA for
  every county because the source reports only % implementation / free-text remarks, not an
  explicit "stalled" designation — treating <100%-complete as "stalled" would be an unsupported
  inference (a project at 80% could simply be legitimately in progress and on schedule).
  `value_kes` is left NA because the monetary columns are inconsistent across counties (some
  tables report Contract Sum + Budget + Amount Paid + FY Expenditure, others only Budget + Amount
  Paid, etc.), and reliably identifying/summing a single comparable "value" field per county
  without risking double-counting or wrong-column errors was not possible in the time available.

- Secondary/news coverage reviewed for context (NOT used for CSV figures, since no official
  structured per-county table could be directly fetched/read from them): an Eastleigh Voice
  article (inaccessible, HTTP 403) citing an unspecified 2023/24 Auditor-General report figure of
  "688 stalled projects worth Sh23.3 billion" and "249 projects worth Sh20 billion across 33
  counties"; and separate reporting on a later (FY2025/26-period) COB release citing "237 projects
  stalled/abandoned/underutilised across 32 counties, worth KSh 13.7 billion". These aggregate,
  national-level figures were not attributed to individual counties in a verifiable, directly-read
  table and were therefore excluded from the CSV.

- Also reviewed: COB "Consolidated County Reviews" publication list
  (https://cob.go.ke/publications/consolidated-county-reviews/), which lists all COB County
  Budget Implementation Review Reports from FY2022/23 through FY2025/26. Only the FY2022/23 report
  was downloaded and parsed (see above); an attempt to download the FY2023/24 report
  (https://cob.go.ke/download/county-governments-budget-implementation-review-report-for-the-financial-year-2023-24/?wpdmdl=16104)
  repeatedly produced a corrupted PDF (0 readable pages despite a valid PDF header and plausible
  file size) and was not used.

- Office of the Auditor-General county government audit reports page
  (https://www.oagkenya.go.ke/2023-2024-county-government-audit-reports/) was located but returned
  only a cookie-consent page on fetch; individual county audit report PDFs (which reportedly
  contain stalled-project findings per the news coverage above) were not individually downloaded
  given the time budget.

## 5. Optional: water/electricity/sanitation access (2019 Census Vol IV) and KMHFL health
facility counts by county

NOT retrieved. A brief search located the Kenya Master Health Facility List (KMHFL) dashboard
(https://kmhfl.health.go.ke/#/facility_filter/results) and the 2023 Kenya Health Facility Census
(total of 14,883 facilities nationally, no county breakdown found in the time available without
scraping the interactive dashboard), and the 2019 Census Volume IV was not fetched at all. These
are flagged as gaps rather than populated with estimated figures, per the "optional if easily
available" instruction and the "never estimate" rule.

## Other sources consulted (discovery only, not directly cited for figures)

- https://www.knbs.or.ke/gross-county-product/ (GCP landing page, used to discover edition PDFs)
- https://www.knbs.or.ke/reports/gross-county-product-2023/ and
  https://www.knbs.or.ke/reports/2025-gross-county-product/ (edition landing pages)
- https://repository.knbs.or.ke/entities/publication/4960bddb-e24b-40f8-9c96-afa4b1e16549 (GCP 2021
  repository record)
- https://www.knbs.or.ke/comprehensive-poverty-report/ and the "Comprehensive Poverty Report"
  wpdmpro link (resolved to the KNBS homepage HTML rather than a PDF; not usable — superseded by
  the "Basic Report on Well-Being in Kenya" source used above)
- https://statistics.knbs.or.ke/nada/index.php/catalog/68/pdf-documentation (2009 census metadata,
  confirms the 158-district tabulation and the existence of a separate political-units volume that
  could not be located directly)
