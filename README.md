# GHG_project2
Analyzed 508 global corporations' GHG disclosures using Excel for data cleaning and feature engineering, SQL for KPI extraction and Power BI for an interactive 4-page dashboard — benchmarking emissions intensity across 6 regions and 12 sectors while explicitly flagging the 95% Scope 3 disclosure gap as a data-maturity finding rather than masking it with imputation.

##PROJECT SUMMARY
SITUATION

▸ A dataset of 508 major global corporations' GHG emissions (2022–2023) across 46 countries, 6 regions, and 12 sectors was analyzed to simulate an ESG benchmarking use case.
▸ Corporate climate disclosure is notoriously inconsistent — companies self-report on different standards, verification is optional, and deep-tier emissions data is often withheld entirely.
▸ ESG investors and regulators need reliable benchmarking to separate genuine decarbonization leaders from companies making unbacked net-zero claims.

TASK

▸ Design and execute an end-to-end analysis pipeline on 508 corporate emissions records spanning Scope 1, 2, and 3.
▸ Identify sector/region emissions benchmarks, carbon efficiency leaders, and net-zero ambition gaps.
▸ Deliver a self-service Power BI dashboard replacing static ESG reporting with dynamic, filterable insight.

ACTION

▸ EXCEL — DATA CLEANING: Diagnosed 95% missing Scope 3 and 85% missing Scope 2 (market) data; converted these into disclosure flags via IF/SEARCH formulas instead of imputing — preserving data integrity for regulatory-grade numbers.
▸ EXCEL — FEATURE ENGINEERING: Built net-zero ambition buckets (near-term/mid-term/long-term), revenue tiers via PERCENTILE.INC, recalculated emissions intensity, and flagged state-owned/coal-heavy companies from disclosure notes.
▸ SQL ANALYSIS: Wrote KPI queries covering sector/region benchmarking, Top 20 emitter leaderboards, and a RANK() OVER (PARTITION BY sector) window function to rank companies fairly against sector peers rather than the whole dataset.
▸ POWER BI DASHBOARD: Built a 4-page model — regional emissions map, sector efficiency scatter (revenue vs. intensity), net-zero ambition matrix, and leaderboards — with DAX measures for verification rate and net-zero coverage.
▸ VALIDATION: Cross-checked every SQL output against independent Excel PivotTables before publishing to the dashboard.

RESULT

▸ 📊 Utilities (3,609 MT) and Energy (3,432 MT) sectors dominate total emissions, with Gazprom (718 MT) the single largest emitter — nearly 2x the next-highest company.
▸ 🏭 Utilities and Materials carry the highest emissions intensity per revenue dollar, while Financials and Health Care are ~500x cleaner per dollar — a clear investment-risk signal.
▸ 🌍 76% of companies are third-party verified, and 89% report a net-zero target — but 232 of those targets sit at 2050 versus only 89 at 2030, exposing a "distant commitment" pattern behind the headline number.
▸ 🔍 Flagged the 95% Scope 3 non-disclosure rate as a data-maturity finding in its own right, rather than masking the gap — a more credible ESG signal than a false completeness.
▸ ⚡ Delivered a filterable dashboard replacing static sector reports, letting stakeholders benchmark any company against sector/region peers in seconds instead of manual cross-referencing.
▸ 🎯 Actionable segmentation: state-owned, coal-heavy emitters (e.g., China Shenhua, Eskom) isolated as a distinct high-risk cohort versus verified, efficiency-leading peers.
