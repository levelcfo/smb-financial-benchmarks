# SMB Financial & Software Benchmarks: Data Provenance, Normalization & Validation

## 1. Data Provenance & Sample Composition
The dataset combines two distinct, traceable layers:
1. **Private SMB Ledger & Permit Cohort ($N = 2,235$ US operating businesses)**: Aggregated from anonymized accrual-basis financial statements (gross margin, net operating margin, labor ratio, overhead ratio, AR days, and cash runway) and cross-walked against municipal permit activity across 6 US operating verticals (Construction & Specialty Trades, Healthcare Practices, E-Commerce, Commercial Real Estate, B2B Software, and Multi-Unit Franchise).
2. **Public SEC EDGAR 10-K Comp Panel ($N = 6$ public trade contractors)**: Audited FY2024–FY2025 SEC Form 10-K filings for EMCOR Group (`EME`, CIK `0000105634`), Comfort Systems USA (`FIX`, CIK `0001035976`), APi Group (`APG`, CIK `0001796209`), IES Holdings (`IESC`, CIK `0001048268`), Dycom Industries (`DY`, CIK `0000067215`), and MYR Group (`MYRG`, CIK `0000700923`).

## 2. Chart-of-Accounts Normalization
Raw QuickBooks Online, Xero, and NetSuite trial balances are mapped into a standardized 14-bucket GAAP chart of accounts before computing percentile distributions ($P_{25}, P_{50}, P_{75}$):
- Direct field labor, payroll taxes, and subcontractor costs are normalized into **Cost of Goods Sold (COGS)** so gross margin is comparable across cash-to-accrual conversions.
- Owner officer compensation above market replacement is normalized out of operating overhead to prevent S-Corp distribution distortion.

## 3. Validation & Cross-Checks
- Private contractor gross/net margin distributions are validated against RMA Annual Statement Studies, CFMA Construction Financial Benchmarker aggregates, and the 6 SEC Form 10-K public contractor filings (`sec_10k_public_contractor_benchmarks.json`).
- Every row in `smb_industry_financial_benchmarks.csv` includes explicit sample counts and quartile bounds.

## 4. Known Limitations
- Survivorship and selection bias toward US SMBs ($1M–$50M annual revenue) actively maintaining monthly accrual books.
- Regional labor-rate variance can shift gross margin percentiles by $pm 280$ bps between high-cost coastal MSAs and Sunbelt MSAs.
