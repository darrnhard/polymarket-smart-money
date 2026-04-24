# Changelog

All notable changes to this project are documented here.  
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-04-24

### Added
- Full activity backfill for rn1, sovereign, swisstony (6.8M events total)
- Adaptive time-window chunked pagination with recursive bisection
- Per-window ledger checkpointing for resumable fetches
- Deduplication by transactionHash with composite fallback for SPLIT/MERGE events
- 15-category rule-based market classifier (82% coverage across 29k+ unique titles)
- Behavioral analysis: holding period, position sizing, entry price distributions
- Cross-wallet market overlap analysis (Venn diagram)
- Lead/follow timing hierarchy: sovereign → swisstony → rn1
- Trade burst analysis (size and duration distributions)
- Position averaging behavior (multi-session DCA detection)
- Concurrent position count over time (daily active markets)
- All visualizations committed to `plots/` (10 charts)
- Rendered HTML notebooks in `docs/` for zero-setup viewing
- Executive summary research memo (`docs/EXECUTIVE_SUMMARY.md`)
- Deferred analysis plan files (`plan/`)

### Architecture
- Python 3.14 + pandas 2.x Arrow string compatibility fix
- fastparquet as parquet engine (pyarrow incompatible with Python 3.14)
- Per-wallet parquet files (~890 MB total, gitignored)
- Positions snapshot saved as CSV (lightweight, current state only)

---

## [Unreleased] — Phase 2

- Real-time wallet monitoring for sovereign signal detection
- Copy trading execution engine with proportional sizing
- Paper trading simulation layer
- Gamma API market resolution fetch (unlocks win rate, PnL, Sortino)
- Kelly fraction sizing calibration
