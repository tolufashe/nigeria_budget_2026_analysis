### **DATA DOCUMENTATION**

**Project:** 2026 Nigeria Federal Budget — National Storytelling

\---

#### **SECTION 1 — DATA SOURCES**

Three primary sources were used. All are official government publications downloaded from the Federal Republic of Nigeria Budget Office ([budgetoffice.gov.ng](https://budgetoffice.gov.ng)).

**Source 1: \[2026 Appropriation Bill]** **Length:** 10 pages. This is the enacted law passed by the National Assembly authorising government spending. It serves as the most authoritative source for top-level figures.

* *Pages used:* Page 1 for macro figures (Total Budget, Debt Service, Recurrent, Capital). Page 4 for the debt service breakdown (domestic, foreign, sinking funds). Pages 4 through 9 for individual ministry capital allocations.

**Source 2: \[2026 Appropriation Bill Details]** **Length:** 2,790 pages. This document provides the granular breakdown behind the Bill, detailing allocations across personnel, overhead, and capital.

* *Pages used:* Pages 1 and 2 only (the MDA summary table).

**Source 3: \[2026–2028 Medium Term Expenditure Framework and Fiscal Strategy Paper (MTEF/FSP)]** **Length:** 65 pages. This serves as the government's economic roadmap detailing the assumptions and historical context behind the 2026 budget.

* *Pages used:* Page 11 (statements on debt constraints), Page 15 (2024 parameter performance), Page 18 (2024 expenditure outturns), Page 21 (2025 capital execution data), Pages 31–33 (2026 framework and 2027 projections), and Pages 54–55 (extraction of the ₦149.39 Trillion Total Public Debt stock trend).

#### **SECTION 2 — EVALUATIVE BENCHMARKS \& SECONDARY REFERENCES**

To measure the budget's impact critically, official numbers were tested against established international standards.

* **\[The Abuja Declaration (2001)]:** African Union member states pledged a minimum of 15% of their national budgets to health. This was used to benchmark Nigeria's health allocation.
* **\[UNESCO Education Financing Recommendations]:** Sets a global standard of 15% to 26% of public expenditure for education. This was used to benchmark the education allocation.
* **\[BudgIT 2026 Budget Report]:** Used strictly as a secondary reference for visual layout and structural inspiration. No primary figures were extracted from this civic document; all dataset numbers trace back exclusively to official federal publications.
* **Additional sources: CBN Fiscal Policy Historical** and **PwC Nigeria Budget Insights 2026 / BudgIT**

#### **SECTION 3 — CLEANING \& ENGINEERING DECISIONS**

**Decision 1: Full Naira Formatting to Prevent Cascade Errors** All amounts were entered in full Naira in the primary dataset (e.g., 58,472,628,944,759). Billion and Trillion columns were derived by formula. Hardcoding rounded figures was avoided to prevent rounding errors from compounding across calculations.

**Decision 2: Defining the "Security" Sector** To provide a comprehensive view of national security spending, the analysis deliberately expanded beyond the military. The "Security Sector" was defined by aggregating four major portfolios: The Ministry of Defence, the Ministry of Police Affairs, the Ministry of Interior (which houses Civil Defence, Immigration, and Correctional Services), and the National Security Adviser (NSA). This ensures the ₦5.85 Trillion security figure reflects the true, total cost of federal security operations.  true, total cost of federal security operations, not just military allocations.

**Decision 3: Differentiating Old Contractor Debt from New Capital** Two line items in the capital budget were identified as debt repayment rather than new infrastructure (Head 243 for ₦1.7 trillion and Head 244 for ₦100 billion). These were explicitly separated in the Capital Expenditure sheet to accurately reflect the true scope of new infrastructure funding.

**Decision 4: Calculating Exact 2025 Capital Performance** While the MTEF loosely states that capital performance was "less than 10 percent," the exact performance rate (7.72%) was calculated for this dataset using the raw MTEF figures: ₦834.8 billion released against a prorated target of ₦10,810.42 billion.

**Decision 5: Handling Multilateral Loan-Funded Capital** An initial approach considered excluding multilateral/bilateral loan-funded capital to isolate discretionary federal spending. However, a review of heavily loan-funded ministries (e.g., Power) revealed that applying this consistently would require project-level data omitted from the summary Bill. To maintain data integrity, the full totals were kept intact, and contextual notes were added to flag heavily loan-funded sectors.

**Decision 6: Flagging the NSA Capital Transparency Gap** During the security breakdown analysis, it was noted that the National Security Adviser (NSA) holds the highest proportion of capital spending among security agencies (₦286.9 billion), yet the Appropriation Bill provides no itemization of these projects. This was formally logged in the dataset as a transparency gap.

**Decision 7: Custom Cross-Sector Engineering (Defence vs. Health)** To evaluate opportunity costs, a custom metric was engineered comparing the personnel wage bill of the Defence sector strictly against the *entire* allocation (personnel, overhead, and capital) of the Health sector. This was documented in the Security Breakdown sheet to validate the narrative priority analysis.

**Decision 8: Statutory Transfer Treatment for INEC** The Bill lists INEC's ₦1.01 trillion allocation under Statutory Transfers as a single line without an internal breakdown. This was recorded as a statutory transfer total without estimating a breakdown the source document does not explicitly provide.

**Decision 9: Rounding Disclosure** All figures displayed in Billion and Trillion columns are rounded to two or three decimal places for readability. This is display rounding only; all underlying calculations reference the full Naira figures.

#### **SECTION 4 — DATASET STRUCTURE**

The final dataset consists of five sheets.

* **Sheet 1: Overview** — Macroeconomic summary of Revenue, Total Budget, and Expenditure Pillars.
* **Sheet 2: Debt vs National Priorities** — Comparative analysis of debt servicing against health and education allocations, incorporating total public debt context and international benchmarks.
* **Sheet 3: Security Breakdown** — Disaggregation of personnel, overhead, and capital allocations across the four major security MDAs, including cross-sector custom metrics.
* **Sheet 4: Capital Expenditure** — Review of infrastructure spending allocations, hidden debt liabilities, and historical execution rates.
* **Sheet 5: RAW\_EXPORT (Master Dataset)** — The fully normalized, unformatted master dataset containing all aggregated figures.

