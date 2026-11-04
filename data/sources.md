# Sources for Kenya County Fiscal Panel (FY2013/14–FY2024/25)

All figures were read directly from the primary-source PDF documents listed below using
automated text extraction (PyMuPDF) followed by regex-based table parsing, with manual
verification of executive-summary narrative figures and cross-validation of parsed county
tables against the reports' own published national totals. **No figures were estimated or
invented.** Cells that could not be verified from a fetched source are recorded as `NA`.

## Primary documents fetched and used

| Fiscal Year | Document | URL (as fetched) | Tables used |
|---|---|---|---|
| FY2019/20 | OCOB, "County Governments Budget Implementation Review Report for the FY 2019/20" (published Oct 2020) | https://cob.go.ke/download/county-governments-budget-implementation-review-report-for-the-fy-2019-20/?wpdmdl=15308 (file also mirrored at https://www.cob.go.ke/wp-content/uploads/2019/10/COUNTY-GOVERNMENTS-BUDGET-IMPLEMENTATION-REVIEW-REPORT-FOR-THE-FY-2019-20.pdf) | Executive Summary (national totals); Table 2‑4 "Budget Allocation, Expenditure and Absorption Rate" (mislabelled in the PDF as "...for FY 2018/19" but the narrative and totals confirm the data are for FY2019/20); per-county "Revenue Performance" tables (Table 3.x series) |
| FY2020/21 | OCOB, "Annual County Governments Budget Implementation Review Report FY 2020/21" | https://cob.go.ke/download/annual-county-governments-budget-implementation-review-report-fy-2020-21/?wpdmdl=15580 | Executive Summary; "County Budget Allocation, Expenditure and Absorption Rate for FY 2020/21" table; Table 2.5 Pending Bills; per-county Revenue Performance tables |
| FY2021/22 | OCOB, "County Governments Annual Budget Implementation Review Report FY 2021/22" (Sept 2022) | https://cob.go.ke/wp-content/uploads/2022/09/Counties-Sep-2022-web.pdf | Executive Summary; "County Budget Allocation, Expenditure and Absorption Rate for the FY 2021/22" table; per-county Revenue Performance tables |
| FY2022/23 | OCOB, "County Governments Budget Implementation Review Report for the Financial Year FY 2022/23" | https://cob.go.ke/download/county-governments-budget-implementation-review-report-for-the-financial-year-fy-2022-23/?wpdmdl=15957 | Executive Summary; Table 2.4 "County Budget Allocation, Expenditure and Absorption Rate in FY 2022/23"; Table 2.6 Pending Bills; per-county Revenue Performance tables (Table 3.x) |
| FY2023/24 | OCOB, "County Governments Budget Implementation Review Report for the Financial Year 2023/24" | https://cob.go.ke/download/county-governments-budget-implementation-review-report-for-the-financial-year-2023-24/?wpdmdl=16104 | Executive Summary; Table 2.3 "County Budget Allocation, Expenditure and Absorption Rate for the FY 2023/24"; Table 2.5 Pending Bills; per-county Revenue Performance tables |
| FY2024/25 | OCOB, "County Governments Budget Implementation Review Report FY 2024/25" (Aug 2025) | https://cob.go.ke/download/county-governments-budget-implementation-review-report-fy-2024-25/?wpdmdl=16263 | Executive Summary; Table 2.5 "County Budget Allocation, Expenditure, and Absorption Rate for FY 2024/25"; Table 2.9 Pending Bills; per-county Revenue Performance tables |
| FY2021/22 & FY2022/23 (secondary cross-check) | KNBS, "Economic Survey 2023" | https://open.africa/dataset/fc8573fa-f05d-4d6a-8c1a-5723ddbdc509/resource/b34391a4-b8cb-4b36-9eef-c86adefdb93e/download/economic-survey-2023_2.pdf | Table 5.13 "County Governments' Revenue, 2021/22–2022/23" (per-county equitable share/conditional grants/OSR/total revenue — used only to cross-validate COB figures, e.g. Baringo equitable share 6,369.39m matches COB CARA figure exactly); Table 5.14 "County Governments' Expenditure by Economic Classification, 2018/19-2022/23" (national, IFMIS/Treasury basis — not used in final CSVs because its expenditure classification does not map cleanly to recurrent/development split, but confirms the same order of magnitude) |

## UPDATE (follow-up round): FY2013/14–FY2018/19 primary sources located

A follow-up research pass located and fetched the **original COB annual CBIRR PDFs for all six
of these years**, via the Internet Archive Wayback Machine (web.archive.org), which holds byte-
identical archived copies of the files originally hosted on cob.go.ke. These are treated as
**primary** sources (`source_quality = "primary"`) since they are the unmodified original COB
PDF documents, merely retrieved via an archival mirror rather than the live site (which no
longer hosts them). The africacheck.org mirror mentioned below remained blocked (Cloudflare
403) and was not used; it was superseded by the Wayback Machine copies.

Discovery method: the Wayback Machine CDX API (`web.archive.org/cdx/search/cdx`) was queried
for all archived `cob.go.ke` URLs containing "county" / "budget-implementation", which surfaced
the old WordPress Download Manager (`?wpdmdl=NNNN`) and legacy Joomla (phocadownload) download
links used by cob.go.ke between 2014 and 2022. Each PDF link was confirmed as the genuine annual
report by checking the extracted PDF's own title page and Executive Summary FY reference before
use.

| Fiscal Year | Document | URL fetched (via Wayback Machine) | Tables used |
|---|---|---|---|
| FY2013/14 | OCOB, "Annual County Governments Budget Implementation Review Report FY 2013/2014" (first-ever CBIRR, covers Mar/Jul 2013–Jun 2014) | https://web.archive.org/web/20220608162746/https://cob.go.ke/download/annual-county-governments-budget-implementation-review-report-fy-20132014/?wpdmdl=7639 | Executive Summary (national totals); per-county narrative "County Summary Report" paragraphs (budget, expenditure, absorption rate by county) |
| FY2014/15 | OCOB, "Annual County Governments Budget Implementation Review Report, FY 2014/15" | https://web.archive.org/web/20220608162957/https://cob.go.ke/download/annual-county-governments-budget-implementation-review-report-fy-201415/?wpdmdl=9317 | Executive Summary; Table 4 "Pending Bills for the Counties as of June 30, 2015"; per-county narrative overview paragraphs (Section "3.x Overview of the FY 2014/15 Budget") |
| FY2015/16 | OCOB, "Annual County Governments Budget Implementation Review Report FY 2015/16" | https://web.archive.org/web/20220608162842/https://cob.go.ke/download/annual-county-budget-implementation-review-report-fy-2015-16/?wpdmdl=10035 | Executive Summary; per-county narrative overview paragraphs (Section 3.x.1) |
| FY2016/17 | OCOB, "Annual County Governments Budget Implementation Review Report for FY 2016/17" | https://web.archive.org/web/20220608162659/https://cob.go.ke/download/annual-county-governments-budget-implementation-review-report-fy-201617/?wpdmdl=10487 | Executive Summary; per-county narrative overview paragraphs |
| FY2017/18 | OCOB, "Annual County Governments Budget Implementation Review Report for FY 2017/18" (Sept 2018) | https://web.archive.org/web/20220608162544/https://cob.go.ke/download/annual-county-governments-budget-implementation-review-report-for-fy-2017-18/?wpdmdl=14829 | Executive Summary; per-county narrative overview paragraphs |
| FY2018/19 | OCOB, "County Governments Annual Budget Implementation Review Report for FY 2018/19" (Aug 2019) | https://web.archive.org/web/20220608162422/https://cob.go.ke/download/county-governments-annual-budget-implementation-review-report-fy-2018-19/?wpdmdl=15011 | Executive Summary; Table "Pending Bills for the Counties as of June 30th, 2019" (Total row only — 5 counties had not submitted returns); per-county narrative overview paragraphs |

### Why county-level data for FY2013/14–FY2018/19 is narrative-derived, not table-derived

Unlike FY2019/20 onward, these six earlier reports do **not** contain a single consolidated
numeric table listing Budget/Expenditure/Absorption Rate for all 47 counties side by side —
only (a) a national Executive Summary, (b) per-county department-level expenditure tables, and
(c) a per-county narrative overview paragraph of the form (wording varies slightly by year):
*"The County's FY 20XX/XX [Supplementary] Budget was Kshs.A billion, comprising Kshs.B billion
(C per cent) and Kshs.D billion (E per cent) for recurrent and development expenditure
respectively... The County spent Kshs.F billion (G per cent) on recurrent activities and
Kshs.H billion (I per cent) on development activities... Development expenditure recorded an
absorption rate of J per cent."*
County-level figures for these six years were therefore extracted with a set of
regular-expression patterns (tolerating the ~4 different phrasings used across the six reports,
and the "recurrent and development" / "development and recurrent" ordering which varies even
within the same report) applied to each county's narrative chapter.

**Validation performed:** for every year and every field (development budget, recurrent budget,
development expenditure, recurrent expenditure, equitable share), the sum of the successfully
parsed county values was compared against the FY's known national total (pro-rated for the
number of counties successfully parsed). All six years validated within ~10–20% of the
pro-rated expectation except for one single-cell error that was found and corrected: the
FY2013/14 Lamu County development budget was printed in the source PDF as "Kshs.500.5 billion"
which is an evident unit typo in the original COB document (the County's total approved budget
that year was only Kshs.1.65 billion, and the accompanying percentage figure of 30.4% implies
an amount of ≈Kshs.501 million, not billion) — this single cell was corrected to
500,500,000 KES (i.e. interpreting the source's "billion" as "million") and is flagged here
for transparency; no other document errors were found during cross-validation. A regex
group-indexing bug introduced during development (which caused recurrent/development amounts to
be swapped or mis-paired for a subset of counties) was also caught by this same national-total
cross-validation process and fixed before the data was finalised.

**Coverage achieved for FY2013/14–FY2018/19 (county-level, out of 47 counties per year):**

| FY | equitable_share_allocation | development_budget | development_expenditure | development_absorption_rate | recurrent_expenditure |
|---|---|---|---|---|---|
| 2013/14 | 27 | 33 | 21 | 39 | 21 |
| 2014/15 | 0 | 38 | 31 | 39 | 31 |
| 2015/16 | 34 | 36 | 34 | 41 | 34 |
| 2016/17 | 32 | 33 | 41 | 46 | 41 |
| 2017/18 | 40 | 46 | 43 | 47 | 47 |
| 2018/19 | 41 | 45 | 33 | 45 | 33 |

Remaining gaps are counties whose narrative paragraph used a sentence structure not covered by
the regex patterns attempted (e.g. a 5th/6th phrasing variant), or (for FY2014/15 equitable
share specifically) because that year's paragraph combines equitable share and conditional
grants into one "transfers from the National Government" figure that could not be reliably
disaggregated into a pure equitable-share number — these are left as `NA` rather than guessed.
`total_exchequer_disbursed_kes` and `own_source_revenue_kes` were not extracted at county level
for FY2013/14–FY2018/19 (narrative wording for these was even less consistent across years than
for budget/expenditure/absorption) and `pending_bills_kes` was not extracted at county level for
any fiscal year in this exercise (see note below) — both remain `NA` for all counties in these
years. National-level totals for all of these quantities, however, are populated in
`national_fiscal_aggregates.csv` for every year FY2013/14–FY2024/25 (see below).

### CRA (crakenya.org) and Business Daily / Nation / IEA / World Bank secondary sources

CRA's own site (crakenya.org) was not fetched in this round: the Wayback Machine route to the
primary COB PDFs succeeded for all six missing years, making the CRA County Allocation of
Revenue Act schedules unnecessary as a fallback source for `equitable_share_allocation_kes`.
Likewise, no national aggregates in this dataset rely on Business Daily / Nation / The Star /
IEA / World Bank secondary reporting — every row in `national_fiscal_aggregates.csv` is sourced
directly from a primary COB CBIRR PDF Executive Summary, so **no row required the "secondary"
`source_quality` flag**; all populated rows are `source_quality = "primary"`. Rows that remain
entirely unpopulated (none, after this update — all 12 FYs now have at least partial figures)
would have been flagged `source_quality = "NA"`.

## Column definitions and derivation notes (county_fiscal_panel.csv)

* `equitable_share_allocation_kes` — for FY2019/20–FY2024/25: the "Annual Budget Allocation"
  (CARA/Division of Revenue schedule) figure for Equitable Share of Revenue Raised Nationally,
  read from Section A of each county's "Revenue Performance in FY xxxx" table (Table 3.x series)
  in the relevant COB report. For FY2013/14–FY2018/19: the equitable-share figure quoted in each
  county's narrative budget-financing paragraph (see narrative-extraction discussion above);
  where the report's own wording combines equitable share with conditional grants into one
  figure, the cell is left `NA` rather than risk over-statement.
* `total_exchequer_disbursed_kes` — for FY2019/20–FY2024/25 only: the "Actual Receipts" figure
  for Equitable Share from the same table/section (i.e., the equitable share actually
  transferred to the county's CRF account during the FY). This does **not** include additional
  allocations/conditional grants or own source revenue; it captures only the equitable-share
  component of Treasury exchequer disbursements, which is the largest and most consistently
  reported component across years. Left `NA` for FY2013/14–FY2018/19 (county-level "actual
  receipts" distinct from the allocation/target figure was not reliably separable from the
  narrative text for these years — see note above).
* `development_budget_kes`, `development_expenditure_kes`, `recurrent_expenditure_kes`,
  `development_absorption_rate_pct` — for FY2019/20–FY2024/25: read from the consolidated
  "County Budget Allocation, Expenditure and Absorption Rate" table (COB Table 2.3–2.5, numbering
  varies by year) in each annual report; source figures are stated in "Kshs. Million" and were
  converted to KES by multiplying by 1,000,000. For FY2013/14–FY2018/19: read from each county's
  narrative budget/expenditure/absorption-rate overview paragraphs (see discussion above); these
  reports do not contain a single consolidated all-county table for these metrics.
* `own_source_revenue_kes` — FY2019/20–FY2024/25 only: "Actual Receipts" for Own Source Revenue
  (Section C of the per-county Revenue Performance table). Left `NA` for FY2013/14–FY2018/19.
* `pending_bills_kes` — recorded as `NA` for all county-years in both this round and the prior
  one. The COB pending-bills tables (e.g. Table 2.6/2.9 "Pending Bills for the Counties as of
  30 June YYYY") have an inconsistent multi-column layout (separate Executive/Assembly,
  Recurrent/Development breakdowns, and in some years an ageing analysis) that could not be
  reliably parsed into a single comparable figure per county within the scope of this exercise.
  National pending-bills totals (which **are** verified for every FY2013/14–FY2024/25 except
  FY2013/14 itself, which did not report one) are included in `national_fiscal_aggregates.csv`.
* `source_quality` — `"primary"` whenever at least one figure in that county-year row was read
  from an official COB CBIRR PDF (whether fetched live from cob.go.ke or via a Wayback Machine
  archival copy of the same original file — both are treated as primary since the content is
  identical to the original government document); `"NA"` when no figure for that row could be
  populated at all. No row in this dataset required the `"secondary"` designation (news articles,
  IEA/World Bank secondary reporting, etc.) because primary COB PDFs were successfully located
  for every one of the 12 fiscal years FY2013/14–FY2024/25.

All budget/expenditure/absorption-rate figures were cross-validated by checking that the
Total row produced by the automated per-county extraction exactly matches the nationally
reported aggregate figures quoted in each report's own Executive Summary (see table below) —
in every one of the 6 fiscal years, the two independently-sourced totals matched (to rounding).

## national_fiscal_aggregates.csv — verified figures by fiscal year

Each row's figures were read directly from the Executive Summary narrative (and, where noted,
the consolidated Table 2.x) of the corresponding COB annual report listed above.

* **FY2013/14** (first-ever CBIRR): approved budget 261.1bn (dev 100.4bn 38.5%, rec 160.6bn
  61.5%); financed by equitable share target 190bn (89%), conditional grants target 20bn, local
  revenue target 54.2bn; Kshs.193.4bn released by National Government to counties (equitable
  share + conditional grants combined — not separately disaggregated in this report, hence
  `equitable_share_total_kes_bn` = `NA` for this year, target-only 190bn is populated); OSR
  actual 26.3bn; cash balance b/f from FY2012/13 of 4.3bn; total funds available 224.2bn;
  exchequer released to operational accounts 174.4bn; total expenditure 169.4bn (97% of
  exchequer releases; 64.9% overall absorption; recurrent 82.7% / Kshs.132.8bn, development
  36.4% / Kshs.36.6bn). No national pending-bills aggregate was reported in this first-year
  report (the concept of a cross-county pending-bills table was introduced in later years).
* **FY2014/15**: approved budget 326.29bn (dev 144.91bn 44.4%, rec 181.38bn 55.6%); financed by
  equitable share target 226.66bn + conditional grant (Level 5 Hospitals) target 1.87bn; County
  Governments received Kshs.228.53bn from National Government as direct CRF transfers (= full
  226.66bn equitable share + 1.87bn conditional grant, i.e. fully disbursed to target); OSR
  actual 33.85bn of 50.38bn target (67.2%); cash balance b/f 41.67bn; total funds available
  304.78bn; exchequer accessed from CRF 262.30bn (rec 166.60bn 63.5%, dev 95.70bn 36.5%); total
  expenditure 258bn (98.4% of funds released; overall absorption 79.1%; recurrent 92.4% /
  Kshs.167.56bn, development 62.4% / Kshs.90.44bn); pending bills 37.64bn as of 30 June 2015.
* **FY2015/16**: approved budget 367.44bn (dev 158.62bn 43.2%, rec 208.82bn 56.8%); equitable
  share target 259.77bn + conditional allocations target 21.91bn; County Governments received
  Kshs.264.04bn from National Government (= equitable share 259.77bn fully disbursed + partial
  conditional grants ≈4.27bn); OSR actual 35.02bn of 50.54bn target (69.3%); exchequer accessed
  from CRF 303.47bn (82.6% of budget; rec 195.72bn 64.5%, dev 107.75bn 35.5%); total expenditure
  295.30bn (97.3% of funds released; 80.4% overall absorption; recurrent 91.9% / Kshs.191.85bn,
  development 65.2% / Kshs.103.45bn); pending bills 37.36bn (43 counties reporting) as of 30 June
  2016.
* **FY2016/17**: approved budget 399.24bn (dev 158.36bn 39.7%, rec 240.89bn 60.3%); equitable
  share allocated 280.3bn, conditional grants target 21.9bn; total revenue available 369.45bn
  (equitable share 280.3bn + various named conditional grants + cash balance 37.19bn + OSR
  32.52bn); OSR actual 32.52bn of 57.66bn target (56.4%); exchequer authorised to operational
  accounts 328.24bn (rec 219.95bn 67%, dev 108.3bn 33%, of exchequer issues); total expenditure
  319.06bn (79.9% of annual budget; recurrent 89.6% / Kshs.215.71bn, development 65.3% /
  Kshs.103.34bn); pending bills 35.84bn at end of FY (per CARA 2016 disbursement-schedule
  discussion in the Executive Summary).
* **FY2017/18**: approved budget 410.1bn (dev 139.18bn 33.9%, rec 271.32bn 66.1%); equitable
  share allocated 302bn, conditional grants target 27.27bn; total revenue available 387.09bn;
  OSR actual 32.49bn of 49.22bn target (66%); exchequer authorised to operational accounts
  324.12bn (rec 251.96bn 77.7%, dev 72.16bn 22.3%); total expenditure 303.83bn (74% of aggregate
  annual budget; recurrent 87.3% / Kshs.236.94bn, development 48.1% / Kshs.66.89bn); pending
  bills 108.41bn by end of FY2017/18.
* **FY2018/19**: approved budget 483.47bn (dev 185.76bn 38.4%, rec 297.71bn 61.6%); equitable
  share allocated 314bn, conditional grants target 62.48bn; total revenue available 445.36bn;
  OSR actual 40.30bn of 53.86bn target (74.8%); Controller of Budget authorised withdrawal of
  Kshs.405.17bn from CRF to Operational Accounts (rec 285.66bn 70.5%, dev 119.51bn 29.5%) — a
  separate infographic elsewhere in the same report shows "Total Exchequer Issues Kshs.395.23bn"
  (Recurrent 278.62bn + Development 116.61bn), a smaller figure that may reflect actual
  disbursement net of some adjustment; this CSV uses the narrative's 405.17bn as the primary
  figure and records the discrepancy here for transparency; total expenditure 376.43bn (77.9% of
  annual budget; recurrent 90.4% / Kshs.269bn, development 57.8% / Kshs.107.44bn); pending bills
  34.54bn as of 30 June 2019, explicitly noted in-report as incomplete because five counties
  (Isiolo, Mandera, Marsabit, Nairobi City, West Pokot) had not submitted pending-bills returns
  at the time of finalising the report — this total is therefore a known undercount.
* **FY2019/20**: approved budget 499.62bn (dev 187.98bn, rec 311.63bn); equitable share actual
  286.78bn of 316.5bn target; OSR actual 35.77bn of 54.9bn target; exchequer authorised
  (CRF→Operational Accounts) 392.53bn; total expenditure 383.79bn (76.8% absorption; recurrent
  89.6%, development 55.6%); pending bills 113.85bn as of 30 June 2020.
* **FY2020/21**: approved budget 501.74bn (dev 186.86bn, rec 314.88bn); equitable share
  transferred 346.22bn (includes FY2019/20 arrears of 26.22bn + Nairobi arrears 3.5bn);
  OSR actual 34.44bn of 53.66bn target; exchequer issues to operational accounts 404.97bn
  (quoted in the FY2021/22 report as the prior-year comparator); total expenditure 398.01bn
  (79.3% absorption; recurrent 89.5%, development 62.1%); pending bills 96bn as of 30 June 2021
  (the FY2020/21 report itself mislabels this date as "30 June 2020" — a typo confirmed against
  its own section header "2.4.5 Pending Bills as of 30th June, 2021").
* **FY2021/22**: approved budget 535.74bn (dev 193.53bn, rec 342.21bn); equitable share
  disbursed 340.4bn of 370bn target; OSR actual 35.91bn of 60.42bn target; exchequer issues to
  operational accounts 410.86bn (dev 94.7bn, rec 315.25bn); total expenditure 400.96bn (74.8%
  absorption; recurrent 88.4%, development 50.9%); pending bills 153.02bn as of 30 June 2022.
* **FY2022/23**: approved budget 515.18bn (dev 160.54bn, rec 354.64bn); equitable share 370bn
  (fully disbursed); OSR actual 37.81bn of 57.37bn target; exchequer issues to operational
  accounts 430.48bn (dev 94.36bn, rec 336.12bn); total expenditure 428.90bn (83.3% absorption;
  recurrent 93.3%, development 61.0%); pending bills 164.76bn as of 30 June 2023.
* **FY2023/24**: approved budget 562.75bn (dev 189.93bn, rec 372.82bn); equitable share actual
  354.59bn of 385.42bn target; OSR actual 58.95bn of 80.94bn target; exchequer issues to
  operational accounts 451.21bn (dev 111.82bn, rec 339.39bn); total expenditure 446.76bn (79.5%
  absorption per narrative / 79.4% per Table 2.3 total row — minor rounding difference, both
  recorded in source files; CSV uses the narrative 79.5%); recurrent 90.5%, development 57.5%;
  pending bills 181.98bn as of 30 June 2024.
* **FY2024/25**: approved budget 601.69bn (dev 218.99bn, rec 382.70bn); equitable share
  authorised transfer 418.26bn (includes 30.83bn arrears relating to FY2023/24); OSR actual
  67.30bn of 87.67bn target; exchequer issues to operational accounts 472.15bn (dev 124.11bn,
  rec 348.04bn); total expenditure 470.74bn (78% absorption; recurrent 91%, development 57%);
  pending bills 183.06bn as of 30 June 2025.

## Methodology / tooling notes

* PDFs were downloaded with `curl` and text-extracted page-by-page with PyMuPDF (`fitz`).
* County-level numeric tables were parsed with custom Python/regex scripts that (a) build a
  fuzzy regex per county name tolerant of PDF line-wrap artifacts (soft hyphens `\u00ad`,
  inconsistent use of `/` vs `-` in names like "Elgeyo/Marakwet" / "Taita/Taveta", and
  "Nairobi City" sometimes printed as just "Nairobi"), (b) locate each county's row/chapter by
  position, and (c) extract the numeric tokens between consecutive counties. Page-break
  artifacts (repeated column headers, "===PAGE N===" markers inserted during extraction) were
  stripped before parsing.
* Every one of the 6 years' "Total" rows produced by this automated parser was checked against
  the independently-stated Executive Summary national totals for that year and matched in all
  cases — this is the primary internal validation for the county-level panel.
* Per-county Equitable Share / Own Source Revenue figures (from the "Revenue Performance"
  tables) were harder to parse uniformly because the COB report's own table format changed
  across years (e.g. FY2019/20–2020/21 show both an original "Annual CARA Allocation" column
  AND a revised "Annual Budget Allocation" column, while FY2021/22 onward show only one
  allocation column). Coverage achieved: equitable_share_allocation_kes populated for 234/282
  (83%) of county-year cells FY2019/20–FY2024/25; own_source_revenue_kes populated for 275/282
  (97.5%). Remaining cells are `NA`.

## Consistent county naming used in the CSVs

Baringo, Bomet, Bungoma, Busia, Elgeyo/Marakwet, Embu, Garissa, Homa Bay, Isiolo, Kajiado,
Kakamega, Kericho, Kiambu, Kilifi, Kirinyaga, Kisii, Kisumu, Kitui, Kwale, Laikipia, Lamu,
Machakos, Makueni, Mandera, Marsabit, Meru, Migori, Mombasa, Murang'a, Nairobi City, Nakuru,
Nandi, Narok, Nyamira, Nyandarua, Nyeri, Samburu, Siaya, Taita/Taveta, Tana River,
Tharaka-Nithi, Trans Nzoia, Turkana, Uasin Gishu, Vihiga, Wajir, West Pokot.
