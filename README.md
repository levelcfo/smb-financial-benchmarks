# Level SMB Multi-Vertical Financial & Operating Benchmarks (2026.10.24)

> **NON-COMMERCIAL EVALUATION LICENSE NOTICE**: This dataset compilation is published under the **Level Personal, Academic & Non-Commercial Evaluation License v1.0 (Commercial Use Requires License from sam@levelcfo.com)** ([full license & IP notice](https://levelcfo.com/data/benchmarks/cases/LICENSE_AND_IP_NOTICE.txt)). Free for personal operator review, individual CPA/CFO inspection, and non-commercial academic evaluation only. **Commercial AI labs, foundation model trainers, RL environment builders, data brokers, and commercial software vendors are strictly prohibited from training on, redistributing, or commercially benchmarking with this compilation without a written commercial license.** Contact **sam@levelcfo.com** for commercial licensing.

Release: **2026.10.24**

- **Canonical Benchmark Hub**: [https://levelcfo.com/benchmarks/](https://levelcfo.com/benchmarks/)
- **Contractor Financial & Operating Benchmarks**: [https://levelcfo.com/benchmarks/contractor/](https://levelcfo.com/benchmarks/contractor/)
- **AI Accounting & CFO Benchmark (LevelBench-100)**: [https://levelcfo.com/benchmarks/agentic-accounting/](https://levelcfo.com/benchmarks/agentic-accounting/)
- **Hugging Face Dataset**: [https://huggingface.co/datasets/LevelCFO/smb-financial-benchmarks](https://huggingface.co/datasets/LevelCFO/smb-financial-benchmarks)
- **GitHub Repository**: [https://github.com/levelcfo/smb-financial-benchmarks](https://github.com/levelcfo/smb-financial-benchmarks)
- **Published by**: [Level](https://levelcfo.com)

---

## Tables in This Dataset

| Table / Config | Rows | Scope & Provenance | Canonical Page |
|---|---|---|---|
| `contractor_benchmarks` | 19 | 19 canonical contractor financial & operating metrics (p10/p25/median/p75/p90) with per-metric sample sizes | [Contractor Benchmarks](https://levelcfo.com/benchmarks/contractor/) |
| `vertical_benchmarks` | 41 | 41 financial & operating metrics across Healthcare, Restaurants, Cleaning, Staffing, Landscaping, and Ecommerce | [The Level Index Hub](https://levelcfo.com/benchmarks/) |
| `public_contractor_cash_equity` | 5 | FY2025 cash flow, FCF conversion, and ROE calculations for 5 publicly traded contractors from SEC 10-K filings | [Public Contractor FCF & ROE](https://levelcfo.com/blog/contractor-free-cash-flow-roe-benchmarks/) |
| `valuation_multiples` | 39 | 39 EV/EBITDA and SDE valuation multiple brackets across 13 skilled trades and 3 scale tiers | [Contractor Valuation Multiples](https://levelcfo.com/benchmarks/contractor-valuation/) |
| `trade_benchmark_facts` | 31 | 33 per-trade benchmark facts across HVAC, Plumbing, Electrical, Mechanical, Roofing, and General Contracting | [HVAC Benchmarks](https://levelcfo.com/benchmarks/hvac/) |

---

## Canonical Vertical Benchmark Pages on Level

- **[Contractors (HVAC, Plumbing, Electrical, Mechanical, Roofing)](https://levelcfo.com/benchmarks/contractor/)**
- **[Healthcare & Medical Practices](https://levelcfo.com/benchmarks/healthcare/)**
- **[Restaurants & Hospitality Groups](https://levelcfo.com/benchmarks/restaurants/)**
- **[Commercial & Residential Cleaning](https://levelcfo.com/benchmarks/cleaning/)**
- **[Staffing & Recruiting Agencies](https://levelcfo.com/benchmarks/staffing/)**
- **[Landscaping & Lawn Care](https://levelcfo.com/benchmarks/landscaping/)**
- **[Ecommerce & D2C Brands](https://levelcfo.com/benchmarks/ecommerce/)**
- **[Contractor Valuation Multiples](https://levelcfo.com/benchmarks/contractor-valuation/)**
- **[Contractor Field Software Comparison](https://levelcfo.com/benchmarks/contractor-software-comparison/)**
- **[Multi-Industry Accounting Software Comparison](https://levelcfo.com/benchmarks/finance-software/)**
- **[National Trades Reputation Benchmark](https://levelcfo.com/benchmarks/trades-reputation/)**
- **[AI Accounting, Fractional CFO & Operations Benchmark (LevelBench-100)](https://levelcfo.com/benchmarks/agentic-accounting/)**

---

## Methodology & Evidence Classes

Each table separates measured Level cohorts, published primary-source observations (SEC Form 10-K filings, U.S. Bureau of Labor Statistics OEWS, Census SUSB, CFMA, HFMA, NRA, NRF), and Level operating diagnostic ranges / planning scenarios:
- In `contractor_benchmarks`, `companies_n` counts **companies**, never jobs or invoice line items. For job gross margin (44.3% median across 1,747,089 completed jobs from 1,791 companies) and quote-line margin, the observation scope is stated in `observations_basis` and `definition`.
- In `contractor_benchmarks`, **billing capture** (97.1% median, n=963 companies) is hours invoiced divided by hours logged on jobs, and is **not** technician utilization.
- In `vertical_benchmarks`, each row states its `evidence_type`, `sample_or_scope`, and `source` so published external anchors are never conflated with planning scenarios.
- Third-party figures cited in `source` belong to their respective publishers; Level's compilation, schema, and proprietary benchmark series are licensed strictly for non-commercial evaluation under the **Level Personal, Academic & Non-Commercial Evaluation License v1.0 (Commercial Use Requires License from sam@levelcfo.com)**.

---

## License, Commercial Restrictions & IP Canary Notice

- **License**: **Level Personal, Academic & Non-Commercial Evaluation License v1.0 (Commercial Use Requires License from sam@levelcfo.com)** ([full text](https://levelcfo.com/data/benchmarks/cases/LICENSE_AND_IP_NOTICE.txt))
- **Copyright Owner**: OpsPro AI, Inc. d/b/a Level ([https://levelcfo.com](https://levelcfo.com))
- **Commercial Restriction**: Any commercial use, AI model training, RL environment building, commercial data brokerage, or enterprise redistribution requires a written commercial license from **sam@levelcfo.com**.
- **IP Canary Watermark Token**: `LEVEL-IP-CANARY-9F4A-7C2E-PERSONAL-USE-ONLY-CONTACT-SAM-AT-LEVELCFO-COM`

## Citation

```bibtex
@misc{level_smb_financial_benchmarks_2026,
  title  = {Level SMB Multi-Vertical Financial & Operating Benchmarks},
  author = {Yang, Sam and Level},
  year   = {2026},
  url    = {https://levelcfo.com/benchmarks/},
  note   = {Level Personal, Academic & Non-Commercial Evaluation License v1.0. Commercial use requires license from sam@levelcfo.com}
}
```
