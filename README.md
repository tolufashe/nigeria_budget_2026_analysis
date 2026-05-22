# Nigeria 2026 Federal Budget — Investigative Data Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Data-driven investigation of Nigeria's 2026 Federal Budget (N58.47 trillion), examining debt servicing vs. social sector spending, security allocation efficiency, and capital budget execution — built entirely on official government documents.

---

## Overview

This project analyses Nigeria's 2026 Federal Budget using three official government sources: the 2026 Appropriation Bill, the 2026 Appropriation Bill Details (2,790 pages), and the 2026-2028 Medium Term Expenditure Framework and Fiscal Strategy Paper (MTEF/FSP).

Three questions drove the analysis:

1. How much of Nigeria's future is being sacrificed to service past debts?
2. Why does insecurity persist despite massive security allocations?
3. Does the capital budget represent real infrastructure or another cycle of unfulfilled promises?

---

## Key Findings

### Nigeria pays creditors 3.5 times more than it invests in health and education combined

| Item | Amount | Share of Budget |
|---|---|---|
| Debt Servicing | N15.91 trillion | 27.2% |
| Education | N2.40 trillion | 4.1% |
| Health | N2.15 trillion | 3.7% |
| Education + Health Combined | N4.55 trillion | 7.8% |

The Abuja Declaration commits African governments to 15% of national budgets for healthcare. Nigeria allocated 3.68%. UNESCO recommends 15-26% for education. Nigeria allocated 4.10%.

### Security spending is dominated by salaries, not operations

The security sector receives N5.85 trillion across four portfolios (Defence, Police Affairs, Interior, National Security Adviser). In Police Affairs, less than 5% reaches actual equipment and infrastructure.

### Capital execution has collapsed

In 2025, only 7.72% of the capital budget was released by Q3 — calculated from raw MTEF figures (N834.8 billion released against a prorated target of N10,810.42 billion). The 2026 capital target is nearly double last year's figure with no structural change to explain improved performance.

### Debt trajectory

| Year | Debt Service | YoY Change |
|---|---|---|
| 2023 (Actual) | N6.78 trillion | — |
| 2024 (Actual) | N12.63 trillion | +N5.85 trillion |
| 2026 (Budgeted) | N15.91 trillion | +N3.28 trillion |
| 2027 (Projected) | N19.50 trillion | +N3.59 trillion |

In 2024, for every N100 Nigeria earned, N60 went to debt payments.

---

## Data Sources

All figures trace back exclusively to official federal publications. No figures were sourced from secondary aggregators.

| Source | Use |
|---|---|
| 2026 Appropriation Bill (10 pages) | Top-level budget figures, debt service breakdown, ministry capital allocations |
| 2026 Appropriation Bill Details (2,790 pages) | Ministry-level personnel, overhead, and capital breakdowns |
| 2026-2028 MTEF/FSP (65 pages) | Historical context, debt trends, 2025 capital execution data, 2027 projections |

Benchmarks used: Abuja Declaration (2001), UNESCO Education Financing Recommendations, World Bank revenue-to-debt-servicing data.

---

## Data Engineering Decisions

**Full Naira formatting:** All amounts entered in full Naira (e.g. 58,472,628,944,759). Billion and Trillion columns derived by formula to prevent rounding errors from compounding.

**Security sector definition:** The security sector was deliberately expanded beyond the military to aggregate four portfolios: Defence, Police Affairs, Interior, and National Security Adviser. This ensures the N5.85 trillion figure reflects the true total cost of federal security operations.

**Old contractor debt separated from new capital:** Two capital budget line items were identified as debt repayment rather than new infrastructure (Head 243: N1.7 trillion; Head 244: N100 billion). These were explicitly separated to accurately reflect the true scope of new infrastructure funding.

**Exact 2025 capital performance calculated:** While the MTEF loosely states capital performance was "less than 10 percent," the exact rate (7.72%) was calculated using raw MTEF figures.

**NSA capital transparency gap flagged:** The National Security Adviser holds the highest proportion of capital spending among security agencies (N286.9 billion), yet the Appropriation Bill provides no itemisation of these projects. Formally logged as a transparency gap.

---

## Repository Structure

```
nigeria-budget-2026-analysis/
├── data/
│   └── nigeria_budget_2026_clean.csv      # Structured dataset exported from source
├── Nigeria_2026_Budget_Report.pdf         # Full investigative report
├── DATA_DOCUMENTATION.md                  # Sourcing decisions, cleaning methodology, citations
└── README.md
```

---

## Team

Group 25 — Data Analytics Programme, Stage 5

- John Olaoluwa Tolufashe — Lead Data Analyst, data cleaning, dataset engineering, documentation
- Thekem — Lead Visualizer, charts, fact-checking
- Oluwanifesimi Samuel — Investigative Writer, final report

---

## Contact

John Olaoluwa Tolufashe · [tolufashejohn@gmail.com](mailto:tolufashejohn@gmail.com) · [GitHub](https://github.com/tolufashe)

---

*Built using Google Sheets and official Nigerian government publications*
