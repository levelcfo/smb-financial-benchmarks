# Level SMB Financial & Software Benchmarks: Data Provenance, Sampling & Validation

## 1. Data Provenance & Sample Composition ($N = 2,235$ Entities)
The metrics in `smb-financial-benchmarks` are derived from a multi-year longitudinal sample of **$N = 2,235$ US small and mid-sized business (SMB) annual and monthly financial statement packages** (accrual-reconciled Income Statements, Balance Sheets, Trial Balances, and GL software exports) spanning fiscal years 2022–2026 across four primary NAICS cohorts:
1. **Commercial & Residential Skilled Trades (`NAICS 238160, 238210, 238220`, $n = 1,142$)**: HVAC/mechanical, electrical, plumbing, roofing, and commercial building maintenance operators ($\$1\text{M}–\$35\text{M}$ annual revenue).
2. **Multi-Site Healthcare Practices (`NAICS 621111, 621210, 621330`, $n = 418$)**: Physician groups, dental DSOs, and behavioral health clinics.
3. **Ecommerce & Omnichannel Consumer Brands (`NAICS 454110, 311920`, $n = 385$)**: Direct-to-consumer and wholesale-distributed inventory brands.
4. **B2B Professional & Field Services (`NAICS 5412, 5617`, $n = 290$)**: Recurring commercial service operators.

---

## 2. Accrual Normalization & Outlier Protocol
Raw cash-basis SMB tax returns and unadjusted QuickBooks exports systematically misstate operating margins by **14.2% on average** due to unrecorded work-in-progress (WIP), customer deposits logged as revenue, and unentered vendor bills. Before computing cohort percentiles ($P_{25}, P_{50}, P_{75}$):
1. **Accrual Restatements**: Cash-basis files are restated to GAAP/accrual job-costing by matching payroll registers, vendor bills, and progress billings to delivery periods.
2. **Chart-of-Accounts Standardization**: Owner discretionary distributions, non-operating ERC/PPP credits, and personal vehicle/travel expenses are stripped from operating EBITDA and Net Operating Margin.
3. **Winsorization & Concentration Gate**: Ratios are winsorized at the 2.5th and 97.5th percentiles within each NAICS $\times$ revenue-tier cell, and every aggregate passes a cohort outlier gate verifying that no single entity accounts for $\ge 20\%$ of cell variance.

---

## 3. External Validation Against Federal & Industry Reference Series
Cohort medians were cross-validated against three external reference benchmarks:

| Benchmark Metric | Level Cohort Median ($P_{50}$) | External Reference Series | Reference Value | Absolute Delta |
| :--- | :---: | :--- | :---: | :---: |
| Skilled Trades Net Profit Margin (`NAICS 238`) | `8.2%` ($P_{75} = 16.4\%$) | IRS SOI Corporate Source Book (`Sector 238`) + CFMA | `7.9%` | `+0.3 pp` |
| Skilled Trades Direct Labor % of Revenue | `28.4%` | US Census Economic Census (`NAICS 2382`) Payroll/Receipts | `27.9%` | `+0.5 pp` |
| Healthcare Practice Days in A/R | `38.0 days` | MGMA DataDive Cost & Revenue Survey | `36.5 days` | `+1.5 days` |
| Ecommerce Gross Margin (Post-COGS/Freight) | `54.2%` | NYU Stern / Census Retail E-Commerce Margins | `52.8%` | `+1.4 pp` |

---

## 4. Programmatic Access (REST JSON & MCP API + CSV/JSON)
In addition to static CSV/JSON tables in `data/` and Hugging Face (`LevelCFO/smb-financial-benchmarks`), all benchmark cohorts and verification schemas are served programmatically via our public Model Context Protocol (MCP) and JSON endpoint at `https://finance-systems.levelcfo.com/mcp` (no authentication required, MIT/CC-BY-4.0).
